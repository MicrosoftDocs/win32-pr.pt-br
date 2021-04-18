---
description: Computa o produto de duas funções representadas usando SH (f e g).
ms.assetid: 632400a4-2ac9-438d-85f7-869101f350c8
title: Função D3DXSHMultiply2 (D3dx9math. h)
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
ms.openlocfilehash: f7b9adaf5caf7b4b2d35035fd5c2a916298b0c8c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105795453"
---
# <a name="d3dxshmultiply2-function-d3dx9mathh"></a>Função D3DXSHMultiply2 (D3dx9math. h)

Computa o produto de duas funções representadas usando SH (f e g).

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

*pout* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

O ponteiro para a saída SH Ylm de função de base é armazenado em l \* l + m + l.

</dd> <dt>

*PF* \[ no\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Entrada SH coeffs para a primeira função.

</dd> <dt>

*PG* \[ no\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Segundo conjunto de entrada SH coeffs.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para SH coeficientes de saída.

## <a name="remarks"></a>Comentários

A ordem é um número entre 2 e 6, inclusive. Dessa forma, essa página documenta várias funções: D3DXSHMultiply2, D3DXSHMultiply3,... D3DXSHMultiply6.

Computa o produto de duas funções representadas usando SH (f e g), em que *pout* \[ i \] = int (y i (s) f (s) \_ \* \* g (s)), em que y \_ i (s) é a função base i i, f (s) e g (s) são funções sh (Sum \_ i ( \_ s) \* c \_ i)). A ordem o determina os comprimentos das matrizes, em que sempre deve haver O ^ 2 coeficientes. Em geral, o produto de duas funções SH de Order O gera uma função SH da ordem 2 \* o-1, mas os resultados são truncados. Isso significa que o produto faz o mudo (f \* g = = g \* f), mas não associa (f \* (g \* h)! = (f \* g) \* h.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
