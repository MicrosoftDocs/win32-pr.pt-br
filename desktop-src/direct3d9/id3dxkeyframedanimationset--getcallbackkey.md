---
description: 'Método ID3DXKeyframedAnimationSet:: GetCallbackKey – Obtém informações sobre um retorno de chamada específico no conjunto de animações.'
ms.assetid: a1d3ca96-2852-420a-aa5c-a434970e5523
title: 'Método ID3DXKeyframedAnimationSet:: GetCallbackKey (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f3ebbf93bd482a2259ffdaaf272c65b5e86d5270
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090314"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkey-method"></a>Método ID3DXKeyframedAnimationSet:: GetCallbackKey

Obtém informações sobre um retorno de chamada específico no conjunto de animações.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCallbackKey(
  [in]  UINT               Animation,
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Animação* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice de animação.

</dd> <dt>

*pCallbackKeys* \[ fora\]
</dt> <dd>

Tipo: **[ **\_ retorno de chamada LPD3DXKEY**](d3dxkey-callback.md)**

Ponteiro para a [**função de retorno de chamada**](d3dxkey-callback.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
