---
title: Recuperando informações
description: O RTMv2 permite que um cliente recupere as informações referenciadas por um determinado identificador usando as funções RtmGetEntityInfo, RtmGetDestInfo, RtmGetRouteInfo e RtmGetNextHopInfo.
ms.assetid: a3fc2020-eac4-40a1-9a6e-6eaa2bcc582c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058a87c9463011aec55b0c6c8c0574ff1e013f23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159409"
---
# <a name="retrieving-information"></a>Recuperando informações

O RTMv2 permite que um cliente recupere as informações referenciadas por um determinado identificador usando as funções [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)e [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) .

Essas chamadas de função têm funções correspondentes ([**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo), [**RtmReleaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)) para liberar os identificadores associados à estrutura de informações retornada pelo Gerenciador de tabela de roteamento.

> [!Note]  
> As informações para clientes estão disponíveis somente na instância atual e na família de endereços.

 

Para obter um exemplo de código que mostra como usar essas funções, consulte [procurar a melhor rota](search-for-the-best-route.md).

## <a name="using-rtmgetexactmatchroute-and-rtmgetexactmatchdestination"></a>Usando RtmGetExactMatchRoute e RtmGetExactMatchDestination

As funções [**RtmGetExactMatchRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute) e [**RtmGetExactMatchDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination) são usadas pelos clientes para localizar uma rota ou um destino específico. Essas funções economizam tempo fazendo o trabalho de comparação para o cliente.

Por exemplo, quando o RIP atualiza uma rota, o RIP deve manter as informações de métrica antigas. O RIP procura a rota e suas informações. Em seguida, o RIP pode copiar as informações e atualizar a rota.

## <a name="using-rtmgetmostspecificdestination"></a>Usando RtmGetMostSpecificDestination

A função [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination) é usada para localizar o destino que melhor corresponde ao prefixo de rede especificado.

Por exemplo, o Gerenciador do grupo de multicast usa essa função para executar uma verificação de encaminhamento de caminho reverso (RPF) em um único endereço. A função também pode ser usada para localizar o próximo salto local para um determinado próximo salto remoto.

Para obter um exemplo de código que mostra como usar essas funções, consulte [procurar rotas usando uma árvore de prefixo](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md) e [Pesquisar a melhor rota](search-for-the-best-route.md).

## <a name="using-rtmgetlessspecificdestination"></a>Usando RtmGetLessSpecificDestination

A função [**RtmGetLessSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination) é usada para localizar o destino que é a melhor correspondência seguinte para o prefixo de rede especificado. Essa função pode ser chamada repetidamente para retornar a próxima correspondência menos específica com sucesso, até que nenhum outro destino corresponda.

Essa função é chamada após uma chamada para [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination).

Para obter o código de exemplo que ilustra como usar essas funções, consulte [Pesquisar rotas usando uma árvore de prefixo](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md).

## <a name="using-rtmisbestroute"></a>Usando RtmIsBestRoute

A função [**RtmIsBestRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute) permite que um cliente descubra rapidamente se uma rota específica é a melhor rota para um destino. Por exemplo, um cliente pode precisar armazenar uma rota específica somente se for a melhor rota. Portanto, o cliente pode chamar essa função, em vez de enumerar todas as rotas e fazer a comparação em si.

 

 




