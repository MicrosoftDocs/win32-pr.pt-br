---
description: Salva uma textura em um arquivo.
ms.assetid: b14dd893-e967-4be9-81e8-aeb52035d91c
title: Função D3DXSaveTextureToFile (D3dx9tex.h)
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
ms.openlocfilehash: 954b761f8980a7397be1c79fbd8beb88ddbb29f29ce74557ca90cc77dee2ea5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988304"
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

*pDestFile* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo da imagem de destino. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados de cadeia de caracteres será resolvido para LPCSTR. Consulte Observações.

</dd> <dt>

*DestFormat* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**

[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) especificando o formato de arquivo a ser usado ao salvar. Essa função dá suporte à salvação em todos os formatos **D3DXIMAGE \_ FILEFORMAT,** exceto o Mapa Portátil (.ppm) e o Adaptador gráfico Targa/Truevision (.tga).

</dd> <dt>

*pSrcTexture* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Ponteiro para a interface [**IDirect3DBaseTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) que contém a textura a ser salva.

</dd> <dt>

*pSrcPalette* \[ Em\]
</dt> <dd>

Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Ponteiro para uma [**estrutura PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que contém uma paleta de 256 cores. Este parâmetro pode ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentários

A configuração do compilador também determina a versão da função. Se Unicode for definido, a chamada de função será resolvida para D3DXSaveTextureToFileW. Caso contrário, a chamada de função será resolvida para D3DXSaveTextureToFileA porque as cadeias de caracteres ANSI estão sendo usadas.

Essa função lida com a conversão de e para formatos de textura compactados.

Se o volume for nãodinâmico (devido a um parâmetro de uso definido como 0 na criação) e localizado na memória de vídeo (o pool de memória definido como D3DPOOL \_ DEFAULT), **D3DXSaveTextureToFile** falhará porque O D3DX não pode bloquear volumes nãodinâmicos localizados na memória de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXSaveSurfaceToFile**](d3dxsavesurfacetofile.md)
</dt> <dt>

[**D3DXSaveVolumeToFile**](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
