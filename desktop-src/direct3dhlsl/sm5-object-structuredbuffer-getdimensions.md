---
title: 'Função StructuredBuffer:: GetDimensions'
description: 'Obtém as dimensões do recurso. | Função StructuredBuffer:: GetDimensions'
ms.assetid: 423ea79c-4440-4837-b637-95180a1d5019
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
ms.openlocfilehash: 2b3d7c879c77386ddee80a63053711b8ae34ee8c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298241"
---
# <a name="structuredbuffergetdimensions-function"></a>Função StructuredBuffer:: GetDimensions

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

O número de estruturas no recurso.

</dd> <dt>

*Stride* \[ fora\]
</dt> <dd>

Tipo: **uint**

O stride, em bytes, de cada elemento da estrutura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

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

 

 




