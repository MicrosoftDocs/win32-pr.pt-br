---
description: Obtém o local atual dentro da largura, altura e profundidade obtidas com o valor do sistema [**DispatchRaysDimensions**](dispatchraysdimensions.md) intrínseco.
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
ms.openlocfilehash: aa26400c26aba4ee9e647bcd0a79bad3f3d52f7c
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2020
ms.locfileid: "105781349"
---
# <a name="dispatchraysindex"></a>DispatchRaysIndex 

Obtém o local atual dentro da largura, altura e profundidade obtidas com o valor do sistema [**DispatchRaysDimensions**](dispatchraysdimensions.md) intrínseco.

## <a name="syntax"></a>Sintaxe

```syntax
uint3 DispatchRaysIndex();
```

## <a name="remarks"></a>Comentários

Essa função pode ser chamada nos seguintes tipos de sombreador raytracing.

* [**Sombreador de todos os cliques**](any-hit-shader.md)
* [**Sombreador resgatável**](callable-shader.md)
* [**Sombreador do clique mais próximo**](closest-hit-shader.md)
* [**Sombreador de interseção**](intersection-shader.md)
* [**Sombreador de resolução**](miss-shader.md)
* [**Sombreador da geração de raio**](ray-generation-shader.md)

## <a name="see-also"></a>Confira também

* [Referência HLSL de raytracing do Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
