---
description: Etapa 6.
ms.assetid: 53e4f5b7-c85d-4b44-9a0c-0ad05ca872cc
title: Etapa 6. Adicionar suporte para COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e477cc22650604bce623874c0afbba1063609e44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810384"
---
# <a name="step-6-add-support-for-com"></a>Etapa 6. Adicionar suporte para COM

Esta é a etapa 6 do tutorial [escrevendo filtros de transformação](writing-transform-filters.md).

A etapa final é adicionar suporte para COM.

## <a name="reference-counting"></a>Contagem de referência

Você não precisa implementar [**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) ou [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Todas as classes de filtro e PIN derivam de [**CUnknown**](cunknown.md), que lida com a contagem de referência.

## <a name="queryinterface"></a>QueryInterface

Todas as classes de filtro e PIN implementam [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para quaisquer interfaces com que herdam. Por exemplo, [**CTransformFilter**](ctransformfilter.md) herda [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (por meio de [**CBaseFilter**](cbasefilter.md)). Se o filtro não expõe nenhuma interface adicional, você não precisa fazer mais nada.

Para expor interfaces adicionais, substitua o método [**CUnknown:: NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) . Por exemplo, suponha que o filtro implemente uma interface personalizada chamada IMyCustomInterface. Para expor essa interface aos clientes, faça o seguinte:

-   Derive a classe de filtro dessa interface.
-   Coloque a macro [**Declare \_ IUnknown**](declare-iunknown.md) na seção da declaração pública.
-   Substitua [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) para verificar a IID da sua interface e retornar um ponteiro para o filtro.

O código a seguir mostra estas etapas:


```C++
CMyFilter : public CBaseFilter, public IMyCustomInterface
{
public:
    DECLARE_IUNKNOWN
    STDMETHODIMP NonDelegatingQueryInterface(REFIID iid, void **ppv);
};
STDMETHODIMP CMyFilter::NonDelegatingQueryInterface(REFIID iid, void **ppv)
{
    if (riid == IID_IMyCustomInterface) {
        return GetInterface(static_cast<IMyCustomInterface*>(this), ppv);
    }
    return CBaseFilter::NonDelegatingQueryInterface(riid,ppv);
}
```



Para obter mais informações, consulte [como implementar IUnknown](how-to-implement-iunknown.md).

## <a name="object-creation"></a>Criação de objetos

Se você planeja empacotar seu filtro em uma DLL e disponibilizá-lo para outros clientes, você deve dar suporte a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) e a outras funções com relacionadas. A biblioteca de classes base implementa a maior parte disso; Você só precisa fornecer algumas informações sobre seu filtro. Esta seção fornece uma breve visão geral do que fazer. Para obter detalhes, consulte [como criar uma DLL de filtro do DirectShow](how-to-create-a-dll.md).

Primeiro, escreva um método de classe estática que retorne uma nova instância do seu filtro. Você pode nomear esse método como desejar, mas a assinatura deve corresponder à mostrada no exemplo a seguir:


```C++
CUnknown * WINAPI CRleFilter::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr)
{
    CRleFilter *pFilter = new CRleFilter();
    if (pFilter== NULL) 
    {
        *pHr = E_OUTOFMEMORY;
    }
    return pFilter;
}
```



Em seguida, declare uma matriz global de instâncias de classe [**CFactoryTemplate**](cfactorytemplate.md) , denominada *\_ modelos g*. Cada classe **CFactoryTemplate** contém informações de registro para um filtro. Vários filtros podem residir em uma única DLL; basta incluir entradas **CFactoryTemplate** adicionais. Você também pode declarar outros objetos COM, como páginas de propriedades.


```C++
static WCHAR g_wszName[] = L"My RLE Encoder";
CFactoryTemplate g_Templates[] = 
{
  { 
    g_wszName,
    &CLSID_RLEFilter,
    CRleFilter::CreateInstance,
    NULL,
    NULL
  }
};
```



Defina um inteiro global chamado *g \_ cTemplates* cujo valor é igual ao tamanho da matriz de *\_ modelos g* :


```C++
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);  
```



Por fim, implemente as funções de registro de DLL. O exemplo a seguir mostra a implementação mínima para essas funções:


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}
STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



## <a name="filter-registry-entries"></a>Filtrar entradas do registro

Os exemplos anteriores mostram como registrar o CLSID de um filtro para COM. Para muitos filtros, isso é suficiente. Em seguida, o cliente deve criar o filtro usando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) e adicioná-lo ao grafo de filtro chamando [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter). Em alguns casos, no entanto, talvez você queira fornecer informações adicionais sobre o filtro no registro. Essas informações são as seguintes:

-   Permite que os clientes descubram o filtro usando o [mapeador de filtro](filter-mapper.md) ou o [enumerador de dispositivo do sistema](system-device-enumerator.md).
-   Permite que o Gerenciador de gráficos de filtro descubra o filtro durante a criação automática de grafo.

O exemplo a seguir registra o filtro de codificador RLE na categoria de compactador de vídeo. Para obter detalhes, consulte [como registrar filtros do DirectShow](how-to-register-directshow-filters.md). Certifique-se de ler a seção [diretrizes para registrar filtros](guidelines-for-registering-filters.md), que descreve as práticas recomendadas para o registro de filtro.


```C++
// Declare media type information.
FOURCCMap fccMap = FCC('MRLE'); 
REGPINTYPES sudInputTypes = { &MEDIATYPE_Video, &GUID_NULL };
REGPINTYPES sudOutputTypes = { &MEDIATYPE_Video, (GUID*)&fccMap };

// Declare pin information.
REGFILTERPINS sudPinReg[] = {
    // Input pin.
    { 0, FALSE, // Rendered?
         FALSE, // Output?
         FALSE, // Zero?
         FALSE, // Many?
         0, 0, 
         1, &sudInputTypes  // Media types.
    },
    // Output pin.
    { 0, FALSE, // Rendered?
         TRUE, // Output?
         FALSE, // Zero?
         FALSE, // Many?
         0, 0, 
         1, &sudOutputTypes      // Media types.
    }
};
 
// Declare filter information.
REGFILTER2 rf2FilterReg = {
    1,                // Version number.
    MERIT_DO_NOT_USE, // Merit.
    2,                // Number of pins.
    sudPinReg         // Pointer to pin information.
};

STDAPI DllRegisterServer(void)
{
    HRESULT hr = AMovieDllRegisterServer2(TRUE);
    if (FAILED(hr))
    {
        return hr;
    }
    IFilterMapper2 *pFM2 = NULL;
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);
    if (SUCCEEDED(hr))
    {
        hr = pFM2->RegisterFilter(
            CLSID_RLEFilter,                // Filter CLSID. 
            g_wszName,                       // Filter name.
            NULL,                            // Device moniker. 
            &CLSID_VideoCompressorCategory,  // Video compressor category.
            g_wszName,                       // Instance data.
            &rf2FilterReg                    // Filter information.
            );
        pFM2->Release();
    }
    return hr;
}

STDAPI DllUnregisterServer()
{
    HRESULT hr = AMovieDllRegisterServer2(FALSE);
    if (FAILED(hr))
    {
        return hr;
    }
    IFilterMapper2 *pFM2 = NULL;
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);
    if (SUCCEEDED(hr))
    {
        hr = pFM2->UnregisterFilter(&CLSID_VideoCompressorCategory, 
            g_wszName, CLSID_RLEFilter);
        pFM2->Release();
    }
    return hr;
}
```



Além disso, os filtros não precisam ser empacotados dentro de DLLs. Em alguns casos, você pode escrever um filtro especializado que é projetado apenas para um aplicativo específico. Nesse caso, você pode compilar a classe de filtro diretamente em seu aplicativo e criá-la com o `new` operador, conforme mostrado no exemplo a seguir:


```C++
#include "MyFilter.h"  // Header file that declares the filter class.
// Compile and link MyFilter.cpp.
int main()
{
    IBaseFilter *pFilter = 0;
    {
        // Scope to hide pF.
        CMyFilter* pF = new MyFilter();
        if (!pF)
        {
            printf("Could not create MyFilter.\n");
            return 1;
        }
        pF->QueryInterface(IID_IBaseFilter, 
            reinterpret_cast<void**>(&pFilter));
    }
    
    /* Now use pFilter as normal. */
    
    pFilter->Release();  // Deletes the filter.
    return 0;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conexão inteligente](intelligent-connect.md)
</dt> <dt>

[Gravando filtros do DirectShow](writing-directshow-filters.md)
</dt> <dt>

[Gravando filtros de transformação](writing-transform-filters.md)
</dt> </dl>

 

 
