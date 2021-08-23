---
description: Recupere o dispositivo associado ao objeto sprite.
ms.assetid: 9119b232-22c8-4b05-b584-ce176370ca97
title: Método ID3DX10Sprite::GetDevice (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 13513b6fcd2bdb952eda17f10cc81406ff484a20dce3f690d43dd3b5c28eb08f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634246"
---
# <a name="id3dx10spritegetdevice-method"></a>Método ID3DX10Sprite::GetDevice

Recupere o dispositivo associado ao objeto sprite.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDevice(
  [out] ID3D10Device **ppDevice
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppDevice* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

Endereço de um ponteiro para uma interface ID3D10Device, que representa o objeto de dispositivo Direct3D associado ao objeto sprite.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Chamar esse método aumentará a contagem de referência interna na interface ID3D10Device.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




