---
description: Inicie a renderização de um mapa de ambiente esférico.
ms.assetid: b0634120-f5ad-48b3-979a-30b0a53d22a2
title: 'Método ID3DXRenderToEnvMap:: BeginSphere (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginSphere
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 872aa06734ae818ef248b03fbc14dcd1c33fe815
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298563"
---
# <a name="id3dxrendertoenvmapbeginsphere-method"></a>Método ID3DXRenderToEnvMap:: BeginSphere

Inicie a renderização de um mapa de ambiente esférico.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT BeginSphere(
  [in] LPDIRECT3DTEXTURE9 pTex
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTeX* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa a textura a ser renderizada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL. E \_ falha

## <a name="remarks"></a>Comentários

Consulte [**ID3DXRenderToEnvMap:: face**](id3dxrendertoenvmap--face.md) para desenhar a face.

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

 

 
