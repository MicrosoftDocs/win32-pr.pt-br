---
description: Inicie a renderização de um mapa de ambiente cúbico.
ms.assetid: 0f02b2e2-8132-4994-ab07-c79a1b7821dd
title: 'Método ID3DXRenderToEnvMap:: BeginCube (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginCube
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 081e96425a7928cb1cd4a5a3ee48479d562c5c30a2f9017665acd32ffb539244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293270"
---
# <a name="id3dxrendertoenvmapbegincube-method"></a>Método ID3DXRenderToEnvMap:: BeginCube

Inicie a renderização de um mapa de ambiente cúbico.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT BeginCube(
  [in] LPDIRECT3DCUBETEXTURE9 pCubeTex
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCubeTex* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**

Ponteiro para uma interface [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) que representa a textura do cubo a ser renderizada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Consulte [**ID3DXRenderToEnvMap:: face**](id3dxrendertoenvmap--face.md) para desenhar cada uma das 6 faces.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> <dt>

[**ID3DXRenderToEnvMap:: End**](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
