---
description: Chama ID3DXSprite::Flush e restaura o estado do dispositivo como era antes de ID3DXSprite::Begin ser chamado.
ms.assetid: 603c69f7-13a8-4646-b367-6f2d21b1a2a0
title: Método ID3DXSprite::End (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aeade03ea423d08e412fe35f7c710c9d449cd74c3ed742627ed62954c6011f0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094110"
---
# <a name="id3dxspriteend-method"></a>Método ID3DXSprite::End

Chama [**ID3DXSprite::Flush**](id3dxsprite--flush.md) e restaura o estado do dispositivo como era antes de [**ID3DXSprite::Begin**](id3dxsprite--begin.md) ser chamado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT End();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentários

**ID3DXSprite::End** não pode ser usado como um substituto para [**IDirect3DDevice9::EndScene**](/windows/desktop/api) ou [**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite::Begin**](id3dxsprite--begin.md)
</dt> </dl>

 

 




