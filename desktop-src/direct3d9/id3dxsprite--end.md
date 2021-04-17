---
description: 'Chama ID3DXSprite:: flush e restaura o estado do dispositivo para como ele estava antes de ID3DXSprite:: Begin foi chamado.'
ms.assetid: 603c69f7-13a8-4646-b367-6f2d21b1a2a0
title: 'Método ID3DXSprite:: End (D3dx9core. h)'
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
ms.openlocfilehash: f2991cb8a4ae62b5d9ec71450d8e55fbdcdce050
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370983"
---
# <a name="id3dxspriteend-method"></a>Método ID3DXSprite:: End

Chama [**ID3DXSprite:: flush**](id3dxsprite--flush.md) e restaura o estado do dispositivo para como ele estava antes de [**ID3DXSprite:: Begin**](id3dxsprite--begin.md) foi chamado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT End();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentários

**ID3DXSprite:: End** não pode ser usado como um substituto para [**IDirect3DDevice9:: endcena**](/windows/desktop/api) ou [**ID3DXRenderToSurface:: endcena**](id3dxrendertosurface--endscene.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite:: Begin**](id3dxsprite--begin.md)
</dt> </dl>

 

 




