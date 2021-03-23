---
title: Usando tabelas de descritores
description: As tabelas de descritores, cada uma identificando um intervalo em um heap de descritor, são associadas a Slots definidos pela assinatura raiz atual em uma lista de comandos.
ms.assetid: 4ECEC07A-7ABC-4C5F-B23C-36F0D92643FE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e589274fbb93e48e4d65e545a62999e654b7688f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104019"
---
# <a name="using-descriptor-tables"></a><span data-ttu-id="24fc2-103">Usando tabelas de descritores</span><span class="sxs-lookup"><span data-stu-id="24fc2-103">Using Descriptor Tables</span></span>

<span data-ttu-id="24fc2-104">As tabelas de descritores, cada uma identificando um intervalo em um heap de descritor, são associadas a Slots definidos pela assinatura raiz atual em uma lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="24fc2-104">Descriptor tables, each identifying a range in a descriptor heap, are bound at slots defined by the current root signature on a command list.</span></span>

-   [<span data-ttu-id="24fc2-105">Indexando tabelas de descritores</span><span class="sxs-lookup"><span data-stu-id="24fc2-105">Indexing Descriptor Tables</span></span>](#indexing-descriptor-tables)
-   [<span data-ttu-id="24fc2-106">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="24fc2-106">Related topics</span></span>](#related-topics)

<span data-ttu-id="24fc2-107">Os sombreadores podem localizar recursos referenciados pelos descritores que compõem a tabela de descritores.</span><span class="sxs-lookup"><span data-stu-id="24fc2-107">Shaders can locate resources referenced by the descriptors that make up the descriptor table.</span></span> <span data-ttu-id="24fc2-108">Outras associações de recurso-buffers de índice, buffer de vértice, buffers de saída de fluxo, destinos de renderização e estêncil de profundidade são feitos diretamente em uma lista de comandos em vez de por meio de descritores.</span><span class="sxs-lookup"><span data-stu-id="24fc2-108">Other resource bindings - Index Buffers, Vertex Buffer, Stream Output Buffers, Render Targets, and Depth Stencil are done directly on a command list rather than via descriptors.</span></span> <span data-ttu-id="24fc2-109">Para resumir:</span><span class="sxs-lookup"><span data-stu-id="24fc2-109">To summarize:</span></span>

<span data-ttu-id="24fc2-110">As referências de recurso a seguir podem compartilhar a mesma tabela e heap de descritores:</span><span class="sxs-lookup"><span data-stu-id="24fc2-110">The following resource references can share the same descriptor table and heap:</span></span>

-   <span data-ttu-id="24fc2-111">Exibições de recursos do sombreador</span><span class="sxs-lookup"><span data-stu-id="24fc2-111">Shader resource views</span></span>
-   <span data-ttu-id="24fc2-112">Exibições de acesso não ordenado</span><span class="sxs-lookup"><span data-stu-id="24fc2-112">Unordered access views</span></span>
-   <span data-ttu-id="24fc2-113">Exibições de buffer de constantes</span><span class="sxs-lookup"><span data-stu-id="24fc2-113">Constant buffer views</span></span>

<span data-ttu-id="24fc2-114">As seguintes referências de recurso devem estar em seu próprio heap de descritor:</span><span class="sxs-lookup"><span data-stu-id="24fc2-114">The following resource references must be in their own descriptor heap:</span></span>

-   <span data-ttu-id="24fc2-115">Amostradores</span><span class="sxs-lookup"><span data-stu-id="24fc2-115">Samplers</span></span>

<span data-ttu-id="24fc2-116">Os recursos a seguir não são colocados em tabelas de descritores ou heaps, mas são associados diretamente usando listas de comandos:</span><span class="sxs-lookup"><span data-stu-id="24fc2-116">The following resources are not placed in descriptor tables or heaps, but are bound directly using command lists:</span></span>

-   <span data-ttu-id="24fc2-117">Buffers de índice</span><span class="sxs-lookup"><span data-stu-id="24fc2-117">Index buffers</span></span>
-   <span data-ttu-id="24fc2-118">Buffers de vértice</span><span class="sxs-lookup"><span data-stu-id="24fc2-118">Vertex buffers</span></span>
-   <span data-ttu-id="24fc2-119">Buffers de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="24fc2-119">Stream output buffers</span></span>
-   <span data-ttu-id="24fc2-120">Destinos de renderização</span><span class="sxs-lookup"><span data-stu-id="24fc2-120">Render targets</span></span>
-   <span data-ttu-id="24fc2-121">Exibições de estêncil de profundidade</span><span class="sxs-lookup"><span data-stu-id="24fc2-121">Depth stencil views</span></span>

## <a name="indexing-descriptor-tables"></a><span data-ttu-id="24fc2-122">Indexando tabelas de descritores</span><span class="sxs-lookup"><span data-stu-id="24fc2-122">Indexing Descriptor Tables</span></span>

<span data-ttu-id="24fc2-123">Os sombreadores não podem indexar dinamicamente os limites da tabela do descritor de um determinado site de chamada no sombreador.</span><span class="sxs-lookup"><span data-stu-id="24fc2-123">Shaders cannot dynamically index across descriptor table boundaries from a given call-site in the shader.</span></span> <span data-ttu-id="24fc2-124">No entanto, a seleção de um descritor dentro de uma tabela de descritores pode ser indexada dinamicamente no código do sombreador dentro dos intervalos do mesmo tipo de descritor (como indexação em uma região contígua de SRVs).</span><span class="sxs-lookup"><span data-stu-id="24fc2-124">However, the selection of a descriptor within a descriptor table is allowed to be dynamically indexed in shader code within ranges of the same descriptor type (such as indexing across a contiguous region of SRVs).</span></span>

## <a name="related-topics"></a><span data-ttu-id="24fc2-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="24fc2-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24fc2-126">Tabelas de descritores</span><span class="sxs-lookup"><span data-stu-id="24fc2-126">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> </dl>

 

 




