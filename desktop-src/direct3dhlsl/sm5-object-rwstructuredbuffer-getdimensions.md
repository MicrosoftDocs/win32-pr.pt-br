---
title: 'Função RWStructuredBuffer:: GetDimensions'
description: 'Obtém as dimensões do recurso. | Função RWStructuredBuffer:: GetDimensions'
ms.assetid: 842b3d21-2e2b-4906-93ee-0252b2e8cf85
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
ms.openlocfilehash: 0e3868f33e372472999c29bffdd8e12bc8ef09b7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968283"
---
# <a name="rwstructuredbuffergetdimensions-function"></a>Função RWStructuredBuffer:: GetDimensions

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

Nothing

## <a name="remarks"></a>Comentários

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

 

 




