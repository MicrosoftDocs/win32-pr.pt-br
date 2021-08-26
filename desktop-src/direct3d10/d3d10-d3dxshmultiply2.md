---
description: Calcula o produto de duas funções cônicas esféricas (f e g). Ambas as funções são da ordem N = 2.
ms.assetid: 9e0942ce-e39d-4147-9472-cda8a97fd390
title: Função D3DXSHMultiply2 (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply2
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c6fba685a763a00e529e70b7c0f08a97706f3c5f2be4dba7c923ed5b4b102742
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069996"
---
# <a name="d3dxshmultiply2-function-d3dx10mathh"></a>Função D3DXSHMultiply2 (D3DX10Math.h)

Calcula o produto de duas funções cônicas esféricas (*f* e *g*). Ambas as funções são da ordem N = 2.

## <a name="syntax"></a>Sintaxe


```C++
FLOAT* D3DXSHMultiply2(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ponteiro para os coeficientes sh de saída — a função base *Y* lm é armazenada em lÂmico + *m* + l. A ordem *N* determina o comprimento da matriz, em que sempre deve haver *N* coeficientes âmicos.

</dd> <dt>

*pF* \[ Em\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Coeficientes sh de entrada para a primeira função.

</dd> <dt>

*pG* \[ Em\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Segundo conjunto de coeficientes SH de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ponteiro para coeficientes de saída sh.

## <a name="remarks"></a>Comentários

O produto de duas funções SH da ordem N = 2 gera uma função SH da ordem 2 × *N* - 1 = 3, mas os resultados são truncados. Isso significa que o produto é commutado ( *f* × *g* g × f ), mas não associa  =   ( *f* × (*g* × *h*) ≠ ( *f* × *g*) × *h* ). 

Essa função usa a seguinte equação:


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



em que y i(s) é a função base de SH e em que \_ f(s) e g(s) usam a seguinte função SH:


```
sum_i(y_i(s)*c_i)
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
