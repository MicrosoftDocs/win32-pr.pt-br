---
description: Usando o resolvedor de origem
ms.assetid: 94e2a411-96b8-4506-8491-78f4f5f286ce
title: Usando o resolvedor de origem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e992199b097ff3f3337f92216b684d68e46bca13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165284"
---
# <a name="using-the-source-resolver"></a><span data-ttu-id="d09ec-103">Usando o resolvedor de origem</span><span class="sxs-lookup"><span data-stu-id="d09ec-103">Using the Source Resolver</span></span>

<span data-ttu-id="d09ec-104">O resolvedor de origem utiliza um fluxo de bytes ou uma URL e cria a origem de mídia adequada para esse conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d09ec-104">The source resolver takes a URL or byte stream and creates the appropriate media source for that content.</span></span> <span data-ttu-id="d09ec-105">Para criar o resolvedor de origem, chame [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver).</span><span class="sxs-lookup"><span data-stu-id="d09ec-105">To create the source resolver, call [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver).</span></span> <span data-ttu-id="d09ec-106">Essa função retorna um ponteiro de interface [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) .</span><span class="sxs-lookup"><span data-stu-id="d09ec-106">This function returns an [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) interface pointer.</span></span>

<span data-ttu-id="d09ec-107">O resolvedor de origem tem métodos síncronos e assíncronos.</span><span class="sxs-lookup"><span data-stu-id="d09ec-107">The source resolver has both synchronous and asynchronous methods.</span></span> <span data-ttu-id="d09ec-108">Se você estiver usando o resolvedor de origem do seu thread de aplicativo principal, os métodos assíncronos tornarão sua interface do usuário mais responsiva.</span><span class="sxs-lookup"><span data-stu-id="d09ec-108">If you are using the source resolver from your main application thread, the asynchronous methods will make your user interface more responsive.</span></span> <span data-ttu-id="d09ec-109">Os métodos síncronos podem ser bloqueados por um período de tempo perceptível, especialmente se o resolvedor de origem precisar abrir um recurso de rede.</span><span class="sxs-lookup"><span data-stu-id="d09ec-109">The synchronous methods can block for a noticeable amount of time, particularly if the source resolver must open a network resource.</span></span>

<span data-ttu-id="d09ec-110">Os métodos síncronos são:</span><span class="sxs-lookup"><span data-stu-id="d09ec-110">The synchronous methods are:</span></span>

-   [<span data-ttu-id="d09ec-111">**IMFSourceResolver::CreateObjectFromURL**</span><span class="sxs-lookup"><span data-stu-id="d09ec-111">**IMFSourceResolver::CreateObjectFromURL**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)
-   [<span data-ttu-id="d09ec-112">**IMFSourceResolver::CreateObjectFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="d09ec-112">**IMFSourceResolver::CreateObjectFromByteStream**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream)

<span data-ttu-id="d09ec-113">Os métodos assíncronos são:</span><span class="sxs-lookup"><span data-stu-id="d09ec-113">The asynchronous methods are:</span></span>

-   [<span data-ttu-id="d09ec-114">**IMFSourceResolver::BeginCreateObjectFromURL**</span><span class="sxs-lookup"><span data-stu-id="d09ec-114">**IMFSourceResolver::BeginCreateObjectFromURL**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)
-   [<span data-ttu-id="d09ec-115">**IMFSourceResolver::BeginCreateObjectFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="d09ec-115">**IMFSourceResolver::BeginCreateObjectFromByteStream**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream)

<span data-ttu-id="d09ec-116">Para os métodos assíncronos, cada método tem um método **end...** correspondente para concluir a solicitação assíncrona e um método **Cancel...** para cancelar uma solicitação pendente.</span><span class="sxs-lookup"><span data-stu-id="d09ec-116">For the asynchronous methods, each method has a corresponding **End...** method to complete the asynchronous request, and a **Cancel...** method to cancel a pending request.</span></span> <span data-ttu-id="d09ec-117">Para obter mais informações sobre métodos assíncronos no Media Foundation, consulte [métodos de retorno de chamada assíncrono](asynchronous-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="d09ec-117">For more information about asynchronous methods in Media Foundation, see [Asynchronous Callback Methods](asynchronous-callback-methods.md).</span></span>

<span data-ttu-id="d09ec-118">O exemplo de código a seguir cria uma fonte de mídia de uma URL.</span><span class="sxs-lookup"><span data-stu-id="d09ec-118">The following code example creates a media source from a URL.</span></span> <span data-ttu-id="d09ec-119">Este exemplo usa o método síncrono.</span><span class="sxs-lookup"><span data-stu-id="d09ec-119">This example uses the synchronous method.</span></span>


```C++
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="d09ec-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d09ec-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d09ec-121">Resolvedor de origem</span><span class="sxs-lookup"><span data-stu-id="d09ec-121">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 



