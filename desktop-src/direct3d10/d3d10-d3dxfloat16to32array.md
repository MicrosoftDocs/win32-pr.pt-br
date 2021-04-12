---
description: Converte uma matriz de floats de 16 bits em floats de 32 bits.
ms.assetid: cf07a21d-9ea3-4fbe-ab8f-564e2bbb8d60
title: Função D3DXFloat16To32Array (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a813553234c9e59ad34720da6f380977779e5d96
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298647"
---
# <a name="d3dxfloat16to32array-function-d3dx10mathh"></a>Função D3DXFloat16To32Array (D3DX10Math. h)

Converte uma matriz de floats de 16 bits em floats de 32 bits.

## <a name="syntax"></a>Sintaxe


```C++
FLOAT* D3DXFloat16To32Array(
  _In_       FLOAT       *pOut,
  _In_ const D3DXFLOAT16 *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para a matriz de flutuações de 32 bits.

</dd> <dt>

*fixar* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md) \***

Ponteiro para uma matriz de floats de 16 bits.

</dd> <dt>

*n* \[ em\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de elementos na matriz.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para uma matriz de flutuações de 32 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
