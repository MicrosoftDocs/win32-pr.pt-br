---
description: Define um valor de albedo para cada Texel, substituindo valores albedo anteriores.
ms.assetid: 2928c861-a07e-4099-b04f-cdfa41e70874
title: 'Método ID3DXPRTEngine:: SetPerTexelAlbedo (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c6f17e4d3d3922c8e9d54b880f969c14b781935da34eab29b4ec1eb5d4d5421c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985546"
---
# <a name="id3dxprtenginesetpertexelalbedo-method"></a>Método ID3DXPRTEngine:: SetPerTexelAlbedo

Define um valor de albedo para cada Texel, substituindo valores albedo anteriores.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetPerTexelAlbedo(
  [in] LPDIRECT3DTEXTURE9        pAlbedoTexture,
  [in] UINT                      NumChannels,
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAlbedoTexture* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Ponteiro para um objeto de textura [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) no qual armazenar valores de albedo.

</dd> <dt>

*NumChannels* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de canais de cores a serem definidos. Defina como 1 para especificar os materiais em cinza (R = G = B) ou 3 para habilitar os efeitos de sangramento de cor.

</dd> <dt>

*PGH* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**

Ponteiro opcional para um objeto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) . Se não for fornecido, um objeto auxiliar de medianiz de textura será criado e destruído internamente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLED3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ WASSTILLDRAWING, e \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
