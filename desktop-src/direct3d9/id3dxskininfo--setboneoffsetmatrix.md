---
description: Define a matriz de deslocamento do Bone.
ms.assetid: f8ac1117-510d-42af-a6bf-422cbaaf6b74
title: 'Método ID3DXSkinInfo:: SetBoneOffsetMatrix (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneOffsetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 283d36bb68e33cfa0e2349bab304b0cdde7ef77e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103663962"
---
# <a name="id3dxskininfosetboneoffsetmatrix-method"></a>Método ID3DXSkinInfo:: SetBoneOffsetMatrix

Define a matriz de deslocamento do Bone.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetBoneOffsetMatrix(
  [in]       DWORD      Bone,
  [in] const D3DXMATRIX *pBoneTransform
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Bone* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número do Bone.

</dd> <dt>

*pBoneTransform* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para a matriz de deslocamento do Bone.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Os nomes de Bone são retornados por [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::GetBoneOffsetMatrix**](id3dxskininfo--getboneoffsetmatrix.md)
</dt> </dl>

 

 
