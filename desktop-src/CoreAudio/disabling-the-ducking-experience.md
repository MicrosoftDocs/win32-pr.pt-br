---
description: Um usuário pode desabilitar a Experiência padrão de ressalvação fornecida pelo sistema usando as opções disponíveis na guia Comunicações do painel de controle Windows multimídia, Mmsys.cpl.
ms.assetid: 5604b927-99f8-450f-a48c-b38d782584de
title: Desabilitando a experiência de ressalvamento padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473b0bab8c3575d416cc72b7e931b4c85160bdaacc6031611ad80394f44b9098
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828547"
---
# <a name="disabling-the-default-ducking-experience"></a>Desabilitando a experiência de ressalvamento padrão

Um usuário pode [](stream-attenuation.md) desabilitar a Experiência padrão de ressalvamento  fornecida pelo sistema usando as opções disponíveis na guia Comunicações do painel de controle Windows multimídia, Mmsys.cpl.

Quando a replicação é aplicada, um efeito de esmaeamento e esmaeçamento é usado por um período de 1 segundo. Um aplicativo de jogo pode não querer que o fluxo de comunicação interfira no áudio do jogo. Alguns aplicativos de mídia podem achar que a experiência de reprodução está em movimento quando a música esmaece novamente. Esses tipos de aplicativos podem optar por não participar da experiência de replicação.

Programaticamente, um cliente WASAPI direto pode optar por usar o gerenciador de sessão para a sessão de áudio que fornece controle de volume para os fluxos de não comunicação. Observe que, mesmo que um cliente opte por não fazer isso, ele ainda receberá notificações de ressalvação do sistema.

Para não se desatar, o cliente deve obter uma referência à interface [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) do gerenciador de sessão. Para não usar a experiência de ressarção, use as seguintes etapas:

1.  Insinue o enumerador de dispositivo e use-o para obter uma referência ao ponto de extremidade do dispositivo que o aplicativo de mídia está usando para renderizar o fluxo de não comunicação.
2.  Ative o gerenciador de sessão do ponto de extremidade do dispositivo e receba uma referência à interface [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) do gerenciador de sessão.
3.  Usando o ponteiro [**IAudioSessionManager2,**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) obter uma referência à interface [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) do gerenciador de sessão.
4.  Consulte o [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) da interface [**IAudioSessionControl.**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
5.  Chame [**IAudioSessionControl2::SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) e passe **TRUE** ou **FALSE** para especificar a preferência de redução. A preferência especificada pode ser alterada dinamicamente durante a sessão. Observe que a alteração de aceitação não tem efeito até que o fluxo seja interrompido e iniciado novamente.

O código a seguir mostra como um aplicativo pode especificar sua preferência de replicação. O chamador da função deve passar **TRUE** ou **FALSE** no parâmetro DuckingOptOutChecked. Dependendo do valor passado, a redução é habilitada ou desabilitada por meio de [**IAudioSessionControl2::SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference).


```C++
////////////////////////////////////////////////////////////////////
//Description: Specifies the ducking options for the application.
//Parameters: 
//    If DuckingOptOutChecked is TRUE system ducking is disabled; 
//    FALSE, system ducking is enabled.
////////////////////////////////////////////////////////////////////

HRESULT DuckingOptOut(bool DuckingOptOutChecked)
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator* pDeviceEnumerator NULL;
    IMMDevice* pEndpoint = NULL;
    IAudioSessionManager2* pSessionManager2 = NULL;
    IAudioSessionControl* pSessionControl = NULL;
    IAudioSessionControl2* pSessionControl2 = NULL;


    //  Start with the default endpoint.

    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), 
                          NULL, 
                          CLSCTX_INPROC_SERVER, 
                          IID_PPV_ARGS(&pDeviceEnumerator));
    
    if (SUCCEEDED(hr))
    {
        hr = pDeviceEnumerator>GetDefaultAudioEndpoint(eRender, eConsole, &pEndpoint);

        pDeviceEnumerator>Release();
        pDeviceEnumerator = NULL;
    }

    // Activate session manager.
    if (SUCCEEDED(hr))
    {
        hr = pEndpoint->Activate(__uuidof(IAudioSessionManager2), 
                                 CLSCTX_INPROC_SERVER,
                                 NULL, 
                                 reinterpret_cast<void **>(&pSessionManager2));
        pEndpoint->Release();
        pEndpoint = NULL;
    }
    if (SUCCEEDED(hr))
    {
        hr = pSessionManager2->GetAudioSessionControl(NULL, 0, &pSessionControl);
        
        pSessionManager2->Release();
        pSessionManager2 = NULL;
    }

    if (SUCCEEDED(hr))
    {
        hr = pSessionControl->QueryInterface(
                  __uuidof(IAudioSessionControl2),
                  (void**)&pSessionControl2);
                
        pSessionControl->Release();
        pSessionControl = NULL;
    }

    //  Sync the ducking state with the specified preference.

    if (SUCCEEDED(hr))
    {
        if (DuckingOptOutChecked)
        {
            hr = pSessionControl2->SetDuckingPreference(TRUE);
        }
        else
        {
            hr = pSessionControl2->SetDuckingPreference(FALSE);
        }
        pSessionControl2->Release();
        pSessionControl2 = NULL;
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

[Fornecendo um comportamento de desaqueamento personalizado](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Considerações de implementação para notificações de replicação](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Obter eventos de desaqueamento](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



