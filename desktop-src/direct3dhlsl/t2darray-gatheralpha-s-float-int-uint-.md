---
title: 'Função Texture2DArray:: GatherAlpha (S, float, int, uint)'
description: 'Retorna os quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, juntamente com o status de mapeamento de bloco. | Função Texture2DArray:: GatherAlpha (S, float, int, uint)'
ms.assetid: B04F29A7-0EC9-49F0-9662-00F1DD0F3E5B
keywords:
- HLSL da função GatherAlpha
topic_type:
- apiref
api_name:
- GatherAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6efa67eb0f2e3eed33f18788443723fadce825a381511019dcc24d941656865c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788286"
---
# <a name="texture2darraygatheralphasfloatintuint-function"></a>Função Texture2DArray:: GatherAlpha (S, float, int, uint)

Retorna os quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, juntamente com o status de mapeamento de bloco.

## <a name="syntax"></a>Sintaxe


``` syntax
TemplateType GatherAlpha(
  in  SamplerState S,
  in  float        Location,
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

## <a name="return-value"></a>Valor retornado

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

[Métodos GatherAlpha](texture2darray-gatheralpha.md)
</dt> </dl>

 

 
