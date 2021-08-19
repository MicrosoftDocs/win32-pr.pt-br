---
description: Calcula o produto de duas funções representadas usando SH (f e g).
ms.assetid: 632400a4-2ac9-438d-85f7-869101f350c8
title: Função D3DXSHMultiply2 (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply2
- D3DXSHMultiply3
- D3DXSHMultiply4
- D3DXSHMultiply5
- D3DXSHMultiply6
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 00219ed1c38105562591b63e6bef64b949b2ab4443aed68e0e6b9d64cb156cc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849686"
---
# <a name="d3dxshmultiply2-function-d3dx9mathh"></a>Função D3DXSHMultiply2 (D3dx9math.h)

Calcula o produto de duas funções representadas usando SH (f e g).

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

Ponteiro para os coeficientes sh de saída – a função base Ylm é armazenada em \* l l + m+l.

</dd> <dt>

*pF* \[ Em\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Coeffs sh de entrada para a primeira função.

</dd> <dt>

*pG* \[ Em\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Segundo conjunto de coeffs SH de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ponteiro para coeficientes de saída sh.

## <a name="remarks"></a>Comentários

A ordem é um número entre 2 e 6, inclusive. Portanto, essa página documenta várias funções: D3DXSHMultiply2, D3DXSHMultiply3, ... D3DXSHMultiply6.

Calcula o produto de duas funções representadas usando SH (f e g), em que *pOut* \[ i = \] int(y \_ \* i(s) f(s) g(s)), em que y i(s) é a função de base de SH \* \_ ith, f(s) e g(s) são funções SH (soma \_ i(y \_ i(s) \* c \_ i)). A ordem O determina os comprimentos das matrizes, em que sempre deve haver coeficientes O^2. Em geral, o produto de duas funções SH da ordem O gera uma função SH da ordem 2 O - 1, mas os resultados \* são truncados. Isso significa que o produto é commutado (f g == g f), mas não associa \* \* (f \* (g \* h) != (f \* g) \* h.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
