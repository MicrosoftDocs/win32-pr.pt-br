---
description: Função D3DXFloat16To32Array (D3dx9math. h) – converte uma matriz de floats de 16 bits em floats de 32 bits.
ms.assetid: cabb2888-76e4-403b-99ab-f7d62478bf43
title: Função D3DXFloat16To32Array (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat16To32Array
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 171b148b112cf2064d0d9a3f89451ab0fc8c2d75
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107594"
---
# <a name="d3dxfloat16to32array-function-d3dx9mathh"></a>Função D3DXFloat16To32Array (D3dx9math. h)

Converte uma matriz de floats de 16 bits em floats de 32 bits.

## <a name="syntax"></a>Sintaxe


```C++
FLOAT* D3DXFloat16To32Array(
  _Inout_       FLOAT       *pOut,
  _In_    const D3DXFLOAT16 *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para a matriz de flutuações de 32 bits.

</dd> <dt>

*fixar* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXFLOAT16**](d3dxfloat16.md) \***

Ponteiro para uma matriz de floats de 16 bits.

</dd> <dt>

*n* \[ em\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de elementos na matriz.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para uma matriz de flutuações de 32 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
