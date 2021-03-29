---
title: 'Função Texture2D:: GatherCmp (S, float, float, int, uint)'
description: 'Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna a comparação contra um valor de comparação junto com o status de mapeamento de bloco. | Função Texture2D:: GatherCmp (S, float, float, int, uint)'
ms.assetid: A6610587-97C3-4CE5-86A7-3411D422BC8F
keywords:
- HLSL da função GatherCmp
topic_type:
- apiref
api_name:
- GatherCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: be8246053e0f7ba6357bdd68dc59059fd225bbc8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968480"
---
# <a name="texture2dgathercmpsfloatfloatintuint-function"></a>Função Texture2D:: GatherCmp (S, float, float, int, uint)

Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna a comparação contra um valor de comparação junto com o status de mapeamento de bloco.

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

*Deslocamento* \[ no\]
</dt> <dd>

Tipo: **Int2**

O deslocamento em texels aplicado às coordenadas de textura antes da amostragem. Deve ser um valor literal.

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

[Métodos GatherCmp](texture2d-gathercmp.md)
</dt> </dl>

 

 
