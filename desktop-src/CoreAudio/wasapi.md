---
description: Sobre WASAPI
ms.assetid: 452b9725-b0b9-4888-bbb5-a23e0067e840
title: Sobre WASAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3effb34ec0cde0a53d0eb6f6e9718aa13fc308417b33427f168364afc32086ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088176"
---
# <a name="about-wasapi"></a>Sobre WASAPI

O Windows API de Sessão de Áudio (WASAPI) permite que os aplicativos cliente gerenciem o fluxo de dados de áudio entre o aplicativo e um dispositivo de [ponto de extremidade de áudio](audio-endpoint-devices.md).

Arquivos de header Audioclient.h e Audiopolicy.h definem as interfaces WASAPI.

Cada fluxo de áudio é membro de uma sessão [de áudio.](audio-sessions.md) Por meio da abstração de sessão, um cliente WASAPI pode identificar um fluxo de áudio como membro de um grupo de fluxos de áudio relacionados. O sistema pode gerenciar todos os fluxos na sessão como uma única unidade.

O mecanismo de áudio é o componente de áudio do modo [de usuário por](user-mode-audio-components.md) meio do qual os aplicativos compartilham acesso a um dispositivo de ponto de extremidade de áudio. O mecanismo de áudio transporta dados de áudio entre um buffer de ponto de extremidade e um dispositivo de ponto de extremidade. Para reproduzir um fluxo de áudio por meio de um dispositivo de ponto de extremidade de renderização, um aplicativo grava periodicamente dados de áudio em um buffer de ponto de extremidade de renderização. O mecanismo de áudio combina os fluxos de vários aplicativos. Para registrar um fluxo de áudio de um dispositivo de ponto de extremidade de captura, um aplicativo lê periodicamente os dados de áudio de um buffer de ponto de extremidade de captura.

WASAPI consiste em várias interfaces. A primeira delas é a interface [**IAudioClient.**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) Para acessar as interfaces WASAPI, primeiro um cliente obtém uma referência à interface **IAudioClient** de um dispositivo de ponto de extremidade de áudio chamando o método [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) com o *parâmetro iid* definido como IAudioClient **reFIID.** \_ O cliente chama o [**método IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) para inicializar um fluxo em um dispositivo de ponto de extremidade. Depois de inicializar um fluxo, o cliente pode obter referências a outras interfaces WASAPI chamando o [**método IAudioClient::GetService.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)

Muitos dos métodos no WASAPI retornam o código de erro AUDCLNT E DEVICE INVALIDATED se o dispositivo de ponto de extremidade de áudio que um aplicativo cliente \_ está usando se torna \_ \_ inválido. Frequentemente, o aplicativo pode se recuperar desse erro. Para obter mais informações, consulte [Recuperando de um erro Invalid-Device erro](recovering-from-an-invalid-device-error.md).

WASAPI implementa as interfaces a seguir.



| Interface                                            | Descrição                                                                                                                                                     |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)   | Permite que um cliente leia dados de entrada de um buffer de ponto de extremidade de captura.                                                                                             |
| [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)                 | Permite que um cliente crie e inicialize um fluxo de áudio entre um aplicativo de áudio e o mecanismo de áudio ou o buffer de hardware de um dispositivo de ponto de extremidade de áudio. |
| [**IAudioClock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)                   | Permite que um cliente monitore a taxa de dados de um fluxo e a posição atual no fluxo.                                                                        |
| [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)     | Permite que um cliente escreva dados de saída em um buffer de ponto de extremidade de renderização.                                                                                           |
| [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) | Permite que um cliente configure os parâmetros de controle para uma sessão de áudio e monitore eventos na sessão.                                                 |
| [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) | Permite que um cliente acesse os controles de sessão e controles de volume para sessões de áudio específicas do processo e entre processos.                                 |
| [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)     | Permite que um cliente controle e monitore os níveis de volume de todos os canais em um fluxo de áudio.                                                           |
| [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)   | Permite que um cliente controle os níveis de volume de todos os canais na sessão de áudio ao que o fluxo pertence.                                          |
| [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)     | Permite que um cliente controle o nível de volume mestre de uma sessão de áudio.                                                                                        |



 

Os clientes WASAPI que exigem notificação de eventos relacionados à sessão devem implementar a interface a seguir.



| Interface                                          | Descrição                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) | Fornece notificações de eventos relacionados à sessão, como alterações no nível do volume, nome de exibição e estado da sessão. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciamento de Fluxo](stream-management.md)
</dt> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

 



