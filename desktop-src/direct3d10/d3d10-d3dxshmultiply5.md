---
description: Computa o produto de duas funções de harmônica esféricas (f e g). Ambas as funções são da ordem N = 5.
ms.assetid: c72231a1-9db3-4701-b7ad-4509028ce508
title: Função D3DXSHMultiply5 (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply5
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a022fa883a1b1e809f965ec94813741a285447e9f6935c1adca370b5aef6c061
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990766"
---
# <a name="d3dxshmultiply5-function"></a>Função D3DXSHMultiply5

Computa o produto de duas funções de harmônica esféricas (f e g). Ambas as funções são da ordem N = 5.

## <a name="syntax"></a>Sintaxe


```C++
FLOAT* D3DXSHMultiply5(
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

Ponteiro para a saída SH dieficientes – a função base *Y* LM é armazenada em *l*² + *m* + l. A ordem N determina o comprimento da matriz, onde sempre deve haver *N*² coeficientes.

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

## <a name="return-value"></a>Valor retornado

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para SH coeficientes de saída.

## <a name="remarks"></a>Comentários

O produto de duas funções SH de Order N = 5 gera uma função SH da ordem 2 × *N* -1 = 9, mas os resultados são truncados. Isso significa que o produto está mudo ( *f* × *g*  =  *g* × *f* ), mas não associa ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).

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

 

 
