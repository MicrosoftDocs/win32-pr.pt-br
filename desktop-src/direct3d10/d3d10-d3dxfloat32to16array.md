---
description: Função D3DXFloat32To16Array (D3DX10Math. h) – converte uma matriz de 32 bits floats em floats de 16 bits.
ms.assetid: 2114cf25-cc83-4c4a-9db5-ecc0f8ff1e85
title: Função D3DXFloat32To16Array (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat32To16Array
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 600cc2cd333aaea08b38c252c206c1a74c1ca059
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103514"
---
# <a name="d3dxfloat32to16array-function-d3dx10mathh"></a>Função D3DXFloat32To16Array (D3DX10Math. h)

Converte uma matriz de 32-bit floats em floats de 16 bits.

## <a name="syntax"></a>Sintaxe


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _In_       D3DXFLOAT16 *pOut,
  _In_ const FLOAT       *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ no\]
</dt> <dd>

Tipo: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***

Ponteiro para a matriz de floats de 16 bits.

</dd> <dt>

*fixar* \[ no\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Ponteiro para uma matriz de flutuações de 32 bits.

</dd> <dt>

*n* \[ em\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O número de elementos na matriz.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***

Ponteiro para uma matriz de floats de 16 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
