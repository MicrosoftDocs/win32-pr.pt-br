---
title: Função Texture2D::GatherCmpAlpha(S,float,float,int)
description: Para quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, retorna uma comparação de seu componente alfa em relação a um valor de comparação. | Função Texture2D::GatherCmpAlpha(S,float,float,int)
ms.assetid: 6fa60604-1eac-405d-bffa-3055569b7a09
keywords:
- Função GatherCmpAlpha HLSL
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f6e350ed14482646562121d910a8bd35f30403acf8dbde7df249ee1bc6ca800a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789599"
---
# <a name="texture2dgathercmpalphasfloatfloatint-function"></a>Função Texture2D::GatherCmpAlpha(S,float,float,int)

Para quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, retorna uma comparação de seu componente alfa em relação a um valor de comparação.

## <a name="syntax"></a>Sintaxe

``` syntax
float4 GatherCmpAlpha(
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

[Métodos GatherCmpAlpha](texture2d-gathercmpalpha.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




