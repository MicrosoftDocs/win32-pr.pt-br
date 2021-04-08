---
description: Sobre o WASAPI
ms.assetid: 452b9725-b0b9-4888-bbb5-a23e0067e840
title: Sobre o WASAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f869319f3100b797e58c7b43597869c9767ac037
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920403"
---
# <a name="about-wasapi"></a>Sobre o WASAPI

A API de sessão de áudio do Windows (WASAPI) permite que os aplicativos cliente gerenciem o fluxo de dados de áudio entre o aplicativo e um [dispositivo de ponto de extremidade de áudio](audio-endpoint-devices.md).

Os arquivos de cabeçalho Audioclient. h e Audiopolicy. h definem as interfaces WASAPI.

Cada fluxo de áudio é um membro de uma [sessão de áudio](audio-sessions.md). Por meio da abstração de sessão, um cliente WASAPI pode identificar um fluxo de áudio como um membro de um grupo de fluxos de áudio relacionados. O sistema pode gerenciar todos os fluxos na sessão como uma única unidade.

O mecanismo de áudio é o [componente de áudio do modo de usuário](user-mode-audio-components.md) por meio do qual os aplicativos compartilham o acesso a um dispositivo de ponto de extremidade de áudio. O mecanismo de áudio transporta dados de áudio entre um buffer de ponto de extremidade e um dispositivo de ponto de extremidade. Para reproduzir um fluxo de áudio por meio de um dispositivo de ponto de extremidade de renderização, um aplicativo grava periodicamente os dados de áudio em um buffer de ponto de extremidade O mecanismo de áudio combina os fluxos de vários aplicativos. Para gravar um fluxo de áudio de um dispositivo de ponto de extremidade de captura, um aplicativo lê periodicamente dados de áudio de um buffer de ponto de extremidade de captura.

O WASAPI consiste em várias interfaces. A primeira delas é a interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) . Para acessar as interfaces WASAPI, um cliente primeiro obtém uma referência à interface **IAudioClient** de um dispositivo de ponto de extremidade de áudio chamando o método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) com o parâmetro *IID* definido como **REFIID** IID \_ IAudioClient. O cliente chama o método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) para inicializar um fluxo em um dispositivo de ponto de extremidade. Depois de inicializar um fluxo, o cliente pode obter referências às outras interfaces WASAPI chamando o método [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) .

Muitos dos métodos em WASAPI retornam o código de erro AUDCLNT \_ E \_ \_ o dispositivo invalidado se o dispositivo de ponto de extremidade de áudio que um aplicativo cliente está usando se tornar inválido. Frequentemente, o aplicativo pode se recuperar desse erro. Para obter mais informações, consulte [recuperando de um erro de Invalid-Device](recovering-from-an-invalid-device-error.md).

WASAPI implementa as interfaces a seguir.



| Interface                                            | Descrição                                                                                                                                                     |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)   | Permite que um cliente leia dados de entrada de um buffer de ponto de extremidade de captura.                                                                                             |
| [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)                 | Permite que um cliente crie e inicialize um fluxo de áudio entre um aplicativo de áudio e o mecanismo de áudio ou o buffer de hardware de um dispositivo de ponto de extremidade de áudio. |
| [**IAudioClock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)                   | Permite que um cliente monitore a taxa de dados de um fluxo e a posição atual no fluxo.                                                                        |
| [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)     | Permite que um cliente grave dados de saída em um buffer de ponto de extremidade de renderização.                                                                                           |
| [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) | Permite que um cliente configure os parâmetros de controle para uma sessão de áudio e monitore eventos na sessão.                                                 |
| [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) | Permite que um cliente acesse os controles de sessão e os controles de volume para sessões de áudio de processo cruzado e específicas de processo.                                 |
| [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)     | Permite que um cliente controle e monitore os níveis de volume para todos os canais em um fluxo de áudio.                                                           |
| [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)   | Permite que um cliente controle os níveis de volume para todos os canais na sessão de áudio a que o fluxo pertence.                                          |
| [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)     | Permite que um cliente controle o nível de volume mestre de uma sessão de áudio.                                                                                        |



 

Os clientes WASAPI que exigem a notificação de eventos relacionados à sessão devem implementar a interface a seguir.



| Interface                                          | Descrição                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) | Fornece notificações de eventos relacionados à sessão, como alterações no nível do volume, no nome de exibição e no estado da sessão. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciamento de fluxo](stream-management.md)
</dt> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

 



