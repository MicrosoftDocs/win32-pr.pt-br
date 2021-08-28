---
title: Função reversebits
description: Inverte a ordem dos bits, por componente.
ms.assetid: dad46e25-9980-4645-98eb-d834db704fc8
keywords:
- função reversebits HLSL
topic_type:
- apiref
api_name:
- reversebits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9f055764c04f552fe9d7afda2adf1e401352cf3fc3dd3ead16c4ca6377bd4fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853716"
---
# <a name="reversebits-function"></a>Função reversebits

Inverte a ordem dos bits, por componente.

## <a name="syntax"></a>Sintaxe

``` syntax
uint reversebits(
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

O valor de entrada, com a ordem de bits invertida.

## <a name="remarks"></a>Comentários

As seguintes versões sobrecarregadas também estão disponíveis:

``` syntax
uint2 reversebits(uint2 value);
uint3 reversebits(uint3 value);
uint4 reversebits(uint4 value);
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

 

 




