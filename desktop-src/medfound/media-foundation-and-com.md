---
description: Microsoft Media Foundation usa uma combinação de construções COM, mas não é uma API totalmente baseada em COM.
ms.assetid: d58ca46f-8f3a-4a12-b948-1ea7ab568788
title: Media Foundation e COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb7d05bac6a3f4deef2c004c6980ef1351c3823
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105769646"
---
# <a name="media-foundation-and-com"></a><span data-ttu-id="dc4da-103">Media Foundation e COM</span><span class="sxs-lookup"><span data-stu-id="dc4da-103">Media Foundation and COM</span></span>

<span data-ttu-id="dc4da-104">Microsoft Media Foundation usa uma combinação de construções COM, mas não é uma API totalmente baseada em COM.</span><span class="sxs-lookup"><span data-stu-id="dc4da-104">Microsoft Media Foundation uses a mix of COM constructs, but is not a fully COM-based API.</span></span> <span data-ttu-id="dc4da-105">Este tópico descreve a interação entre COM e Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="dc4da-105">This topic describes the interaction between COM and Media Foundation.</span></span> <span data-ttu-id="dc4da-106">Ele também define algumas práticas recomendadas para o desenvolvimento de Media Foundation componentes de plug-in.</span><span class="sxs-lookup"><span data-stu-id="dc4da-106">It also defines some best practices for developing Media Foundation plug-in components.</span></span> <span data-ttu-id="dc4da-107">Seguir essas práticas pode ajudá-lo a evitar alguns erros de programação comuns, mas sutis.</span><span class="sxs-lookup"><span data-stu-id="dc4da-107">Following these practices can help you to avoid some common but subtle programming errors.</span></span>

-   [<span data-ttu-id="dc4da-108">Práticas recomendadas para aplicativos</span><span class="sxs-lookup"><span data-stu-id="dc4da-108">Best Practices for Applications</span></span>](#best-practices-for-applications)
-   [<span data-ttu-id="dc4da-109">Práticas recomendadas para componentes de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dc4da-109">Best Practices for Media Foundation Components</span></span>](#best-practices-for-media-foundation-components)
-   [<span data-ttu-id="dc4da-110">Resumo</span><span class="sxs-lookup"><span data-stu-id="dc4da-110">Summary</span></span>](#summary)
-   [<span data-ttu-id="dc4da-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dc4da-111">Related topics</span></span>](#related-topics)

## <a name="best-practices-for-applications"></a><span data-ttu-id="dc4da-112">Práticas recomendadas para aplicativos</span><span class="sxs-lookup"><span data-stu-id="dc4da-112">Best Practices for Applications</span></span>

<span data-ttu-id="dc4da-113">No Media Foundation, o processamento assíncrono e os retornos de chamada são tratados por [filas de trabalho](work-queues.md).</span><span class="sxs-lookup"><span data-stu-id="dc4da-113">In Media Foundation, asynchronous processing and callbacks are handled by [work queues](work-queues.md).</span></span> <span data-ttu-id="dc4da-114">As filas de trabalho sempre têm threads de MTA (multithreaded apartment), de modo que um aplicativo terá uma implementação mais simples se for executado em um thread MTA também.</span><span class="sxs-lookup"><span data-stu-id="dc4da-114">Work queues always have multithreaded apartment (MTA) threads, so an application will have a simpler implementation if it runs on an MTA thread as well.</span></span> <span data-ttu-id="dc4da-115">Portanto, é recomendável chamar [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) com o sinalizador de **\_ vários threads de coinit** .</span><span class="sxs-lookup"><span data-stu-id="dc4da-115">Therefore, it is recommended to call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) with the **COINIT\_MULTITHREADED** flag.</span></span>

<span data-ttu-id="dc4da-116">Media Foundation não empacota objetos STA (single-threaded apartment) para threads de fila de trabalho.</span><span class="sxs-lookup"><span data-stu-id="dc4da-116">Media Foundation does not marshal single-threaded apartment (STA) objects to work queue threads.</span></span> <span data-ttu-id="dc4da-117">Nem garante que as invariáveis de STA sejam mantidas.</span><span class="sxs-lookup"><span data-stu-id="dc4da-117">Nor does it ensure that STA invariants are maintained.</span></span> <span data-ttu-id="dc4da-118">Portanto, um aplicativo STA deve ter cuidado para não passar objetos STA ou proxies para Media Foundation APIs.</span><span class="sxs-lookup"><span data-stu-id="dc4da-118">Therefore, an STA application must be careful to not pass STA objects or proxies to Media Foundation APIs.</span></span> <span data-ttu-id="dc4da-119">Os objetos que são somente STA não têm suporte no Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="dc4da-119">Objects that are STA-only are not supported in Media Foundation.</span></span>

<span data-ttu-id="dc4da-120">Se você tiver um proxy STA para um MTA ou um objeto de thread livre, o objeto poderá ser empacotado para um proxy MTA usando um retorno de chamada de fila de trabalho.</span><span class="sxs-lookup"><span data-stu-id="dc4da-120">If you have an STA proxy to an MTA or free-threaded object, the object can be marshaled to an MTA proxy by using a work-queue callback.</span></span> <span data-ttu-id="dc4da-121">A função [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pode retornar um ponteiro bruto ou um proxy STA, dependendo do modelo de objeto definido no registro para esse CLSID.</span><span class="sxs-lookup"><span data-stu-id="dc4da-121">The [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function can return either a raw pointer or an STA proxy, depending on the object model defined in the registry for that CLSID.</span></span> <span data-ttu-id="dc4da-122">Se um proxy STA for retornado, você não deverá passar o ponteiro para uma API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="dc4da-122">If an STA proxy is returned, you must not pass the pointer to a Media Foundation API.</span></span>

<span data-ttu-id="dc4da-123">Por exemplo, suponha que você queira passar um ponteiro **IPropertyStore** para o método [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) .</span><span class="sxs-lookup"><span data-stu-id="dc4da-123">For example, suppose that you want to pass an **IPropertyStore** pointer to the [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) method.</span></span> <span data-ttu-id="dc4da-124">Você pode chamar **PSCreateMemoryPropertyStore** para criar o ponteiro **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="dc4da-124">You might call **PSCreateMemoryPropertyStore** to create the **IPropertyStore** pointer.</span></span> <span data-ttu-id="dc4da-125">Se você estiver chamando de um STA, deverá realizar marshaling do ponteiro antes de passá-lo para **BeginCreateObjectFromURL**.</span><span class="sxs-lookup"><span data-stu-id="dc4da-125">If you are calling from an STA, you must marshal the pointer before passing it to **BeginCreateObjectFromURL**.</span></span>

<span data-ttu-id="dc4da-126">O código a seguir mostra como realizar marshaling de um proxy STA para uma API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="dc4da-126">The following code shows how to marshal an STA proxy to a Media Foundation API.</span></span>


```C++
class CCreateSourceMarshalCallback
    : public IMFAsyncCallback
{
public:
    CCreateSourceMarshalCallback(
        LPCWSTR szURL, 
        IMFSourceResolver* pResolver, 
        IPropertyStore* pSourceProps, 
        IMFAsyncCallback* pCompletionCallback, 
        HRESULT& hr
        )
        : m_szURL(szURL), 
          m_pResolver(pResolver), 
          m_pCompletionCallback(pCompletionCallback),
          m_pGIT(NULL),
          m_cRef(1)
    {
        hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable, NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&m_pGIT));

        if(SUCCEEDED(hr))
        {
            hr = m_pGIT->RegisterInterfaceInGlobal(
                pSourceProps, IID_IPropertyStore, &m_dwInterfaceCookie);
        }
    }
    ~CCreateSourceMarshalCallback()
    {
        SafeRelease(&m_pResolver);
        SafeRelease(&m_pCompletionCallback);
        SafeRelease(&m_pGIT);
    }


    STDMETHOD_(ULONG, AddRef)()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHOD_(ULONG, Release)()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (0 == cRef)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHOD(QueryInterface)(REFIID riid, LPVOID* ppvObject)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CCreateSourceMarshalCallback, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppvObject);

    }

    STDMETHOD(GetParameters)(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        return E_NOTIMPL;
    }

    STDMETHOD(Invoke)(IMFAsyncResult* pResult)
    {
        IPropertyStore *pSourceProps = NULL;

        HRESULT hr = m_pGIT->GetInterfaceFromGlobal(
            m_dwInterfaceCookie, 
            IID_PPV_ARGS(&pSourceProps)
            );

        if(SUCCEEDED(hr))
        {
            hr = m_pResolver->BeginCreateObjectFromURL(
                m_szURL, MF_RESOLUTION_MEDIASOURCE, pSourceProps, NULL, 
                m_pCompletionCallback, NULL);
        }

        SafeRelease(&pSourceProps);
        return hr;
    }

private:
    LPCWSTR m_szURL;
    IMFSourceResolver *m_pResolver;
    IMFAsyncCallback *m_pCompletionCallback;
    IGlobalInterfaceTable *m_pGIT;
    DWORD m_dwInterfaceCookie;
    LONG m_cRef;
};
```



<span data-ttu-id="dc4da-127">Para obter mais informações sobre a tabela de interface global, consulte [**IGlobalInterfaceTable**](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span><span class="sxs-lookup"><span data-stu-id="dc4da-127">For more information about the global interface table, see [**IGlobalInterfaceTable**](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span></span>

<span data-ttu-id="dc4da-128">Se você estiver usando Media Foundation em processo, os objetos retornados de Media Foundation métodos e funções serão ponteiros diretos para o objeto.</span><span class="sxs-lookup"><span data-stu-id="dc4da-128">If you are using Media Foundation in-process, objects returned from Media Foundation methods and functions are direct pointers to the object.</span></span> <span data-ttu-id="dc4da-129">Para Media Foundation de processo cruzado, esses objetos podem ser proxies MTA e devem ser empacotados em um thread STA, se necessário.</span><span class="sxs-lookup"><span data-stu-id="dc4da-129">For cross-process Media Foundation, these objects may be MTA proxies, and should be marshaled into an STA thread if needed there.</span></span> <span data-ttu-id="dc4da-130">Da mesma forma, os objetos obtidos dentro de um retorno de chamada — por exemplo, uma topologia do evento [MESessionTopologyStatus](mesessiontopologystatus.md) — são ponteiros diretos quando Media Foundation é usado em processo, mas são proxies MTA quando Media Foundation é usado em processo cruzado.</span><span class="sxs-lookup"><span data-stu-id="dc4da-130">Similarly, objects obtained inside a callback — for example, a topology from the [MESessionTopologyStatus](mesessiontopologystatus.md) event — are direct pointers when Media Foundation is used in-process, but are MTA proxies when Media Foundation is used cross-process.</span></span>

> [!Note]  
> <span data-ttu-id="dc4da-131">O cenário mais comum para usar Media Foundation processo cruzado é com o [caminho de mídia protegido](protected-media-path.md) (PMP).</span><span class="sxs-lookup"><span data-stu-id="dc4da-131">The most common scenario for using Media Foundation cross-process is with the [Protected Media Path](protected-media-path.md) (PMP).</span></span> <span data-ttu-id="dc4da-132">No entanto, esses comentários se aplicam a qualquer situação quando Media Foundation APIs são usadas por meio de RPC.</span><span class="sxs-lookup"><span data-stu-id="dc4da-132">However, these remarks apply to any situation when Media Foundation APIs are used through RPC.</span></span>

 

<span data-ttu-id="dc4da-133">Todas as implementações de [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) devem ser compatíveis com o MTA.</span><span class="sxs-lookup"><span data-stu-id="dc4da-133">All implementations of [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) should be MTA-compatible.</span></span> <span data-ttu-id="dc4da-134">Esses objetos não precisam ser objetos COM.</span><span class="sxs-lookup"><span data-stu-id="dc4da-134">These objects do not need to be COM objects at all.</span></span> <span data-ttu-id="dc4da-135">Mas, se estiverem, eles não poderão ser executados no STA.</span><span class="sxs-lookup"><span data-stu-id="dc4da-135">But if they are, they cannot run in the STA.</span></span> <span data-ttu-id="dc4da-136">A função [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) será invocada em um thread de fila de pesquisa MTA e o objeto [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) fornecido será um ponteiro de objeto direto ou um proxy MTA.</span><span class="sxs-lookup"><span data-stu-id="dc4da-136">The [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) function will be invoked on an MTA workqueue thread, and the provided [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) object will be either a direct object pointer or an MTA proxy.</span></span>

## <a name="best-practices-for-media-foundation-components"></a><span data-ttu-id="dc4da-137">Práticas recomendadas para componentes de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dc4da-137">Best Practices for Media Foundation Components</span></span>

<span data-ttu-id="dc4da-138">Há duas categorias de objetos Media Foundation que precisam se preocupar COM o COM.</span><span class="sxs-lookup"><span data-stu-id="dc4da-138">There are two categories of Media Foundation objects that need to be concerned about COM.</span></span> <span data-ttu-id="dc4da-139">Alguns componentes, como transformações ou manipuladores de fluxo de bytes, são objetos COM completos criados pelo CLSID.</span><span class="sxs-lookup"><span data-stu-id="dc4da-139">Some components, such as transforms or byte stream handlers, are full COM objects created by CLSID.</span></span> <span data-ttu-id="dc4da-140">Esses objetos devem seguir as regras para Apartments COM, para Media Foundation em processo e em processo cruzado.</span><span class="sxs-lookup"><span data-stu-id="dc4da-140">These objects must follow the rules for COM apartments, for both in-process and cross-process Media Foundation.</span></span> <span data-ttu-id="dc4da-141">Outros componentes de Media Foundation não são objetos COM completos, mas precisam de proxies COM para reprodução entre processos.</span><span class="sxs-lookup"><span data-stu-id="dc4da-141">Other Media Foundation components are not full COM objects, but do need COM proxies for cross-process playback.</span></span> <span data-ttu-id="dc4da-142">Os objetos nessa categoria incluem fontes de mídia e objeto de ativação.</span><span class="sxs-lookup"><span data-stu-id="dc4da-142">Objects in this category include media sources and activation object.</span></span> <span data-ttu-id="dc4da-143">Esses objetos poderão ignorar problemas de apartamento se eles forem usados apenas para Media Foundation em processo.</span><span class="sxs-lookup"><span data-stu-id="dc4da-143">These objects can ignore apartment issues if they will be used only for in-process Media Foundation.</span></span>

<span data-ttu-id="dc4da-144">Embora nem todos os objetos de Media Foundation sejam objetos COM, todas as interfaces de Media Foundation derivam de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="dc4da-144">Although not all Media Foundation objects are COM objects, all Media Foundation interfaces derive from [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="dc4da-145">Portanto, todos os objetos de Media Foundation devem implementar **IUnknown** de acordo com as especificações com, incluindo as regras para contagem de referência e [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="dc4da-145">Therefore, all Media Foundation objects must implement **IUnknown** according to COM specifications, including the rules for reference counting and [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="dc4da-146">Todos os objetos de referência contados também devem garantir que o [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) não permitirá que o módulo seja descarregado enquanto os objetos ainda persistirem.</span><span class="sxs-lookup"><span data-stu-id="dc4da-146">All reference counted objects should also ensure that [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) will not allow the module to be unloaded while the objects still persist.</span></span>

<span data-ttu-id="dc4da-147">Os componentes de Media Foundation não podem ser objetos STA.</span><span class="sxs-lookup"><span data-stu-id="dc4da-147">Media Foundation components cannot be STA objects.</span></span> <span data-ttu-id="dc4da-148">Muitos objetos de Media Foundation não precisam ser objetos COM.</span><span class="sxs-lookup"><span data-stu-id="dc4da-148">Many Media Foundation objects do not need to be COM objects at all.</span></span> <span data-ttu-id="dc4da-149">Mas, se estiverem, eles não poderão ser executados no STA.</span><span class="sxs-lookup"><span data-stu-id="dc4da-149">But if they are, they cannot run in the STA.</span></span> <span data-ttu-id="dc4da-150">Todos os componentes de Media Foundation devem ser thread-safe.</span><span class="sxs-lookup"><span data-stu-id="dc4da-150">All Media Foundation components must be thread-safe.</span></span> <span data-ttu-id="dc4da-151">Alguns objetos de Media Foundation devem ser de thread livre ou de apartamento neutro também.</span><span class="sxs-lookup"><span data-stu-id="dc4da-151">Some Media Foundation objects must be free-threaded or apartment-neutral as well.</span></span> <span data-ttu-id="dc4da-152">A tabela a seguir especifica os requisitos para implementações de interface personalizada:</span><span class="sxs-lookup"><span data-stu-id="dc4da-152">The following table specifies the requirements for custom interface implementations:</span></span>



| <span data-ttu-id="dc4da-153">Interface</span><span class="sxs-lookup"><span data-stu-id="dc4da-153">Interface</span></span>                                                          | <span data-ttu-id="dc4da-154">Category</span><span class="sxs-lookup"><span data-stu-id="dc4da-154">Category</span></span>            | <span data-ttu-id="dc4da-155">Apartamento necessário</span><span class="sxs-lookup"><span data-stu-id="dc4da-155">Required apartment</span></span>       |
|--------------------------------------------------------------------|---------------------|--------------------------|
| [<span data-ttu-id="dc4da-156">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="dc4da-156">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)                                 | <span data-ttu-id="dc4da-157">Proxy de processo cruzado</span><span class="sxs-lookup"><span data-stu-id="dc4da-157">Cross-process proxy</span></span> | <span data-ttu-id="dc4da-158">Livre de threads ou neutros</span><span class="sxs-lookup"><span data-stu-id="dc4da-158">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="dc4da-159">**IMFByteStreamHandler**</span><span class="sxs-lookup"><span data-stu-id="dc4da-159">**IMFByteStreamHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)               | <span data-ttu-id="dc4da-160">Objeto COM</span><span class="sxs-lookup"><span data-stu-id="dc4da-160">COM object</span></span>          | <span data-ttu-id="dc4da-161">MTA</span><span class="sxs-lookup"><span data-stu-id="dc4da-161">MTA</span></span>                      |
| [<span data-ttu-id="dc4da-162">**IMFContentProtectionManager**</span><span class="sxs-lookup"><span data-stu-id="dc4da-162">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) | <span data-ttu-id="dc4da-163">Proxy de processo cruzado</span><span class="sxs-lookup"><span data-stu-id="dc4da-163">Cross-process proxy</span></span> | <span data-ttu-id="dc4da-164">Livre de threads ou neutros</span><span class="sxs-lookup"><span data-stu-id="dc4da-164">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="dc4da-165">**IMFQualityManager**</span><span class="sxs-lookup"><span data-stu-id="dc4da-165">**IMFQualityManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)                     | <span data-ttu-id="dc4da-166">Objeto COM</span><span class="sxs-lookup"><span data-stu-id="dc4da-166">COM object</span></span>          | <span data-ttu-id="dc4da-167">Livre de threads ou neutros</span><span class="sxs-lookup"><span data-stu-id="dc4da-167">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="dc4da-168">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="dc4da-168">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                           | <span data-ttu-id="dc4da-169">Proxy de processo cruzado</span><span class="sxs-lookup"><span data-stu-id="dc4da-169">Cross-process proxy</span></span> | <span data-ttu-id="dc4da-170">Livre de threads ou neutros</span><span class="sxs-lookup"><span data-stu-id="dc4da-170">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="dc4da-171">**IMFSchemeHandler**</span><span class="sxs-lookup"><span data-stu-id="dc4da-171">**IMFSchemeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)                       | <span data-ttu-id="dc4da-172">Objeto COM</span><span class="sxs-lookup"><span data-stu-id="dc4da-172">COM object</span></span>          | <span data-ttu-id="dc4da-173">MTA</span><span class="sxs-lookup"><span data-stu-id="dc4da-173">MTA</span></span>                      |
| [<span data-ttu-id="dc4da-174">**IMFTopoLoader**</span><span class="sxs-lookup"><span data-stu-id="dc4da-174">**IMFTopoLoader**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)                             | <span data-ttu-id="dc4da-175">Objeto COM</span><span class="sxs-lookup"><span data-stu-id="dc4da-175">COM object</span></span>          | <span data-ttu-id="dc4da-176">Livre de threads ou neutros</span><span class="sxs-lookup"><span data-stu-id="dc4da-176">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="dc4da-177">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="dc4da-177">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                               | <span data-ttu-id="dc4da-178">Objeto COM</span><span class="sxs-lookup"><span data-stu-id="dc4da-178">COM object</span></span>          | <span data-ttu-id="dc4da-179">MTA</span><span class="sxs-lookup"><span data-stu-id="dc4da-179">MTA</span></span>                      |



 

<span data-ttu-id="dc4da-180">Pode haver requisitos adicionais, dependendo da implementação.</span><span class="sxs-lookup"><span data-stu-id="dc4da-180">There may be additional requirements depending upon the implementation.</span></span> <span data-ttu-id="dc4da-181">Por exemplo, se um coletor de mídia implementar outra interface que permita que o aplicativo faça chamadas de função diretas para o coletor, o coletor precisaria ser de thread livre ou neutro, para que pudesse lidar com chamadas diretas de processos cruzados.</span><span class="sxs-lookup"><span data-stu-id="dc4da-181">For example, if a media sink implements another interface that enables the application to make direct function calls to the sink, the sink would need to be free-threaded or neutral, so that it could handle direct cross-process calls.</span></span> <span data-ttu-id="dc4da-182">Qualquer objeto pode ser de segmento livre; Esta tabela especifica os requisitos mínimos.</span><span class="sxs-lookup"><span data-stu-id="dc4da-182">Any object may be free-threaded; this table specifies the minimum requirements.</span></span>

<span data-ttu-id="dc4da-183">A maneira recomendada para implementar objetos livres de threads ou neutros é agregar o marshaler de thread livre.</span><span class="sxs-lookup"><span data-stu-id="dc4da-183">The recommended way to implement free-threaded or neutral objects is by aggregating the free-threaded marshaler.</span></span> <span data-ttu-id="dc4da-184">Para obter mais detalhes, consulte a documentação do MSDN em [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler).</span><span class="sxs-lookup"><span data-stu-id="dc4da-184">For more details, see the MSDN documentation on [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler).</span></span> <span data-ttu-id="dc4da-185">De acordo com o requisito de não passar objetos STA ou proxies para Media Foundation APIs, os objetos de thread livre não precisam se preocupar com o marshaling de ponteiros de entrada STA em componentes de thread livre.</span><span class="sxs-lookup"><span data-stu-id="dc4da-185">In accordance with the requirement not to pass STA objects or proxies to Media Foundation APIs, free-threaded objects do not need to worry about marshaling STA input pointers in free-threaded components.</span></span>

<span data-ttu-id="dc4da-186">Os componentes que usam a fila de trabalho de função longa (**\_ \_ \_ \_ função longa da fila de retorno de chamada MFASYNC**) devem exercer mais cuidado.</span><span class="sxs-lookup"><span data-stu-id="dc4da-186">Components that use the long-function work queue (**MFASYNC\_CALLBACK\_QUEUE\_LONG\_FUNCTION**) must exercise more care.</span></span> <span data-ttu-id="dc4da-187">Os threads na fila de funções de longa duração criam seu próprio STA.</span><span class="sxs-lookup"><span data-stu-id="dc4da-187">Threads in the long function workqueue create their own STA.</span></span> <span data-ttu-id="dc4da-188">Os componentes que usam a fila de funções de longa duração para retornos de chamada devem evitar a criação de objetos COM nesses threads e precisam ter cuidado para realizar marshaling de proxies para o STA, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="dc4da-188">Components that use the long function workqueue for callbacks should avoid creating COM objects on these threads, and need to be careful to marshal proxies to the STA as necessary.</span></span>

## <a name="summary"></a><span data-ttu-id="dc4da-189">Resumo</span><span class="sxs-lookup"><span data-stu-id="dc4da-189">Summary</span></span>

<span data-ttu-id="dc4da-190">Os aplicativos terão um tempo mais fácil se interagirem com Media Foundation de um thread MTA, mas é possível ter cuidado ao usar Media Foundation de um thread STA.</span><span class="sxs-lookup"><span data-stu-id="dc4da-190">Applications will have an easier time if they interact with Media Foundation from an MTA thread, but it is possible with some care to use Media Foundation from an STA thread.</span></span> <span data-ttu-id="dc4da-191">Media Foundation não trata componentes STA, e os aplicativos devem ter cuidado para não passar objetos STA para Media Foundation APIs.</span><span class="sxs-lookup"><span data-stu-id="dc4da-191">Media Foundation does not handle STA components, and applications should be careful not to pass STA objects to Media Foundation APIs.</span></span> <span data-ttu-id="dc4da-192">Alguns objetos têm requisitos adicionais, especialmente objetos executados em uma situação de processo cruzado.</span><span class="sxs-lookup"><span data-stu-id="dc4da-192">Some objects have additional requirements, especially objects that run in a cross-process situation.</span></span> <span data-ttu-id="dc4da-193">Seguir essas diretrizes ajudará a evitar erros COM, deadlocks e atrasos inesperados no processamento de mídia.</span><span class="sxs-lookup"><span data-stu-id="dc4da-193">Following these guidelines will help avoid COM errors, deadlocks, and unexpected delays in media processing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc4da-194">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dc4da-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc4da-195">APIs da plataforma Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dc4da-195">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> <dt>

[<span data-ttu-id="dc4da-196">Arquitetura Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dc4da-196">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 
