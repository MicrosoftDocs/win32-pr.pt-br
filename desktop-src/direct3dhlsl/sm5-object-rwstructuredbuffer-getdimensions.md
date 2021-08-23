---
title: Função RWStructuredBuffer::GetDimensions
description: Obtém as dimensões do recurso. | Função RWStructuredBuffer::GetDimensions
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
ms.openlocfilehash: 760a546d7d60afbb41438416a9602ab55981834acd9969bc535c9a82df6e5e50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789922"
---
# <a name="rwstructuredbuffergetdimensions-function"></a>Função RWStructuredBuffer::GetDimensions

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

*numStructs* \[ out\]
</dt> <dd>

Tipo: **uint**

O número de estruturas no recurso.

</dd> <dt>

*stride* \[ out\]
</dt> <dd>

Tipo: **uint**

O stride, em bytes, de cada elemento de estrutura.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Nada

## <a name="remarks"></a>Comentários

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

 

 




