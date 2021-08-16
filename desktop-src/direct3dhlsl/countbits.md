---
title: Função countbits
description: Conta o número de bits (por componente) definido no inteiro de entrada.
ms.assetid: c4fafbc8-e21c-48cb-b433-8241a989ec85
keywords:
- função countbits HLSL
topic_type:
- apiref
api_name:
- countbits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f3816152b91fd03348e64c7a36dd41e8b620bd5e5ef8f4463538c44ef974485
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793964"
---
# <a name="countbits-function"></a>Função countbits

Conta o número de bits (por componente) definido no inteiro de entrada.

## <a name="syntax"></a>Sintaxe

``` syntax
uint countbits(
  in uint value
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*value* \[ Em\]
</dt> <dd>

Tipo: **uint**

O valor de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint**

O número de bits.

## <a name="remarks"></a>Comentários

As seguintes versões sobrecarregadas também estão disponíveis:

``` syntax
uint count_bits(uint value);
uint2 count_bits(uint2 value);
uint3 count_bits(uint3 value);
uint4 count_bits(uint4 value);
```

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) e modelos de sombreador superior | sim       |



 

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




