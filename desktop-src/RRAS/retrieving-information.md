---
title: Recuperando informações
description: O RTMv2 permite que um cliente recupere as informações referenciadas por um determinado handle usando as funções RtmGetEntityInfo, RtmGetDestInfo, RtmGetRouteInfo e RtmGetNextHopInfo.
ms.assetid: a3fc2020-eac4-40a1-9a6e-6eaa2bcc582c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51958fccc8a07e8846705945d9210f4259dfd89b1e3cefccd65d57dd0f033757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028016"
---
# <a name="retrieving-information"></a>Recuperando informações

O RTMv2 permite que um cliente recupere as informações referenciadas por um determinado handle usando as funções [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)e [**RtmGetNextHopInfo.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo)

Essas chamadas de função têm funções correspondentes ([**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo), [**RtmReleaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)) para liberar os alças associados à estrutura de informações retornada pelo gerenciador de tabela de roteamento.

> [!Note]  
> As informações para clientes estão disponíveis apenas na instância atual e na família de endereços.

 

Para ver o código de exemplo que mostra como usar essas funções, [consulte Pesquisar a melhor rota.](search-for-the-best-route.md)

## <a name="using-rtmgetexactmatchroute-and-rtmgetexactmatchdestination"></a>Usando RtmGetExactMatchRoute e RtmGetExactMatchDestination

As [**funções RtmGetExactMatchRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute) e [**RtmGetExactMatchDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination) são usadas pelos clientes para encontrar uma rota ou destino específico. Essas funções economizam tempo fazendo o trabalho de comparação para o cliente.

Por exemplo, quando o UPDATE atualiza uma rota, o ROT deve reter as informações de métrica antigas. O RIP pesquisa a rota e suas informações. Em seguida, o RIP pode copiar as informações e atualizar a rota.

## <a name="using-rtmgetmostspecificdestination"></a>Usando RtmGetMostSpecificDestination

A [**função RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination) é usada para localizar o destino que melhor corresponde ao prefixo de rede especificado.

Por exemplo, o gerenciador de grupos multicast usa essa função para executar uma verificação de RPF (encaminhamento de caminho reverso) em um único endereço. A função também pode ser usada para encontrar o próximo salto local para um próximo salto remoto determinado.

Para um código de exemplo que mostra como usar essas funções, consulte Pesquisar rotas usando uma árvore [de prefixo](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md) e [Pesquisar a melhor rota.](search-for-the-best-route.md)

## <a name="using-rtmgetlessspecificdestination"></a>Usando RtmGetLessSpecificDestination

A [**função RtmGetLessSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination) é usada para localizar o destino que é a próxima melhor combinação para o prefixo de rede especificado. Essa função pode ser chamada repetidamente para retornar a próxima combinação sucessiva menos específica, até que nenhum outro destino seja corresponder.

Essa função é chamada após uma chamada para [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination).

Para um código de exemplo que ilustra como usar essas funções, consulte [Pesquisar rotas usando uma árvore de prefixo](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md).

## <a name="using-rtmisbestroute"></a>Usando RtmIsBestRoute

A [**função RtmIsTubeRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute) permite que um cliente descubra rapidamente se uma rota específica é ou não a melhor rota para um destino. Por exemplo, um cliente pode precisar armazenar uma rota específica somente se for a melhor rota. Portanto, o cliente pode chamar essa função, em vez de enumerar todas as rotas e fazer a própria comparação.

 

 




