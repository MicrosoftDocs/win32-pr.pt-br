---
description: Alterações de formato dinâmico
ms.assetid: ff60de5a-3edc-405d-aa02-8704b96d5e87
title: Alterações de formato dinâmico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ce6d30b13458694b740bfb7bed8498c0f54d5b19648a484c5330d2b7627eab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998356"
---
# <a name="dynamic-format-changes"></a>Alterações de formato dinâmico

Quando dois filtros se conectam, eles concordam com um tipo de mídia, que descreve o formato dos dados que o filtro upstream fornecerá. Na maioria dos casos, o tipo de mídia é fixo durante a conexão. No entanto, DirectShow oferece suporte limitado para filtros para alterar o tipo de mídia. Quando um filtro alterna os tipos de mídia, ele é chamado de alteração *de formato dinâmico.* Se você estiver escrevendo um filtro DirectShow, deve estar ciente dos mecanismos para alterações de formato dinâmico. Mesmo que o filtro não seja suportado por essas alterações, ele deverá responder corretamente se outro filtro solicitar um novo formato.

DirectShow define vários mecanismos distintos para alterações de formato dinâmico, dependendo do estado do grafo de filtro e do tipo de alteração necessária.

-   Se o grafo for interrompido, os pinos poderão se reconectar e renegociar o tipo de mídia. Para obter mais informações, consulte [Reconectando pinos](reconnecting-pins.md).
-   Alguns filtros podem reconectar pinos mesmo enquanto o grafo está ativo (em execução ou em pausa). Para obter mais informações sobre esse mecanismo, consulte [Reconexão dinâmica.](dynamic-reconnection.md)

Caso contrário, se o grafo estiver ativo, mas os filtros em questão não deem suporte a reconexões de pino dinâmico, haverá três mecanismos possíveis para alterar o formato:

-   [QueryAccept (Downstream)](queryaccept--downstream.md) é usado quando Se um pino de saída propor uma alteração de formato para seu par downstream, mas somente se o novo formato não exigir um buffer maior.
-   [QueryAccept (Upstream)](queryaccept--upstream.md) é usado quando um pino de entrada propõe uma alteração de formato para seu par upstream. O novo formato pode ter o mesmo tamanho ou pode ser maior.
-   [ReceiveConnection](receiveconnection.md) é usado quando um pino de saída propõe uma alteração de formato para seu par downstream e o novo formato requer um buffer maior.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Manipulando alterações de formato do renderador de vídeo](handling-format-changes-from-the-video-renderer.md)
</dt> </dl>

 

 



