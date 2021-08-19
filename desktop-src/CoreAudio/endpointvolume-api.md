---
description: EndpointVolume API
ms.assetid: 1fe1cd57-a0a4-4e08-ab52-3b6e66d14e79
title: EndpointVolume API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22965e882a2f7d413ae58690fc9bc5f8134aba0e7b26838ca38c74d7f0093c98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018444"
---
# <a name="endpointvolume-api"></a>EndpointVolume API

A API EndpointVolume permite que clientes especializados controlem e monitorem os níveis de volume de dispositivos [de ponto de extremidade de áudio](audio-endpoint-devices.md). Um cliente obtém referências às interfaces na API EndpointVolume obtendo a interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) de um dispositivo de ponto de extremidade de áudio e chamando o método [**IMMDevice::Activate.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)

O arquivo de header Endpointvolume.h define as interfaces na API EndpointVolume.

Aplicativos de áudio que usam a [API MMDevice](mmdevice-api.md) e [WASAPI](wasapi.md) normalmente usam a interface [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) para controlar os níveis de volume por sessão. Somente dois tipos de aplicativos de áudio exigem o uso da API EndpointVolume. Esses tipos de aplicativos são:

-   Aplicativos que gerenciam os níveis de volume mestre de dispositivos de ponto de extremidade de áudio, semelhantes Windows programa de controle de volume, Sndvol.exe.
-   Professional aplicativos de áudio ("pro audio") que exigem acesso de modo exclusivo a dispositivos de ponto de extremidade de áudio.

O uso inadequado da API EndpointVolume pode interferir Windows política de áudio e interromper as configurações de volume do sistema do usuário.

Se um dispositivo de ponto de extremidade de áudio implementar controles de volume de hardware e mudo, a API EndpointVolume usará esses controles para gerenciar o volume do dispositivo. Caso contrário, a API EndpointVolume implementará os controles no software, de forma transparente para o cliente.

Se um dispositivo tiver controles de volume de hardware e mudo, as alterações feitas nas configurações de volume e mudo do dispositivo por meio da API EndpointVolume afetarão o nível de volume no modo compartilhado e no modo exclusivo. Se um dispositivo não tiver controles de volume de hardware e mudo, as alterações feitas no volume de software e nos controles de mute por meio da API EndpointVolume afetarão o nível de volume no modo compartilhado, mas não no modo exclusivo. No modo exclusivo, o cliente e o dispositivo trocam dados de áudio diretamente, ignorando os controles de software.

Para aplicativos que devem gerenciar controles de volume e mudo de hardware, a API EndpointVolume oferece duas vantagens potenciais em relação à [API DeviceTopology](devicetopology-api.md).

Primeiro, vários dispositivos de adaptador de áudio não têm controles de volume de hardware. Se um dispositivo não tiver um controle de volume de hardware, a interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) na API EndpointVolume implementará automaticamente um controle de volume de software no fluxo de ou para esse dispositivo. Para um cliente da API EndpointVolume, o resultado é o mesmo se o controle de volume é implementado em hardware pelo dispositivo ou no software pela interface da API EndpointVolume.

Em segundo lugar, mesmo que o dispositivo de adaptador implemente controles de volume de hardware, um aplicativo que usa a API DeviceTopology para implementar um algoritmo de travessia de topologia pode falhar ao encontrar o controle que está procurando. Normalmente, esse aplicativo é projetado para percorrer a topologia de hardware de um dispositivo específico ou conjunto de dispositivos relacionados. O aplicativo corre o risco de falhar se tentar percorrer a topologia de um dispositivo com o que ele não foi especificamente projetado ou testado.

Somente aplicativos especializados que devem acessar funções de hardware diferentes de controles de volume e mudo exigem o uso da API DeviceTopology. Para aplicativos que exigem controle apenas do nível de volume de um fluxo de modo exclusivo, a API EndpointVolume é mais simples de usar e funciona de forma confiável com uma variedade maior de dispositivos de hardware de áudio.

Para exemplos de código que usam as interfaces na API EndpointVolume, consulte os seguintes tópicos:

-   [Controles de volume do ponto de extremidade](endpoint-volume-controls.md)
-   [Medidores de pico](peak-meters.md)

Para ver um exemplo que usa a API EndpointVolume, consulte [EndpointVolume](endpointvolume.md) no SDK do Windows.

A API EndpointVolume implementa as interfaces a seguir.



| Interface                                                | Descrição                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)     | Representa os controles de volume no fluxo de áudio de ou para um dispositivo de ponto de extremidade de áudio. |
| [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) | Representa um medidor de pico no fluxo de áudio de ou para um dispositivo de ponto de extremidade de áudio.        |



 

Além disso, os clientes da API EndpointVolume que exigem notificação de volume e alterações de muting em dispositivos de ponto de extremidade de áudio devem implementar a interface a seguir.



| Interface                                                            | Descrição                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | Fornece notificações quando o nível de volume ou o estado de muting de um dispositivo de ponto de extremidade de áudio muda. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controles de volume](volume-controls.md)
</dt> <dt>

[**IMMDevice Interface**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)
</dt> <dt>

[**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
</dt> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

 



