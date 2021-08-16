---
description: Um aplicativo de mídia que deseja fornecer uma experiência de replicação personalizada deve escutar as notificações de eventos quando um fluxo de comunicação é aberto ou fechado no sistema.
ms.assetid: 709ad912-6b03-4ad3-bc47-ad8b6bd6de45
title: Obter eventos de desaqueamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5869aa02a64ef3b7d035743b9bee3c91d295448c4d89d659862c5efc81d89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828257"
---
# <a name="getting-ducking-events"></a>Obter eventos de desaqueamento

Um aplicativo de mídia que deseja fornecer uma experiência de replicação personalizada deve escutar as notificações de eventos quando um fluxo de comunicação é aberto ou fechado no sistema. A implementação personalizada pode ser fornecida usando MediaFoundation, DirectShow ou DirectSound, que usam as APIs de Áudio Principal. Um cliente WASAPI direto também poderá substituir o tratamento padrão se souber quando a sessão de comunicação é iniciada e termina.

Para fornecer uma implementação personalizada, um aplicativo de mídia precisa obter notificações do sistema quando um aplicativo de comunicação inicia ou encerra um fluxo de comunicação. O aplicativo de mídia deve implementar a interface [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) e registrar a implementação com o sistema de áudio. Após o registro bem-sucedido, o aplicativo de mídia recebe notificações de eventos na forma de retornos de chamada por meio dos métodos na interface . Para obter mais informações, consulte [Considerações de implementação para notificações de replicação.](handling-audio-ducking-events-from-communication-devices.md)

Para enviar notificações de ressaltos, o sistema de áudio deve saber qual sessão de áudio está escutando os eventos de ressaltos. Cada sessão de áudio é identificada exclusivamente com um GUID – identificador de instância de sessão. O gerenciador de sessão permite que um aplicativo receba informações sobre a sessão, como o título da sessão de áudio, o estado de renderização e o identificador da instância de sessão. O identificador pode ser recuperado usando a interface de controle de política, [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2).

As etapas a seguir resumem o processo de obter o identificador de instância de sessão do aplicativo de mídia:

1.  Insinue o enumerador de dispositivo e use-o para obter uma referência ao ponto de extremidade do dispositivo que o aplicativo de mídia está usando para renderizar o fluxo de não comunicação.
2.  Ative o gerenciador de sessão do ponto de extremidade do dispositivo e receba uma referência à interface [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) do gerenciador de sessão.
3.  Usando o ponteiro [**IAudioSessionManager2,**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) obter uma referência à interface [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) do gerenciador de sessão.
4.  Consulte o [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) da interface [**IAudioSessionControl.**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
5.  Chame [**IAudioSessionControl2::GetSessionInstanceIdentifier**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) e recupere uma cadeia de caracteres que contém o identificador de sessão para a sessão de áudio atual.

Para obter notificações de redução sobre fluxos de comunicação, o aplicativo de mídia chama [**IAudioSessionManager2::RegisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification). O aplicativo de mídia fornece seu identificador de instância de sessão para o sistema de áudio e um ponteiro para a implementação [**IAudioVolumeDuckNotification.**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) O aplicativo agora pode receber notificação de eventos quando um fluxo é aberto no dispositivo de comunicação. Para interromper a notificação, o aplicativo de mídia deve chamar [**IAudioSessionManager2::UnregisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification).

O código a seguir mostra como um aplicativo pode se registrar para receber notificações de replicação. A classe CMediaPlayer é definida em [Considerações de implementação para notificações de ressalto.](handling-audio-ducking-events-from-communication-devices.md) O [exemplo de DuckingMediaPlayer](duckingmediaplayer.md) implementa essa funcionalidade.


```C++
////////////////////////////////////////////////////////////////////
//Description: Registers for duck notifications depending on the 
//             the ducking options specified by the caller.
//Parameters: 
//    If DuckingOptOutChecked is TRUE, the client is registered for
//    to receive ducking notifications; 
//    FALSE, the client's registration is deleted.
////////////////////////////////////////////////////////////////////

HRESULT CMediaPlayer::DuckingOptOut(bool DuckingOptOutChecked)
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator* pDeviceEnumerator NULL;
    IMMDevice* pEndpoint = NULL;
    IAudioSessionManager2* pSessionManager2 = NULL;
    IAudioSessionControl* pSessionControl = NULL;
    IAudioSessionControl2* pSessionControl2 = NULL;

    LPWSTR sessionId = NULL;

    //  Start with the default endpoint.

    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), 
                          NULL, 
                          CLSCTX_INPROC_SERVER, 
                          IID_PPV_ARGS(&pDeviceEnumerator));
    
    if (SUCCEEDED(hr))
    {
        hr = pDeviceEnumerator>GetDefaultAudioEndpoint(
              eRender, eConsole, &pEndpoint);

        pDeviceEnumerator>Release();
        pDeviceEnumerator = NULL;
    }

    // Activate the session manager.
    if (SUCCEEDED(hr))
    {
        hr = pEndpoint->Activate(__uuidof(IAudioSessionManager2), 
                                 CLSCTX_INPROC_SERVER,
                                 NULL, 
                                 reinterpret_cast<void **>
                                 (&pSessionManager2));
        pEndpoint->Release();
        pEndpoint = NULL;
    }
    if (SUCCEEDED(hr))
    {
        hr = pSessionManager2->GetAudioSessionControl(
                                  NULL, 0, &pSessionControl);
        
    }

    if (SUCCEEDED(hr))
    {
        hr = pSessionControl->QueryInterface(
                               IID_PPV_ARGS(&pSessionControl2));
                
        pSessionControl->Release();
        pSessionControl = NULL;
    }

    // Get the session instance identifier.
    
    if (SUCCEEDED(hr))
    {
        hr = pSessionControl2->GetSessionInstanceIdentifier(
                                 sessionId);
                
        pSessionControl2->Release();
        pSessionControl2 = NULL;
    }

    //  Register for ducking events depending on 
    //  the specified preference.

    if (SUCCEEDED(hr))
    {
        if (DuckingOptOutChecked)
        {
            hr = pSessionManager2->RegisterDuckNotification(
                                    sessionId, this);
        }
        else
        {
            hr = pSessionManager2->UnregisterDuckNotification
                                      (FALSE);
        }
        pSessionManager2->Release();
        pSessionManager2 = NULL;
    }
    return hr;
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

[Considerações de implementação para notificações de replicação](handling-audio-ducking-events-from-communication-devices.md)
</dt> </dl>

 

 



