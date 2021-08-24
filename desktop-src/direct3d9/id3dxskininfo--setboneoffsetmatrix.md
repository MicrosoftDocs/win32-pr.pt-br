---
description: Define a matriz de deslocamento de deslocamento de deslocamento.
ms.assetid: f8ac1117-510d-42af-a6bf-422cbaaf6b74
title: Método ID3DXSkinInfo::SetBoneOffsetMatrix (D3DX9Mesh.h)
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
ms.openlocfilehash: 9d5daf20697777cfbf1b72d4ab18936f81c262ba9b23379d6089bffca8b9a516
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674706"
---
# <a name="id3dxskininfosetboneoffsetmatrix-method"></a>Método ID3DXSkinInfo::SetBoneOffsetMatrix

Define a matriz de deslocamento de deslocamento de deslocamento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetBoneOffsetMatrix(
  [in]       DWORD      Bone,
  [in] const D3DXMATRIX *pBoneTransform
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*São Paulo* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número do fragmento.

</dd> <dt>

*pBoneTransform* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para a matriz de deslocamento de deslocamento de deslocamento.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Os nomes de veados são retornados [**por D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::GetBoneOffsetMatrix**](id3dxskininfo--getboneoffsetmatrix.md)
</dt> </dl>

 

 
