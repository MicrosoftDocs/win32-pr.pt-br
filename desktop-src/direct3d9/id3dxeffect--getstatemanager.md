---
description: Obtenha o Gerenciador de estado do efeito.
ms.assetid: 4a09eb2a-2393-40b0-81b9-3c27998c2b77
title: 'Método ID3DXEffect:: getstatemanager (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6700447485d83f2610149b809065ab02140a2e6cf068508b6571d5132844fb0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121637"
---
# <a name="id3dxeffectgetstatemanager-method"></a>Método ID3DXEffect:: getstatemanager

Obtenha o Gerenciador de estado do efeito.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStateManager(
  [out] LPD3DXEFFECTSTATEMANAGER *ppManager
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppManager* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)\***

Retorna um ponteiro para o Gerenciador de estado. Consulte [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

O [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) é uma interface implementada pelo usuário que fornece retornos de chamada em um aplicativo para definir o estado do dispositivo de um efeito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect:: setstatemanager**](id3dxeffect--setstatemanager.md)
</dt> </dl>

 

 




