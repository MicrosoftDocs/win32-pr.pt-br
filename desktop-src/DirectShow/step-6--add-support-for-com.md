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
# <a name="step-6-add-support-for-com"></a><span data-ttu-id="7a1e8-104">Etapa 6.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-104">Step 6.</span></span> <span data-ttu-id="7a1e8-105">Adicionar suporte para COM</span><span class="sxs-lookup"><span data-stu-id="7a1e8-105">Add Support for COM</span></span>

<span data-ttu-id="7a1e8-106">Esta é a etapa 6 do tutorial [escrevendo filtros de transformação](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="7a1e8-106">This is step 6 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="7a1e8-107">A etapa final é adicionar suporte para COM.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-107">The final step is to add support for COM.</span></span>

## <a name="reference-counting"></a><span data-ttu-id="7a1e8-108">Contagem de referência</span><span class="sxs-lookup"><span data-stu-id="7a1e8-108">Reference Counting</span></span>

<span data-ttu-id="7a1e8-109">Você não precisa implementar [**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) ou [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="7a1e8-109">You do not have to implement [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) or [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="7a1e8-110">Todas as classes de filtro e PIN derivam de [**CUnknown**](cunknown.md), que lida com a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-110">All of the filter and pin classes derive from [**CUnknown**](cunknown.md), which handles reference counting.</span></span>

## <a name="queryinterface"></a><span data-ttu-id="7a1e8-111">QueryInterface</span><span class="sxs-lookup"><span data-stu-id="7a1e8-111">QueryInterface</span></span>

<span data-ttu-id="7a1e8-112">Todas as classes de filtro e PIN implementam [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para quaisquer interfaces com que herdam.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-112">All of the filter and pin classes implement [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for any COM interfaces they inherit.</span></span> <span data-ttu-id="7a1e8-113">Por exemplo, [**CTransformFilter**](ctransformfilter.md) herda [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (por meio de [**CBaseFilter**](cbasefilter.md)).</span><span class="sxs-lookup"><span data-stu-id="7a1e8-113">For example, [**CTransformFilter**](ctransformfilter.md) inherits [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (through [**CBaseFilter**](cbasefilter.md)).</span></span> <span data-ttu-id="7a1e8-114">Se o filtro não expõe nenhuma interface adicional, você não precisa fazer mais nada.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-114">If your filter does not expose any additional interfaces, you do not have to do anything else.</span></span>

<span data-ttu-id="7a1e8-115">Para expor interfaces adicionais, substitua o método [**CUnknown:: NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="7a1e8-115">To expose additional interfaces, override the [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method.</span></span> <span data-ttu-id="7a1e8-116">Por exemplo, suponha que o filtro implemente uma interface personalizada chamada IMyCustomInterface.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-116">For example, suppose your filter implements a custom interface named IMyCustomInterface.</span></span> <span data-ttu-id="7a1e8-117">Para expor essa interface aos clientes, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7a1e8-117">To expose this interface to clients, do the following:</span></span>

-   <span data-ttu-id="7a1e8-118">Derive a classe de filtro dessa interface.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-118">Derive your filter class from that interface.</span></span>
-   <span data-ttu-id="7a1e8-119">Coloque a macro [**Declare \_ IUnknown**](declare-iunknown.md) na seção da declaração pública.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-119">Put the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public declaration section.</span></span>
-   <span data-ttu-id="7a1e8-120">Substitua [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) para verificar a IID da sua interface e retornar um ponteiro para o filtro.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-120">Override [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) to check for the IID of your interface and return a pointer to your filter.</span></span>

<span data-ttu-id="7a1e8-121">O código a seguir mostra estas etapas:</span><span class="sxs-lookup"><span data-stu-id="7a1e8-121">The following code shows these steps:</span></span>


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



<span data-ttu-id="7a1e8-122">Para obter mais informações, consulte [como implementar IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="7a1e8-122">For more information, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

## <a name="object-creation"></a><span data-ttu-id="7a1e8-123">Criação de objetos</span><span class="sxs-lookup"><span data-stu-id="7a1e8-123">Object Creation</span></span>

<span data-ttu-id="7a1e8-124">Se você planeja empacotar seu filtro em uma DLL e disponibilizá-lo para outros clientes, você deve dar suporte a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) e a outras funções com relacionadas.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-124">If you plan to package your filter in a DLL and make it available to other clients, you must support [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) and other related COM functions.</span></span> <span data-ttu-id="7a1e8-125">A biblioteca de classes base implementa a maior parte disso; Você só precisa fornecer algumas informações sobre seu filtro.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-125">The base class library implements most of this; you just need to provide some information about your filter.</span></span> <span data-ttu-id="7a1e8-126">Esta seção fornece uma breve visão geral do que fazer.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-126">This section gives a brief overview of what to do.</span></span> <span data-ttu-id="7a1e8-127">Para obter detalhes, consulte [como criar uma DLL de filtro do DirectShow](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="7a1e8-127">For details, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

<span data-ttu-id="7a1e8-128">Primeiro, escreva um método de classe estática que retorne uma nova instância do seu filtro.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-128">First, write a static class method that returns a new instance of your filter.</span></span> <span data-ttu-id="7a1e8-129">Você pode nomear esse método como desejar, mas a assinatura deve corresponder à mostrada no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="7a1e8-129">You can name this method anything you like, but the signature must match the one shown in the following example:</span></span>


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



<span data-ttu-id="7a1e8-130">Em seguida, declare uma matriz global de instâncias de classe [**CFactoryTemplate**](cfactorytemplate.md) , denominada *\_ modelos g*.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-130">Next, declare a global array of [**CFactoryTemplate**](cfactorytemplate.md) class instances, named *g\_Templates*.</span></span> <span data-ttu-id="7a1e8-131">Cada classe **CFactoryTemplate** contém informações de registro para um filtro.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-131">Each **CFactoryTemplate** class contains registry information for one filter.</span></span> <span data-ttu-id="7a1e8-132">Vários filtros podem residir em uma única DLL; basta incluir entradas **CFactoryTemplate** adicionais.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-132">Several filters can reside in a single DLL; simply include additional **CFactoryTemplate** entries.</span></span> <span data-ttu-id="7a1e8-133">Você também pode declarar outros objetos COM, como páginas de propriedades.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-133">You can also declare other COM objects, such as property pages.</span></span>


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



<span data-ttu-id="7a1e8-134">Defina um inteiro global chamado *g \_ cTemplates* cujo valor é igual ao tamanho da matriz de *\_ modelos g* :</span><span class="sxs-lookup"><span data-stu-id="7a1e8-134">Define a global integer named *g\_cTemplates* whose value equals the length of the *g\_Templates* array:</span></span>


```C++
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);  
```



<span data-ttu-id="7a1e8-135">Por fim, implemente as funções de registro de DLL.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-135">Finally, implement the DLL registration functions.</span></span> <span data-ttu-id="7a1e8-136">O exemplo a seguir mostra a implementação mínima para essas funções:</span><span class="sxs-lookup"><span data-stu-id="7a1e8-136">The following example shows the minimal implementation for these functions:</span></span>


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



## <a name="filter-registry-entries"></a><span data-ttu-id="7a1e8-137">Filtrar entradas do registro</span><span class="sxs-lookup"><span data-stu-id="7a1e8-137">Filter Registry Entries</span></span>

<span data-ttu-id="7a1e8-138">Os exemplos anteriores mostram como registrar o CLSID de um filtro para COM.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-138">The previous examples show how to register a filter's CLSID for COM.</span></span> <span data-ttu-id="7a1e8-139">Para muitos filtros, isso é suficiente.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-139">For many filters, this is sufficient.</span></span> <span data-ttu-id="7a1e8-140">Em seguida, o cliente deve criar o filtro usando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) e adicioná-lo ao grafo de filtro chamando [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter).</span><span class="sxs-lookup"><span data-stu-id="7a1e8-140">The client is then expected to create the filter using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) and add it to the filter graph by calling [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter).</span></span> <span data-ttu-id="7a1e8-141">Em alguns casos, no entanto, talvez você queira fornecer informações adicionais sobre o filtro no registro.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-141">In some cases, however, you might want to provide additional information about the filter in the registry.</span></span> <span data-ttu-id="7a1e8-142">Essas informações são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="7a1e8-142">This information does the following:</span></span>

-   <span data-ttu-id="7a1e8-143">Permite que os clientes descubram o filtro usando o [mapeador de filtro](filter-mapper.md) ou o [enumerador de dispositivo do sistema](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="7a1e8-143">Enables clients to discover the filter using the [Filter Mapper](filter-mapper.md) or the [System Device Enumerator](system-device-enumerator.md).</span></span>
-   <span data-ttu-id="7a1e8-144">Permite que o Gerenciador de gráficos de filtro descubra o filtro durante a criação automática de grafo.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-144">Enables the Filter Graph Manager to discover the filter during automatic graph building.</span></span>

<span data-ttu-id="7a1e8-145">O exemplo a seguir registra o filtro de codificador RLE na categoria de compactador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-145">The following example registers the RLE encoder filter in the video compressor category.</span></span> <span data-ttu-id="7a1e8-146">Para obter detalhes, consulte [como registrar filtros do DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="7a1e8-146">For details, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="7a1e8-147">Certifique-se de ler a seção [diretrizes para registrar filtros](guidelines-for-registering-filters.md), que descreve as práticas recomendadas para o registro de filtro.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-147">Be sure to read the section [Guidelines for Registering Filters](guidelines-for-registering-filters.md), which describes the recommended practices for filter registration.</span></span>


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



<span data-ttu-id="7a1e8-148">Além disso, os filtros não precisam ser empacotados dentro de DLLs.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-148">Also, filters do not have to be packaged inside DLLs.</span></span> <span data-ttu-id="7a1e8-149">Em alguns casos, você pode escrever um filtro especializado que é projetado apenas para um aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-149">In some cases, you might write a specialized filter that is designed only for a specific application.</span></span> <span data-ttu-id="7a1e8-150">Nesse caso, você pode compilar a classe de filtro diretamente em seu aplicativo e criá-la com o `new` operador, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="7a1e8-150">In that case, you can compile the filter class directly in your application, and create it with the `new` operator, as shown in the following example:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7a1e8-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7a1e8-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a1e8-152">Conexão inteligente</span><span class="sxs-lookup"><span data-stu-id="7a1e8-152">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> <dt>

[<span data-ttu-id="7a1e8-153">Gravando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="7a1e8-153">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="7a1e8-154">Gravando filtros de transformação</span><span class="sxs-lookup"><span data-stu-id="7a1e8-154">Writing Transform Filters</span></span>](writing-transform-filters.md)
</dt> </dl>

 

 
