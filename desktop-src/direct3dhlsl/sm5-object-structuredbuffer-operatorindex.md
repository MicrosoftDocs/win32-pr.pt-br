---
title: 'Função StructuredBuffer:: Operator'
description: Retorna uma variável de recurso somente leitura de um StructuredBuffer.
ms.assetid: e2a1b0f7-f374-44a3-b567-8a2318e8b2b8
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
ms.openlocfilehash: 1f0d75bdfbcd3bfc560e896416f241f1291120d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085082"
---
# <a name="structuredbufferoperator--function"></a>Função StructuredBuffer:: Operator

Retorna uma variável de recurso somente leitura de um [**StructuredBuffer**](sm5-object-structuredbuffer.md).

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

Uma variável de recurso somente leitura.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[StructuredBuffer](sm5-object-structuredbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




