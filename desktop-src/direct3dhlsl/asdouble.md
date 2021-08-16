---
title: função AsDouble
description: Reinterpreta um valor de conversão (valores de 2 32 bits) em um duplo.
ms.assetid: 55e5276d-81e1-4e7e-8cb4-0beb57d2fb7f
keywords:
- função HLSL
topic_type:
- apiref
api_name:
- asdouble
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e191a2bf9ee7fb46337c3c7dfef7f8dea3525acf936ab745c07e7720f1ac509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626636"
---
# <a name="asdouble-function"></a>função AsDouble

Reinterpreta um valor de conversão (valores de 2 32 bits) em um duplo.

## <a name="syntax"></a>Sintaxe

``` syntax
double asdouble(
  in uint lowbits,
  in uint highbits
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lowbits* \[ no\]
</dt> <dd>

Tipo: **uint**

O padrão baixo de 32 bits do valor de entrada.

</dd> <dt>

*highbits* \[ no\]
</dt> <dd>

Tipo: **uint**

O padrão de alto bit de 32 bits do valor de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **duplo**

A entrada (valores de 2 32 bits) recast como um Double.

## <a name="remarks"></a>Comentários

A seguinte versão sobrecarregada também está disponível:

``` syntax
double2 asdouble(uint2 lowbits, uint2 highbits);
```

Se o valor de entrada for de componentes de 2 32 bits, o tipo de retorno conterá um duplo. Se o valor de entrada for de componentes de 4 32 bits, o tipo de retorno conterá dois duplos. Se o valor de entrada for um tipo de 64 bits, o valor retornado terá o mesmo número de componentes que o valor de entrada.

### <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos | sim       |



 

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




