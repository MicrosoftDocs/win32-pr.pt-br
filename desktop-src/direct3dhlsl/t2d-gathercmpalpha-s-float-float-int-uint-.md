---
title: Função Texture2D::GatherCmpAlpha(S,float,float,int,uint)
description: Para quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, retorna uma comparação de seu componente alfa com um valor de comparação junto com o status de mapeamento de peça. | Função Texture2D::GatherCmpAlpha(S,float,float,int,uint)
ms.assetid: 4E281512-2E0A-49A5-B568-8CE793A854F9
keywords:
- Função GatherCmpAlpha HLSL
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5d4cc054d832bcaea7987fda26f8c000a7c6c2bbfe5e2f13366a99fcddb0e01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671176"
---
# <a name="texture2dgathercmpalphasfloatfloatintuint-function"></a>Função Texture2D::GatherCmpAlpha(S,float,float,int,uint)

Para quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, retorna uma comparação de seu componente alfa com um valor de comparação junto com o status de mapeamento de peça.

## <a name="syntax"></a>Sintaxe


``` syntax
TemplateType GatherCmpAlpha(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
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

*Deslocamento* \[ Em\]
</dt> <dd>

Tipo: **int**

O deslocamento aplicado às coordenadas de textura antes da amostragem.

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

[Métodos GatherCmpAlpha](texture2d-gathercmpalpha.md)
</dt> </dl>

 

 
