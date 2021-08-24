---
description: Método ID3DXRenderToEnvMap::OnResetDevice – use esse método para adquirir recursos e salvar o estado inicial.
ms.assetid: 3e231ad6-858e-4b6a-bbea-0839794bbac7
title: Método ID3DXRenderToEnvMap::OnResetDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1eb90fd50350fb4cbb21be0ff1cb91972481c57e6752b8ce9b603c86e3b050fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628816"
---
# <a name="id3dxrendertoenvmaponresetdevice-method"></a>Método ID3DXRenderToEnvMap::OnResetDevice

Use esse método para adquirir recursos e salvar o estado inicial.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

**ID3DXRenderToEnvMap::OnResetDevice** deve ser chamado sempre que o dispositivo for redefinido (usando [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), antes de qualquer outro método ser chamado. Esse é um bom lugar para adquirir recursos de memória de vídeo e capturar blocos de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
