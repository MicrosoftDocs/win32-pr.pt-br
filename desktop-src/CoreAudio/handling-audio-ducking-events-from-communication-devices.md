---
description: A Experiência de Ressalvamento Padrão fornecida pelo sistema faz com que todos os fluxos de não comunicação disponíveis no sistema quando um fluxo de comunicação é aberto.
ms.assetid: 1b92574e-7cde-49c0-a68e-223492412361
title: Considerações de implementação para notificações de replicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f61d7e67bd456e962442f62f59c3119c756258aadd75334e7736cbc69fba0867
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957315"
---
# <a name="implementation-considerations-for-ducking-notifications"></a>Considerações de implementação para notificações de replicação

A Experiência de Ressalvamento Padrão fornecida pelo sistema faz com que todos os fluxos de não comunicação disponíveis no sistema quando um fluxo de comunicação é aberto. [](stream-attenuation.md) Um aplicativo de mídia pode substituir o tratamento padrão se souber quando a sessão de comunicação é iniciada e termina.

Considere o cenário implementado pelo aplicativo de mídia no [exemplo DedingMediaPlayer.](duckingmediaplayer.md) O aplicativo pausa o fluxo de áudio que ele está reproduzindo quando recebe uma notificação de adoção e continua a reprodução quando recebe uma notificação de desuso. Os eventos pause e continue são refletidos na interface do usuário do aplicativo de mídia. Isso é suportado por meio de duas mensagens de janela definidas pelo aplicativo, WM \_ APP \_ SESSION \_ HACKED e WM APP SESSION \_ \_ UND \_ WM. As notificações de replicação são recebidas de forma assíncrona em segundo plano e o aplicativo de mídia não deve bloquear o thread de notificação para processar as mensagens da janela. As mensagens da janela devem ser processadas no thread da interface do usuário.

O comportamento de ressalvação funciona por meio de um mecanismo de notificação. Para fornecer uma experiência personalizada, o aplicativo de mídia deve implementar a interface [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) e registrar a implementação com o sistema de áudio. Após o registro bem-sucedido, o aplicativo de mídia recebe notificações de eventos na forma de retornos de chamada por meio dos métodos na interface . O gerenciador de sessão que está tratando a sessão de comunicação chama [**IAudioVolumeDuckNotification::OnVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeducknotification) quando o fluxo de comunicação é aberto e chama [**IAudioVolumeDuckNotification::OnVolumeUnduckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeunducknotification) quando o fluxo é fechado no dispositivo de comunicação.

O código a seguir mostra uma implementação de exemplo da interface [**IAudioVolumeDuckNotification.**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) Para obter a definição de CMediaPlayer::D uckingOptOut, consulte Obter eventos de alvo de um dispositivo de comunicação.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando um dispositivo de comunicação](using-the-communication-device.md)
</dt> <dt>

[Experiência padrão de ressalvamento](stream-attenuation.md)
</dt> <dt>

[Desabilitando a experiência de ressalvamento padrão](disabling-the-ducking-experience.md)
</dt> <dt>

[Fornecendo um comportamento de desaqueamento personalizado](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Obter eventos de desaqueamento](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



