---
description: API EndpointVolume
ms.assetid: 1fe1cd57-a0a4-4e08-ab52-3b6e66d14e79
title: API EndpointVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b827045250336aa499e386a8dafedb6ae068b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646412"
---
# <a name="endpointvolume-api"></a>API EndpointVolume

A API EndpointVolume permite que clientes especializados controlem e monitorem os níveis de volume de [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md). Um cliente Obtém referências às interfaces na API EndpointVolume obtendo a interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) de um dispositivo de ponto de extremidade de áudio e chamando o método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) .

O arquivo de cabeçalho Endpointvolume. h define as interfaces na API EndpointVolume.

Os aplicativos de áudio que usam a [API MMDevice](mmdevice-api.md) e [WASAPI](wasapi.md) normalmente usam a interface [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) para controlar os níveis de volume por sessão. Somente dois tipos de aplicativos de áudio exigem o uso da API EndpointVolume. Esses tipos de aplicativos são:

-   Aplicativos que gerenciam os níveis de volume mestre de dispositivos de ponto de extremidade de áudio, semelhantes ao programa de controle de volume do Windows, Sndvol.exe.
-   Aplicativos de áudio profissional ("áudio pro") que exigem acesso de modo exclusivo a dispositivos de ponto de extremidade de áudio.

O uso inadequado da API EndpointVolume pode interferir na política de áudio do Windows e interromper as configurações de volume do sistema do usuário.

Se um dispositivo de ponto de extremidade de áudio implementar o volume de hardware e os controles de mudo, a API do EndpointVolume usará esses controles para gerenciar o volume do dispositivo. Caso contrário, a API EndpointVolume implementa os controles no software, de forma transparente para o cliente.

Se um dispositivo tiver controles de áudio e volume de hardware, as alterações feitas nas configurações de volume e áudio do dispositivo por meio da API EndpointVolume afetarão o nível de volume no modo compartilhado e no modo exclusivo. Se um dispositivo não tiver controles de áudio e de volume de hardware, as alterações feitas no volume de software e nos controles de áudio por meio da API EndpointVolume afetarão o nível de volume no modo compartilhado, mas não no modo exclusivo. No modo exclusivo, o cliente e o dispositivo trocam dados de áudio diretamente, ignorando os controles de software.

Para aplicativos que devem gerenciar o volume de hardware e os controles de mudo, a API do EndpointVolume oferece duas possíveis vantagens sobre a [API do DeviceTopology](devicetopology-api.md).

Primeiro, um número de dispositivos de adaptador de áudio não tem controles de volume de hardware. Se um dispositivo não tem um controle de volume de hardware, a interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) na API EndpointVolume implementa automaticamente um controle de volume de software no fluxo para ou desse dispositivo. Para um cliente da API EndpointVolume, o resultado é o mesmo se o controle de volume for implementado no hardware pelo dispositivo ou no software pela interface de API do EndpointVolume.

Em segundo lugar, mesmo que o dispositivo adaptador implemente controles de volume de hardware, um aplicativo que usa a API DeviceTopology para implementar um algoritmo de passagem de topologia pode falhar ao localizar o controle que ele está procurando. Normalmente, esse aplicativo é projetado para atravessar a topologia de hardware de um determinado dispositivo ou de um conjunto de dispositivos relacionados. Os riscos de aplicativo falham se tentar atravessar a topologia de um dispositivo que não foi especificamente projetado para o ou testado com o.

Somente aplicativos especializados que devem acessar funções de hardware diferentes de controles de volume e sem áudio exigem o uso da API DeviceTopology. Para aplicativos que exigem controle apenas do nível de volume de um fluxo de modo exclusivo, a API EndpointVolume é mais simples de usar e funciona de forma confiável com uma variedade maior de dispositivos de hardware de áudio.

Para obter exemplos de código que usam as interfaces na API EndpointVolume, consulte os seguintes tópicos:

-   [Controles de volume do ponto de extremidade](endpoint-volume-controls.md)
-   [Medidores de pico](peak-meters.md)

Para ver um exemplo que usa a API EndpointVolume, consulte [EndpointVolume](endpointvolume.md) no SDK do Windows.

A API EndpointVolume implementa as interfaces a seguir.



| Interface                                                | Descrição                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)     | Representa os controles de volume no fluxo de áudio de ou para um dispositivo de ponto de extremidade de áudio. |
| [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) | Representa um medidor de pico no fluxo de áudio de ou para um dispositivo de ponto de extremidade de áudio.        |



 

Além disso, os clientes da API EndpointVolume que exigem notificação de alterações de volume e de mudo em dispositivos de ponto de extremidade de áudio devem implementar a interface a seguir.



| Interface                                                            | Descrição                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | Fornece notificações quando o nível de volume ou estado de mudo de um dispositivo de ponto de extremidade de áudio é alterado. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controles de volume](volume-controls.md)
</dt> <dt>

[**Interface IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[**IMMDevice:: ativar**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)
</dt> <dt>

[**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
</dt> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

 



