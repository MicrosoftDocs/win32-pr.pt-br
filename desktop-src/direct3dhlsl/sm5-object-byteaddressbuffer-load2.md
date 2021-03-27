---
title: 'Função ByteAddressBuffer:: Load2 (UINT)'
description: 'Obtém dois valores. | Função ByteAddressBuffer:: Load2 (UINT)'
ms.assetid: 696ce310-4d65-4382-97ec-046160197c67
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
ms.openlocfilehash: 78204fc3d41daf07a54974fbf103685e718ab79d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103663861"
---
# <a name="byteaddressbufferload2uint-function"></a>Função ByteAddressBuffer:: Load2 (UINT)

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

## <a name="return-value"></a>Retornar valor

Tipo: **uint2**

Dois valores.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos Load2](byteaddressbuffer-load2.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




