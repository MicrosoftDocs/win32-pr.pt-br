---
title: Função Texture2D::GatherCmp(S,float,float,int,uint)
description: Para quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, retorna sua comparação com um valor de comparação junto com o status de mapeamento de lado. | Função Texture2D::GatherCmp(S,float,float,int,uint)
ms.assetid: A6610587-97C3-4CE5-86A7-3411D422BC8F
keywords:
- Função GatherCmp HLSL
topic_type:
- apiref
api_name:
- GatherCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8afea2700ec1b4a503db9ec45d2ff2757ccf2a74714ce384f06a498f6f49640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043644"
---
# <a name="texture2dgathercmpsfloatfloatintuint-function"></a>Função Texture2D::GatherCmp(S,float,float,int,uint)

Para quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, retorna sua comparação com um valor de comparação junto com o status de mapeamento de lado.

## <a name="syntax"></a>Sintaxe


``` syntax
TemplateType GatherCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int2         Offset,
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

Tipo: **int2**

O deslocamento em texels aplicado às coordenadas de textura antes da amostragem. Deve ser um valor literal.

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

[Métodos GatherCmp](texture2d-gathercmp.md)
</dt> </dl>

 

 
