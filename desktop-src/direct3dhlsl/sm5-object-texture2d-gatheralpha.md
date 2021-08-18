---
title: Função Texture2D::GatherAlpha(S,float,int)
description: Retorna os componentes alfa dos quatro valores de texel que seriam usados em uma operação de filtragem bi-linear. | Função Texture2D::GatherAlpha(S,float,int)
ms.assetid: 4c980e06-d768-479e-bee3-1b2541c23038
keywords:
- Função GatherAlpha HLSL
topic_type:
- apiref
api_name:
- GatherAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 12ea7c643c8e86925163594856980c20aae09d61cd9421d6060449ed80da81f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789821"
---
# <a name="texture2dgatheralphasfloatint-function"></a>Função Texture2D::GatherAlpha(S,float,int)

Retorna os componentes alfa dos quatro valores de texel que seriam usados em uma operação de filtragem bi-linear.

## <a name="syntax"></a>Sintaxe

``` syntax
TemplateType GatherAlpha(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*s* \[ em\]
</dt> <dd>

Tipo: **sampler**

O índice de amostra baseado em zero.

</dd> <dt>

*local* \[ Em\]
</dt> <dd>

Tipo: **float2**

As coordenadas de exemplo (u,v).

</dd> <dt>

*deslocamento* \[ Em\]
</dt> <dd>

Tipo: **int2**

Um deslocamento que é aplicado à coordenada de textura antes da amostragem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **TemplateType**

Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.

## <a name="remarks"></a>Comentários

As amostras de textura podem ser usadas para interpolação bilinear.

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos GatherAlpha](texture2d-gatheralpha.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




