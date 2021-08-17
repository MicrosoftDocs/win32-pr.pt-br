---
description: Função D3DXVec3TransformArray (D3dx9math.h) – transforma uma matriz (x, y, z, 1) por uma determinada matriz.
ms.assetid: fd7ab674-5e42-4265-afad-ae5a00dabcdb
title: Função D3DXVec3TransformArray (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3cd17da7f3eb8e9c21ab2890ab112194c7f393b89c6761f2b14741e557318efe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122533"
---
# <a name="d3dxvec3transformarray-function-d3dx9mathh"></a>Função D3DXVec3TransformArray (D3dx9math.h)

Transforma uma matriz (x, y, z, 1) por uma determinada matriz.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR4* D3DXVec3TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Ponteiro para a [**matriz D3DXVECTOR4**](d3dxvector4.md) que é o resultado da operação.

</dd> <dt>

*OutStride* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Distância entre vetores no fluxo de dados de saída.

</dd> <dt>

*pV* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para a matriz [**D3DXVECTOR3 de origem.**](d3dxvector3.md)

</dd> <dt>

*VStride* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Distância entre vetores no fluxo de dados de entrada.

</dd> <dt>

*pM* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para a estrutura [**D3DXMATRIX de origem.**](d3dxmatrix.md)

</dd> <dt>

*n* \[ em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de elementos na matriz.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Ponteiro para uma [**matriz transformada D3DXVECTOR4.**](d3dxvector4.md)

## <a name="remarks"></a>Comentários

Essa função transforma a *matriz pV* (x, y, z, 1) pela *matriz pM*.

O valor retornado para essa função é o mesmo valor retornado no *parâmetro pOut.* Dessa forma, a **função D3DXVec3TransformArray** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
