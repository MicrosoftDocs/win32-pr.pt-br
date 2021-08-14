---
title: Função ByteAddressBuffer::Load4(uint)
description: Obtém quatro valores. | Função ByteAddressBuffer::Load4(uint)
ms.assetid: bc74bf29-1c22-4e47-bafc-ecef194f54b8
keywords:
- Função Load4 HLSL
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a623c62ce9038d4e06cfbb952808aeb0530cb2e937c83578d9ef0e71c9b0a038
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509996"
---
# <a name="byteaddressbufferload4uint-function"></a>Função ByteAddressBuffer::Load4(uint)

Obtém quatro valores.

## <a name="syntax"></a>Sintaxe

``` syntax
uint4 Load4(
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

Tipo: **uint4**

Quatro valores.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos Load4](byteaddressbuffer-load4.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




