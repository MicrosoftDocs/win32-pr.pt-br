---
description: Obtém a matriz de deslocamento do Bone.
ms.assetid: 99d47635-ffae-4668-a37c-b15442148fa1
title: 'Método ID3DXSkinInfo:: GetBoneOffsetMatrix (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneOffsetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fce108dc1d0eb08f198ae9375ac35ed149c5e760
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298468"
---
# <a name="id3dxskininfogetboneoffsetmatrix-method"></a>Método ID3DXSkinInfo:: GetBoneOffsetMatrix

Obtém a matriz de deslocamento do Bone.

## <a name="syntax"></a>Sintaxe


```C++
LPD3DXMATRIX GetBoneOffsetMatrix(
  [in] DWORD Bone
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Bone* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número do Bone.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **LPD3DXMATRIX**](d3dxmatrix.md)**

Retorna um ponteiro para a matriz de deslocamento do Bone. Não libere esse ponteiro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**SetBoneOffsetMatrix**](id3dxskininfo--setboneoffsetmatrix.md)
</dt> <dt>

[**GetNumBones**](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 
