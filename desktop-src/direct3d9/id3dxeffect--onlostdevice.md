---
description: Método ID3DXEffect::OnLostDevice – use esse método para liberar todas as referências a recursos de memória de vídeo e excluir todos os stateblocks. Esse método deve ser chamado sempre que um dispositivo for perdido ou antes de redefinir um dispositivo.
ms.assetid: f56925d8-17f7-44c5-a371-3cde41804613
title: Método ID3DXEffect::OnLostDevice (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.OnLostDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d198cb06461fc377933f2dc90c1e3fb687559ef7b83cc7becd9f04bdf1b78d1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118521211"
---
# <a name="id3dxeffectonlostdevice-method"></a>Método ID3DXEffect::OnLostDevice

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

Esse método deve ser chamado sempre que o dispositivo for perdido ou antes que o usuário chama [**IDirect3DDevice9::Reset**](/windows/desktop/api). Mesmo que o dispositivo não tenha sido realmente perdido, **ID3DXEffect::OnLostDevice** será responsável por liberar stateblocks e outros recursos que talvez precisem ser liberados antes de redefinir o dispositivo. Como resultado, o objeto de fonte não pode ser usado novamente antes de chamar **IDirect3DDevice9::Reset** e, em seguida, [**ID3DXEffect::OnResetDevice**](id3dxeffect--onresetdevice.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




