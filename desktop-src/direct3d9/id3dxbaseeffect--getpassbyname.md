---
description: Obtém o alça de uma passagem procurando seu nome.
ms.assetid: 24d043a2-5c87-4a59-80d4-0c81bd7a0b3e
title: Método ID3DXBaseEffect::GetPassByName (D3DX9Effect.h)
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
ms.openlocfilehash: 5837d2b69c793f788c4c89f648402e7924bc2f3af9a92bbbe596c133efe10d1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987756"
---
# <a name="id3dxbaseeffectgetpassbyname-method"></a>Método ID3DXBaseEffect::GetPassByName

Obtém o alça de uma passagem procurando seu nome.

## <a name="syntax"></a>Sintaxe


```C++
D3DXHANDLE GetPassByName(
  [in] D3DXHANDLE hTechnique,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hTechnique* \[ Em\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Lidar com a técnica pai. Consulte [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pName* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Cadeia de caracteres que contém o nome de passagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Retorna o handle da primeira passagem dentro da técnica especificada que tem o nome especificado ou **NULL** se o nome não foi encontrado. Consulte [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
