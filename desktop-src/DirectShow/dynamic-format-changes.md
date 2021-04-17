---
description: Alterações de formato dinâmico
ms.assetid: ff60de5a-3edc-405d-aa02-8704b96d5e87
title: Alterações de formato dinâmico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49496e0b43d9b120f6daf27007cde98191a7765b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105789902"
---
# <a name="dynamic-format-changes"></a>Alterações de formato dinâmico

Quando dois filtros se conectam, eles concordam em um tipo de mídia, que descreve o formato dos dados que o filtro upstream fornecerá. Na maioria dos casos, o tipo de mídia é fixo pela duração da conexão. No entanto, o DirectShow oferece suporte limitado para filtros para alterar o tipo de mídia. Quando um filtro alterna os tipos de mídia, ele é chamado de *alteração de formato dinâmico*. Se estiver escrevendo um filtro do DirectShow, você deve estar ciente dos mecanismos para alterações de formato dinâmico. Mesmo que o filtro não ofereça suporte a essas alterações, ele deverá responder corretamente se outro filtro solicitar um novo formato.

O DirectShow define vários mecanismos distintos para alterações de formato dinâmico, dependendo do estado do grafo de filtro e do tipo de alteração necessário.

-   Se o grafo for interrompido, os Pins poderão se reconectar e renegociar o tipo de mídia. Para obter mais informações, consulte [reconectando Pins](reconnecting-pins.md).
-   Alguns filtros podem reconectar Pins mesmo enquanto o grafo estiver ativo (em execução ou em pausa). Para obter mais informações sobre esse mecanismo, consulte [reconexão dinâmica](dynamic-reconnection.md).

Caso contrário, se o grafo estiver ativo, mas os filtros em questão não oferecerem suporte a reconexões de PIN dinâmico, haverá três mecanismos possíveis para alterar o formato:

-   O [QueryAccept (downstream)](queryaccept--downstream.md) é usado quando um PIN de saída propõe uma alteração de formato para seu par downstream, mas somente se o novo formato não exigir um buffer maior.
-   [QueryAccept (upstream)](queryaccept--upstream.md) é usado quando um PIN de entrada propõe uma alteração de formato para seu ponto de upstream. O novo formato pode ter o mesmo tamanho ou pode ser maior.
-   [ReceiveConnection](receiveconnection.md) é usado quando um PIN de saída propõe uma alteração de formato ao seu par downstream, e o novo formato requer um buffer maior.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Manipulando alterações de formato do processador de vídeo](handling-format-changes-from-the-video-renderer.md)
</dt> </dl>

 

 



