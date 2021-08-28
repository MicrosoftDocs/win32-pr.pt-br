---
description: O roteamento de fluxo é a capacidade de um aplicativo de mídia alternar fluxos entre dispositivos com interrupção mínima para a reprodução ou a sessão de captura.
ms.assetid: fc6efe89-013c-47af-870e-8705fa60c99c
title: Roteamento de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e76944954c969ce458175585076d23ce015ea573a86e3f89dbbcd296aff444
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018224"
---
# <a name="stream-routing"></a>Roteamento de fluxo

*O roteamento* de fluxo é a capacidade de um aplicativo de mídia alternar fluxos entre dispositivos com interrupção mínima para a reprodução ou a sessão de captura.

Um computador pode ter vários dispositivos de renderização e captura. O sistema lista esses dispositivos no painel **de controle** Sons. Nessa lista, um usuário pode definir um dispositivo como o dispositivo padrão para cada função: reprodução, gravação ou quatro funções de comunicação (renderização do console, captura de console, renderização de comunicação ou captura de comunicação). A lista de dispositivos pode ser modificada dinamicamente, pois alguns desses dispositivos podem estar disponíveis temporariamente, por exemplo, um headset USB. Quando vários dispositivos estão disponíveis, o usuário pode alterar o padrão para um dispositivo diferente. O usuário também pode alterar o formato de um dispositivo (taxa de  exemplo, bits por exemplo e assim por diante) na guia Avançado para as propriedades do dispositivo.

Considere um cenário no qual  um usuário seleciona Alto-falantes como o dispositivo padrão para renderizar fluxos de áudio. Em seguida, o usuário conecta um headset USB, seleciona o headset como o novo dispositivo padrão e altera a taxa de amostra do dispositivo de 44,1 kHz para 48 kHz. O usuário deseja reproduzir o fluxo de áudio no headset na nova taxa de exemplo com interrupção mínima para a sessão de streaming.

Nesse cenário, há dois casos que o aplicativo de mídia deve manipular:

-   O fluxo deve ser transferido para o novo dispositivo padrão com interrupção mínima para reprodução.
-   O novo dispositivo deve retomar a reprodução no novo formato (ou seja, o usuário pode alterar mais do que a taxa de exemplo).

No Windows Vista, para dar suporte a esse cenário, o aplicativo de mídia precisava fornecer a implementação para roteamento de fluxo. O aplicativo era responsável por encerrar fluxos existentes e reiniciar os fluxos no novo dispositivo. Se o usuário alterou o dispositivo padrão ou seu formato de combinação foi alterado, todas as sessões associadas foram fechadas e o aplicativo teve que lidar com a recuperação.

No Windows 7, um aplicativo pode transferir um fluxo de um dispositivo padrão existente para um novo ponto de extremidade de áudio padrão. Conjuntos de API de áudio de alto nível, como Media Foundation, DirectSound e WAVE, implementam o recurso de roteamento de fluxo. Os aplicativos de mídia que usam esses conjuntos de API para reproduzir ou capturar um fluxo do dispositivo padrão usam a implementação padrão e não terão que modificar o aplicativo. No entanto, se seu aplicativo de mídia usar MMDeviceAPI ou WASAPI diretamente, o aplicativo precisará fornecer a implementação de roteamento de fluxo.

> [!Note]  
> MMDeviceAPI e WASAPI são componentes principais da API de Áudio que um aplicativo pode usar para renderizar ou capturar um fluxo em um dispositivo. O MMDeviceAPI descobre o novo dispositivo de ponto de extremidade de áudio e o WASAPI gerencia o fluxo de dados de áudio entre um aplicativo de mídia e o dispositivo de ponto de extremidade de áudio.

 

Para implementar o recurso de roteamento de fluxo, o aplicativo deve escutar as notificações enviadas por MMDeviceAPI e WASAPI quando:

-   O dispositivo padrão é alterado pelo usuário.
-   O dispositivo padrão existente é removido e um novo dispositivo padrão é adicionado.
-   O formato do dispositivo é alterado.

Ao lidar com essas notificações, um aplicativo pode executar as operações de gerenciamento de fluxo necessárias durante a transferência do fluxo para o novo dispositivo padrão. Além disso, o aplicativo pode renderizar ou capturar fluxos existentes usando o novo formato especificado pelo usuário enquanto uma sessão de renderização está ativa.

Esta seção contém os seguintes tópicos:

-   [Obter o ponto de extremidade do dispositivo para roteamento de fluxo](getting-the-default-device-endpoint-for-stream-routing.md)
-   [Notificações relevantes para roteamento de fluxo](relevant-device-notifications-for-stream-routing.md)
-   [Considerações sobre implementação de roteamento de fluxo](stream-routing-implementation-considerations.md)

Os exemplos a seguir, incluídos no SDK do Windows, demonstram como um aplicativo pode lidar com notificações de roteamento de fluxo.

-   [RenderSharedTimerDriven](rendersharedtimerdriven.md)
-   [RenderSharedEventDriven](rendersharedeventdriven.md)
-   [RenderExclusiveTimerDriven](renderexclusivetimerdriven.md)
-   [RenderExclusiveEventDriven](renderexclusiveeventdriven.md)
-   [CaptureSharedTimerDriven](capturesharedtimerdriven.md)
-   [CaptureSharedEventDriven](capturesharedeventdriven.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciamento de Fluxo](stream-management.md)
</dt> <dt>

[Sobre a API MMDevice](mmdevice-api.md)
</dt> <dt>

[Sobre WASAPI](wasapi.md)
</dt> </dl>

 

 



