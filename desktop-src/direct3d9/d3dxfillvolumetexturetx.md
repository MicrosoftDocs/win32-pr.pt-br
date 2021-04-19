---
description: Usa uma função HLSL (linguagem de sombreamento de alto nível) compilada para preencher cada Texel de cada nível de mipmap de uma textura.
ms.assetid: f082e1d2-c433-482c-9288-58e5c558cdc5
title: Função D3DXFillVolumeTextureTX (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillVolumeTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de310ee6171924a5d2b61071d47c421739f15833
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105785327"
---
# <a name="d3dxfillvolumetexturetx-function"></a>Função D3DXFillVolumeTextureTX

Usa uma função HLSL (linguagem de sombreamento de alto nível) compilada para preencher cada Texel de cada nível de mipmap de uma textura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXFillVolumeTextureTX(
  _In_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER      pTextureShader
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTexture* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**

Ponteiro para um objeto [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , representando a textura a ser preenchida.

</dd> <dt>

*pTextureShader* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**

Ponteiro para um objeto sombreador de textura [**ID3DXTextureShader**](id3dxtextureshader.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ não disponível, D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

O destino de textura deve ser uma função HLSL que contenha a seguinte semântica:

-   Um parâmetro de entrada deve usar uma semântica de posição.
-   Um parâmetro de entrada deve usar uma semântica PSIZE.
-   A função deve retornar um parâmetro que usa a semântica de cor.

Os parâmetros de entrada podem estar em qualquer ordem. Para obter um exemplo, consulte [ **D3DXFillTextureTX**](d3dxfilltexturetx.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXFillTextureTX**](d3dxfilltexturetx.md)
</dt> <dt>

[**D3DXFillCubeTextureTX**](d3dxfillcubetexturetx.md)
</dt> </dl>

 

 
