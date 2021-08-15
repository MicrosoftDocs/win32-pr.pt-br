---
description: Recupera o dispositivo Direct3D associado à superfície de renderização.
ms.assetid: 579cf7da-b8e0-4d9f-93b8-b1f47c3d5654
title: Método ID3DXRenderToSurface::GetDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b7b8ea6887eb1b18b1e2eb28a811f05f10e9df4614ddb8dbc02371acc176c866
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729600"
---
# <a name="id3dxrendertosurfacegetdevice-method"></a>Método ID3DXRenderToSurface::GetDevice

Recupera o dispositivo Direct3D associado à superfície de renderização.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppDevice* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***

Endereço de um ponteiro para uma interface [**IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa o objeto de dispositivo Direct3D associado à superfície de renderização.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL. Chamar esse método aumentará a contagem de referência interna na interface [**IDirect3DDevice9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) Certifique-se de [**chamar IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) quando terminar de usar essa interface **IDirect3DDevice9** ou você terá uma perda de memória.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> </dl>

 

 
