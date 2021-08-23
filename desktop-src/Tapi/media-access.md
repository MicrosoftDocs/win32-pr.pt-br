---
description: Os recursos de mídia são diferentes com a TAPI 2,2 (TAPI/C) em oposição à TAPI 3 (COM), em grande parte porque a API COM tem acesso aos provedores de serviços de mídia (MSPs).
ms.assetid: 73042eb1-b2d6-4dcb-b40e-f8f3933dcdb0
title: Acesso à mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f2fc67e18a85718a10a0489656d4b423dd2f9f849a876ea5eec0543017611f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575606"
---
# <a name="media-access"></a>Acesso à mídia

Os recursos de mídia são diferentes com a TAPI 2,2 (TAPI/C) em oposição à TAPI 3 (COM), em grande parte porque a API COM tem acesso aos provedores de serviços de mídia (MSPs). Para obter mais informações sobre o MSPs, consulte [sobre o MSP (provedor de serviços de mídia)](./about-the-media-service-provider-msp-.md). Para obter mais informações sobre operações de fluxo de mídia, consulte [controle de mídia](./device-control.md).

Os dois conceitos mais importantes para um aplicativo são o tipo de mídia (ou o modo) e o fluxo. O tipo é o formulário no qual os dados são transmitidos. Para obter mais informações e uma lista de tipos definidos pela TAPI, [consulte \_ constantes LINEMEDIAMODE](linemediamode--constants.md). O fluxo de mídia é o fluxo de dados real. Um MSP pode fornecer acesso direto ao fluxo. Os aplicativos TAPI 2,2 têm algum acesso, mas, principalmente, fazem referência a outras APIs para implementar tais controles.

Essas APIs incluem a API de onda, a API de comunicação e a MCI (interface de controle de mídia). A API de forma de onda é usada para programação de multimídia, a API de comunicação é o conjunto de funções de comunicação fornecidas pelo SDK (Software Development Kit) da plataforma e o MCI fornece uma interface generalizada de alto nível para controlar dispositivos de mídia.

Por exemplo, para dispositivos de linha, um aplicativo pode usar TAPI 2,2 para estabelecer uma conexão com outra estação. Depois que a conexão é estabelecida, o aplicativo pode usar a API de onda (ou a API WaveAudio do MCI) no dispositivo associado para reproduzir (enviar) e gravar (receber) dados de áudio pela conexão. Da mesma forma, se o fluxo de mídia de conexão for de um modem, um aplicativo usará as extensões de configuração de modem da API de comunicações para controlar o fluxo de mídia.

Para fornecer a TAPI 2,2 com acesso de fluxo de mídia para um telefone ou uma chamada em um dispositivo de linha, o provedor de serviços deve implementar o SPI de telefonia e o SPI (interface de dispositivo) de mídia apropriado ou a DDI. O provedor de serviços pode dar suporte a linhas e telefones simultaneamente.

Como essas classes de dispositivo e operações de fluxo de mídia funcionam de forma independente uma da outra, a coordenação de seu uso deve ocorrer no nível do aplicativo. Vários aplicativos que compartilham chamadas e fluxos de mídia provavelmente exigirão a coordenação de suas atividades no nível do aplicativo para evitar o uso conflitante da TAPI e da API de fluxo de mídia.

A TAPI relata alterações no tipo de fluxo de mídia (voz, fax, modem de dados e assim por diante) para aplicativos participantes. Esse processo é, às vezes, chamado de [*classificação de chamada*](c-tapgloss.md). O mecanismo usado para determinar o tipo de fluxo de mídia é específico para o provedor de serviços. Por exemplo, um provedor de serviços pode filtrar o fluxo de mídia para energia ou tons que caracterizam o tipo de mídia, ou pode usar toque distintivo, dados trocados em mensagens pela rede ou conhecimento sobre o chamador ou ID chamado para fazer essa determinação.

-   [Monitoramento de chamada](call-monitoring.md)
-   [Controle de mídia](/previous-versions/windows/desktop/legacy/ms736578(v=vs.85))
-   [Coleta de dígitos](digit-gathering.md)
-   [Gerando dígitos de banda e tons](generating-inband-digits-and-tones.md)

 

 
