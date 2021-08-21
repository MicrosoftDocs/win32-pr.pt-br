---
title: 'Função Texture2DArray:: GatherCmpBlue (S, float, float, int, uint)'
description: 'Para quatro valores Texel que seriam usados em uma operação de filtragem de bi linear, o retorna uma comparação de seu componente azul em relação a um valor de comparação junto com o status de mapeamento de bloco. | Função Texture2DArray:: GatherCmpBlue (S, float, float, int, uint)'
ms.assetid: 60456C17-F7A4-408A-93A2-DF695CBBEEAA
keywords:
- HLSL da função GatherCmpBlue
topic_type:
- apiref
api_name:
- GatherCmpBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2720081b1228f649239ca281fcc762a51600abde42cc9f76794c368e4c1ffb53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118284996"
---
# <a name="texture2darraygathercmpbluesfloatfloatintuint-function"></a>Função Texture2DArray:: GatherCmpBlue (S, float, float, int, uint)

Para quatro valores Texel que seriam usados em uma operação de filtragem de bi linear, o retorna uma comparação de seu componente azul em relação a um valor de comparação junto com o status de mapeamento de bloco.

## <a name="syntax"></a>Sintaxe


``` syntax
TemplateType GatherCmpBlue(
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

Tipo: **int**

O deslocamento aplicado às coordenadas de textura antes da amostragem.

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



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos GatherCmpBlue](texture2darray-gathercmpblue.md)
</dt> </dl>

 

 
