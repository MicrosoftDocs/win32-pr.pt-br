---
description: Define a influência mínima do Bone. Influenciar valores menores do que isso é ignorado.
ms.assetid: 9af19c9e-bb6e-4f93-973f-5c38f88eea3d
title: 'Método ID3DXSkinInfo:: SetMinBoneInfluence (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetMinBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: abe9f1d7f9c54b9c3086160b974e2bc7dc659eb6dae3ff647f059627ff3ef145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747476"
---
# <a name="id3dxskininfosetminboneinfluence-method"></a>Método ID3DXSkinInfo:: SetMinBoneInfluence

Define a influência mínima do Bone. Influenciar valores menores do que isso é ignorado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMinBoneInfluence(
  [in] FLOAT MinInfl
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MinInfl* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valor mínimo de influência. Influenciar valores menores do que isso é ignorado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::GetMinBoneInfluence**](id3dxskininfo--getminboneinfluence.md)
</dt> </dl>

 

 
