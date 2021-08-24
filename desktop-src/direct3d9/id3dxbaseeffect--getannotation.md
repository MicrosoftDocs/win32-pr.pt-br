---
description: Obtém o alça de uma anotação.
ms.assetid: 433d73b7-9371-4d76-8b34-a64c608eb1a3
title: Método ID3DXBaseEffect::GetAnnotation (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotation
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c35deeb04e7cf21be429976c102fdf7c3126b1691b3f63725fc994ef79f7ad42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279006"
---
# <a name="id3dxbaseeffectgetannotation-method"></a>Método ID3DXBaseEffect::GetAnnotation

Obtém o alça de uma anotação.

## <a name="syntax"></a>Sintaxe


```C++
D3DXHANDLE GetAnnotation(
  [in] D3DXHANDLE hObject,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hObject* \[ Em\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Lidar com uma técnica, passar ou parâmetro de nível superior. Consulte [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*Índice* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice de anotação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Retorna o handle da anotação especificada ou **NULL** se o índice era inválido. Consulte [Handles (Direct3D 9)](handles.md).

## <a name="remarks"></a>Comentários

As anotações são dados específicos do usuário que podem ser anexados a qualquer técnica, passagem ou parâmetro. Consulte [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
