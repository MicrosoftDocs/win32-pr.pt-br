---
description: Computa o produto de duas funções de harmônica esféricas (f e g). Ambas as funções são da ordem N = 6.
ms.assetid: 3b68b238-c1ae-4ab8-89ed-bdf815463143
title: Função D3DXSHMultiply6 (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply6
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b442d6d8c64d7c1ef0b202bd2cfa5d6d625280eb7320609a11ea89420c2bc215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989996"
---
# <a name="d3dxshmultiply6-function"></a>Função D3DXSHMultiply6

Computa o produto de duas funções de harmônica esféricas (f e g). Ambas as funções são da ordem N = 6.

## <a name="syntax"></a>Sintaxe


```C++
FLOAT* D3DXSHMultiply6(
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

Ponteiro para a saída SH dieficientes – a função base *Y* LM é armazenada em l ² + *m* + l. A ordem *N* determina o comprimento da matriz, onde sempre deve haver *N*² coeficientes.

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

O produto de duas funções SH de Order N = 6 gera uma função SH da ordem 2 × *N* -1 = 11, mas os resultados são truncados. Isso significa que o produto está mudo ( *f* × *g*  =  *g* × *f* ), mas não associa ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).

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

 

 
