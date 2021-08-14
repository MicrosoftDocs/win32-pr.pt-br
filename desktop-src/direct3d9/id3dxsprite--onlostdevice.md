---
description: Método ID3DXSprite::OnLostDevice – use esse método para liberar todas as referências a recursos de memória de vídeo e excluir todos os stateblocks. Esse método deve ser chamado sempre que um dispositivo for perdido ou antes de redefinir um dispositivo.
ms.assetid: 60028f18-21fe-428b-9bee-d5359671da81
title: Método ID3DXSprite::OnLostDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8431fd8b7c8e106e6eca1b28498befb828c67880d173bd5141e771885cbab1a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985195"
---
# <a name="id3dxspriteonlostdevice-method"></a>Método ID3DXSprite::OnLostDevice

Use esse método para liberar todas as referências a recursos de memória de vídeo e excluir todos os stateblocks. Esse método deve ser chamado sempre que um dispositivo for perdido ou antes de redefinir um dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Esse método deve ser chamado sempre que o dispositivo for perdido ou antes que o usuário chama [**IDirect3DDevice9::Reset**](/windows/desktop/api). Mesmo que o dispositivo não tenha sido realmente perdido, **ID3DXSprite::OnLostDevice** será responsável por liberar stateblocks e outros recursos que talvez precisem ser liberados antes de redefinir o dispositivo. Como resultado, o objeto de fonte não pode ser usado novamente antes de chamar **IDirect3DDevice9::Reset** e, em seguida, [**ID3DXSprite::OnResetDevice**](id3dxsprite--onresetdevice.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 




