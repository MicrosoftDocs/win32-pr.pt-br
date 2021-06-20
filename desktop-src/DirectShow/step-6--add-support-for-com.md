---
description: Adicione suporte para COM como parte da gravação de um filtro de transformação. Esta é a etapa final deste tutorial.
ms.assetid: 53e4f5b7-c85d-4b44-9a0c-0ad05ca872cc
title: Etapa 6. Adicionar suporte para COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097d51fa440812311edde9ce448916c66721a507
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406769"
---
# <a name="step-6-add-support-for-com"></a><span data-ttu-id="e6b1c-105">Etapa 6.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-105">Step 6.</span></span> <span data-ttu-id="e6b1c-106">Adicionar suporte para COM</span><span class="sxs-lookup"><span data-stu-id="e6b1c-106">Add Support for COM</span></span>

<span data-ttu-id="e6b1c-107">Esta é a etapa 6 do tutorial [escrevendo filtros de transformação](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="e6b1c-107">This is step 6 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="e6b1c-108">A etapa final é adicionar suporte para COM.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-108">The final step is to add support for COM.</span></span>

## <a name="reference-counting"></a><span data-ttu-id="e6b1c-109">Contagem de referência</span><span class="sxs-lookup"><span data-stu-id="e6b1c-109">Reference Counting</span></span>

<span data-ttu-id="e6b1c-110">Você não precisa implementar [**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) ou [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="e6b1c-110">You do not have to implement [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) or [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="e6b1c-111">Todas as classes de filtro e PIN derivam de [**CUnknown**](cunknown.md), que lida com a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-111">All of the filter and pin classes derive from [**CUnknown**](cunknown.md), which handles reference counting.</span></span>

## <a name="queryinterface"></a><span data-ttu-id="e6b1c-112">QueryInterface</span><span class="sxs-lookup"><span data-stu-id="e6b1c-112">QueryInterface</span></span>

<span data-ttu-id="e6b1c-113">Todas as classes de filtro e PIN implementam [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para quaisquer interfaces com que herdam.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-113">All of the filter and pin classes implement [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for any COM interfaces they inherit.</span></span> <span data-ttu-id="e6b1c-114">Por exemplo, [**CTransformFilter**](ctransformfilter.md) herda [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (por meio de [**CBaseFilter**](cbasefilter.md)).</span><span class="sxs-lookup"><span data-stu-id="e6b1c-114">For example, [**CTransformFilter**](ctransformfilter.md) inherits [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (through [**CBaseFilter**](cbasefilter.md)).</span></span> <span data-ttu-id="e6b1c-115">Se o filtro não expõe nenhuma interface adicional, você não precisa fazer mais nada.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-115">If your filter does not expose any additional interfaces, you do not have to do anything else.</span></span>

<span data-ttu-id="e6b1c-116">Para expor interfaces adicionais, substitua o método [**CUnknown:: NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="e6b1c-116">To expose additional interfaces, override the [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method.</span></span> <span data-ttu-id="e6b1c-117">Por exemplo, suponha que o filtro implemente uma interface personalizada chamada IMyCustomInterface.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-117">For example, suppose your filter implements a custom interface named IMyCustomInterface.</span></span> <span data-ttu-id="e6b1c-118">Para expor essa interface aos clientes, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e6b1c-118">To expose this interface to clients, do the following:</span></span>

-   <span data-ttu-id="e6b1c-119">Derive a classe de filtro dessa interface.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-119">Derive your filter class from that interface.</span></span>
-   <span data-ttu-id="e6b1c-120">Coloque a macro [**Declare \_ IUnknown**](declare-iunknown.md) na seção da declaração pública.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-120">Put the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public declaration section.</span></span>
-   <span data-ttu-id="e6b1c-121">Substitua [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) para verificar a IID da sua interface e retornar um ponteiro para o filtro.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-121">Override [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) to check for the IID of your interface and return a pointer to your filter.</span></span>

<span data-ttu-id="e6b1c-122">O código a seguir mostra essas etapas:</span><span class="sxs-lookup"><span data-stu-id="e6b1c-122">The following code shows these steps:</span></span>


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



<span data-ttu-id="e6b1c-123">Para obter mais informações, consulte [como implementar IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="e6b1c-123">For more information, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

## <a name="object-creation"></a><span data-ttu-id="e6b1c-124">Criação de objetos</span><span class="sxs-lookup"><span data-stu-id="e6b1c-124">Object Creation</span></span>

<span data-ttu-id="e6b1c-125">Se você planeja empacotar seu filtro em uma DLL e disponibilizá-lo para outros clientes, você deve dar suporte a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) e a outras funções com relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-125">If you plan to package your filter in a DLL and make it available to other clients, you must support [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) and other related COM functions.</span></span> <span data-ttu-id="e6b1c-126">A biblioteca de classes base implementa a maior parte disso; Você só precisa fornecer algumas informações sobre seu filtro.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-126">The base class library implements most of this; you just need to provide some information about your filter.</span></span> <span data-ttu-id="e6b1c-127">Esta seção fornece uma breve visão geral do que fazer.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-127">This section gives a brief overview of what to do.</span></span> <span data-ttu-id="e6b1c-128">Para obter detalhes, consulte [como criar uma DLL de filtro do DirectShow](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="e6b1c-128">For details, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

<span data-ttu-id="e6b1c-129">Primeiro, escreva um método de classe estática que retorne uma nova instância do seu filtro.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-129">First, write a static class method that returns a new instance of your filter.</span></span> <span data-ttu-id="e6b1c-130">Você pode nomear esse método como desejar, mas a assinatura deve corresponder à mostrada no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="e6b1c-130">You can name this method anything you like, but the signature must match the one shown in the following example:</span></span>


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



<span data-ttu-id="e6b1c-131">Em seguida, declare uma matriz global de instâncias de classe [**CFactoryTemplate**](cfactorytemplate.md) , denominada *\_ modelos g*.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-131">Next, declare a global array of [**CFactoryTemplate**](cfactorytemplate.md) class instances, named *g\_Templates*.</span></span> <span data-ttu-id="e6b1c-132">Cada classe **CFactoryTemplate** contém informações de registro para um filtro.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-132">Each **CFactoryTemplate** class contains registry information for one filter.</span></span> <span data-ttu-id="e6b1c-133">Vários filtros podem residir em uma única DLL; basta incluir entradas **CFactoryTemplate** adicionais.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-133">Several filters can reside in a single DLL; simply include additional **CFactoryTemplate** entries.</span></span> <span data-ttu-id="e6b1c-134">Você também pode declarar outros objetos COM, como páginas de propriedades.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-134">You can also declare other COM objects, such as property pages.</span></span>


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



<span data-ttu-id="e6b1c-135">Defina um inteiro global chamado *g \_ cTemplates* cujo valor é igual ao tamanho da matriz de *\_ modelos g* :</span><span class="sxs-lookup"><span data-stu-id="e6b1c-135">Define a global integer named *g\_cTemplates* whose value equals the length of the *g\_Templates* array:</span></span>


```C++
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);  
```



<span data-ttu-id="e6b1c-136">Por fim, implemente as funções de registro de DLL.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-136">Finally, implement the DLL registration functions.</span></span> <span data-ttu-id="e6b1c-137">O exemplo a seguir mostra a implementação mínima para essas funções:</span><span class="sxs-lookup"><span data-stu-id="e6b1c-137">The following example shows the minimal implementation for these functions:</span></span>


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



## <a name="filter-registry-entries"></a><span data-ttu-id="e6b1c-138">Filtrar entradas do registro</span><span class="sxs-lookup"><span data-stu-id="e6b1c-138">Filter Registry Entries</span></span>

<span data-ttu-id="e6b1c-139">Os exemplos anteriores mostram como registrar o CLSID de um filtro para COM.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-139">The previous examples show how to register a filter's CLSID for COM.</span></span> <span data-ttu-id="e6b1c-140">Para muitos filtros, isso é suficiente.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-140">For many filters, this is sufficient.</span></span> <span data-ttu-id="e6b1c-141">Em seguida, o cliente deve criar o filtro usando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) e adicioná-lo ao grafo de filtro chamando [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter).</span><span class="sxs-lookup"><span data-stu-id="e6b1c-141">The client is then expected to create the filter using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) and add it to the filter graph by calling [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter).</span></span> <span data-ttu-id="e6b1c-142">Em alguns casos, no entanto, talvez você queira fornecer informações adicionais sobre o filtro no registro.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-142">In some cases, however, you might want to provide additional information about the filter in the registry.</span></span> <span data-ttu-id="e6b1c-143">Essas informações são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="e6b1c-143">This information does the following:</span></span>

-   <span data-ttu-id="e6b1c-144">Permite que os clientes descubram o filtro usando o [mapeador de filtro](filter-mapper.md) ou o [enumerador de dispositivo do sistema](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="e6b1c-144">Enables clients to discover the filter using the [Filter Mapper](filter-mapper.md) or the [System Device Enumerator](system-device-enumerator.md).</span></span>
-   <span data-ttu-id="e6b1c-145">Permite que o Gerenciador de gráficos de filtro descubra o filtro durante a criação automática de grafo.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-145">Enables the Filter Graph Manager to discover the filter during automatic graph building.</span></span>

<span data-ttu-id="e6b1c-146">O exemplo a seguir registra o filtro de codificador RLE na categoria de compactador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-146">The following example registers the RLE encoder filter in the video compressor category.</span></span> <span data-ttu-id="e6b1c-147">Para obter detalhes, consulte [como registrar filtros do DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="e6b1c-147">For details, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="e6b1c-148">Certifique-se de ler a seção [diretrizes para registrar filtros](guidelines-for-registering-filters.md), que descreve as práticas recomendadas para o registro de filtro.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-148">Be sure to read the section [Guidelines for Registering Filters](guidelines-for-registering-filters.md), which describes the recommended practices for filter registration.</span></span>


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



<span data-ttu-id="e6b1c-149">Além disso, os filtros não precisam ser empacotados dentro de DLLs.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-149">Also, filters do not have to be packaged inside DLLs.</span></span> <span data-ttu-id="e6b1c-150">Em alguns casos, você pode escrever um filtro especializado que é projetado apenas para um aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-150">In some cases, you might write a specialized filter that is designed only for a specific application.</span></span> <span data-ttu-id="e6b1c-151">Nesse caso, você pode compilar a classe de filtro diretamente em seu aplicativo e criá-la com o `new` operador, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="e6b1c-151">In that case, you can compile the filter class directly in your application, and create it with the `new` operator, as shown in the following example:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e6b1c-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e6b1c-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6b1c-153">Conexão inteligente</span><span class="sxs-lookup"><span data-stu-id="e6b1c-153">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> <dt>

[<span data-ttu-id="e6b1c-154">Gravando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="e6b1c-154">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="e6b1c-155">Gravando filtros de transformação</span><span class="sxs-lookup"><span data-stu-id="e6b1c-155">Writing Transform Filters</span></span>](writing-transform-filters.md)
</dt> </dl>

 

 
