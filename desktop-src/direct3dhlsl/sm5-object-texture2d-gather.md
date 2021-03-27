---
title: 'Função Texture2D:: gather (S, float, int)'
description: 'Retorna os quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear. | Função Texture2D:: gather (S, float, int)'
ms.assetid: 5d196c1c-8cc9-4add-9d33-654294314ee2
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
ms.openlocfilehash: 4d0a58be0580572441f91a3b3f637601d70cd9c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103663909"
---
# <a name="texture2dgathersfloatint-function"></a>Função Texture2D:: gather (S, float, int)

Retorna os quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.

## <a name="syntax"></a>Sintaxe

``` syntax
TemplateType Gather(
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

O deslocamento aplicado às coordenadas de textura antes da amostragem.

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

[Reunir métodos](texture2d-gather.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




