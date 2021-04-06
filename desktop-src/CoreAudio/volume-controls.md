---
description: Controles de volume
ms.assetid: b1799372-8d2c-4774-995d-e7926a159d0a
title: Controles de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758fd25d4157030071a47ac8eec26dc0e4d50e4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826474"
---
# <a name="volume-controls"></a>Controles de volume

Os clientes que gerenciam fluxos de modo compartilhado normalmente usam as interfaces [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) e [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) no [WASAPI](wasapi.md) para controlar e monitorar os níveis de volume de fluxo. Por meio dos métodos na interface **ISimpleAudioVolume** , o cliente pode obter e definir os níveis de volume das [sessões de áudio](audio-sessions.md) às quais os fluxos de modo compartilhado pertencem. Se SNDVOL ou outro aplicativo alterar o nível de volume da sessão, o cliente poderá receber a notificação da alteração por meio da interface **IAudioSessionEvents** .

Os clientes que gerenciam fluxos de modo exclusivo normalmente usam as interfaces [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) e [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) na [API EndpointVolume](endpointvolume-api.md) para controlar e monitorar os níveis de volume de fluxo. Por meio dos métodos na interface **IAudioEndpointVolume** , o cliente pode obter e definir o nível de volume de um [dispositivo de ponto de extremidade de áudio](audio-endpoint-devices.md). Se SNDVOL ou outro aplicativo alterar o nível de volume do dispositivo de ponto de extremidade, o cliente poderá receber a notificação da alteração por meio da interface **IAudioEndpointVolumeCallback** .

Conforme explicado em [sessões de áudio](audio-sessions.md), o SNDVOL é o programa de controle de volume do sistema. Ele exibe os controles de volume para os dispositivos de ponto de extremidade de renderização de áudio no sistema. (Atualmente, ele não exibe os controles de volume para dispositivos de ponto de extremidade de captura de áudio.) Para exibir os controles de volume de um dispositivo específico, clique em **dispositivo** na barra de menus e selecione um nome de dispositivo na lista de dispositivos disponíveis.

A janela SNDVOL separa os controles de volume de um dispositivo em dois grupos. A caixa de grupo no lado esquerdo da janela é rotulada como **dispositivo**. A caixa **dispositivo** contém um único controle de volume que é controlado pela interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) . As alterações que o usuário faz a esse controle de volume podem ser monitoradas por meio da interface [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) .

A caixa de grupo no lado direito da janela SNDVOL é rotulada como **aplicativos**. A caixa **aplicativos** contém os controles de volume para os aplicativos que atualmente compartilham o dispositivo. Para aplicativos que usam o dispositivo no modo compartilhado, os controles de volume representam os níveis de volume que são controlados pela interface [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) . As alterações que o usuário faz para esses controles de volume podem ser monitoradas por meio da interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) .

Embora um aplicativo de modo compartilhado possa usar sua interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) para monitorar as alterações que o usuário faz no controle de volume do aplicativo na caixa **aplicativos** na janela SNDVOL, o aplicativo não pode monitorar alterações nos controles de volume de outros aplicativos não relacionados. Da mesma forma, um aplicativo pode alterar os níveis de volume de suas sessões de áudio por meio da interface [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) , mas não pode alterar os níveis de volume de sessões que pertencem a outros aplicativos não relacionados.

No entanto, dois ou mais aplicativos relacionados (ou instâncias do mesmo aplicativo) podem compartilhar o mesmo controle de volume na caixa **aplicativos** na janela SNDVOL, seja atribuindo seus fluxos de áudio à mesma sessão entre processos ou associando suas respectivas sessões ao mesmo parâmetro de agrupamento. Para obter mais informações, consulte [sessões de áudio](audio-sessions.md) e parâmetros de [agrupamento](grouping-parameters.md).

O WASAPI fornece duas interfaces adicionais, [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) e [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume), para controlar os níveis de volume de fluxos de modo compartilhado. Essas interfaces são usadas principalmente por clientes especializados que exigem controle sobre os níveis de volume de canais individuais em uma sessão ou fluxos individuais em uma sessão.

A [API DeviceTopology](devicetopology-api.md) permite que os clientes acessem os controles de volume nas topologias de adaptadores de áudio. No entanto, os clientes que gerenciam fluxos de modo exclusivo normalmente usam a API EndpointVolume em vez da API DeviceTopology para controlar os níveis de volume de fluxo. A API EndpointVolume simplifica o controle do volume de um dispositivo de ponto de extremidade de duas maneiras. Primeiro, se um dispositivo de ponto de extremidade implementar um controle de volume de hardware, a API DeviceTopology exigirá que o cliente percorra a topologia do dispositivo na pesquisa do controle de hardware. Por outro lado, a API EndpointVolume localiza automaticamente o controle de volume de hardware para o cliente. Em segundo lugar, se o dispositivo de ponto de extremidade não implementar um controle de volume de hardware, um cliente DeviceTopology deverá implementar um controle de volume no software. Por outro lado, a API EndpointVolume substitui automaticamente um controle de volume de software para o controle de hardware ausente.

As seções a seguir descrevem os controles de volume para sessões de áudio e para dispositivos de ponto de extremidade de áudio:

-   [Controles de volume de sessão](session-volume-controls.md)
-   [Controles de volume do ponto de extremidade](endpoint-volume-controls.md)
-   [API EndpointVolume](endpointvolume-api.md)
-   [Controles de volume de áudio cônico](audio-tapered-volume-controls.md)
-   [Medidores de pico](peak-meters.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação](programming-guide.md)
</dt> </dl>

 

 



