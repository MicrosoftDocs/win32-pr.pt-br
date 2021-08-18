---
title: Função RWStructuredBuffer::Operator
description: Retorna uma variável de recurso. | Função RWStructuredBuffer::Operator
ms.assetid: e821b60e-38db-463f-b0c6-47f2a4c9ccee
keywords:
- Função de operador HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ad2e8085a52a920f7fe87a2820398877167a137c14c4ebe39bacd71ae2ba0324
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509315"
---
# <a name="rwstructuredbufferoperator--function"></a>Função RWStructuredBuffer::Operator

Retorna uma variável de recurso.

## <a name="syntax"></a>Sintaxe

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pos* \[ Em\]
</dt> <dd>

Tipo: **uint**

A posição do índice.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **R**

Uma variável de recurso.

## <a name="remarks"></a>Comentários

Um recurso estruturado pode ser indexado ainda mais com base nos nomes de componentes das estruturas.

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[RWStructuredBuffer](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




