---
description: Função D3DXFillCubeTextureTX – usa uma função HLSL (linguagem de sombreador de alto nível) compilada para preencher cada nível de mipmap de uma textura.
ms.assetid: a0c36967-57e6-4771-8e9f-f32949c12001
title: Função D3DXFillCubeTextureTX (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillCubeTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: afdf80cf1557f8b08709536ef49b08206873f5758c4b02a12008b27b4413a116
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731794"
---
# <a name="d3dxfillcubetexturetx-function"></a>Função D3DXFillCubeTextureTX

Usa uma função HLSL (linguagem de sombreador de alto nível) compilada para preencher cada nível de mipmap de uma textura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXFillCubeTextureTX(
  _In_ LPDIRECT3DCUBETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER    pTextureShader
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTexture* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**

Ponteiro para um [**objeto IDirect3DCubeTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) que representa a textura a ser preenchida.

</dd> <dt>

*pTextureShader* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**

Ponteiro para um objeto de sombreador de textura [**ID3DXTextureShader.**](id3dxtextureshader.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

O destino de textura deve ser uma função HLSL que aceita a seguinte semântica:

-   Um parâmetro de entrada deve usar uma semântica POSITION.
-   Um parâmetro de entrada deve usar uma semântica PSIZE.
-   A função deve retornar um parâmetro que usa a semântica COLOR.

Os parâmetros de entrada podem estar em qualquer ordem. Para ver um exemplo, [ **consulte D3DXFillTextureTX**](d3dxfilltexturetx.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXFillVolumeTextureTX**](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 
