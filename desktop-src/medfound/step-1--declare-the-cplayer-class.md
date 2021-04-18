---
description: Este tópico é a etapa 1 do tutorial como reproduzir arquivos de mídia com Media Foundation.
ms.assetid: 10767bbf-3b47-4df1-be73-18678397c0ab
title: 'Etapa 1: declarar a classe CPlayer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1593842ecece68fcd3c4cca35a7e2e28eac503c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793617"
---
# <a name="step-1-declare-the-cplayer-class"></a><span data-ttu-id="515a8-103">Etapa 1: declarar a classe CPlayer</span><span class="sxs-lookup"><span data-stu-id="515a8-103">Step 1: Declare the CPlayer Class</span></span>

<span data-ttu-id="515a8-104">Este tópico é a etapa 1 do tutorial [como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="515a8-104">This topic is step 1 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="515a8-105">O código completo é mostrado no exemplo de [reprodução de sessão de mídia](media-session-playback-example.md)do tópico.</span><span class="sxs-lookup"><span data-stu-id="515a8-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="515a8-106">Neste tutorial, a funcionalidade de reprodução é encapsulada na `CPlayer` classe.</span><span class="sxs-lookup"><span data-stu-id="515a8-106">In this tutorial, playback functionality is encapsulated in the `CPlayer` class.</span></span> <span data-ttu-id="515a8-107">A classe `CPlayer` é declarada da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="515a8-107">The `CPlayer` class is declared as follows:</span></span>


```C++
const UINT WM_APP_PLAYER_EVENT = WM_APP + 1;   

    // WPARAM = IMFMediaEvent*, WPARAM = MediaEventType

enum PlayerState
{
    Closed = 0,     // No session.
    Ready,          // Session was created, ready to open a file. 
    OpenPending,    // Session is opening a file.
    Started,        // Session is playing a file.
    Paused,         // Session is paused.
    Stopped,        // Session is stopped (ready to play). 
    Closing         // Application has closed the session, but is waiting for MESessionClosed.
};

class CPlayer : public IMFAsyncCallback
{
public:
    static HRESULT CreateInstance(HWND hVideo, HWND hEvent, CPlayer **ppPlayer);

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IMFAsyncCallback methods
    STDMETHODIMP  GetParameters(DWORD*, DWORD*)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
    STDMETHODIMP  Invoke(IMFAsyncResult* pAsyncResult);

    // Playback
    HRESULT       OpenURL(const WCHAR *sURL);
    HRESULT       Play();
    HRESULT       Pause();
    HRESULT       Stop();
    HRESULT       Shutdown();
    HRESULT       HandleEvent(UINT_PTR pUnkPtr);
    PlayerState   GetState() const { return m_state; }

    // Video functionality
    HRESULT       Repaint();
    HRESULT       ResizeVideo(WORD width, WORD height);
    
    BOOL          HasVideo() const { return (m_pVideoDisplay != NULL);  }

protected:
    
    // Constructor is private. Use static CreateInstance method to instantiate.
    CPlayer(HWND hVideo, HWND hEvent);

    // Destructor is private. Caller should call Release.
    virtual ~CPlayer(); 

    HRESULT Initialize();
    HRESULT CreateSession();
    HRESULT CloseSession();
    HRESULT StartPlayback();

    // Media event handlers
    virtual HRESULT OnTopologyStatus(IMFMediaEvent *pEvent);
    virtual HRESULT OnPresentationEnded(IMFMediaEvent *pEvent);
    virtual HRESULT OnNewPresentation(IMFMediaEvent *pEvent);

    // Override to handle additional session events.
    virtual HRESULT OnSessionEvent(IMFMediaEvent*, MediaEventType) 
    { 
        return S_OK; 
    }

protected:
    long                    m_nRefCount;        // Reference count.

    IMFMediaSession         *m_pSession;
    IMFMediaSource          *m_pSource;
    IMFVideoDisplayControl  *m_pVideoDisplay;

    HWND                    m_hwndVideo;        // Video window.
    HWND                    m_hwndEvent;        // App window to receive events.
    PlayerState             m_state;            // Current state of the media session.
    HANDLE                  m_hCloseEvent;      // Event to wait on while closing.
};
```



<span data-ttu-id="515a8-108">Aqui estão algumas coisas a serem observadas `CPlayer` :</span><span class="sxs-lookup"><span data-stu-id="515a8-108">Here are some things to note about `CPlayer`:</span></span>

-   <span data-ttu-id="515a8-109">O **evento de \_ \_ player de \_ aplicativo do WM** constante define uma mensagem de janela privada.</span><span class="sxs-lookup"><span data-stu-id="515a8-109">The constant **WM\_APP\_PLAYER\_EVENT** defines a private window message.</span></span> <span data-ttu-id="515a8-110">Essa mensagem é usada para notificar o aplicativo sobre eventos de sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="515a8-110">This message is used to notify the application about Media Session events.</span></span> <span data-ttu-id="515a8-111">Consulte [Step 5: tratar eventos de sessão de mídia](step-5--handle-media-session-events.md).</span><span class="sxs-lookup"><span data-stu-id="515a8-111">See [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md).</span></span>
-   <span data-ttu-id="515a8-112">A `PlayerState` enumeração define os possíveis Estados do `CPlayer` objeto.</span><span class="sxs-lookup"><span data-stu-id="515a8-112">The `PlayerState` enumeration defines the possible states of the `CPlayer` object.</span></span>
-   <span data-ttu-id="515a8-113">A `CPlayer` classe implementa a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , que é usada para obter notificações de eventos da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="515a8-113">The `CPlayer` class implements the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface, which is used to get event notifications from the Media Session.</span></span>
-   <span data-ttu-id="515a8-114">O `CPlayer` Construtor é privado.</span><span class="sxs-lookup"><span data-stu-id="515a8-114">The `CPlayer` constructor is private.</span></span> <span data-ttu-id="515a8-115">O aplicativo chama o `CreateInstance` método estático para criar uma instância da `CPlayer` classe.</span><span class="sxs-lookup"><span data-stu-id="515a8-115">The application calls the static `CreateInstance` method to create an instance of the `CPlayer` class.</span></span>
-   <span data-ttu-id="515a8-116">O `CPlayer` destruidor também é privado.</span><span class="sxs-lookup"><span data-stu-id="515a8-116">The `CPlayer` destructor is also private.</span></span> <span data-ttu-id="515a8-117">A `CPlayer` classe implementa **IUnknown**, portanto, o tempo de vida do objeto é controlado por meio de sua contagem de referência (*m \_ nRefCount*).</span><span class="sxs-lookup"><span data-stu-id="515a8-117">The `CPlayer` class implements **IUnknown**, so the object's lifetime is controlled through its reference count (*m\_nRefCount*).</span></span> <span data-ttu-id="515a8-118">Para destruir o objeto, o aplicativo chama **IUnknown:: Release**, não **delete**.</span><span class="sxs-lookup"><span data-stu-id="515a8-118">To destroy the object, the application calls **IUnknown::Release**, not **delete**.</span></span>
-   <span data-ttu-id="515a8-119">O `CPlayer` objeto gerencia a sessão de mídia e a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="515a8-119">The `CPlayer` object manages both the Media Session and the media source.</span></span>

## <a name="implement-iunknown"></a><span data-ttu-id="515a8-120">Implementar IUnknown</span><span class="sxs-lookup"><span data-stu-id="515a8-120">Implement IUnknown</span></span>

<span data-ttu-id="515a8-121">A `CPlayer` classe implementa [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback), que herda **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="515a8-121">The `CPlayer` class implements [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback), which inherits **IUnknown**.</span></span>

<span data-ttu-id="515a8-122">O código mostrado aqui é uma implementação razoavelmente padrão de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="515a8-122">The code shown here is a fairly standard implementation of **IUnknown**.</span></span> <span data-ttu-id="515a8-123">Se preferir, você pode usar o Active Template Library (ATL) para implementar esses métodos.</span><span class="sxs-lookup"><span data-stu-id="515a8-123">If you prefer, you can use the Active Template Library (ATL) to implement these methods.</span></span> <span data-ttu-id="515a8-124">No entanto, `CPlayer` o não oferece suporte a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ou a qualquer recurso com avançado, portanto, não há um motivo impressionante para usar o ATL aqui.</span><span class="sxs-lookup"><span data-stu-id="515a8-124">However, `CPlayer` does not support [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) or any advanced COM features, so there is no overwhelming reason to use ATL here.</span></span>


```C++
HRESULT CPlayer::QueryInterface(REFIID riid, void** ppv)
{
    static const QITAB qit[] = 
    {
        QITABENT(CPlayer, IMFAsyncCallback),
        { 0 }
    };
    return QISearch(this, qit, riid, ppv);
}

ULONG CPlayer::AddRef()
{
    return InterlockedIncrement(&m_nRefCount);
}

ULONG CPlayer::Release()
{
    ULONG uCount = InterlockedDecrement(&m_nRefCount);
    if (uCount == 0)
    {
        delete this;
    }
    return uCount;
}
```



<span data-ttu-id="515a8-125">Em seguida: [etapa 2: criar o objeto CPlayer](step-2--create-the-cplayer-object.md)</span><span class="sxs-lookup"><span data-stu-id="515a8-125">Next: [Step 2: Create the CPlayer Object](step-2--create-the-cplayer-object.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="515a8-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="515a8-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="515a8-127">Reprodução de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="515a8-127">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="515a8-128">Como reproduzir arquivos de mídia com Media Foundation</span><span class="sxs-lookup"><span data-stu-id="515a8-128">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
