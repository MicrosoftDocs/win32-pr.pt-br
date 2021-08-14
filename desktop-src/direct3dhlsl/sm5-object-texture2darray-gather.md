---
title: 'Função Texture2DArray:: gather (S, float, int)'
description: 'Retorna os quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear. | Função Texture2DArray:: gather (S, float, int)'
ms.assetid: b0355158-01c8-45a1-bb5d-29a8c43b1685
keywords:
- Coletar HLSL da função
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f684efa4cb597a640b78a2cdd08074d47fec3b4ec2f8a4a6fe6bcf993fd53ca3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119367796"
---
# <a name="texture2darraygathersfloatint-function"></a>Função Texture2DArray:: gather (S, float, int)

Retorna os quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.

## <a name="syntax"></a>Sintaxe

``` syntax
TemplateType Gather(
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

O deslocamento aplicado às coordenadas de textura antes da amostragem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **TemplateType**

Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Reunir métodos](texture2darray-gather.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




