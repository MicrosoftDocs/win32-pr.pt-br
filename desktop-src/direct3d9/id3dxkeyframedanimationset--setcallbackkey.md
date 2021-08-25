---
description: Define informações sobre um retorno de chamada específico no conjunto de animação.
ms.assetid: 899f3a85-c878-4eeb-8bda-fc4e9083bd1f
title: Método ID3DXKeyframedAnimationSet::SetCallbackKey (D3dx9 bluetoothm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetCallbackKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5998842927019868249278465eaf7bf9bd4ab62c3bfe83537a0eba420f87aeb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847756"
---
# <a name="id3dxkeyframedanimationsetsetcallbackkey-method"></a>Método ID3DXKeyframedAnimationSet::SetCallbackKey

Define informações sobre um retorno de chamada específico no conjunto de animação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetCallbackKey(
  [in]  UINT               Animation,
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Animação* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice de animação.

</dd> <dt>

*pCallbackKeys* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXKEY \_ CALLBACK**](d3dxkey-callback.md)**

Ponteiro para a [**função de retorno de chamada**](d3dxkey-callback.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
