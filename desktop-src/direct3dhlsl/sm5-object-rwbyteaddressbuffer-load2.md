---
title: 'Função RWByteAddressBuffer:: Load2 (UINT)'
description: 'Obtém dois valores. | Função RWByteAddressBuffer:: Load2 (UINT)'
ms.assetid: a00396cb-e68d-479e-ab3f-4c52f2cfc3bc
keywords:
- HLSL da função Load2
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f71fd2d0585803fb10de3fddfa29c10838d73e32ba7d63b5619be91b042cb71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725053"
---
# <a name="rwbyteaddressbufferload2uint-function"></a>Função RWByteAddressBuffer:: Load2 (UINT)

Obtém dois valores.

## <a name="syntax"></a>Sintaxe

``` syntax
uint2 Load2(
  in uint address
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*endereço* \[ no\]
</dt> <dd>

Tipo: **uint**

O endereço de entrada em bytes, que deve ser um múltiplo de 4.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint2**

Dois valores.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos Load2](rwbyteaddressbuffer-load2.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




