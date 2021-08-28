---
description: 'Método ID3DXEffect:: OnResetDevice – Use este método para adquirir novamente os recursos e salvar o estado inicial.'
ms.assetid: 782f3537-f61c-4faa-a0b8-d60c516ba241
title: 'Método ID3DXEffect:: OnResetDevice (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.OnResetDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9c48d93bc5ebf6aa10816f384090da871188220c8b7d0ed17b1f042f292e9024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121509"
---
# <a name="id3dxeffectonresetdevice-method"></a>Método ID3DXEffect:: OnResetDevice

Use este método para readquirir recursos e salvar o estado inicial.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

**ID3DXEffect:: OnResetDevice** deve ser chamado cada vez que o dispositivo for redefinido (usando [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), antes que quaisquer outros métodos sejam chamados. Este é um bom lugar para readquirir recursos de memória de vídeo e capturar blocos de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
