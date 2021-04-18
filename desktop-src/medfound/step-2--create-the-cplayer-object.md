---
description: Este tópico é a etapa 2 do tutorial como reproduzir arquivos de mídia com Media Foundation.
ms.assetid: b489312f-ab8c-4ec6-8070-f5848034087e
title: 'Etapa 2: criar o objeto CPlayer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021ffa383506c0ab1be8d6c1ca327f67ed8f52f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788684"
---
# <a name="step-2-create-the-cplayer-object"></a><span data-ttu-id="1473f-103">Etapa 2: criar o objeto CPlayer</span><span class="sxs-lookup"><span data-stu-id="1473f-103">Step 2: Create the CPlayer Object</span></span>

<span data-ttu-id="1473f-104">Este tópico é a etapa 2 do tutorial [como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="1473f-104">This topic is step 2 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="1473f-105">O código completo é mostrado no exemplo de [reprodução de sessão de mídia](media-session-playback-example.md)do tópico.</span><span class="sxs-lookup"><span data-stu-id="1473f-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="1473f-106">Para criar uma instância da `CPlayer` classe, o aplicativo chama o método estático `CPlayer::CreateInstance` .</span><span class="sxs-lookup"><span data-stu-id="1473f-106">To create an instance of the `CPlayer` class, the application calls the static `CPlayer::CreateInstance` method.</span></span> <span data-ttu-id="1473f-107">Esse método usa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="1473f-107">This method takes the following parameters:</span></span>

-   <span data-ttu-id="1473f-108">*hVideo* especifica a janela para exibir o vídeo.</span><span class="sxs-lookup"><span data-stu-id="1473f-108">*hVideo* specifies the window to display video.</span></span>
-   <span data-ttu-id="1473f-109">*hEvent* especifica uma janela para receber eventos.</span><span class="sxs-lookup"><span data-stu-id="1473f-109">*hEvent* specifies a window to receive events.</span></span> <span data-ttu-id="1473f-110">É válido passar o mesmo identificador para ambos os identificadores de janela.</span><span class="sxs-lookup"><span data-stu-id="1473f-110">It is valid to pass the same handle for both window handles.</span></span>
-   <span data-ttu-id="1473f-111">*ppPlayer* recebe um ponteiro para uma nova `CPlayer` instância.</span><span class="sxs-lookup"><span data-stu-id="1473f-111">*ppPlayer* receives a pointer to a new `CPlayer` instance.</span></span>

<span data-ttu-id="1473f-112">O código a seguir mostra o `CreateInstance` método:</span><span class="sxs-lookup"><span data-stu-id="1473f-112">The following code shows the `CreateInstance` method:</span></span>


```C++
//  Static class method to create the CPlayer object.

HRESULT CPlayer::CreateInstance(
    HWND hVideo,                  // Video window.
    HWND hEvent,                  // Window to receive notifications.
    CPlayer **ppPlayer)           // Receives a pointer to the CPlayer object.
{
    if (ppPlayer == NULL)
    {
        return E_POINTER;
    }

    CPlayer *pPlayer = new (std::nothrow) CPlayer(hVideo, hEvent);
    if (pPlayer == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pPlayer->Initialize();
    if (SUCCEEDED(hr))
    {
        *ppPlayer = pPlayer;
    }
    else
    {
        pPlayer->Release();
    }
    return hr;
}

HRESULT CPlayer::Initialize()
{
    // Start up Media Foundation platform.
    HRESULT hr = MFStartup(MF_VERSION);
    if (SUCCEEDED(hr))
    {
        m_hCloseEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
        if (m_hCloseEvent == NULL)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
        }
    }
    return hr;
}
```



<span data-ttu-id="1473f-113">O código a seguir mostra o `CPlayer` Construtor:</span><span class="sxs-lookup"><span data-stu-id="1473f-113">The following code shows the `CPlayer` constructor:</span></span>


```C++
CPlayer::CPlayer(HWND hVideo, HWND hEvent) : 
    m_pSession(NULL),
    m_pSource(NULL),
    m_pVideoDisplay(NULL),
    m_hwndVideo(hVideo),
    m_hwndEvent(hEvent),
    m_state(Closed),
    m_hCloseEvent(NULL),
    m_nRefCount(1)
{
}
```



<span data-ttu-id="1473f-114">O construtor faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1473f-114">The constructor does the following:</span></span>

1.  <span data-ttu-id="1473f-115">Chama [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) para inicializar a plataforma de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="1473f-115">Calls [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) to initialize the Media Foundation platform.</span></span>
2.  <span data-ttu-id="1473f-116">Cria um evento de redefinição automática.</span><span class="sxs-lookup"><span data-stu-id="1473f-116">Creates an auto-reset event.</span></span> <span data-ttu-id="1473f-117">Esse evento é usado ao fechar a sessão de mídia; consulte [Step 7: desligar a sessão de mídia](step-7--shut-down-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="1473f-117">This event is used when closing the Media Session; see [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md).</span></span>

<span data-ttu-id="1473f-118">O destruidor desliga a sessão de mídia, conforme descrito na [etapa 7: desligar a sessão de mídia](step-7--shut-down-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="1473f-118">The destructor shuts down the Media Session, as described in [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md).</span></span>


```C++
CPlayer::~CPlayer()
{
    assert(m_pSession == NULL);  
    // If FALSE, the app did not call Shutdown().

    // When CPlayer calls IMediaEventGenerator::BeginGetEvent on the
    // media session, it causes the media session to hold a reference 
    // count on the CPlayer. 
    
    // This creates a circular reference count between CPlayer and the 
    // media session. Calling Shutdown breaks the circular reference 
    // count.

    // If CreateInstance fails, the application will not call 
    // Shutdown. To handle that case, call Shutdown in the destructor. 

    Shutdown();
}
```



<span data-ttu-id="1473f-119">Observe que o construtor e o destruidor são ambos métodos de classe protegidos.</span><span class="sxs-lookup"><span data-stu-id="1473f-119">Note that the constructor and destructor are both protected class methods.</span></span> <span data-ttu-id="1473f-120">O aplicativo cria o objeto usando o `CreateInstance` método estático.</span><span class="sxs-lookup"><span data-stu-id="1473f-120">The application creates the object using the static `CreateInstance` method.</span></span> <span data-ttu-id="1473f-121">Ele destrói o objeto chamando **IUnknown:: Release**, em vez de usar explicitamente **delete**.</span><span class="sxs-lookup"><span data-stu-id="1473f-121">It destroys the object by calling **IUnknown::Release**, rather than explicitly using **delete**.</span></span>

<span data-ttu-id="1473f-122">Em seguida: [etapa 3: abrir um arquivo de mídia](step-3--open-a-media-file.md)</span><span class="sxs-lookup"><span data-stu-id="1473f-122">Next: [Step 3: Open a Media File](step-3--open-a-media-file.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="1473f-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1473f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1473f-124">Reprodução de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="1473f-124">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="1473f-125">Como reproduzir arquivos de mídia com Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1473f-125">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



