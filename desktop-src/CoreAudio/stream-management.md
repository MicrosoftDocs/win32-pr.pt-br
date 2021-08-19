---
description: Gerenciamento de fluxo
ms.assetid: 936d8d69-e86c-418b-b5b0-c4fbbfa1dd49
title: Gerenciamento de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669e3be8af4532f9045c08f07400d47c423d507d4e11da4ada0b1a279c52772d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077430"
---
# <a name="stream-management"></a>Gerenciamento de fluxo

Depois de enumerar os [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md) no sistema e identificar um dispositivo de processamento ou de captura adequado, a próxima tarefa para um aplicativo cliente de áudio é abrir uma conexão com o dispositivo de ponto de extremidade e gerenciar o fluxo de dados de áudio nessa conexão. O [WASAPI](wasapi.md) permite que os clientes criem e gerenciem fluxos de áudio.

O WASAPI implementa várias interfaces para fornecer serviços de gerenciamento de fluxo para clientes de áudio. A interface principal é [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient). Um cliente obtém a interface **IAudioClient** para um dispositivo de ponto de extremidade de áudio chamando o método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) (com o parâmetro *IID* definido como **REFIID** IID \_ IAudioClient) no objeto de ponto de extremidade.

O cliente chama os métodos na interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) para fazer o seguinte:

-   Descobrir quais formatos de áudio o dispositivo de ponto de extremidade dá suporte.
-   Obter o tamanho do buffer do ponto de extremidade.
-   Obtenha o formato e a latência do fluxo.
-   Inicie, pare e redefina o fluxo que flui por meio do dispositivo de ponto de extremidade.
-   Acessar serviços de áudio adicionais.

Para criar um fluxo, um cliente chama o método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) . Por meio desse método, o cliente especifica o formato de dados para o fluxo, o tamanho do buffer de ponto de extremidade e se o fluxo opera no modo compartilhado ou exclusivo.

Os métodos restantes na interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) se enquadram em dois grupos:

-   Métodos que podem ser chamados somente após o fluxo ter sido aberto por [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).
-   Métodos que podem ser chamados a qualquer momento antes ou depois da chamada de [**inicialização**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .

Os métodos a seguir podem ser chamados somente após a chamada para [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize):

-   [**IAudioClient:: getbuffersize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize)
-   [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding)
-   [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
-   [**IAudioClient::GetStreamLatency**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getstreamlatency)
-   [**IAudioClient:: Reset**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-reset)
-   [**IAudioClient:: iniciar**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start)
-   [**IAudioClient:: Stop**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop)

Os métodos a seguir podem ser chamados antes ou depois da chamada [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) :

-   [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod)
-   [**IAudioClient::GetMixFormat**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getmixformat)
-   [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported)

Para acessar os serviços adicionais de cliente de áudio, o cliente chama o método [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) . Por meio desse método, o cliente pode obter referências às seguintes interfaces:

-   [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)

    Grava dados de renderização em um buffer de ponto de extremidade de renderização de áudio.

-   [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)

    Lê dados capturados de um buffer de ponto de extremidade de captura de áudio.

-   [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)

    Comunica-se com o Gerenciador de sessão de áudio para configurar e gerenciar a sessão de áudio associada ao fluxo.

-   [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)

    Controla o nível de volume da sessão de áudio que está associada ao fluxo.

-   [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)

    Controla os níveis de volume dos canais individuais na sessão de áudio que está associada ao fluxo.

-   [**IAudioClock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)

    Monitora a taxa de dados de fluxo e a posição do fluxo.

Além disso, os clientes do WASAPI que exigem a notificação de eventos relacionados à sessão devem implementar a seguinte interface:

-   [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)

    Para receber notificações de eventos, o cliente passa um ponteiro para sua interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) para o método [**IAudioSessionControl:: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) como um parâmetro de chamada.

Por fim, um cliente pode usar uma API de nível superior para criar um fluxo de áudio, mas também exigir acesso aos controles de sessão e controles de volume para a sessão que contém o fluxo. Uma API de nível superior normalmente não fornece esse acesso. O cliente pode obter os controles para uma sessão específica por meio da interface [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) . Essa interface permite que o cliente obtenha as interfaces [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) e [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) para uma sessão sem exigir que o cliente use a interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) para criar um fluxo e atribuir o fluxo à sessão. Um cliente obtém a interface **IAudioSessionManager** para um dispositivo de ponto de extremidade de áudio chamando o método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) (com o parâmetro *IID* definido como **REFIID** IID \_ IAudioSessionManager) no objeto de ponto de extremidade.

As interfaces [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol), [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)e [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) são definidas no arquivo de cabeçalho Audiopolicy. h. Todas as outras interfaces WASAPI são definidas no arquivo de cabeçalho Audioclient. h.

As seções a seguir descrevem como usar o WASAPI para gerenciar fluxos de áudio:

-   [Sobre o WASAPI](wasapi.md)
-   [Renderizando um fluxo](rendering-a-stream.md)
-   [Capturando um fluxo](capturing-a-stream.md)
-   [Gravação de loopback](loopback-recording.md)
-   [Fluxos de modo exclusivo](exclusive-mode-streams.md)
-   [Recuperando de um erro de Invalid-Device](recovering-from-an-invalid-device-error.md)
-   [Usando um dispositivo de comunicação](using-the-communication-device.md)
-   [Roteamento de fluxo](stream-routing.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação](programming-guide.md)
</dt> </dl>

 

 



