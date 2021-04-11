---
description: Computa o produto de duas funções de harmônica esféricas (f e g). Ambas as funções são da ordem N = 4.
ms.assetid: 05427a18-447e-45d7-a851-e580298c9a1f
title: Função D3DXSHMultiply4 (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply4
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 13e8b62674ccbabbb03259f06b79f330424ddf84
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173109"
---
# <a name="d3dxshmultiply4-function"></a>Função D3DXSHMultiply4

Computa o produto de duas funções de harmônica esféricas (*f* e *g*). Ambas as funções são da ordem N = 4.

## <a name="syntax"></a>Sintaxe


```C++
FLOAT* D3DXSHMultiply4(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para a saída SH-ineficientes – a função base *Y* LM é armazenada em l ² + *m* + l. A ordem *N* determina o comprimento da matriz, onde sempre deve haver *N*² coeficientes.

</dd> <dt>

*PF* \[ no\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Entrada SH coeficientes para a primeira função.

</dd> <dt>

*PG* \[ no\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Segundo conjunto de entrada SH coeficientes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para SH coeficientes de saída.

## <a name="remarks"></a>Comentários

O produto de duas funções SH de Order N = 4 gera uma função SH da ordem 2 × *N* -1 = 7, mas os resultados são truncados. Isso significa que o produto está mudo ( *f* × *g*  =  *g* × *f* ), mas não associa ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).

Essa função usa a seguinte equação:


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



em que y \_ i (s) é a função base i sh e em que f (s) e g (s) usam a seguinte função sh:


```
sum_i(y_i(s)*c_i)
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
