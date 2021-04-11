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
# <a name="retrieving-information"></a><span data-ttu-id="ca500-103">Recuperando informações</span><span class="sxs-lookup"><span data-stu-id="ca500-103">Retrieving Information</span></span>

<span data-ttu-id="ca500-104">O RTMv2 permite que um cliente recupere as informações referenciadas por um determinado identificador usando as funções [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)e [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) .</span><span class="sxs-lookup"><span data-stu-id="ca500-104">RTMv2 allows a client to retrieve the information referred to by a given handle using the [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo), and [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) functions.</span></span>

<span data-ttu-id="ca500-105">Essas chamadas de função têm funções correspondentes ([**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo), [**RtmReleaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)) para liberar os identificadores associados à estrutura de informações retornada pelo Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="ca500-105">These function calls have corresponding functions ([**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo), [**RtmReleaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)) to release the handles associated with the information structure returned by the routing table manager.</span></span>

> [!Note]  
> <span data-ttu-id="ca500-106">As informações para clientes estão disponíveis somente na instância atual e na família de endereços.</span><span class="sxs-lookup"><span data-stu-id="ca500-106">Information for clients is available only in the current instance and address family.</span></span>

 

<span data-ttu-id="ca500-107">Para obter um exemplo de código que mostra como usar essas funções, consulte [procurar a melhor rota](search-for-the-best-route.md).</span><span class="sxs-lookup"><span data-stu-id="ca500-107">For sample code that shows how to use these functions, see [Search For the Best Route](search-for-the-best-route.md).</span></span>

## <a name="using-rtmgetexactmatchroute-and-rtmgetexactmatchdestination"></a><span data-ttu-id="ca500-108">Usando RtmGetExactMatchRoute e RtmGetExactMatchDestination</span><span class="sxs-lookup"><span data-stu-id="ca500-108">Using RtmGetExactMatchRoute and RtmGetExactMatchDestination</span></span>

<span data-ttu-id="ca500-109">As funções [**RtmGetExactMatchRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute) e [**RtmGetExactMatchDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination) são usadas pelos clientes para localizar uma rota ou um destino específico.</span><span class="sxs-lookup"><span data-stu-id="ca500-109">The [**RtmGetExactMatchRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute) and [**RtmGetExactMatchDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination) functions are used by clients to find a specific route or destination.</span></span> <span data-ttu-id="ca500-110">Essas funções economizam tempo fazendo o trabalho de comparação para o cliente.</span><span class="sxs-lookup"><span data-stu-id="ca500-110">These functions save time by doing the comparison work for the client.</span></span>

<span data-ttu-id="ca500-111">Por exemplo, quando o RIP atualiza uma rota, o RIP deve manter as informações de métrica antigas.</span><span class="sxs-lookup"><span data-stu-id="ca500-111">For example, when RIP updates a route, RIP must retain the old metric information.</span></span> <span data-ttu-id="ca500-112">O RIP procura a rota e suas informações.</span><span class="sxs-lookup"><span data-stu-id="ca500-112">RIP searches for the route and its information.</span></span> <span data-ttu-id="ca500-113">Em seguida, o RIP pode copiar as informações e atualizar a rota.</span><span class="sxs-lookup"><span data-stu-id="ca500-113">Then RIP can copy the information and update the route.</span></span>

## <a name="using-rtmgetmostspecificdestination"></a><span data-ttu-id="ca500-114">Usando RtmGetMostSpecificDestination</span><span class="sxs-lookup"><span data-stu-id="ca500-114">Using RtmGetMostSpecificDestination</span></span>

<span data-ttu-id="ca500-115">A função [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination) é usada para localizar o destino que melhor corresponde ao prefixo de rede especificado.</span><span class="sxs-lookup"><span data-stu-id="ca500-115">The [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination) function is used to locate the destination that best matches the specified network prefix.</span></span>

<span data-ttu-id="ca500-116">Por exemplo, o Gerenciador do grupo de multicast usa essa função para executar uma verificação de encaminhamento de caminho reverso (RPF) em um único endereço.</span><span class="sxs-lookup"><span data-stu-id="ca500-116">For example, the multicast group manager uses this function to perform a reverse-path-forwarding (RPF) check on a single address.</span></span> <span data-ttu-id="ca500-117">A função também pode ser usada para localizar o próximo salto local para um determinado próximo salto remoto.</span><span class="sxs-lookup"><span data-stu-id="ca500-117">The function can also be used to find the local next hop for a given remote next hop.</span></span>

<span data-ttu-id="ca500-118">Para obter um exemplo de código que mostra como usar essas funções, consulte [procurar rotas usando uma árvore de prefixo](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md) e [Pesquisar a melhor rota](search-for-the-best-route.md).</span><span class="sxs-lookup"><span data-stu-id="ca500-118">For sample code that shows how to use these functions, see [Search for Routes Using a Prefix Tree](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md) and [Search For the Best Route](search-for-the-best-route.md).</span></span>

## <a name="using-rtmgetlessspecificdestination"></a><span data-ttu-id="ca500-119">Usando RtmGetLessSpecificDestination</span><span class="sxs-lookup"><span data-stu-id="ca500-119">Using RtmGetLessSpecificDestination</span></span>

<span data-ttu-id="ca500-120">A função [**RtmGetLessSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination) é usada para localizar o destino que é a melhor correspondência seguinte para o prefixo de rede especificado.</span><span class="sxs-lookup"><span data-stu-id="ca500-120">The [**RtmGetLessSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination) function is used to locate the destination that is the next-best match for the specified network prefix.</span></span> <span data-ttu-id="ca500-121">Essa função pode ser chamada repetidamente para retornar a próxima correspondência menos específica com sucesso, até que nenhum outro destino corresponda.</span><span class="sxs-lookup"><span data-stu-id="ca500-121">This function can be called repeatedly to return the next successive less-specific match, until no more destinations match.</span></span>

<span data-ttu-id="ca500-122">Essa função é chamada após uma chamada para [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination).</span><span class="sxs-lookup"><span data-stu-id="ca500-122">This function is called after a call to [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination).</span></span>

<span data-ttu-id="ca500-123">Para obter o código de exemplo que ilustra como usar essas funções, consulte [Pesquisar rotas usando uma árvore de prefixo](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md).</span><span class="sxs-lookup"><span data-stu-id="ca500-123">For sample code that illustrates how to use these functions, see [Search for Routes Using a Prefix Tree](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md).</span></span>

## <a name="using-rtmisbestroute"></a><span data-ttu-id="ca500-124">Usando RtmIsBestRoute</span><span class="sxs-lookup"><span data-stu-id="ca500-124">Using RtmIsBestRoute</span></span>

<span data-ttu-id="ca500-125">A função [**RtmIsBestRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute) permite que um cliente descubra rapidamente se uma rota específica é a melhor rota para um destino.</span><span class="sxs-lookup"><span data-stu-id="ca500-125">The [**RtmIsBestRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute) function enables a client to quickly find out whether or not a particular route is the best route to a destination.</span></span> <span data-ttu-id="ca500-126">Por exemplo, um cliente pode precisar armazenar uma rota específica somente se for a melhor rota.</span><span class="sxs-lookup"><span data-stu-id="ca500-126">For example, a client may need to store a particular route only if it is the best route.</span></span> <span data-ttu-id="ca500-127">Portanto, o cliente pode chamar essa função, em vez de enumerar todas as rotas e fazer a comparação em si.</span><span class="sxs-lookup"><span data-stu-id="ca500-127">Therefore, the client can call this function, instead of enumerating all routes and making the comparison itself.</span></span>

 

 




