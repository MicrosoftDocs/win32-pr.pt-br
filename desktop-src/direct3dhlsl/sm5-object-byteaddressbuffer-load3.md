---
title: 'Função ByteAddressBuffer:: Load3 (UINT)'
description: 'Obtém três valores. | Função ByteAddressBuffer:: Load3 (UINT)'
ms.assetid: 79afeb36-e0e7-44a2-b252-8e3577f4c1a5
keywords:
- HLSL da função Load3
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e3975d454fcbb8c5dfa8cdef8d7f5718143546f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968495"
---
# <a name="byteaddressbufferload3uint-function"></a>Função ByteAddressBuffer:: Load3 (UINT)

Obtém três valores.

## <a name="syntax"></a>Sintaxe

``` syntax
uint3 Load3(
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

## <a name="return-value"></a>Retornar valor

Tipo: **uint3**

Três valores.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos Load3](byteaddressbuffer-load3.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




