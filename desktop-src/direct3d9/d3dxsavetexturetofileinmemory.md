---
description: Salva uma textura em um arquivo de imagem.
ms.assetid: 8dcfd58a-ae1e-43c3-8ff1-94e3fa398b0f
title: Função D3DXSaveTextureToFileInMemory (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveTextureToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 864362d016190abc4168bdfa66714be371b7811d29b281612e6ba7dc3e0f4889
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749816"
---
# <a name="d3dxsavetexturetofileinmemory-function"></a>Função D3DXSaveTextureToFileInMemory

Salva uma textura em um arquivo de imagem.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXSaveTextureToFileInMemory(
  _Out_       LPD3DXBUFFER           *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT   DestFormat,
  _In_        LPDIRECT3DBASETEXTURE9 pSrcTexture,
  _In_  const PALETTEENTRY           *pSrcPalette
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppDestBuf* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Endereço de um ponteiro para um [**ID3DXBuffer**](id3dxbuffer.md) que armazenará a imagem.

</dd> <dt>

*DestFormat* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**

[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) especificando o formato de arquivo a ser usado ao salvar. Essa função dá suporte à salvação em todos os formatos **D3DXIMAGE \_ FILEFORMAT,** exceto o Mapa Portátil (.ppm) e o Adaptador gráfico Targa/Truevision (.tga).

</dd> <dt>

*pSrcTexture* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Ponteiro para a interface [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) que contém a imagem a ser salva.

</dd> <dt>

*pSrcPalette* \[ Em\]
</dt> <dd>

Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Ponteiro para uma [**estrutura PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que contém uma paleta de 256 cores. Este parâmetro pode ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Essa função lida com a conversão de e para formatos de textura compactados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXSaveSurfaceToFileInMemory**](d3dxsavesurfacetofileinmemory.md)
</dt> <dt>

[**D3DXSaveVolumeToFileInMemory**](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
