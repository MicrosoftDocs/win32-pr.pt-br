---
title: Função ByteAddressBuffer::Load2(uint)
description: Obtém dois valores. | Função ByteAddressBuffer::Load2(uint)
ms.assetid: 696ce310-4d65-4382-97ec-046160197c67
keywords:
- Função Load2 HLSL
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fac3b1cd0fffca1a68089c3c21bfd5d6aea5f270493319b044a0bbe290d88a5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119845726"
---
# <a name="byteaddressbufferload2uint-function"></a>Função ByteAddressBuffer::Load2(uint)

Obtém dois valores.

## <a name="syntax"></a>Sintaxe

``` syntax
uint2 Load2(
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

Tipo: **uint2**

Dois valores.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos Load2](byteaddressbuffer-load2.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




