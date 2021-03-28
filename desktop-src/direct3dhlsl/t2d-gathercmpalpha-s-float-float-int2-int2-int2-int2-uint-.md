---
title: 'Função Texture2D:: GatherCmpAlpha (S, float, float, Int2, Int2, Int2, Int2, uint)'
description: 'Para quatro valores de Texel que seriam usados em uma operação de filtragem de bi linear, o retorna uma comparação de seu componente alfa em relação a um valor de comparação junto com o status de mapeamento de bloco. | Função Texture2D:: GatherCmpAlpha (S, float, float, Int2, Int2, Int2, Int2, uint)'
ms.assetid: 4DB56BE2-503A-4D51-89FB-E4DD91EBF028
keywords:
- HLSL da função GatherCmpAlpha
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e1962dc10b5ef45ba3ad7d7196872fd4d27708c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172830"
---
# <a name="texture2dgathercmpalphasfloatfloatint2int2int2int2uint-function"></a>Função Texture2D:: GatherCmpAlpha (S, float, float, Int2, Int2, Int2, Int2, uint)

Para quatro valores de Texel que seriam usados em uma operação de filtragem de bi linear, o retorna uma comparação de seu componente alfa em relação a um valor de comparação junto com o status de mapeamento de bloco.

## <a name="syntax"></a>Sintaxe


``` syntax
TemplateType GatherCmpAlpha(
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

Tipo: **samplestate**

O índice de amostra baseado em zero.

</dd> <dt>

*Local* \[ do no\]
</dt> <dd>

Tipo: **float**

As coordenadas de exemplo (u, v).

</dd> <dt>

*Comparevalue* \[ no\]
</dt> <dd>

Tipo: **float**

Um valor para comparar cada valor de amostra.

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

</dd> <dt>

*Status* \[ do fora\]
</dt> <dd>

Tipo: **uint**

O status da operação. Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features). Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.

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

[Métodos GatherCmpAlpha](texture2d-gathercmpalpha.md)
</dt> </dl>

 

 
