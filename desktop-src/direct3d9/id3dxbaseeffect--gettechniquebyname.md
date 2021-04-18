---
description: Obtém o identificador de uma técnica pesquisando seu nome.
ms.assetid: 34871229-ad63-4575-8c60-f27d7f7dddce
title: 'Método ID3DXBaseEffect:: GetTechniqueByName (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechniqueByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5827527bf5151b121958c3f5803ef8a7e74f8d60
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105787762"
---
# <a name="id3dxbaseeffectgettechniquebyname-method"></a>Método ID3DXBaseEffect:: GetTechniqueByName

Obtém o identificador de uma técnica pesquisando seu nome.

## <a name="syntax"></a>Sintaxe


```C++
D3DXHANDLE GetTechniqueByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Cadeia de caracteres que contém o nome da técnica.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Retorna o identificador da primeira técnica que tem o nome especificado ou **NULL** se o nome não foi encontrado. Consulte [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
