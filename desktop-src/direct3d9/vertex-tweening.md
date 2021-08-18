---
description: A interpolação de vértices combina duas posições fornecidas pelo usuário (ou normais).
ms.assetid: vs|directx_sdk|~\vertex_tweening.htm
title: Interpolação de vértice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8486f53e4eb1a3a003b15255baeb50d30f0ed205f4259625d7d66ba33e8274c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519217"
---
# <a name="vertex-tweening-direct3d-9"></a>Interpolação de vértice (Direct3D 9)

A interpolação de vértices combina duas posições fornecidas pelo usuário (ou normais). A interpolação é mutuamente exclusiva da mistura de vértices com pesos. A interpolação é executada antes da iluminação e do recorte e é habilitada pela configuração de D3DRS \_ VERTEXBLEND para D3DVBF \_ interpolação. A posição do vértice resultante é computada por:


```
POSITION = POSITION1 * (1.0 - TWEENFACTOR) + POSITION2 * TWEENFACTOR
```



A mesma abordagem é usada para calcular Normals. Para obter mais informações, consulte [usando a interpolação de vértices (Direct3D 9)](using-vertex-tweening.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mesclagem de geometria](geometry-blending.md)
</dt> </dl>

 

 



