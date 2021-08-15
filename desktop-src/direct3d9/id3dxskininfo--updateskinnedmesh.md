---
description: Aplica a procapação de software aos vértices de destino com base nas matrizes atuais.
ms.assetid: 4858dfd4-dc0d-4852-9165-8ae1b40386d4
title: 'Método ID3DXSkinInfo:: UpdateSkinnedMesh (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.UpdateSkinnedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 22b36e1836570a10647f5b737a68afa1e65a4dce80fe9d49061a3eee8a799651
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729448"
---
# <a name="id3dxskininfoupdateskinnedmesh-method"></a>Método ID3DXSkinInfo:: UpdateSkinnedMesh

Aplica a procapação de software aos vértices de destino com base nas matrizes atuais.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UpdateSkinnedMesh(
  [in] const D3DXMATRIX *pBoneTransforms,
  [in] const D3DXMATRIX *pBoneInvTransposeTransforms,
  [in]       LPCVOID    pVerticesSrc,
  [in]       PVOID      pVerticesDst
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pBoneTransforms* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Matriz de transformação de Bone.

</dd> <dt>

*pBoneInvTransposeTransforms* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Transpose inversa da matriz de transformação Bone.

</dd> <dt>

*pVerticesSrc* \[ no\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Ponteiro para o buffer que contém os vértices de origem.

</dd> <dt>

*pVerticesDst* \[ no\]
</dt> <dd>

Tipo: **[ **pVoid**](../winprog/windows-data-types.md)**

Ponteiro para o buffer que contém os vértices de destino.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Quando usado para vértices de capa com dois elementos position, esse método diverte o segundo elemento position com o inverso do Bone em vez do próprio Bone.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
