---
title: 'Função TextureCube:: GatherCmp (S, float, float, uint)'
description: 'Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna a comparação contra um valor de comparação. | Função TextureCube:: GatherCmp (S, float, float, uint)'
ms.assetid: 655F4851-708A-478B-BB31-9DC8CDD480D0
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
ms.openlocfilehash: e9346d3acc5422035d01dcc3f36b053825b9240ff10497af53207b05226efa09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118506598"
---
# <a name="texturecubegathercmpsfloatfloatuint-function"></a>Função TextureCube:: GatherCmp (S, float, float, uint)

Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna a comparação contra um valor de comparação.

## <a name="syntax"></a>Sintaxe


``` syntax
TemplateType GatherCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
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

[Métodos GatherCmp](texturecube-gathercmp.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
