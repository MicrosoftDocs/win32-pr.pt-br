---
description: Função D3DXFloat32To16Array (D3dx9math.h) – converte uma matriz de floats de 32 bits em floats de 16 bits.
ms.assetid: 00f7ae77-d2b5-4244-8fe9-6fea475700b7
title: Função D3DXFloat32To16Array (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2d4b02a85a22d8490b36ad32511af0d85294045502d4e32ba82b757ac34e21ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027726"
---
# <a name="d3dxfloat32to16array-function-d3dx9mathh"></a>Função D3DXFloat32To16Array (D3dx9math.h)

Converte uma matriz de floats de 32 bits em floats de 16 bits.

## <a name="syntax"></a>Sintaxe


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _Inout_       D3DXFLOAT16 *pOut,
  _In_    const FLOAT       *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXFLOAT16**](d3dxfloat16.md)\***

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

Tipo: **[ **D3DXFLOAT16**](d3dxfloat16.md)\***

Ponteiro para uma matriz de floats de 16 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
