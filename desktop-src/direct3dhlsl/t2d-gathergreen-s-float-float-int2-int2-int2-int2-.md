---
title: 'Função Texture2D:: GatherGreen (S, float, Int2, Int2, Int2, Int2)'
description: 'Retorna os componentes verdes dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear. | Função Texture2D:: GatherGreen (S, float, Int2, Int2, Int2, Int2)'
ms.assetid: 043434C0-BB12-4A08-A3E5-34C9738DEBDB
keywords:
- HLSL da função GatherGreen
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af1bbaf4052bab32ab1841542bfb63322de154ba
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104506418"
---
# <a name="texture2dgathergreensfloatint2int2int2int2-function"></a>Função Texture2D:: GatherGreen (S, float, Int2, Int2, Int2, Int2)

Retorna os componentes verdes dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.

## <a name="syntax"></a>Sintaxe


``` syntax
TemplateType GatherGreen(
  in SamplerState S,
  in float        Location,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*S* \[ em\]
</dt> <dd>

Tipo: **samplestate**

O índice de amostra baseado em zero.

</dd> <dt>

*Local* \[ do no\]
</dt> <dd>

Tipo: **float**

As coordenadas de exemplo (u, v).

</dd> <dt>

*Offset1* \[ no\]
</dt> <dd>

Tipo: **Int2**

O primeiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.

</dd> <dt>

*Offset2* \[ no\]
</dt> <dd>

Tipo: **Int2**

O segundo componente de deslocamento aplicado às coordenadas de textura antes da amostragem.

</dd> <dt>

*Offset3* \[ no\]
</dt> <dd>

Tipo: **Int2**

O terceiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.

</dd> <dt>

*Offset4* \[ no\]
</dt> <dd>

Tipo: **Int2**

O quarto componente de deslocamento aplicado às coordenadas de textura antes da amostragem.

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

[Métodos GatherGreen](texture2d-gathergreen.md)
</dt> </dl>

 

 




