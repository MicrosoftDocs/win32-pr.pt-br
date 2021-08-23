---
description: Restaura o estado do dispositivo como estava quando ID3DXLine::Begin foi chamado.
ms.assetid: 06243c30-2d1d-4101-a373-46fd9a0d88d3
title: Método ID3DXLine::End (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 371463bfc24cbdba63ac51c9b729c267b9d020dd260d6d1b6c6a378bb38c3524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987226"
---
# <a name="id3dxlineend-method"></a>Método ID3DXLine::End

Restaura o estado do dispositivo como estava quando [**ID3DXLine::Begin**](id3dxline--begin.md) foi chamado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT End();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

**ID3DXLine::End** não pode ser usado como um substituto para [**IDirect3DDevice9::EndScene**](/windows/desktop/api) ou [**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine::Begin**](id3dxline--begin.md)
</dt> </dl>

 

 




