---
title: 'Função Texture2D:: GatherRed (S, float, int, uint)'
description: 'Retorna os componentes vermelhos dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, juntamente com o status de mapeamento de bloco. | Função Texture2D:: GatherRed (S, float, int, uint)'
ms.assetid: B49F738F-FB5C-4004-A3F3-D87C566DB597
keywords:
- HLSL da função GatherRed
topic_type:
- apiref
api_name:
- GatherRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1a6b7cd9c31748cdebebcc6c7f791b9b32e4ec1bf1db67d4e7a17b4944d7a3b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117723939"
---
# <a name="texture2dgatherredsfloatintuint-function"></a>Função Texture2D:: GatherRed (S, float, int, uint)

Retorna os componentes vermelhos dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, juntamente com o status de mapeamento de bloco.

## <a name="syntax"></a>Sintaxe


``` syntax
TemplateType GatherRed(
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

[Métodos GatherRed](texture2d-gatherred.md)
</dt> </dl>

 

 
