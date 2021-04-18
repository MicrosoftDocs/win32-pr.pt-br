---
description: Obtém o identificador de uma passagem procurando seu nome.
ms.assetid: 24d043a2-5c87-4a59-80d4-0c81bd7a0b3e
title: 'Método ID3DXBaseEffect:: GetPassByName (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 2cd96a9d91f0e822b3e869bd8f0c965f0f951f44
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105780662"
---
# <a name="id3dxbaseeffectgetpassbyname-method"></a>Método ID3DXBaseEffect:: GetPassByName

Obtém o identificador de uma passagem procurando seu nome.

## <a name="syntax"></a>Sintaxe


```C++
D3DXHANDLE GetPassByName(
  [in] D3DXHANDLE hTechnique,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hTechnique* \[ no\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador da técnica pai. Consulte [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pname* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Cadeia de caracteres que contém o nome da passagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Retorna o identificador da primeira passagem dentro da técnica especificada que tem o nome especificado ou **nulo** se o nome não foi encontrado. Consulte [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
