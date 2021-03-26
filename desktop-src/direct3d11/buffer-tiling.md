---
title: Buffers colocados lado a lado
description: Um recurso de buffer é dividido em blocos de 64KB, com algum espaço vazio no último bloco se o tamanho não é um múltiplo de 64KB.
ms.assetid: 979EFCF3-1FE1-412A-A19D-F1B1CF86423B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061fafa009e554499822c90c8fb6c0c8f34e47f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823799"
---
# <a name="buffer-tiling"></a><span data-ttu-id="20e39-103">Buffers colocados lado a lado</span><span class="sxs-lookup"><span data-stu-id="20e39-103">Buffer tiling</span></span>

<span data-ttu-id="20e39-104">Um recurso de [buffer](overviews-direct3d-11-resources-buffers.md) é dividido em blocos de 64 KB, com espaço vazio no último bloco, se o tamanho não for um múltiplo de 64 KB.</span><span class="sxs-lookup"><span data-stu-id="20e39-104">A [Buffer](overviews-direct3d-11-resources-buffers.md) resource is divided into 64KB tiles, with some empty space in the last tile if the size is not a multiple of 64KB.</span></span>

<span data-ttu-id="20e39-105">Buffers estruturados não devem ter nenhuma restrição sobre a distância lado a lado.</span><span class="sxs-lookup"><span data-stu-id="20e39-105">Structured buffers must have no constraint on the stride to be tiled.</span></span> <span data-ttu-id="20e39-106">Mas as otimizações de desempenho possível no hardware para o uso de [**StructuredBuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) pode ser sacrificada, tornando-os lado a lado em primeiro lugar.</span><span class="sxs-lookup"><span data-stu-id="20e39-106">But possible performance optimizations in hardware for using [**StructuredBuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) can be sacrificed by making them tiled in the first place.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20e39-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="20e39-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20e39-108">Como a área de um recurso do lado do ladrilho é colocada</span><span class="sxs-lookup"><span data-stu-id="20e39-108">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 