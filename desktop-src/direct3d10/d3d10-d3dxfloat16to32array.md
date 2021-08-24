---
description: Função D3DXFloat16To32Array (D3DX10Math.h) – converte uma matriz de floats de 16 bits em floats de 32 bits.
ms.assetid: cf07a21d-9ea3-4fbe-ab8f-564e2bbb8d60
title: Função D3DXFloat16To32Array (D3DX10Math.h)
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
ms.openlocfilehash: 00e5b7847e89687cf0b9414d3845652c0943661a2fc801fd4016eb54a8677c91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677746"
---
# <a name="d3dxfloat16to32array-function-d3dx10mathh"></a>Função D3DXFloat16To32Array (D3DX10Math.h)

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

*pOut* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ponteiro para a matriz de floats de 32 bits.

</dd> <dt>

*pIn* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md) \***

Ponteiro para uma matriz de floats de 16 bits.

</dd> <dt>

*n* \[ em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de elementos na matriz.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ponteiro para uma matriz de floats de 32 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
