---
description: Cria uma textura de volume a partir de um arquivo. Essa é uma função mais avançada do que D3DXCreateVolumeTextureFromFileInMemory.
ms.assetid: 1a43f906-1826-40a3-a7a9-a0536c977164
title: Função D3DXCreateVolumeTextureFromFileInMemoryEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f09439be9410b59ccaa446c2f00ee79963a21cc6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105790510"
---
# <a name="d3dxcreatevolumetexturefromfileinmemoryex-function"></a>Função D3DXCreateVolumeTextureFromFileInMemoryEx

Cria uma textura de volume a partir de um arquivo. Essa é uma função mais avançada do que [**D3DXCreateVolumeTextureFromFileInMemory**](d3dxcreatevolumetexturefromfileinmemory.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateVolumeTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    LPCVOID                  pSrcData,
  _In_    UINT                     SrcDataSize,
  _In_    UINT                     Width,
  _In_    UINT                     Height,
  _In_    UINT                     Depth,
  _In_    UINT                     MipLevels,
  _In_    DWORD                    Usage,
  _In_    D3DFORMAT                Format,
  _In_    D3DPOOL                  Pool,
  _In_    DWORD                    Filter,
  _In_    DWORD                    MipFilter,
  _In_    D3DCOLOR                 ColorKey,
  _Inout_ D3DXIMAGE_INFO           *pSrcInfo,
  _Out_   PALETTEENTRY             *pPalette,
  _Out_   LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura.

</dd> <dt>

*pSrcData* \[ no\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Ponteiro para o arquivo na memória a partir da qual criar a textura de volume.

</dd> <dt>

*SrcDataSize* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Tamanho do arquivo na memória, em bytes.

</dd> <dt>

*Largura* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Largura em pixels. Se esse valor for zero ou D3DX \_ padrão, as dimensões serão obtidas do arquivo. A dimensão máxima à qual um driver dá suporte (para largura, altura e profundidade) pode ser encontrada em MaxVolumeExtent em [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

*Altura* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Altura, em pixels. Se esse valor for zero ou D3DX \_ padrão, as dimensões serão obtidas do arquivo. A dimensão máxima à qual um driver dá suporte (para largura, altura e profundidade) pode ser encontrada em MaxVolumeExtent em [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

*Profundidade* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Profundidade, em pixels. Se esse valor for zero ou D3DX \_ padrão, as dimensões serão obtidas do arquivo. A dimensão máxima à qual um driver dá suporte (para largura, altura e profundidade) pode ser encontrada em MaxVolumeExtent em [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

*MipLevels* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de níveis de MIP solicitados. Se esse valor for zero ou D3DX \_ padrão, uma cadeia de mipmap completa será criada.

</dd> <dt>

*Uso* \[ do no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0, D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ Dynamic. Definir esse sinalizador como D3DUSAGE \_ RENDERTARGET indica que a superfície deve ser usada como um destino de renderização. O recurso pode então ser passado para o parâmetro *pNewRenderTarget* do método [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) . Se D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ Dynamic for especificado, o *pool* deverá ser definido como D3DPOOL \_ padrão e o aplicativo deverá verificar se o dispositivo dá suporte a essa operação chamando [**CheckDeviceFormat**](/windows/desktop/api). D3DUSAGE \_ Dynamic indica que a superfície deve ser manipulada dinamicamente. Para obter mais informações sobre como usar texturas dinâmicas, consulte [usando texturas dinâmicas](performance-optimizations.md).

</dd> <dt>

*Formato* \[ no\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato de pixel solicitado para a textura. A textura retornada pode ter um formato diferente daquele especificado pelo *formato*. Os aplicativos devem verificar o formato da textura retornada. Se [D3DFMT \_ desconhecido](other-d3dx-constants.md), o formato será extraído do arquivo. Se D3DFMT \_ do \_ arquivo, o formato será levado exatamente como está no arquivo e a chamada falhará se isso violar os recursos do dispositivo.

</dd> <dt>

*Pool* \[ de no\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , que descreve a classe de memória na qual a textura deve ser colocada.

</dd> <dt>

*Filtrar* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md) controlando como a imagem é filtrada. A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação de pontilhado de filtro de D3DX de \_ \_ triângulo \| D3DX \_ \_ .

</dd> <dt>

*MipFilter* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md) controlando como a imagem é filtrada. A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação da \_ caixa de filtro D3DX \_ . Além disso, use o bits 27-31 para especificar o número de níveis MIP a serem ignorados (da parte superior da cadeia mipmap) quando uma textura. DDS for carregada na memória; Isso permite que você pule até 32 níveis.

</dd> <dt>

*COLORKEY* \[ no\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

Valor [**D3DCOLOR**](d3dcolor.md) a ser substituído por preto transparente ou 0 para desabilitar o COLORKEY. Essa é sempre uma cor ARGB de 32 bits, independente do formato de imagem de origem. Alfa é significativo e deve geralmente ser definido como FF para chaves de cor opacas. Portanto, para preto opaco, o valor seria igual a 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **\_ informações de D3DXIMAGE**](d3dximage-info.md)\***

Ponteiro para uma estrutura de [**\_ informações de D3DXIMAGE**](d3dximage-info.md) a ser preenchida com uma descrição dos dados no arquivo de imagem de origem, ou **NULL**.

</dd> <dt>

*pPalette* \[ fora\]
</dt> <dd>

Tipo: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***

Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , representando uma paleta de cor de 256 para preencher ou **NULL**.

</dd> <dt>

*ppVolumeTexture* \[ fora\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***

Endereço de um ponteiro para uma interface [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , que representa o objeto de textura criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ não disponível, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, e \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Essa função dá suporte aos seguintes formatos de arquivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm e. tga. Consulte [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).

Ao ignorar os níveis de mipmap ao carregar um arquivo. DDS, use a \_ \_ macro D3DX \_ ignorar \_ os níveis de MIP do DDS para gerar o valor de *MipFilter* . Essa macro usa o número de níveis a serem ignorados e o tipo de filtro e retorna o valor do filtro, que seria passado para o parâmetro *MipFilter* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3DXCreateVolumeTextureFromFile**](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromFileEx**](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromFileInMemory**](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromResource**](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromResourceEx**](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
