---
title: Função Texture2D::GatherBlue(S,float,int)
description: Retorna os componentes azuis dos quatro valores de texel que seriam usados em uma operação de filtragem bi-linear. | Função Texture2D::GatherBlue(S,float,int)
ms.assetid: 6d753ef2-2818-4990-81df-52dda044d21d
keywords:
- Função GatherBlue HLSL
topic_type:
- apiref
api_name:
- GatherBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caadf785617ee1e28e2bfffef4d7ccb534bff8d760b982ccc2284920475729a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789811"
---
# <a name="texture2dgatherbluesfloatint-function"></a>Função Texture2D::GatherBlue(S,float,int)

Retorna os componentes azuis dos quatro valores de texel que seriam usados em uma operação de filtragem bi-linear.

## <a name="syntax"></a>Sintaxe

``` syntax
TemplateType GatherBlue(
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

[Métodos GatherBlue](texture2d-gatherblue.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




