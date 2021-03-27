---
title: 'Função Texture2DArray:: GatherBlue (S, float, int)'
description: 'Retorna os componentes azuis dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear. | Função Texture2DArray:: GatherBlue (S, float, int)'
ms.assetid: f81596b5-afd1-4baf-b6c0-ca4661a3ef22
keywords:
- HLSL da função GatherBlue
topic_type:
- apiref
api_name:
- GatherBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1844b898deca767b04aba438f4784a54a5afa112
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989165"
---
# <a name="texture2darraygatherbluesfloatint-function"></a>Função Texture2DArray:: GatherBlue (S, float, int)

Retorna os componentes azuis dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.

## <a name="syntax"></a>Sintaxe

``` syntax
TemplateType GatherBlue(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*s* \[ em\]
</dt> <dd>

Tipo: **amostra**

O índice de amostra baseado em zero.

</dd> <dt>

*local* \[ do no\]
</dt> <dd>

Tipo: **float3**

As coordenadas de exemplo (u, v).

</dd> <dt>

*deslocamento* \[ no\]
</dt> <dd>

Tipo: **Int2**

Um deslocamento que é aplicado à coordenada de textura antes da amostragem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **TemplateType**

Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.

## <a name="remarks"></a>Comentários

Os exemplos de textura podem ser usados para interpolação bilinear.

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos GatherBlue](texture2darray-gatherblue.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




