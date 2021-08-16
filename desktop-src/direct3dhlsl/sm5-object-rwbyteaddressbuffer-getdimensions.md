---
title: 'Função RWByteAddressBuffer:: GetDimensions'
description: 'Obtém o comprimento do buffer. | Função RWByteAddressBuffer:: GetDimensions'
ms.assetid: 7d78aa0d-75b8-43d5-85d9-0a6fb04ae64f
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
ms.openlocfilehash: 2271f563251cfdb9c6f2a2174c91dc8c271c7354a2b10b9b2e7e55cb4af09d0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725141"
---
# <a name="rwbyteaddressbuffergetdimensions-function"></a>Função RWByteAddressBuffer:: GetDimensions

Obtém o comprimento do buffer.

## <a name="syntax"></a>Sintaxe

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*esmaecer* \[\]
</dt> <dd>

Tipo: **uint**

O comprimento, em bytes, do buffer.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




