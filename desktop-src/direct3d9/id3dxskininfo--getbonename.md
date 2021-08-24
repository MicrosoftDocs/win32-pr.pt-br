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
ms.openlocfilehash: fa56b175d9047935b9f92829823ba2608536ddabb90cb0ad674b86b73cc17475
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674726"
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

## <a name="return-value"></a>Valor retornado

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

 

 
