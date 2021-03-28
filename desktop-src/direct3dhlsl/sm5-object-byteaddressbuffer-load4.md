---
title: 'Função ByteAddressBuffer:: Load4 (UINT)'
description: 'Obtém quatro valores. | Função ByteAddressBuffer:: Load4 (UINT)'
ms.assetid: bc74bf29-1c22-4e47-bafc-ecef194f54b8
keywords:
- HLSL da função Load4
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 18ce27e7d02a414165aab169e40a6ab14cdd8c4c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968494"
---
# <a name="byteaddressbufferload4uint-function"></a>Função ByteAddressBuffer:: Load4 (UINT)

Obtém quatro valores.

## <a name="syntax"></a>Sintaxe

``` syntax
uint4 Load4(
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

Tipo: **uint4**

Quatro valores.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos Load4](byteaddressbuffer-load4.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




