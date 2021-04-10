---
description: Inicie a renderização de um mapa de ambiente parabólico.
ms.assetid: 80456084-f5f5-4dfe-805a-7eaaf7f7cb2a
title: 'Método ID3DXRenderToEnvMap:: BeginParabolic (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginParabolic
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5a818abb424fa55bc01eca7ce9f64bc5629a7d50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012084"
---
# <a name="id3dxrendertoenvmapbeginparabolic-method"></a>Método ID3DXRenderToEnvMap:: BeginParabolic

Inicie a renderização de um mapa de ambiente parabólico.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT BeginParabolic(
  [in] LPDIRECT3DTEXTURE9 pTexZPos,
  [in] LPDIRECT3DTEXTURE9 pTexZNeg
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTexZPos* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa a textura de renderização positiva.

</dd> <dt>

*pTexZNeg* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa a textura de renderização negativa.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL. E \_ falha

## <a name="remarks"></a>Comentários

Consulte [**ID3DXRenderToEnvMap:: face**](id3dxrendertoenvmap--face.md) para desenhar as faces.

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

 

 
