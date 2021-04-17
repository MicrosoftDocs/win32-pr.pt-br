---
description: Obtém o identificador de uma anotação pesquisando seu nome.
ms.assetid: da4e2805-5f06-4a9b-836f-85a8c154c502
title: 'Método ID3DXBaseEffect:: GetAnnotationByName (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotationByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 00698030488b8f4ae788367f87b8d569476292ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763513"
---
# <a name="id3dxbaseeffectgetannotationbyname-method"></a>Método ID3DXBaseEffect:: GetAnnotationByName

Obtém o identificador de uma anotação pesquisando seu nome.

## <a name="syntax"></a>Sintaxe


```C++
D3DXHANDLE GetAnnotationByName(
  [in] D3DXHANDLE hObject,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hObject* \[ no\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador de um parâmetro de técnica, de passagem ou de nível superior. Consulte [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pname* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Cadeia de caracteres que contém o nome da anotação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Retorna o identificador da anotação especificada ou **NULL** se o nome não foi encontrado. Consulte [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
