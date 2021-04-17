---
description: Os objetos Stream são uma abstração do fluxo de mídia ou dos fluxos associados a uma sessão de chamada.
ms.assetid: 4bd7a305-69ff-4892-bf03-df9c6479adab
title: Objetos de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeb89dbacf73baaffbca9aa3791aa73937a69e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784080"
---
# <a name="stream-objects"></a>Objetos de fluxo

Os objetos Stream são uma abstração do fluxo de mídia ou dos fluxos associados a uma sessão de chamada. As interfaces e os métodos expostos nos objetos Stream e substream permitem que um aplicativo exerça controles muito detalhados, como pausar um fluxo, adicionar novos tipos de mídia a uma sessão de comunicações ou ajustar o volume de áudio de um participante de conferência específico.

Os dois tipos principais de fluxo são o fluxo e o Subfluxo. As interfaces e os métodos de uma implementação padrão são semelhantes para ambos, mas o Subfluxo permite um nível inferior de controle. Todos os provedores de serviços de mídia (MSPs) devem implementar as interfaces básicas de controle de fluxo, mas o suporte a subfluxos é opcional.

Além disso, alguns provedores de serviços implementam [interfaces específicas do provedor](provider-specific-interfaces.md) para fluxos. Por exemplo, o IPConf MSP fornece controles de nível de participante. Consulte [IPConf MSP interfaces](ipconf-msp-interfaces.md) para obter um resumo. Para outras interfaces que podem ser implementadas, consulte a documentação do provedor de serviços.

O MSP e a TAPI criam objetos Stream para uma chamada durante a configuração inicial de uma sessão de saída ou de entrada. O aplicativo é responsável por identificar os terminais apropriados para esses fluxos e selecionar os terminais nos fluxos.

Observe que, em alguns casos, um MSP pode exigir que o aplicativo pare ou PAUSE fluxos antes de determinadas operações de sessão de chamada.

As interfaces de fluxo são documentadas na [referência de MSPI (interface do provedor de serviço de mídia)](media-service-provider-interface-mspi-reference.md).

O exemplo [selecionar um](select-a-terminal.md) código de terminal mostra um exemplo de como enumerar fluxos e selecionar os terminais neles.

 

 



