---
description: Obtém o identificador de uma função procurando seu nome.
ms.assetid: 1e2e2dae-5084-47f3-9812-3dbf609bd70b
title: 'Método ID3DXBaseEffect:: GetFunctionByName (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: bcc16fa8136332e2a5d1a87956e1d4cc6a2a562b7e4e3531efbcc09f1314978b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121969"
---
# <a name="id3dxbaseeffectgetfunctionbyname-method"></a>Método ID3DXBaseEffect:: GetFunctionByName

Obtém o identificador de uma função procurando seu nome.

## <a name="syntax"></a>Sintaxe


```C++
D3DXHANDLE GetFunctionByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Cadeia de caracteres que contém o nome da função.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Retorna o identificador da função especificada ou **NULL** se o nome não foi encontrado. Consulte [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
