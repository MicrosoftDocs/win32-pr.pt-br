---
title: Tabelas de descritores
description: Uma tabela de descritores é logicamente uma matriz de descritores.
ms.assetid: 5faf294f-acd5-4b39-92f4-1d6b2abe3040
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10414f8458006029f3279203e949b43410911fd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105046"
---
# <a name="descriptor-tables"></a><span data-ttu-id="d92ed-103">Tabelas de descritores</span><span class="sxs-lookup"><span data-stu-id="d92ed-103">Descriptor Tables</span></span>

<span data-ttu-id="d92ed-104">Uma tabela de descritores é logicamente uma matriz de descritores.</span><span class="sxs-lookup"><span data-stu-id="d92ed-104">A descriptor table is logically an array of descriptors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d92ed-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="d92ed-105">In this section</span></span>



| <span data-ttu-id="d92ed-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="d92ed-106">Topic</span></span>                                                                                 | <span data-ttu-id="d92ed-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d92ed-107">Description</span></span>                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d92ed-108">Visão geral das tabelas de descritores</span><span class="sxs-lookup"><span data-stu-id="d92ed-108">Descriptor Tables Overview</span></span>](descriptor-tables-overview.md)<br/>               | <span data-ttu-id="d92ed-109">Cada tabela de descritores armazena os descritores de um ou mais tipos-SRVs, UAVe, CBVs e amostras.</span><span class="sxs-lookup"><span data-stu-id="d92ed-109">Each descriptor table stores descriptors of one or more types - SRVs, UAVe, CBVs, and Samplers.</span></span> <span data-ttu-id="d92ed-110">Uma tabela de descritores não é uma alocação de memória; é simplesmente um deslocamento e um comprimento em um heap de descritor.</span><span class="sxs-lookup"><span data-stu-id="d92ed-110">A descriptor table is not an allocation of memory; it is simply an offset and length into a descriptor heap.</span></span><br/> |
| [<span data-ttu-id="d92ed-111">Usando tabelas de descritores</span><span class="sxs-lookup"><span data-stu-id="d92ed-111">Using Descriptor Tables</span></span>](using-descriptor-tables.md)<br/>                     | <span data-ttu-id="d92ed-112">As tabelas de descritores, cada uma identificando um intervalo em um heap de descritor, são associadas a Slots definidos pela assinatura raiz atual em uma lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="d92ed-112">Descriptor tables, each identifying a range in a descriptor heap, are bound at slots defined by the current root signature on a command list.</span></span> <br/>                                                               |
| [<span data-ttu-id="d92ed-113">Uso avançado de tabelas de descritores</span><span class="sxs-lookup"><span data-stu-id="d92ed-113">Advanced Use of Descriptor Tables</span></span>](advanced-use-of-descriptor-tables.md)<br/> | <span data-ttu-id="d92ed-114">As seções a seguir fornecem informações sobre o uso avançado de tabelas de descritores.</span><span class="sxs-lookup"><span data-stu-id="d92ed-114">The following sections provide information about the advanced use of descriptor tables.</span></span><br/>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="d92ed-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d92ed-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d92ed-116">Heaps de descritores</span><span class="sxs-lookup"><span data-stu-id="d92ed-116">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> <dt>

[<span data-ttu-id="d92ed-117">Associação de recursos</span><span class="sxs-lookup"><span data-stu-id="d92ed-117">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="d92ed-118">Assinaturas raiz</span><span class="sxs-lookup"><span data-stu-id="d92ed-118">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 





