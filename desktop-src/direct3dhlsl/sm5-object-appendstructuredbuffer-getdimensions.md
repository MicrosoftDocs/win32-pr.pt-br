---
title: 'Função AppendStructuredBuffer:: GetDimensions'
description: 'Obtém as dimensões do recurso. | Função AppendStructuredBuffer:: GetDimensions'
ms.assetid: 41ed86d5-25c0-48bd-add9-792eb89605c3
keywords:
- Função GetDimensions HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96f40417834b8e23a9e746e4e4e3df93b96c1fc2affc7cd9147842e389dc99d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790647"
---
# <a name="appendstructuredbuffergetdimensions-function"></a>Função AppendStructuredBuffer:: GetDimensions

Obtém as dimensões do recurso.

## <a name="syntax"></a>Sintaxe

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*numStructs* \[ fora\]
</dt> <dd>

Tipo: **uint**

O número de estruturas.

</dd> <dt>

*Stride* \[ fora\]
</dt> <dd>

Tipo: **uint**

O número de bytes em cada elemento.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[AppendStructuredBuffer](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




