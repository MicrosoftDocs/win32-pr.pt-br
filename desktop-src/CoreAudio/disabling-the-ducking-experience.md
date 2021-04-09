---
description: Um usuário pode desabilitar a experiência de pato padrão fornecida pelo sistema usando as opções disponíveis na guia comunicações do painel de controle multimídia do Windows, Mmsys.cpl.
ms.assetid: 5604b927-99f8-450f-a48c-b38d782584de
title: Desabilitando a experiência de pato padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed33fa7d9473cb5c68a018b98bff8a826612387e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089630"
---
# <a name="disabling-the-default-ducking-experience"></a>Desabilitando a experiência de pato padrão

Um usuário pode desabilitar a [experiência de pato padrão](stream-attenuation.md) fornecida pelo sistema usando as opções disponíveis na guia **comunicações** do painel de controle multimídia do Windows, Mmsys.cpl.

Quando o pato é aplicado, um efeito de esmaecimento e esmaecimento é usado por um período de 1 segundo. Um aplicativo de jogo pode não querer que o fluxo de comunicação interfira no áudio do jogo. Alguns aplicativos de mídia podem descobrir que a experiência de reprodução é dissonante quando a música esmaece de volta. Esses tipos de aplicativos podem optar por não participar da experiência de pato.

Programaticamente, um cliente WASAPI direto pode recusar usando o Gerenciador de sessão para a sessão de áudio que fornece controle de volume para os fluxos que não são de comunicação. Observe que, mesmo que um cliente não esteja no pato, ele ainda recebe notificações de pato do sistema.

Para recusar o pato, o cliente deve obter uma referência à interface [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) do Gerenciador de sessão. Para recusar a experiência de pato, use as seguintes etapas:

1.  Instancie o enumerador de dispositivo e use-o para obter uma referência ao ponto de extremidade do dispositivo que o aplicativo de mídia está usando para renderizar o fluxo de não comunicação.
2.  Ative o Gerenciador de sessão no ponto de extremidade do dispositivo e obtenha uma referência para a interface [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) do Gerenciador de sessão.
3.  Usando o ponteiro [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) , obtenha uma referência à interface [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) do Gerenciador de sessão.
4.  Consulte o [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) da interface [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) .
5.  Chame [**IAudioSessionControl2:: SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) e passe **true** ou **false** para especificar a preferência de pato. A preferência especificada pode ser alterada dinamicamente durante a sessão. Observe que a alteração de recusa não tem efeito até que o fluxo seja interrompido e iniciado novamente.

O código a seguir mostra como um aplicativo pode especificar sua preferência de pato. O chamador da função deve passar **true** ou **false** no parâmetro DuckingOptOutChecked. Dependendo do valor passado, o pato está habilitado ou desabilitado por meio de [**IAudioSessionControl2:: SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference).


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

[Experiência de pato padrão](stream-attenuation.md)
</dt> <dt>

[Fornecendo um comportamento personalizado de pato](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Considerações de implementação para notificações de pato](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Obtendo eventos de pato](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



