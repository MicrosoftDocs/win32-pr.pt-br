---
title: Função firstbithigh
description: Obtém o local do primeiro bit de conjunto começando do bit de ordem mais alto e trabalhando para baixo, por componente.
ms.assetid: 0fa89a9e-1706-44f7-8dd3-c37af5c11ddc
keywords:
- HLSL da função firstbithigh
topic_type:
- apiref
api_name:
- firstbithigh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4da4956aa3a12d064566a3767423f42039b01355
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366200"
---
# <a name="firstbithigh-function"></a>Função firstbithigh

Obtém o local do primeiro bit de conjunto começando do bit de ordem mais alto e trabalhando para baixo, por componente.

## <a name="syntax"></a>Sintaxe

``` syntax
int firstbithigh(
  in int value
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do no\]
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

O valor de entrada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

O local do primeiro bit definido.

## <a name="remarks"></a>Comentários

Para um inteiro assinado, o primeiro bit significativo é zero para um número negativo.

As seguintes versões sobrecarregadas também estão disponíveis:

``` syntax
int2 firstbithigh(int2 value);
int3 firstbithigh(int3 value);
int4 firstbithigh(int4 value);
uint firstbithigh(uint value);
uint2 firstbithigh(uint2 value);
uint3 firstbithigh(uint3 value);
uint4 firstbithigh(uint4 value);
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

 

 