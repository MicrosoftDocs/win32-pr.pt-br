---
description: Determina se um parâmetro é usado pela técnica.
ms.assetid: ac50c0d3-93d9-4477-a854-d0b53df28c90
title: 'Método ID3DXEffect:: IsParameterUsed (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.IsParameterUsed
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 80b0e69ec4f46541840d5b381cd25d056b25240a00a9ae84b0aaf46a79295ed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295997"
---
# <a name="id3dxeffectisparameterused-method"></a>Método ID3DXEffect:: IsParameterUsed

Determina se um parâmetro é usado pela técnica.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsParameterUsed(
  [in] D3DXHANDLE hParameter,
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hParameter* \[ no\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo para o parâmetro. Consulte [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*hTechnique* \[ no\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo da técnica. Consulte [Handles (Direct3D 9)](handles.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Retornará **true** se o parâmetro estiver sendo usado e retornará **false** se o parâmetro não estiver sendo usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
