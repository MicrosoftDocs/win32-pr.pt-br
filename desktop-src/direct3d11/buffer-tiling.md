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
# <a name="buffer-tiling"></a>Buffers colocados lado a lado

Um recurso de [buffer](overviews-direct3d-11-resources-buffers.md) é dividido em blocos de 64 KB, com espaço vazio no último bloco, se o tamanho não for um múltiplo de 64 KB.

Buffers estruturados não devem ter nenhuma restrição sobre a distância lado a lado. Mas as otimizações de desempenho possível no hardware para o uso de [**StructuredBuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) pode ser sacrificada, tornando-os lado a lado em primeiro lugar.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como a área de um recurso do lado do ladrilho é colocada](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 