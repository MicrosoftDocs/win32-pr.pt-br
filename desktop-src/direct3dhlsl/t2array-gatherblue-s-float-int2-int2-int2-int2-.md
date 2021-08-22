---
title: Função GatherBlue(S,float,int2,int2,int2,int2) (referência HLSL)
description: Retorna os componentes azuis dos quatro valores de texel que seriam usados em uma operação de filtragem bi-linear. | Função GatherBlue(S,float,int2,int2,int2,int2) (referência HLSL)
ms.assetid: 0DDD3235-4F12-4D74-975A-F70A271C1FC0
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
ms.openlocfilehash: 8d23ae18d403f83145b5746fa33b56fbadb9ea5d9a4b3f5b3ca79e13e5da7eb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043654"
---
# <a name="gatherbluesfloatint2int2int2int2-function-hlsl-reference"></a>Função GatherBlue(S,float,int2,int2,int2,int2) (referência HLSL)

Retorna os componentes azuis dos quatro valores de texel que seriam usados em uma operação de filtragem bi-linear.

## <a name="syntax"></a>Sintaxe


``` syntax
TemplateType GatherBlue(
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

Tipo: **SamplerState**

O índice de amostra baseado em zero.

</dd> <dt>

*Localização* \[ Em\]
</dt> <dd>

Tipo: **float**

As coordenadas de exemplo (u,v).

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

[Métodos GatherBlue](texture2darray-gatherblue.md)
</dt> </dl>

 

 




