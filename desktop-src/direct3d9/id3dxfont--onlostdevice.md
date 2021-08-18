---
description: Método ID3DXFont::OnLostDevice – use esse método para liberar todas as referências a recursos de memória de vídeo e excluir todos os stateblocks. Esse método deve ser chamado sempre que um dispositivo for perdido ou antes de redefinir um dispositivo.
ms.assetid: 1abc4e01-65c6-4034-8cbb-891a2234ad33
title: Método ID3DXFont::OnLostDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2824fc76bc631802a759dc1d6281406a1c42cf4292e80dc2b80c2a1b33b502a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629876"
---
# <a name="id3dxfontonlostdevice-method"></a>Método ID3DXFont::OnLostDevice

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

Esse método deve ser chamado sempre que o dispositivo for perdido ou antes de o usuário chamar [**Redefinir**](/windows/desktop/api). Mesmo que o dispositivo não tenha sido realmente perdido, **OnLostDevice** é responsável por liberar stateblocks e outros recursos que talvez precisem ser liberados antes de redefinir o dispositivo. Como resultado, o objeto de fonte não pode ser usado novamente antes de chamar **Redefinir** e, em seguida, [**OnResetDevice**](id3dxfont--onresetdevice.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 




