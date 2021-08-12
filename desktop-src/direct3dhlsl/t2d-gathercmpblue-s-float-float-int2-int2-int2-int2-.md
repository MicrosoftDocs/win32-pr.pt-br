---
title: Função Texture2D::GatherCmpBlue(S,float,float,int2,int2,int2,int2)
description: Para quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, retorna uma comparação de seu componente azul em relação a um valor de comparação. | Função Texture2D::GatherCmpBlue(S,float,float,int2,int2,int2,int2)
ms.assetid: DAA41BF3-6037-404F-9B35-C5F1302367B9
keywords:
- Função GatherCmpBlue HLSL
topic_type:
- apiref
api_name:
- GatherCmpBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 26638d790223f362dc2ba5d23f5f70500fe967fd6e026aef8321875b02872dbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285016"
---
# <a name="texture2dgathercmpbluesfloatfloatint2int2int2int2-function"></a>Função Texture2D::GatherCmpBlue(S,float,float,int2,int2,int2,int2)

Para quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, retorna uma comparação de seu componente azul em relação a um valor de comparação.

## <a name="syntax"></a>Sintaxe


``` syntax
TemplateType GatherCmpBlue(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
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

Tipo: **SamplerState**

O índice de amostra baseado em zero.

</dd> <dt>

*Localização* \[ Em\]
</dt> <dd>

Tipo: **float**

As coordenadas de exemplo (u,v).

</dd> <dt>

*CompareValue* \[ Em\]
</dt> <dd>

Tipo: **float**

Um valor para comparar cada um com cada valor amostrado.

</dd> <dt>

*Offset1* \[ Em\]
</dt> <dd>

Tipo: **int2**

O primeiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.

</dd> <dt>

*Offset2* \[ Em\]
</dt> <dd>

Tipo: **int2**

O segundo componente de deslocamento aplicado às coordenadas de textura antes da amostragem.

</dd> <dt>

*Offset3* \[ Em\]
</dt> <dd>

Tipo: **int2**

O terceiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.

</dd> <dt>

*Offset4* \[ Em\]
</dt> <dd>

Tipo: **int2**

O quarto componente de deslocamento aplicado às coordenadas de textura antes da amostragem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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

[Métodos GatherCmpBlue](texture2d-gathercmpblue.md)
</dt> </dl>

 

 




