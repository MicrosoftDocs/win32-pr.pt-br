---
description: Validar uma técnica.
ms.assetid: d69eaafa-da4d-4599-86fb-83d72e1664cc
title: Método ID3DXEffect::ValidateTechnique (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.ValidateTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4ba3f6422c373c63a9b147ded8f288f642dcd880805cbd1d8b638b3f0e7f8f8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951696"
---
# <a name="id3dxeffectvalidatetechnique-method"></a>Método ID3DXEffect::ValidateTechnique

Validar uma técnica.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ValidateTechnique(
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hTechnique* \[ Em\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo. Consulte [Handles (Direct3D 9)](handles.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DERR \_ CONFLICTINGRENDERSTATE, D3DERR \_ CONFLICTINGTEXTUREFILTER, \_ D3DERR DEVICELOST, D3DERR \_ DRIVERINTERNALERROR, D3DERR \_ TOOMANYOPERATIONS, \_ D3DERR \_ UNSUPPORTEDALPHAARG, D3DERR UNSUPPORTEDALPHAOPERATION, D3DERR \_ UNSUPPORTEDCOLORARG, \_ D3DERR UNSUPPORTEDCOLOROPERATION, D3DERR \_ UNSUPPORTEDFACTORVALUE, D3DERR \_ UNSUPPORTEDTEXTUREFILTER E D3DERR \_ WRONGTEXTUREFORMAT.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect::SetTechnique**](id3dxeffect--settechnique.md)
</dt> </dl>

 

 




