---
description: Tessellates a malha determinada usando o esquema de mosaico de N-patch.
ms.assetid: e804905d-ee0b-484f-a621-58b197bd370b
title: Função D3DXTessellateNPatches (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateNPatches
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1df63068f3eef608f797f8048231e744412c32f9e01a31a089c50f8a46465a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122718"
---
# <a name="d3dxtessellatenpatches-function"></a>Função D3DXTessellateNPatches

Tessellates a malha determinada usando o esquema de mosaico de N-patch.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXTessellateNPatches(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const CONST DWORD  *pAdjacencyIn,
  _In_        FLOAT        NumSegs,
  _In_        BOOL         QuadraticInterpNormals,
  _Out_       LPD3DXMESH   *ppMeshOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMeshIn* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , representando a malha para incluí.

</dd> <dt>

*pAdjacencyIn* \[ no\]
</dt> <dd>

Tipo: **CONST const DWORD \***

Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha de origem. Esse parâmetro pode ser **nulo**.

</dd> <dt>

*NumSegs* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Número de segmentos por borda para incluí.

</dd> <dt>

*QuadraticInterpNormals* \[ no\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Defina como **true** para usar a interpolação quadrática para Normals; Defina como **false** para interpolação linear.

</dd> <dt>

*ppMeshOut* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Endereço de um ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , representando a malha mosaico retornada.

</dd> <dt>

*ppAdjacencyOut* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) . Se o valor desse parâmetro não for definido como **NULL**, esse buffer conterá uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha de saída. Esse parâmetro pode ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Essa função tessellates usando o algoritmo N-patch.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
