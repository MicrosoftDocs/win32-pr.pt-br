---
description: Dimensiona um vetor 4D.
ms.assetid: b185a9b9-f768-4b50-aa6c-667c71eac39a
title: Função D3DXVec4Scale (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Scale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 12f030330d01e004d80de92920c84f8cc8ffc47fe009582d64d34497bb684418
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118956"
---
# <a name="d3dxvec4scale-function"></a>Função D3DXVec4Scale

Dimensiona um vetor 4D.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR4* D3DXVec4Scale(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Ponteiro para a [**estrutura D3DXVECTOR4**](d3dxvector4.md) que é o resultado da operação.

</dd> <dt>

*pV* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Ponteiro para a estrutura [**D3DXVECTOR4 de**](d3dxvector4.md) origem.

</dd> <dt>

*s* \[ em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor de dimensionamento.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Ponteiro para a [**estrutura D3DXVECTOR4**](d3dxvector4.md) que é o vetor dimensionado.

## <a name="remarks"></a>Comentários

O valor retornado para essa função é o mesmo valor retornado no *parâmetro pOut.* Dessa forma, a **função D3DXVec4Scale** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec4Add**](d3dxvec4add.md)
</dt> <dt>

[**D3DXVec4Subtract**](d3dxvec4subtract.md)
</dt> </dl>

 

 
