---
description: Composição e disposição em camadas
ms.assetid: c1aefd92-b47f-4af1-8299-9ba401ad5fe8
title: Composição e disposição em camadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7dce1e1df87b5ffc5c65e9090c6fb7266b972d3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105778496"
---
# <a name="composition-and-layering"></a><span data-ttu-id="f418e-103">Composição e disposição em camadas</span><span class="sxs-lookup"><span data-stu-id="f418e-103">Composition and Layering</span></span>

<span data-ttu-id="f418e-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="f418e-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="f418e-105">Em uma coleção de faixas, a primeira faixa tem a prioridade mais baixa (prioridade 0) e cada faixa subsequente tem uma prioridade um nível acima.</span><span class="sxs-lookup"><span data-stu-id="f418e-105">In a collection of tracks, the first track has the lowest priority (priority 0) and each subsequent track has a priority one level higher.</span></span> <span data-ttu-id="f418e-106">Em cada nível de prioridade, os clipes de origem nesse controle ocultam os clipes de origem nas faixas abaixo dela, a menos que essa camada também contenha uma transição.</span><span class="sxs-lookup"><span data-stu-id="f418e-106">At each priority level, the source clips in that track hide the source clips in the tracks below it, unless that layer also contains a transition.</span></span> <span data-ttu-id="f418e-107">Assim, você pode imaginar que o DES faz várias passagens ao renderizar.</span><span class="sxs-lookup"><span data-stu-id="f418e-107">Thus you can imagine DES making several passes when it renders.</span></span>

<span data-ttu-id="f418e-108">Primeiro, ele processa Track 0.</span><span class="sxs-lookup"><span data-stu-id="f418e-108">First, it renders track 0.</span></span> <span data-ttu-id="f418e-109">Não há nada "em" Track 0 ", portanto, as regiões vazias são renderizadas como uma imagem preta sólida.</span><span class="sxs-lookup"><span data-stu-id="f418e-109">There is nothing "under" Track 0, so empty regions are rendered as a solid black image.</span></span> <span data-ttu-id="f418e-110">As transições nessa camada ocorrem entre a imagem preta e a trilha 0 ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="f418e-110">Transitions in this layer occur between the black image and track 0 or vice versa.</span></span> <span data-ttu-id="f418e-111">O DES dispõe da trilha 1 sobre o Track 0, gerando qualquer transição entre as duas faixas.</span><span class="sxs-lookup"><span data-stu-id="f418e-111">DES lays track 1 on top of track 0, generating any transitions between the two tracks.</span></span> <span data-ttu-id="f418e-112">O resultado é a composição das duas faixas.</span><span class="sxs-lookup"><span data-stu-id="f418e-112">The result is the composite of the two tracks.</span></span> <span data-ttu-id="f418e-113">Em seguida, ele coloca o Track 2 nesta composição.</span><span class="sxs-lookup"><span data-stu-id="f418e-113">Next, it places track 2 onto this composite.</span></span> <span data-ttu-id="f418e-114">As transições nessa camada ocorrem entre a composição e a faixa 2.</span><span class="sxs-lookup"><span data-stu-id="f418e-114">Transitions at this layer occur between the composite and track 2.</span></span> <span data-ttu-id="f418e-115">O processo continua até que a última faixa (de prioridade mais alta) seja colocada inativa.</span><span class="sxs-lookup"><span data-stu-id="f418e-115">The process continues until the last (highest-priority) track is put down.</span></span>

<span data-ttu-id="f418e-116">Quando várias faixas são compostas juntas, elas se comportam como uma única faixa (chamada de faixa virtual).</span><span class="sxs-lookup"><span data-stu-id="f418e-116">When several tracks are composited together, they behave like a single track (called a virtual track).</span></span> <span data-ttu-id="f418e-117">O objeto de composição encapsula esse comportamento, fazendo transições complexas possíveis.</span><span class="sxs-lookup"><span data-stu-id="f418e-117">The composition object encapsulates this behavior, making complex transitions possible.</span></span> <span data-ttu-id="f418e-118">Por exemplo, um clipe de vídeo pode apagar para um segundo clipe, enquanto a composição (ambos os clipes mais o apagamento) esmaece para um terceiro clipe.</span><span class="sxs-lookup"><span data-stu-id="f418e-118">For example, one video clip can wipe to a second clip, while the composite (both clips plus the wipe) fades to a third clip.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f418e-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f418e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f418e-120">Introdução com os serviços de edição do DirectShow</span><span class="sxs-lookup"><span data-stu-id="f418e-120">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



