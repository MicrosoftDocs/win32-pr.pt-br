---
title: Função RWByteAddressBuffer::Load3(uint)
description: Obtém três valores. | Função RWByteAddressBuffer::Load3(uint)
ms.assetid: cf8c4c5d-4748-43d7-896e-33ed07c94b9e
keywords:
- Função Load3 HLSL
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fee675dfe8707c5a67073355bcffbe4924d05780dea487125f4b5b00c2019801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117905756"
---
# <a name="rwbyteaddressbufferload3uint-function"></a>Função RWByteAddressBuffer::Load3(uint)

Obtém três valores.

## <a name="syntax"></a>Sintaxe

``` syntax
uint3 Load3(
  in uint address
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*endereço* \[ Em\]
</dt> <dd>

Tipo: **uint**

O endereço de entrada em bytes, que deve ser um múltiplo de 4.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint3**

Três valores.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos Load3](rwbyteaddressbuffer-load3.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




