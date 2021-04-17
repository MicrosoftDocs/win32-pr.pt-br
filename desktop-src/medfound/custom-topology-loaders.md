---
description: Carregadores de topologia personalizados
ms.assetid: 3982b07e-3179-45c1-9f17-f2114363f53d
title: Carregadores de topologia personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a8f9e24b207d43620e7b2d09080d244b0a9e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768231"
---
# <a name="custom-topology-loaders"></a><span data-ttu-id="dad2d-103">Carregadores de topologia personalizados</span><span class="sxs-lookup"><span data-stu-id="dad2d-103">Custom Topology Loaders</span></span>

<span data-ttu-id="dad2d-104">Quando um aplicativo enfileira uma topologia parcial na sessão de mídia, a sessão de mídia usa um carregador de topologia para resolver a topologia.</span><span class="sxs-lookup"><span data-stu-id="dad2d-104">When an application queues a partial topology on the Media Session, the Media Session uses a topology loader to resolve the topology.</span></span> <span data-ttu-id="dad2d-105">Por padrão, a sessão de mídia usa a implementação de Media Foundation padrão do carregador de topologia, mas você também pode fornecer uma implementação personalizada.</span><span class="sxs-lookup"><span data-stu-id="dad2d-105">By default, the Media Session uses the standard Media Foundation implementation of the topology loader, but you can also provide a custom implementation.</span></span> <span data-ttu-id="dad2d-106">Isso lhe dá mais controle sobre a topologia final.</span><span class="sxs-lookup"><span data-stu-id="dad2d-106">This gives you more control over the final topology.</span></span> <span data-ttu-id="dad2d-107">Um carregador de topologia personalizado deve implementar a interface [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) .</span><span class="sxs-lookup"><span data-stu-id="dad2d-107">A custom topology loader must implement the [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) interface.</span></span>

<span data-ttu-id="dad2d-108">Para definir um carregador de topologia personalizado na sessão de mídia, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="dad2d-108">To set a custom topology loader on the Media Session, do the following:</span></span>

1.  <span data-ttu-id="dad2d-109">Crie um repositório de atributos vazio chamando [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span><span class="sxs-lookup"><span data-stu-id="dad2d-109">Create an empty attribute store by calling [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>
2.  <span data-ttu-id="dad2d-110">Defina o [**atributo \_ \_ TOPOLOADER da sessão MF**](mf-session-topoloader-attribute.md) no repositório de atributos.</span><span class="sxs-lookup"><span data-stu-id="dad2d-110">Set the [**MF\_SESSION\_TOPOLOADER**](mf-session-topoloader-attribute.md) attribute on the attribute store.</span></span> <span data-ttu-id="dad2d-111">O valor do atributo é o CLSID do carregador personalizado.</span><span class="sxs-lookup"><span data-stu-id="dad2d-111">The value of the attribute is the CLSID of your custom loader.</span></span>
3.  <span data-ttu-id="dad2d-112">Chame [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para criar a sessão de mídia para conteúdo desprotegido ou [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) para criar a sessão de mídia dentro do caminho de mídia protegido (PMP).</span><span class="sxs-lookup"><span data-stu-id="dad2d-112">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create the Media Session for unprotected content, or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) to create the Media Session inside the protected media path (PMP).</span></span>

> [!Note]  
> <span data-ttu-id="dad2d-113">Para usar um carregador de topologia personalizado dentro do PMP, o carregador de topologia deve ser um componente confiável.</span><span class="sxs-lookup"><span data-stu-id="dad2d-113">To use a custom topology loader inside the PMP, the topology loader must be a trusted component.</span></span> <span data-ttu-id="dad2d-114">Para obter mais informações, consulte [proteção de caminho de mídia](protected-media-path.md).</span><span class="sxs-lookup"><span data-stu-id="dad2d-114">For more information, see [Protected Media Path](protected-media-path.md).</span></span>

 

<span data-ttu-id="dad2d-115">O código a seguir mostra como definir um carregador de topologia personalizado na sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="dad2d-115">The following code shows how to set a custom topology loader on the Media Session.</span></span>


```C++
HRESULT CreateSession_CustomTopoLoader(REFCLSID clsid, IMFMediaSession **ppSession)
{
    *ppSession = NULL;

    IMFMediaSession *pSession = NULL;
    IMFAttributes *pConfig = NULL;

    // Create an attribute store to configure the media session.
    HRESULT hr = MFCreateAttributes(&pConfig, 1);

    // Set the CLSID of the custom topology loader.
    if (SUCCEEDED(hr))
    {
        hr = pConfig->SetGUID(MF_SESSION_TOPOLOADER, clsid);
    }

    // Create the media session.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaSession(pConfig, &pSession);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppSession = pSession;
        (*ppSession)->AddRef();
    }

    SafeRelease(&pSession);
    SafeRelease(&pConfig);

    return hr;
}
```



<span data-ttu-id="dad2d-116">Não é necessário implementar todo o algoritmo de carregamento de topologia em seu carregador de topologia.</span><span class="sxs-lookup"><span data-stu-id="dad2d-116">It is not necessary to implement the entire topology-loading algorithm in your topology loader.</span></span> <span data-ttu-id="dad2d-117">Como alternativa, você pode encapsular o carregador de topologia de Media Foundation padrão.</span><span class="sxs-lookup"><span data-stu-id="dad2d-117">As an alternative, you can wrap the standard Media Foundation topology loader.</span></span> <span data-ttu-id="dad2d-118">Em sua implementação do método [**IMFTopoLoader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) , modifique a topologia conforme necessário e passe a topologia modificada para o carregador de topologia padrão.</span><span class="sxs-lookup"><span data-stu-id="dad2d-118">In your implementation of the [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method, modify the topology as needed and pass the modified topology to the standard topology loader.</span></span> <span data-ttu-id="dad2d-119">Em seguida, o carregador de topologia padrão conclui a topologia.</span><span class="sxs-lookup"><span data-stu-id="dad2d-119">Then the standard topology loader completes the topology.</span></span> <span data-ttu-id="dad2d-120">Você também pode modificar a topologia concluída antes de passá-la de volta para a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="dad2d-120">You can also modify the completed topology before passing it back to the Media Session.</span></span>

<span data-ttu-id="dad2d-121">O código a seguir mostra o contorno geral dessa abordagem.</span><span class="sxs-lookup"><span data-stu-id="dad2d-121">The following code shows the general outline of this approach.</span></span> <span data-ttu-id="dad2d-122">Ele não mostra nenhum detalhe do método [**Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) , pois isso dependerá dos requisitos específicos do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dad2d-122">It does not show any details of the [**Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method, because these will depend on the particular requirements of your application.</span></span>


```C++
class CTopoLoader : public IMFTopoLoader
{
public:

    static HRESULT CreateInstance(REFIID iid, void **ppv)
    {
        HRESULT hr = S_OK;

        CTopoLoader *pTopoLoader = new (std::nothrow) CTopoLoader(&hr);
        
        if (pTopoLoader == NULL)
        {
            return E_OUTOFMEMORY;
        }

        if (SUCCEEDED(hr))
        {
            hr = pTopoLoader->QueryInterface(iid, ppv);
        }

        SafeRelease(&pTopoLoader);
        return hr;
    }

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CTopoLoader, IMFTopoLoader),
            { 0 },
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        long cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    // IMTopoLoader methods.
    STDMETHODIMP Load(
        IMFTopology *pInput, 
        IMFTopology **ppOutput, 
        IMFTopology *pCurrent
        )
    {
        HRESULT hr = S_OK;

        // TODO: Add custom topology-building code here.
        //       Modify pInput as needed.

        if (SUCCEEDED(hr))
        {
            hr = m_pTopoLoader->Load(pInput, ppOutput, pCurrent);
        }

        // TODO: Add custom topology-building code here.
        //       Modify ppOutput as needed.

        return hr;
    }

private:
    CTopoLoader(HRESULT *phr) : m_cRef(1), m_pTopoLoader(NULL)
    {
        *phr = MFCreateTopoLoader(&m_pTopoLoader);
    }

    virtual ~CTopoLoader()
    {
        SafeRelease(&m_pTopoLoader);
    }

private:
    long            m_cRef;          // Reference count.
    IMFTopoLoader   *m_pTopoLoader;  // Standard topoloader.
};
```



## <a name="related-topics"></a><span data-ttu-id="dad2d-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dad2d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dad2d-124">**MFCreateTopoLoader**</span><span class="sxs-lookup"><span data-stu-id="dad2d-124">**MFCreateTopoLoader**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader)
</dt> <dt>

[<span data-ttu-id="dad2d-125">Criação de topologia avançada</span><span class="sxs-lookup"><span data-stu-id="dad2d-125">Advanced Topology Building</span></span>](advanced-topology-building.md)
</dt> </dl>

 

 



