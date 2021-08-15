---
title: 'Função Texture2D:: GatherRed (S, float, int)'
description: 'Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente vermelho em relação a um valor de comparação. | Função Texture2D:: GatherRed (S, float, int)'
ms.assetid: 6d2d1556-d52f-4625-93ca-34da399f9a8b
keywords:
- HLSL da função GatherRed
topic_type:
- apiref
api_name:
- GatherRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 879ba1cdad400a065fae46bd858db5569390ae0ae2a2ad338bfb9faed62bbdca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508635"
---
# <a name="texture2dgatherredsfloatint-function"></a>Função Texture2D:: GatherRed (S, float, int)

Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente vermelho em relação a um valor de comparação.

## <a name="syntax"></a>Sintaxe

``` syntax
TemplateType GatherRed(
  in sampler s,
  in float2 location,
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

Tipo: **float2**

As coordenadas de exemplo (u, v).

</dd> <dt>

*deslocamento* \[ no\]
</dt> <dd>

Tipo: **Int2**

Um deslocamento que é aplicado à coordenada de textura antes da amostragem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **TemplateType**

Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.

## <a name="remarks"></a>Comentários

Os exemplos de textura podem ser usados para interpolação bilinear.

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos GatherRed](texture2d-gatherred.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




