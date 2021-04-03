---
description: Carrega uma superfície de um arquivo.
ms.assetid: cbd360b6-6cee-418b-8c45-506e190eb2f6
title: Função D3DXLoadSurfaceFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f53343e436ac78b93bcee30c7da5c9d8eb2dc415
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664101"
---
# <a name="d3dxloadsurfacefromfile-function"></a>Função D3DXLoadSurfaceFromFile

Carrega uma superfície de um arquivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXLoadSurfaceFromFile(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          LPCTSTR            pSrcFile,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDestSurface* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**

Ponteiro para uma interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) . Especifica a superfície de destino, que recebe a imagem.

</dd> <dt>

*pDestPalette* \[ no\]
</dt> <dd>

Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , a paleta de destino de 256 cores ou **NULL**.

</dd> <dt>

*pDestRect* \[ no\]
</dt> <dd>

Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***

Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) . Especifica o retângulo de destino. Defina esse parâmetro como **NULL** para especificar a superfície inteira.

</dd> <dt>

*pSrcFile* \[ no\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados String será resolvido para LPCSTR. Consulte Observações.

</dd> <dt>

*pSrcRect* \[ no\]
</dt> <dd>

Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***

Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) . Especifica o retângulo de origem. Defina esse parâmetro como **NULL** para especificar a imagem inteira.

</dd> <dt>

*Filtrar* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md) controlando como a imagem é filtrada. A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação de pontilhado de filtro de D3DX de \_ \_ triângulo \| D3DX \_ \_ .

</dd> <dt>

*COLORKEY* \[ no\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

Valor [**D3DCOLOR**](d3dcolor.md) a ser substituído por preto transparente ou 0 para desabilitar o COLORKEY. Essa é sempre uma cor ARGB de 32 bits, independente do formato de imagem de origem. Alfa é significativo e normalmente deve ser definido como FF para chaves de cores opacas, portanto, para preto opaco, o valor seria igual a 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **\_ informações de D3DXIMAGE**](d3dximage-info.md)\***

Ponteiro para uma estrutura de [**\_ informações de D3DXIMAGE**](d3dximage-info.md) a ser preenchida com uma descrição dos dados no arquivo de imagem de origem, ou **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

A configuração do compilador também determina a versão da função. Se o Unicode for definido, a chamada de função será resolvida como D3DXLoadSurfaceFromFileW. Caso contrário, a chamada de função é resolvida como D3DXLoadSurfaceFromFileA porque as cadeias de caracteres ANSI estão sendo usadas.

Essa função manipula a conversão de e para formatos de textura compactados e oferece suporte aos seguintes formatos de arquivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm e. tga. Consulte [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).

Gravar em uma superfície de não nível zero não fará com que o retângulo sujo seja atualizado. Se **D3DXLoadSurfaceFromFile** for chamado e a superfície já não tiver sido suja (isso é improvável em cenários de uso normal), o aplicativo precisa chamar [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) explicitamente na superfície.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
