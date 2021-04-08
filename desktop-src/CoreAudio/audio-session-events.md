---
description: Eventos de sessão de áudio
ms.assetid: 6943b405-0807-412b-a149-fc3a8ece1b48
title: Eventos de sessão de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ec5de18c883f817c2f650ccfc48ad0149ac84e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920371"
---
# <a name="audio-session-events"></a><span data-ttu-id="77a24-103">Eventos de sessão de áudio</span><span class="sxs-lookup"><span data-stu-id="77a24-103">Audio Session Events</span></span>

<span data-ttu-id="77a24-104">Um aplicativo que gerencia fluxos de áudio de modo compartilhado pode se registrar para receber notificações quando ocorrerem eventos de sessão.</span><span class="sxs-lookup"><span data-stu-id="77a24-104">An application that manages shared-mode audio streams can register to receive notifications when session events occur.</span></span> <span data-ttu-id="77a24-105">Conforme explicado anteriormente, cada fluxo pertence a uma [sessão de áudio](audio-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="77a24-105">As explained previously, each stream belongs to an [audio session](audio-sessions.md).</span></span> <span data-ttu-id="77a24-106">Um evento de sessão é iniciado por uma alteração no status de uma sessão de áudio.</span><span class="sxs-lookup"><span data-stu-id="77a24-106">A session event is initiated by a change in the status of an audio session.</span></span>

<span data-ttu-id="77a24-107">Um aplicativo cliente pode se registrar para receber notificações dos seguintes tipos de eventos de sessão:</span><span class="sxs-lookup"><span data-stu-id="77a24-107">A client application can register to receive notifications of the following types of session events:</span></span>

-   <span data-ttu-id="77a24-108">O nível de volume mestre ou o estado de mudo da sessão submix foi alterado.</span><span class="sxs-lookup"><span data-stu-id="77a24-108">The master volume level or muting state of the session submix has changed.</span></span>
-   <span data-ttu-id="77a24-109">O nível de volume de um ou mais canais da sessão submix foi alterado.</span><span class="sxs-lookup"><span data-stu-id="77a24-109">The volume level of one or more channels of the session submix has changed.</span></span>
-   <span data-ttu-id="77a24-110">A sessão foi desconectada.</span><span class="sxs-lookup"><span data-stu-id="77a24-110">The session has been disconnected.</span></span>
-   <span data-ttu-id="77a24-111">O estado da atividade da sessão foi alterado para ativo, inativo ou expirado.</span><span class="sxs-lookup"><span data-stu-id="77a24-111">The activity state of the session has changed to active, inactive, or expired.</span></span>
-   <span data-ttu-id="77a24-112">Um novo parâmetro de agrupamento foi atribuído à sessão.</span><span class="sxs-lookup"><span data-stu-id="77a24-112">The session has been assigned a new grouping parameter.</span></span>
-   <span data-ttu-id="77a24-113">Uma propriedade de interface de usuário da sessão (ícone ou nome de exibição) foi alterada.</span><span class="sxs-lookup"><span data-stu-id="77a24-113">A user-interface property of the session (icon or display name) has changed.</span></span>

<span data-ttu-id="77a24-114">O cliente recebe notificações desses eventos por meio dos métodos em sua implementação da interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) .</span><span class="sxs-lookup"><span data-stu-id="77a24-114">The client receives notifications of these events through the methods in its implementation of the [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface.</span></span> <span data-ttu-id="77a24-115">Ao contrário das outras interfaces no WASAPI, que são implementadas pelo módulo do sistema WASAPI, o cliente implementa **IAudioSessionEvents**.</span><span class="sxs-lookup"><span data-stu-id="77a24-115">Unlike the other interfaces in WASAPI, which are implemented by the WASAPI system module, the client implements **IAudioSessionEvents**.</span></span> <span data-ttu-id="77a24-116">Os métodos nesta interface recebem retornos de chamada do módulo do sistema WASAPI quando ocorrem eventos de sessão.</span><span class="sxs-lookup"><span data-stu-id="77a24-116">The methods in this interface receive callbacks from the WASAPI system module when session events occur.</span></span>

<span data-ttu-id="77a24-117">Para começar a receber notificações, o cliente chama o método [**IAudioSessionControl:: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) para registrar sua interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) .</span><span class="sxs-lookup"><span data-stu-id="77a24-117">To begin receiving notifications, the client calls the [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) method to register its [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface.</span></span> <span data-ttu-id="77a24-118">Quando o cliente não requer mais notificações, ele chama o método [**IAudioSessionControl:: UnregisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification) para excluir o registro.</span><span class="sxs-lookup"><span data-stu-id="77a24-118">When the client no longer requires notifications, it calls the [**IAudioSessionControl::UnregisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification) method to delete the registration.</span></span>

<span data-ttu-id="77a24-119">O exemplo de código a seguir mostra uma implementação possível da interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) :</span><span class="sxs-lookup"><span data-stu-id="77a24-119">The following code example shows a possible implementation of the [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface:</span></span>


```C++
//-----------------------------------------------------------
// Client implementation of IAudioSessionEvents interface.
// WASAPI calls these methods to notify the application when
// a parameter or property of the audio session changes.
//-----------------------------------------------------------
class CAudioSessionEvents : public IAudioSessionEvents
{
    LONG _cRef;

public:
    CAudioSessionEvents() :
        _cRef(1)
    {
    }

    ~CAudioSessionEvents()
    {
    }

    // IUnknown methods -- AddRef, Release, and QueryInterface

    ULONG STDMETHODCALLTYPE AddRef()
    {
        return InterlockedIncrement(&_cRef);
    }

    ULONG STDMETHODCALLTYPE Release()
    {
        ULONG ulRef = InterlockedDecrement(&_cRef);
        if (0 == ulRef)
        {
            delete this;
        }
        return ulRef;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(
                                REFIID  riid,
                                VOID  **ppvInterface)
    {
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IAudioSessionEvents) == riid)
        {
            AddRef();
            *ppvInterface = (IAudioSessionEvents*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }

    // Notification methods for audio session events

    HRESULT STDMETHODCALLTYPE OnDisplayNameChanged(
                                LPCWSTR NewDisplayName,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnIconPathChanged(
                                LPCWSTR NewIconPath,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnSimpleVolumeChanged(
                                float NewVolume,
                                BOOL NewMute,
                                LPCGUID EventContext)
    {
        if (NewMute)
        {
            printf("MUTE\n");
        }
        else
        {
            printf("Volume = %d percent\n",
                   (UINT32)(100*NewVolume + 0.5));
        }

        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnChannelVolumeChanged(
                                DWORD ChannelCount,
                                float NewChannelVolumeArray[],
                                DWORD ChangedChannel,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnGroupingParamChanged(
                                LPCGUID NewGroupingParam,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnStateChanged(
                                AudioSessionState NewState)
    {
        char *pszState = "?????";

        switch (NewState)
        {
        case AudioSessionStateActive:
            pszState = "active";
            break;
        case AudioSessionStateInactive:
            pszState = "inactive";
            break;
        }
        printf("New session state = %s\n", pszState);

        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnSessionDisconnected(
              AudioSessionDisconnectReason DisconnectReason)
    {
        char *pszReason = "?????";

        switch (DisconnectReason)
        {
        case DisconnectReasonDeviceRemoval:
            pszReason = "device removed";
            break;
        case DisconnectReasonServerShutdown:
            pszReason = "server shut down";
            break;
        case DisconnectReasonFormatChanged:
            pszReason = "format changed";
            break;
        case DisconnectReasonSessionLogoff:
            pszReason = "user logged off";
            break;
        case DisconnectReasonSessionDisconnected:
            pszReason = "session disconnected";
            break;
        case DisconnectReasonExclusiveModeOverride:
            pszReason = "exclusive-mode override";
            break;
        }
        printf("Audio session disconnected (reason: %s)\n",
               pszReason);

        return S_OK;
    }
};
```



<span data-ttu-id="77a24-120">A classe CAudioSessionEvents no exemplo de código anterior é uma implementação da interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) .</span><span class="sxs-lookup"><span data-stu-id="77a24-120">The CAudioSessionEvents class in the preceding code example is an implementation of the [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface.</span></span> <span data-ttu-id="77a24-121">Essa implementação específica pode fazer parte de um aplicativo de console que imprime informações sobre eventos de sessão em uma janela de prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="77a24-121">This particular implementation might be part of a console application that prints information about session events to a Command Prompt window.</span></span> <span data-ttu-id="77a24-122">Como **IAudioSessionEvents** é herdado de [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), a definição de classe contém implementações dos métodos **IUnknown** [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)e [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="77a24-122">Because **IAudioSessionEvents** inherits from [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), the class definition contains implementations of the **IUnknown** methods [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), and [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="77a24-123">Os métodos públicos restantes na definição de classe são específicos para a interface **IAudioSessionEvents** .</span><span class="sxs-lookup"><span data-stu-id="77a24-123">The remaining public methods in the class definition are specific to the **IAudioSessionEvents** interface.</span></span>

<span data-ttu-id="77a24-124">Alguns clientes podem não estar interessados em monitorar todos os tipos de eventos de sessão.</span><span class="sxs-lookup"><span data-stu-id="77a24-124">Some clients might not be interested in monitoring all types of session events.</span></span> <span data-ttu-id="77a24-125">No exemplo de código anterior, vários métodos de notificação na classe CAudioSessionEvents não fazem nada.</span><span class="sxs-lookup"><span data-stu-id="77a24-125">In the preceding code example, several notification methods in the CAudioSessionEvents class do nothing.</span></span> <span data-ttu-id="77a24-126">Por exemplo, o método [**OnChannelVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged) não faz nada, exceto para retornar o código de status S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="77a24-126">For example, the [**OnChannelVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged) method does nothing except to return status code S\_OK.</span></span> <span data-ttu-id="77a24-127">Esse aplicativo não monitora volumes de canal porque não altera os volumes de canal (chamando os métodos na interface [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) ) e não compartilha a sessão com outros aplicativos que podem alterar os volumes de canal.</span><span class="sxs-lookup"><span data-stu-id="77a24-127">This application does not monitor channel volumes because it does not change the channel volumes (by calling the methods in the [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) interface), and it does not share the session with other applications that might change the channel volumes.</span></span>

<span data-ttu-id="77a24-128">Os únicos três métodos na classe CAudioSessionEvents que notificam o usuário sobre eventos de sessão são [**OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged), [**OnStateChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged)e [**OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected).</span><span class="sxs-lookup"><span data-stu-id="77a24-128">The only three methods in the CAudioSessionEvents class that notify the user of session events are [**OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged), [**OnStateChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged), and [**OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected).</span></span> <span data-ttu-id="77a24-129">Por exemplo, se o usuário executar o programa de controle de volume do sistema, SNDVOL e usar o controle de volume no SNDVOL para alterar o nível de volume do aplicativo, `OnSimpleVolumeChanged` o imprime imediatamente o novo nível de volume.</span><span class="sxs-lookup"><span data-stu-id="77a24-129">For example, if the user runs the system volume-control program, Sndvol, and uses the volume control in Sndvol to change the application's volume level, `OnSimpleVolumeChanged` immediately prints the new volume level.</span></span>

<span data-ttu-id="77a24-130">Para obter um exemplo de código que registra e cancela o registro da interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) de um cliente, consulte [eventos de áudio para aplicativos de áudio herdados](audio-events-for-legacy-audio-applications.md).</span><span class="sxs-lookup"><span data-stu-id="77a24-130">For a code example that registers and unregisters a client's [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface, see [Audio Events for Legacy Audio Applications](audio-events-for-legacy-audio-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="77a24-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="77a24-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77a24-132">Sessões de áudio</span><span class="sxs-lookup"><span data-stu-id="77a24-132">Audio Sessions</span></span>](audio-sessions.md)
</dt> </dl>

 

 
