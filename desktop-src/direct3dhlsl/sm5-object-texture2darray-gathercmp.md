---
title: 'Função Texture2DArray:: GatherCmp (S, float, float, int)'
description: 'Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna a comparação contra um valor de comparação. | Função Texture2DArray:: GatherCmp (S, float, float, int)'
ms.assetid: 7bb86448-cc73-4423-9ef4-149427cffc95
keywords:
- HLSL da função GatherCmp
topic_type:
- apiref
api_name:
- GatherCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fbac4c231f7a7070d3ca4549f3d1189b81292b8c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968312"
---
# <a name="texture2darraygathercmpsfloatfloatint-function"></a>Função Texture2DArray:: GatherCmp (S, float, float, int)

Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna a comparação contra um valor de comparação.

## <a name="syntax"></a>Sintaxe

``` syntax
float4 GatherCmp(
  in SamplerComparisonState s,
  in float3 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*s* \[ em\]
</dt> <dd>

Tipo: **SamplerComparisonState**

O índice de amostra baseado em zero.

</dd> <dt>

*local* \[ do no\]
</dt> <dd>

Tipo: **float3**

As coordenadas de exemplo (u, v).

</dd> <dt>

*comparar \_ valor* \[ em\]
</dt> <dd>

Tipo: **float**

Um valor para comparar cada valor de amostra.

</dd> <dt>

*deslocamento* \[ no\]
</dt> <dd>

Tipo: **Int2**

Um deslocamento que é aplicado à coordenada de textura antes da amostragem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **FLOAT4**

Um valor de quatro componentes, cada componente é o resultado de uma comparação por componente.

## <a name="remarks"></a>Comentários

Os exemplos de textura podem ser usados para interpolação bilinear.

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos GatherCmp](texture2darray-gathercmp.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




