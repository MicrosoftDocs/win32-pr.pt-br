---
description: Salva uma textura em um arquivo.
ms.assetid: b14dd893-e967-4be9-81e8-aeb52035d91c
title: Função D3DXSaveTextureToFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveTextureToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c11cc8b512527fb0610c288fdbaeba6c976604a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763882"
---
# <a name="d3dxsavetexturetofile-function"></a>Função D3DXSaveTextureToFile

Salva uma textura em um arquivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXSaveTextureToFile(
  _In_       LPCTSTR                pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT   DestFormat,
  _In_       LPDIRECT3DBASETEXTURE9 pSrcTexture,
  _In_ const PALETTEENTRY           *pSrcPalette
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDestFile* \[ no\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo da imagem de destino. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados String será resolvido para LPCSTR. Consulte Observações.

</dd> <dt>

*DestFormat* \[ no\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md)**

[**D3DXIMAGE \_ Fileformate**](./d3dximage-fileformat.md) especificando o formato de arquivo a ser usado ao salvar. Essa função dá suporte ao salvamento em todos os formatos de **\_ FileFormat do D3DXIMAGE** , exceto no pixmap portátil (. ppm) e no adaptador gráfico Targa/Truevision (. tga).

</dd> <dt>

*pSrcTexture* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Ponteiro para a interface [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) , que contém a textura a ser salva.

</dd> <dt>

*pSrcPalette* \[ no\]
</dt> <dd>

Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que contém uma paleta de 256 cores. Este parâmetro pode ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentários

A configuração do compilador também determina a versão da função. Se o Unicode for definido, a chamada de função será resolvida como D3DXSaveTextureToFileW. Caso contrário, a chamada de função é resolvida como D3DXSaveTextureToFileA porque as cadeias de caracteres ANSI estão sendo usadas.

Essa função manipula a conversão de e para formatos de textura compactados.

Se o volume for não dinâmico (devido a um parâmetro de uso definido como 0 na criação) e localizado na memória de vídeo (o pool de memória definido como D3DPOOL \_ padrão), **D3DXSaveTextureToFile** falhará porque o D3DX não pode bloquear volumes não dinâmicos localizados na memória de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXSaveSurfaceToFile**](d3dxsavesurfacetofile.md)
</dt> <dt>

[**D3DXSaveVolumeToFile**](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
