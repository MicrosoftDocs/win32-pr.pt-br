---
title: Buffers colocados lado a lado
description: Um recurso de buffer é dividido em blocos de 64KB, com algum espaço vazio no último bloco se o tamanho não é um múltiplo de 64KB.
ms.assetid: 979EFCF3-1FE1-412A-A19D-F1B1CF86423B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36352f492efb88bf220035d737b5767ef086e74ab91ffb4228d7734f838425b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734238"
---
# <a name="buffer-tiling"></a>Buffers colocados lado a lado

Um [recurso](overviews-direct3d-11-resources-buffers.md) de buffer é dividido em blocos de 64KB, com algum espaço vazio no último bloco se o tamanho não for um múltiplo de 64KB.

Buffers estruturados não devem ter nenhuma restrição sobre a distância lado a lado. Mas as otimizações de desempenho possível no hardware para o uso de [**StructuredBuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) pode ser sacrificada, tornando-os lado a lado em primeiro lugar.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como a área de um recurso lado a lado é lado a lado](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 