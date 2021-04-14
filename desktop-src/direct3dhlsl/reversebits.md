---
title: Função reversebits
description: Reverte a ordem dos bits, por componente.
ms.assetid: dad46e25-9980-4645-98eb-d834db704fc8
keywords:
- HLSL da função reversebits
topic_type:
- apiref
api_name:
- reversebits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d98b824883ddc4f06e6c11d30c2759bb0fc2be26
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104453775"
---
# <a name="reversebits-function"></a>Função reversebits

Reverte a ordem dos bits, por componente.

## <a name="syntax"></a>Sintaxe

``` syntax
uint reversebits(
  in uint value
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do no\]
</dt> <dd>

Tipo: **uint**

O valor de entrada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **uint**

O valor de entrada, com a ordem de bits invertida.

## <a name="remarks"></a>Comentários

As seguintes versões sobrecarregadas também estão disponíveis:

``` syntax
uint2 reversebits(uint2 value);
uint3 reversebits(uint3 value);
uint4 reversebits(uint4 value);
```

### <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos | sim       |



 

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




