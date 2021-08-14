---
title: Função RWByteAddressBuffer::Store3
description: Define três valores.
ms.assetid: eaf12b5a-c9c6-413a-9646-3d14e7825460
keywords:
- Função Store3 HLSL
topic_type:
- apiref
api_name:
- Store3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a752ada16db4800e6160ad7b1c2c0b480deee75ff760d0c7f270dac36d1cff51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790058"
---
# <a name="store3-function"></a>Função Store3

Define três valores.

## <a name="syntax"></a>Sintaxe

``` syntax
void Store3(
  in uint address,
  in uint3 values
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

Tipo: **uint3**

Três valores de entrada.

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

 

 




