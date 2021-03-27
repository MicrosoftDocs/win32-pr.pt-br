---
title: 'Função RWStructuredBuffer:: Operator'
description: 'Retorna uma variável de recurso. | Função RWStructuredBuffer:: Operator'
ms.assetid: e821b60e-38db-463f-b0c6-47f2a4c9ccee
keywords:
- Função Operator HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e915d7862f7994d3b438bf3255ee836ede4b3d7d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104506387"
---
# <a name="rwstructuredbufferoperator--function"></a>Função RWStructuredBuffer:: Operator

Retorna uma variável de recurso.

## <a name="syntax"></a>Sintaxe

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pos* \[ no\]
</dt> <dd>

Tipo: **uint**

A posição do índice.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **R**

Uma variável de recurso.

## <a name="remarks"></a>Comentários

Um recurso estruturado pode ser indexado ainda mais com base nos nomes de componentes das estruturas.

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[RWStructuredBuffer](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




