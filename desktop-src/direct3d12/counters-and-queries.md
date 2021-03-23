---
title: Contadores, consultas e predicação
description: Os contadores de saída de fluxo e UAV operam no Direct3D 12 em um método semelhante ao Direct3D 11, embora agora a memória para os contadores deva ser alocada pelo aplicativo, o driver não o faz.
ms.assetid: 8BDDAFEF-57D4-4EF5-BB0C-6C96AF557A45
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314c01b05ac31e5d5f8348b775c8955ae382f5ed
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104548306"
---
# <a name="counters-queries-and-predication"></a><span data-ttu-id="f0905-103">Contadores, consultas e predicação</span><span class="sxs-lookup"><span data-stu-id="f0905-103">Counters, queries, and predication</span></span>

<span data-ttu-id="f0905-104">Este tópico aborda contadores de saída de fluxo, contadores de UAV, consultas e predicação.</span><span class="sxs-lookup"><span data-stu-id="f0905-104">This topic covers stream-output counters, UAV counters, queries, and predication.</span></span>

<span data-ttu-id="f0905-105">Os contadores de saída de fluxo e UAV operam no Direct3D 12 em um método semelhante ao Direct3D 11, embora agora a memória para os contadores deva ser alocada pelo aplicativo, o driver não o faz.</span><span class="sxs-lookup"><span data-stu-id="f0905-105">Stream output and UAV counters operate in Direct3D 12 in a similar method to Direct3D 11, although now memory for the counters must be allocated by the app, the driver does not do it.</span></span> <span data-ttu-id="f0905-106">As consultas no Direct3D 12 são mais diferentes das do Direct3D 11, com a adição de limites e outros processos que eliminam a necessidade de alguns tipos de consulta.</span><span class="sxs-lookup"><span data-stu-id="f0905-106">Queries in Direct3D 12 are more different from those in Direct3D 11, with the addition of fences and other processes that remove the need for some query types.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f0905-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="f0905-107">In this section</span></span>



| <span data-ttu-id="f0905-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="f0905-108">Topic</span></span>                                                           | <span data-ttu-id="f0905-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f0905-109">Description</span></span>                                                                                                                                                                                  |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0905-110">Contadores de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f0905-110">Stream Output Counters</span></span>](stream-output-counters.md)<br/> | <span data-ttu-id="f0905-111">A saída de fluxo é a capacidade da GPU de gravar vértices em um buffer.</span><span class="sxs-lookup"><span data-stu-id="f0905-111">Stream output is the ability of the GPU to write vertices to a buffer.</span></span> <span data-ttu-id="f0905-112">Os contadores de saída do fluxo monitoram o progresso.</span><span class="sxs-lookup"><span data-stu-id="f0905-112">The stream output counters monitor progress.</span></span><br/>                                                               |
| [<span data-ttu-id="f0905-113">Contadores de UAV</span><span class="sxs-lookup"><span data-stu-id="f0905-113">UAV Counters</span></span>](uav-counters.md)<br/>                     | <span data-ttu-id="f0905-114">Os contadores UAV podem ser usados para associar um contador atômico de 32 bits a um UAV (unordened-Access-View).</span><span class="sxs-lookup"><span data-stu-id="f0905-114">UAV counters can be used to associate a 32-bit atomic counter with an unordered-access-view (UAV).</span></span><br/>                                                                                |
| [<span data-ttu-id="f0905-115">Consultas</span><span class="sxs-lookup"><span data-stu-id="f0905-115">Queries</span></span>](queries.md)<br/>                               | <span data-ttu-id="f0905-116">No Direct3D 12, as consultas são agrupadas em matrizes de consultas chamadas de heap de consulta.</span><span class="sxs-lookup"><span data-stu-id="f0905-116">In Direct3D 12, queries are grouped into arrays of queries called a query heap.</span></span> <span data-ttu-id="f0905-117">Um heap de consulta tem um tipo que define os tipos válidos de consultas que podem ser usadas com esse heap.</span><span class="sxs-lookup"><span data-stu-id="f0905-117">A query heap has a type which defines the valid types of queries that can be used with that heap.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="f0905-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f0905-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0905-119">Medição de desempenho</span><span class="sxs-lookup"><span data-stu-id="f0905-119">Performance Measurement</span></span>](performance-measurement.md)
</dt> </dl>

 

 





