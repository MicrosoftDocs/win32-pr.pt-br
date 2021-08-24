---
title: Função Texture2DArray::GatherCmpRed(S,float,float,int2,int2, int2,int2,uint)
description: Para quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, retorna uma comparação de seu componente vermelho em relação a um valor de comparação junto com o status de mapeamento de peça. | Função Texture2DArray::GatherCmpRed(S,float,float,int2,int2, int2,int2,uint)
ms.assetid: E41E1328-AE31-445E-AF01-1DB201E8A278
keywords:
- Função GatherCmpRed HLSL
topic_type:
- apiref
api_name:
- GatherCmpRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 724c3b256824c080623932ea84b3fe2ae2fab625847fc874f7e98c7637e5f2d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118507349"
---
# <a name="texture2darraygathercmpredsfloatfloatint2int2int2int2uint-function"></a>Função Texture2DArray::GatherCmpRed(S,float,float,int2,int2, int2,int2,uint)

Para quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, retorna uma comparação de seu componente vermelho em relação a um valor de comparação junto com o status de mapeamento de peça.

## <a name="syntax"></a>Sintaxe


``` syntax
TemplateType GatherCmpRed(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
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

[Métodos GatherCmpRed](texture2darray-gathercmpred.md)
</dt> </dl>

 

 
