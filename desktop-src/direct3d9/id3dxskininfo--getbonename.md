---
description: Obtém o nome do Bone, do índice Bone.
ms.assetid: f56faf41-c119-4cdd-bb8a-86fc99ff5893
title: 'Método ID3DXSkinInfo:: getbonename (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0566d423d277dc3f39f36f8c1fda297ec917eb7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105782651"
---
# <a name="id3dxskininfogetbonename-method"></a>Método ID3DXSkinInfo:: getbonename

Obtém o nome do Bone, do índice Bone.

## <a name="syntax"></a>Sintaxe


```C++
LPCSTR GetBoneName(
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

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Retorna o nome do Bone. Não libere esta cadeia de caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo:: setossoname**](id3dxskininfo--setbonename.md)
</dt> <dt>

[**ID3DXSkinInfo::GetNumBones**](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 
