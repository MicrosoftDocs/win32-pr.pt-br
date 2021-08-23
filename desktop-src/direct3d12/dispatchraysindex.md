---
description: Obtém o local atual dentro da largura, altura e profundidade obtidas com o valor intrínseco do sistema [**DispatchRaysDimensions.**](dispatchraysdimensions.md)
title: 'DispatchRaysIndex '
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysIndex
api_type:
- NA
ms.openlocfilehash: 1b40987c76f42d41d74b7cb3d41f35cc20bd5a6ac1414ae9b010cedcfa7ef9fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124160"
---
# <a name="dispatchraysindex"></a>DispatchRaysIndex 

Obtém o local atual dentro da largura, altura e profundidade obtidas com o valor intrínseco do sistema [**DispatchRaysDimensions.**](dispatchraysdimensions.md)

## <a name="syntax"></a>Sintaxe

```syntax
uint3 DispatchRaysIndex();
```

## <a name="remarks"></a>Comentários

Essa função pode ser chamada dos seguintes tipos de sombreador de raio.

* [**Sombreador de todos os cliques**](any-hit-shader.md)
* [**Sombreador resgatável**](callable-shader.md)
* [**Sombreador do clique mais próximo**](closest-hit-shader.md)
* [**Sombreador de interseção**](intersection-shader.md)
* [**Sombreador de resolução**](miss-shader.md)
* [**Sombreador da geração de raio**](ray-generation-shader.md)

## <a name="see-also"></a>Confira também

* [Referência HLSL de raytracing do Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
