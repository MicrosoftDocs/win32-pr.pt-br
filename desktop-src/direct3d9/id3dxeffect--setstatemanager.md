---
description: De definir o gerenciador de estado de efeito.
ms.assetid: 87409687-03f1-4593-ae58-3a8ba08e592b
title: Método ID3DXEffect::SetStateManager (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 06b6a7404f664e8ec18247b2eda57c5097cd575a3556853bfe8a9eb67705d071
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295899"
---
# <a name="id3dxeffectsetstatemanager-method"></a>Método ID3DXEffect::SetStateManager

De definir o gerenciador de estado de efeito.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetStateManager(
  [in] LPD3DXEFFECTSTATEMANAGER pManager
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pManager* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)**

Um ponteiro para o gerenciador de estado. Consulte [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

O [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) é uma interface implementada pelo usuário que fornece retornos de chamada em um aplicativo para definir o estado do dispositivo de um efeito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect::GetStateManager**](id3dxeffect--getstatemanager.md)
</dt> </dl>

 

 




