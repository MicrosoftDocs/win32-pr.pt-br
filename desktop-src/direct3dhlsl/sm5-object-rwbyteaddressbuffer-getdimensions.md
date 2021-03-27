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
ms.openlocfilehash: 0d22b6f655802d77a92611fe8699a405aa323873
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298365"
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



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




