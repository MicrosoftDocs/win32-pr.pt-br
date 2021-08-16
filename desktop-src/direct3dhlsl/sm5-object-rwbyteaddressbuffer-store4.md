---
title: Função RWByteAddressBuffer::Store4
description: Define quatro valores.
ms.assetid: 261dd270-79a7-4566-9fbd-52bd8dc3e1bf
keywords:
- Função Store4 HLSL
topic_type:
- apiref
api_name:
- Store4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bc644647616f6c6654023be23aaa8e420dbb85ad439547d1befd44c0ea7b210c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789967"
---
# <a name="store4-function"></a>Função Store4

Define quatro valores.

## <a name="syntax"></a>Sintaxe

``` syntax
void Store4(
  in uint address,
  in uint4 values
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*endereço* \[ Em\]
</dt> <dd>

Tipo: **uint**

O endereço de entrada em bytes, que deve ser um múltiplo de 4.

</dd> <dt>

*valores* \[ Em\]
</dt> <dd>

Tipo: **uint4**

Quatro valores de entrada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




