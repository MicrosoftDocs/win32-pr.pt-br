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
# <a name="audio-session-events"></a>Eventos de sessão de áudio

Um aplicativo que gerencia fluxos de áudio de modo compartilhado pode se registrar para receber notificações quando ocorrerem eventos de sessão. Conforme explicado anteriormente, cada fluxo pertence a uma [sessão de áudio](audio-sessions.md). Um evento de sessão é iniciado por uma alteração no status de uma sessão de áudio.

Um aplicativo cliente pode se registrar para receber notificações dos seguintes tipos de eventos de sessão:

-   O nível de volume mestre ou o estado de mudo da sessão submix foi alterado.
-   O nível de volume de um ou mais canais da sessão submix foi alterado.
-   A sessão foi desconectada.
-   O estado da atividade da sessão foi alterado para ativo, inativo ou expirado.
-   Um novo parâmetro de agrupamento foi atribuído à sessão.
-   Uma propriedade de interface de usuário da sessão (ícone ou nome de exibição) foi alterada.

O cliente recebe notificações desses eventos por meio dos métodos em sua implementação da interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) . Ao contrário das outras interfaces no WASAPI, que são implementadas pelo módulo do sistema WASAPI, o cliente implementa **IAudioSessionEvents**. Os métodos nesta interface recebem retornos de chamada do módulo do sistema WASAPI quando ocorrem eventos de sessão.

Para começar a receber notificações, o cliente chama o método [**IAudioSessionControl:: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) para registrar sua interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) . Quando o cliente não requer mais notificações, ele chama o método [**IAudioSessionControl:: UnregisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification) para excluir o registro.

O exemplo de código a seguir mostra uma implementação possível da interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) :


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



A classe CAudioSessionEvents no exemplo de código anterior é uma implementação da interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) . Essa implementação específica pode fazer parte de um aplicativo de console que imprime informações sobre eventos de sessão em uma janela de prompt de comando. Como **IAudioSessionEvents** é herdado de [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), a definição de classe contém implementações dos métodos **IUnknown** [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)e [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Os métodos públicos restantes na definição de classe são específicos para a interface **IAudioSessionEvents** .

Alguns clientes podem não estar interessados em monitorar todos os tipos de eventos de sessão. No exemplo de código anterior, vários métodos de notificação na classe CAudioSessionEvents não fazem nada. Por exemplo, o método [**OnChannelVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged) não faz nada, exceto para retornar o código de status S \_ OK. Esse aplicativo não monitora volumes de canal porque não altera os volumes de canal (chamando os métodos na interface [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) ) e não compartilha a sessão com outros aplicativos que podem alterar os volumes de canal.

Os únicos três métodos na classe CAudioSessionEvents que notificam o usuário sobre eventos de sessão são [**OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged), [**OnStateChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged)e [**OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected). Por exemplo, se o usuário executar o programa de controle de volume do sistema, SNDVOL e usar o controle de volume no SNDVOL para alterar o nível de volume do aplicativo, `OnSimpleVolumeChanged` o imprime imediatamente o novo nível de volume.

Para obter um exemplo de código que registra e cancela o registro da interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) de um cliente, consulte [eventos de áudio para aplicativos de áudio herdados](audio-events-for-legacy-audio-applications.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sessões de áudio](audio-sessions.md)
</dt> </dl>

 

 
