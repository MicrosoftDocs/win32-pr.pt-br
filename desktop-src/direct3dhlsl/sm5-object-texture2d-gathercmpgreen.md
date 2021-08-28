---
title: Função Texture2D::GatherCmpGreen(S,float,float,int)
description: Para quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, retorna uma comparação de seu componente verde em relação a um valor de comparação. | Função Texture2D::GatherCmpGreen(S,float,float,int)
ms.assetid: 5a11ce0c-56b2-460a-95d7-15688dd158ff
keywords:
- Função GatherCmpGreen HLSL
topic_type:
- apiref
api_name:
- GatherCmpGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44ebf3590a756ea0bb78e6cc9c636523cb584cdd862059418f7b7c9508bfecfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095116"
---
# <a name="texture2dgathercmpgreensfloatfloatint-function"></a>Função Texture2D::GatherCmpGreen(S,float,float,int)

Para quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, retorna uma comparação de seu componente verde em relação a um valor de comparação.

## <a name="syntax"></a>Sintaxe

``` syntax
float4 GatherCmpGreen(
  in SamplerComparisonState s,
  in float2 location,
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

*local* \[ Em\]
</dt> <dd>

Tipo: **float2**

As coordenadas de exemplo (u,v).

</dd> <dt>

*comparar \_ valor* \[ em\]
</dt> <dd>

Tipo: **float**

Um valor para comparar cada um com cada valor amostrado.

</dd> <dt>

*deslocamento* \[ Em\]
</dt> <dd>

Tipo: **int2**

Um deslocamento que é aplicado à coordenada de textura antes da amostragem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **float4**

Um valor de quatro componentes, cada componente é o resultado de uma comparação por componente.

## <a name="remarks"></a>Comentários

As amostras de textura podem ser usadas para interpolação bilinear.

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos GatherCmpGreen](texture2d-gathercmpgreen.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




