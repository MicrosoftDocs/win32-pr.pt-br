---
description: A experiência de pato padrão fornecida pelo sistema patos todos os fluxos de não comunicação disponíveis no sistema quando um fluxo de comunicação é aberto.
ms.assetid: 1b92574e-7cde-49c0-a68e-223492412361
title: Considerações de implementação para notificações de pato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3de07ea23b7cdc8d726ab68a5a6554bf1713a921
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089323"
---
# <a name="implementation-considerations-for-ducking-notifications"></a><span data-ttu-id="01640-103">Considerações de implementação para notificações de pato</span><span class="sxs-lookup"><span data-stu-id="01640-103">Implementation Considerations for Ducking Notifications</span></span>

<span data-ttu-id="01640-104">A [experiência de pato padrão](stream-attenuation.md) fornecida pelo sistema patos todos os fluxos de não comunicação disponíveis no sistema quando um fluxo de comunicação é aberto.</span><span class="sxs-lookup"><span data-stu-id="01640-104">The [Default Ducking Experience](stream-attenuation.md) provided by the system ducks all non-communication streams available in the system when a communication stream opens.</span></span> <span data-ttu-id="01640-105">Um aplicativo de mídia pode substituir o tratamento padrão se ele sabe quando a sessão de comunicação começa e termina.</span><span class="sxs-lookup"><span data-stu-id="01640-105">A media application can override the default handling if it knows when the communication session starts and ends.</span></span>

<span data-ttu-id="01640-106">Considere o cenário implementado pelo aplicativo de mídia no exemplo [DuckingMediaPlayer](duckingmediaplayer.md) .</span><span class="sxs-lookup"><span data-stu-id="01640-106">Consider the scenario implemented by the media application in the [DuckingMediaPlayer](duckingmediaplayer.md) sample.</span></span> <span data-ttu-id="01640-107">O aplicativo pausa o fluxo de áudio que está sendo reproduzido quando recebe uma notificação pato e continua a reprodução quando recebe uma notificação não pato.</span><span class="sxs-lookup"><span data-stu-id="01640-107">The application pauses the audio stream that it is playing when it receives a duck notification and continues playback when it receives an unduck notification.</span></span> <span data-ttu-id="01640-108">Os eventos Pause e continue são refletidos na interface do usuário do aplicativo de mídia.</span><span class="sxs-lookup"><span data-stu-id="01640-108">The pause and continue events are reflected in the media application's user interface.</span></span> <span data-ttu-id="01640-109">Há suporte para isso por meio de duas mensagens de janela definidas pelo aplicativo, a sessão do aplicativo do WM foi \_ \_ \_ zerada e a sessão do aplicativo do WM foi \_ \_ \_ despato.</span><span class="sxs-lookup"><span data-stu-id="01640-109">This is supported through two application-defined window messages, WM\_APP\_SESSION\_DUCKED and WM\_APP\_SESSION\_UNDUCKED.</span></span> <span data-ttu-id="01640-110">As notificações de pato são recebidas de forma assíncrona em segundo plano e o aplicativo de mídia não deve bloquear o thread de notificação para processar as mensagens da janela.</span><span class="sxs-lookup"><span data-stu-id="01640-110">The ducking notifications are received asynchronously in the background and the media application must not block the notification thread to process the window messages.</span></span> <span data-ttu-id="01640-111">As mensagens de janela devem ser processadas no thread da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="01640-111">The window messages must be processed on the user interface thread.</span></span>

<span data-ttu-id="01640-112">O comportamento do pato funciona por meio de um mecanismo de notificação.</span><span class="sxs-lookup"><span data-stu-id="01640-112">The ducking behavior works through a notification mechanism.</span></span> <span data-ttu-id="01640-113">Para fornecer uma experiência personalizada, o aplicativo de mídia deve implementar a interface [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) e registrar a implementação com o sistema de áudio.</span><span class="sxs-lookup"><span data-stu-id="01640-113">To provide a customized experience, the media application must implement the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) interface and register the implementation with the audio system.</span></span> <span data-ttu-id="01640-114">Após o registro bem-sucedido, o aplicativo de mídia recebe notificações de eventos na forma de retornos de chamada por meio dos métodos na interface.</span><span class="sxs-lookup"><span data-stu-id="01640-114">Upon successful registration, the media application receives event notifications in the form of callbacks through the methods in the interface.</span></span> <span data-ttu-id="01640-115">O Gerenciador de sessão que manipula as chamadas de sessão de comunicação [**IAudioVolumeDuckNotification:: OnVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeducknotification) quando o fluxo de comunicação é aberto e, em seguida, chama [**IAudioVolumeDuckNotification:: OnVolumeUnduckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeunducknotification) quando o fluxo é fechado no dispositivo de comunicação.</span><span class="sxs-lookup"><span data-stu-id="01640-115">The session manager handling the communication session calls [**IAudioVolumeDuckNotification::OnVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeducknotification) when the communication stream opens and then calls [**IAudioVolumeDuckNotification::OnVolumeUnduckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeunducknotification) when the stream is closed on the communication device.</span></span>

<span data-ttu-id="01640-116">O código a seguir mostra uma implementação de exemplo da interface [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) .</span><span class="sxs-lookup"><span data-stu-id="01640-116">The following code shows a sample implementation of the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) interface.</span></span> <span data-ttu-id="01640-117">Para obter a definição de CMediaPlayer::D uckingOptOut, consulte obtendo eventos de pato de um dispositivo de comunicação.</span><span class="sxs-lookup"><span data-stu-id="01640-117">For the definition of CMediaPlayer::DuckingOptOut, see Getting Ducking Events from a Communication Device.</span></span>


```C++
class CMediaPlayer : public IAudioVolumeDuckNotification
{
    LONG _refCount;

    HWND _AppWindow;

    ~CMediaPlayer();

    STDMETHOD(OnVolumeDuckNotification) (LPCWSTR sessionID, 
                  UINT32 countCommunicationSessions);
    STDMETHOD(OnVolumeUnduckNotification) (LPCWSTR sessionID);

public:
    CDuckingImpl(HWND hWnd);
    HRESULT DuckingOptOut(bool GetDuckEvents);

    // IUnknown
    IFACEMETHODIMP QueryInterface(__in REFIID riid, __deref_out void **ppv);
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
};

CMediaPlayer::CMediaPlayer(HWND AppWindow) :
        _AppWindow(AppWindow),
        _refCount(1)
{
}
CMediaPlayer::~CMediaPlayer()
{
}

// When we receive a duck notification, 
// post a "Session Ducked" message to the application window.

STDMETHODIMP CMediaPlayer::OnVolumeDuckNotification(LPCWSTR SessionID, 
                                                    UINT32 CountCommunicationsSessions)
{
    PostMessage(_AppWindow, WM_APP_SESSION_DUCKED, 0, 0);
    return 0;
}


// When we receive an unduck notification, 
// post a "Session Unducked" message to the application window.

STDMETHODIMP CMediaPlayer::OnVolumeUnduckNotification(LPCWSTR SessionID)
{
    PostMessage(_AppWindow, WM_APP_SESSION_UNDUCKED, 0, 0);
    return 0;
}

IFACEMETHODIMP CMediaPlayer::QueryInterface(REFIID iid, void **pvObject)
{
    if (pvObject == NULL)
    {
        return E_POINTER;
    }
    *pvObject = NULL;
    if (iid == IID_IUnknown)
    {
        *pvObject = static_cast<IUnknown *>(static_cast<IAudioVolumeDuckNotification *>
                                                                              (this));
        AddRef();
    }
    else if (iid == __uuidof(IAudioVolumeDuckNotification))
    {
        *pvObject = static_cast<IAudioVolumeDuckNotification *>(this);
        AddRef();
    }
    else
    {
        return E_NOINTERFACE;
    }
    return S_OK;
}

IFACEMETHODIMP_(ULONG) CMediaPlayer::AddRef()
{
    return InterlockedIncrement(&_refCount);
}

IFACEMETHODIMP_(ULONG) CMediaPlayer::Release()
{
    LONG refs = InterlockedDecrement(&_refCount);

    if (refs == 0)
    {
        delete this; 
    }

    return refs;   
}
```



## <a name="related-topics"></a><span data-ttu-id="01640-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="01640-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01640-119">Usando um dispositivo de comunicação</span><span class="sxs-lookup"><span data-stu-id="01640-119">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="01640-120">Experiência de pato padrão</span><span class="sxs-lookup"><span data-stu-id="01640-120">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="01640-121">Desabilitando a experiência de pato padrão</span><span class="sxs-lookup"><span data-stu-id="01640-121">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="01640-122">Fornecendo um comportamento personalizado de pato</span><span class="sxs-lookup"><span data-stu-id="01640-122">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="01640-123">Obtendo eventos de pato</span><span class="sxs-lookup"><span data-stu-id="01640-123">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



