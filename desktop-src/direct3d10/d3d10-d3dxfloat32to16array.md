---
description: Função D3DXFloat32To16Array (D3DX10Math.h) – converte uma matriz de floats de 32 bits em floats de 16 bits.
ms.assetid: 2114cf25-cc83-4c4a-9db5-ecc0f8ff1e85
title: Função D3DXFloat32To16Array (D3DX10Math.h)
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
ms.openlocfilehash: f0de2e2cda9724a5bfa12d13171276694bcd8fbcbbd5dffbb81ae185ebbda381
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853406"
---
# <a name="d3dxfloat32to16array-function-d3dx10mathh"></a>Função D3DXFloat32To16Array (D3DX10Math.h)

Converte uma matriz de floats de 32 bits em floats de 16 bits.

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

*pOut* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***

Ponteiro para a matriz de floats de 16 bits.

</dd> <dt>

*pIn* \[ Em\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Ponteiro para uma matriz de floats de 32 bits.

</dd> <dt>

*n* \[ em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

O número de elementos na matriz.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***

Ponteiro para uma matriz de floats de 16 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
