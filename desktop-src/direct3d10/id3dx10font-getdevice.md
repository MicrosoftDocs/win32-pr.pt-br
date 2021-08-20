---
description: Recupere o dispositivo Direct3D associado ao objeto de fonte.
ms.assetid: aad2406e-9461-4a84-9875-74b53d68ef40
title: Método ID3DX10Font::GetDevice (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0abed8fcb2e5c85b64c58f66f7584d1c6af5f5b6b4ed9e2efd7266ea38a5a8dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118100401"
---
# <a name="id3dx10fontgetdevice-method"></a>Método ID3DX10Font::GetDevice

Recupere o dispositivo Direct3D associado ao objeto de fonte.

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

Endereço de um ponteiro para uma interface ID3D10Device, que representa o objeto de dispositivo Direct3D associado ao objeto de fonte.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

> [!Note]  
> Chamar esse método aumentará a contagem de referência interna na interface ID3D10Device. Certifique-se de chamar IUnknown quando terminar de usar essa interface ID3D10Device ou você terá uma perda de memória.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




