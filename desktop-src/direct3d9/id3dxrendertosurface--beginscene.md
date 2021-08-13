---
description: Inicia uma cena.
ms.assetid: 8125c592-b985-42f7-8644-59ba93a1c517
title: Método ID3DXRenderToSurface::BeginScene (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.BeginScene
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce6e120361972ac1ff4dbed5d37808dffa0f010af64feda365f65aad8dd393f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293100"
---
# <a name="id3dxrendertosurfacebeginscene-method"></a>Método ID3DXRenderToSurface::BeginScene

Inicia uma cena.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT BeginScene(
  [in]       LPDIRECT3DSURFACE9 pSurface,
  [in] const D3DVIEWPORT9       *pViewport
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSurface* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**

Ponteiro para uma interface [**IDirect3DSurface9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) que representa a superfície de renderização.

</dd> <dt>

*pViewport* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***

Ponteiro para uma [**estrutura D3DVIEWPORT9,**](d3dviewport9.md) descrevendo o viewport para a cena.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL. D3DERR \_ OUTOFVIDEOMEMORY D3DXERR \_ INVALIDDATA E \_ OUTOFMEMORY

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> <dt>

[**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md)
</dt> </dl>

 

 
