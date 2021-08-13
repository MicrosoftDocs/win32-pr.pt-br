---
title: Função Texture2DArray::GatherGreen(S,float,int2,int2,int2,int2,uint)
description: Retorna os componentes verdes dos quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, juntamente com o status de mapeamento de peças. | Função Texture2DArray::GatherGreen(S,float,int2,int2,int2,int2,uint)
ms.assetid: 994320C6-3BE5-40F9-9B9F-1913134DA71A
keywords:
- Função GatherGreen HLSL
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4bdadf3f4260c39581d77d8334bf418494cf57596c03841a785756fbff797784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118788472"
---
# <a name="texture2darraygathergreensfloatint2int2int2int2uint-function"></a>Função Texture2DArray::GatherGreen(S,float,int2,int2,int2,int2,uint)

Retorna os componentes verdes dos quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, juntamente com o status de mapeamento de peças.

## <a name="syntax"></a>Sintaxe


``` syntax
TemplateType GatherGreen(
  in  SamplerState S,
  in  float        Location,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
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

</dd> <dt>

*Status* \[ out\]
</dt> <dd>

Tipo: **uint**

O status da operação. Você não pode acessar o status diretamente; Em vez disso, passe o status para a [**função intrínseca CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** retornará **TRUE** se todos os valores  da operação de **Exemplo,** **Coletar** ou Carregar correspondente acessarem blocos mapeados em um recurso lado a [lado.](/windows/desktop/direct3d11/direct3d-11-2-features) Se algum valor tiver sido retirado de um tile não mapeado, **CheckAccessFullyMapped** retornará **FALSE.**

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

[Métodos GatherGreen](texture2darray-gathergreen.md)
</dt> </dl>

 

 
