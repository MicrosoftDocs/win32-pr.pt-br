---
description: Salva um volume em um buffer. O método cria um buffer ID3DXBuffer para armazenar os dados e retorna esse objeto.
ms.assetid: 4887ff1f-7904-4764-b284-b2c8e037f806
title: Função D3DXSaveVolumeToFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7daaa41e0cc87ea03a0aedc5fc2f7ca96653329f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172985"
---
# <a name="d3dxsavevolumetofileinmemory-function"></a>Função D3DXSaveVolumeToFileInMemory

Salva um volume em um buffer. O método cria um buffer [**ID3DXBuffer**](id3dxbuffer.md) para armazenar os dados e retorna esse objeto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXSaveVolumeToFileInMemory(
  _Out_       LPD3DXBUFFER         *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT DestFormat,
  _In_        LPDIRECT3DVOLUME9    pSrcVolume,
  _In_  const PALETTEENTRY         *pSrcPalette,
  _In_  const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppDestBuf* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Endereço de um ponteiro para um buffer [**ID3DXBuffer**](id3dxbuffer.md) que armazenará a imagem.

</dd> <dt>

*DestFormat* \[ no\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md)**

[**D3DXIMAGE \_ Fileformate**](./d3dximage-fileformat.md) especificando o formato de arquivo a ser usado ao salvar. Essa função dá suporte ao salvamento em todos os formatos de **\_ FileFormat do D3DXIMAGE** , exceto no pixmap portátil (. ppm) e no adaptador gráfico Targa/Truevision (. tga).

</dd> <dt>

*pSrcVolume* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

Ponteiro para a interface [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) que contém a imagem a ser salva.

</dd> <dt>

*pSrcPalette* \[ no\]
</dt> <dd>

Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que contém uma paleta de 256 cores. Este parâmetro pode ser **NULL**.

</dd> <dt>

*pSrcBox* \[ no\]
</dt> <dd>

Tipo: **const [**D3DBOX**](d3dbox.md) \***

Ponteiro para uma estrutura [**D3DBOX**](d3dbox.md) . Especifica a caixa de origem. Defina esse parâmetro como **NULL** para especificar o volume inteiro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXSaveVolumeToFile**](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
