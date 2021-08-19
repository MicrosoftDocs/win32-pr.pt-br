---
description: Função D3DXCreateVolumeTextureFromFileEx – cria uma textura de volume de um arquivo.
ms.assetid: fa11706a-83cc-4795-957d-6d0e1faf2a8f
title: Função D3DXCreateVolumeTextureFromFileEx (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 47d46f2472bf9c055814ed575584a087dc5922dc104fcbb3a49b2a2b2a93a958
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731885"
---
# <a name="d3dxcreatevolumetexturefromfileex-function"></a>Função D3DXCreateVolumeTextureFromFileEx

Cria uma textura de volume de um arquivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateVolumeTextureFromFileEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    LPCTSTR                  pSrcFile,
  _In_    UINT                     Width,
  _In_    UINT                     Height,
  _In_    UINT                     Depth,
  _In_    UINT                     MipLevels,
  _In_    DWORD                    Usage,
          D3DFORMAT                Format,
  _In_    D3DPOOL                  Pool,
  _In_    DWORD                    Filter,
  _In_    DWORD                    MipFilter,
  _In_    D3DCOLOR                 ColorKey,
  _Inout_ D3DXIMAGE_INFO           *pSrcInfo,
  _Out_   PALETTEENTRY             *pPalette,
  _Out_   LPDIRECT3DVOLUMETEXTURE9 *ppTexture
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa o dispositivo a ser associado à textura.

</dd> <dt>

*pSrcFile* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados de cadeia de caracteres será resolvido para LPCSTR. Consulte Observações.

</dd> <dt>

*Largura* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Largura em pixels. Se esse valor for zero ou D3DX \_ DEFAULT, as dimensões serão retiradas do arquivo. A dimensão máxima que um driver dá suporte (para largura, altura e profundidade) pode ser encontrada em MaxVolumeExtent em [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

*Altura* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Altura, em pixels. Se esse valor for zero ou D3DX \_ DEFAULT, as dimensões serão retiradas do arquivo. A dimensão máxima que um driver dá suporte (para largura, altura e profundidade) pode ser encontrada em MaxVolumeExtent em [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

*Profundidade* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Profundidade, em pixels. Se esse valor for zero ou D3DX \_ DEFAULT, as dimensões serão retiradas do arquivo. A dimensão máxima que um driver dá suporte (para largura, altura e profundidade) pode ser encontrada em MaxVolumeExtent em [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

*MipLevels* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de níveis de mip solicitados. Se esse valor for zero ou D3DX \_ DEFAULT, uma cadeia de mipmap completa será criada.

</dd> <dt>

*Uso* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0, D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ DYNAMIC. Definir esse sinalizador como D3DUSAGE RENDERTARGET indica que a superfície \_ deve ser usada como um destino de renderização. O recurso pode ser passado para o parâmetro *pNewRenderTarget* do [**método SetRenderTarget.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) Se D3DUSAGE RENDERTARGET ou D3DUSAGE DYNAMIC for especificado, o pool deverá ser definido como D3DPOOL DEFAULT e o aplicativo deverá verificar se o dispositivo dá suporte a essa operação chamando \_ \_  \_ [**CheckDeviceFormat**](/windows/desktop/api). D3DUSAGE \_ DYNAMIC indica que a superfície deve ser tratada dinamicamente. Para obter mais informações sobre como usar texturas dinâmicas, consulte [Usando texturas dinâmicas.](performance-optimizations.md)

</dd> <dt>

*Formato* 
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Membro do tipo [enumerado D3DFORMAT,](d3dformat.md) que descreve o formato de pixel solicitado para a textura. A textura retornada pode ter um formato diferente do especificado por *Formatar*. Os aplicativos devem verificar o formato da textura retornada. Se [D3DFMT \_ UNKNOWN](other-d3dx-constants.md), o formato será retirado do arquivo. Se D3DFMT FROM FILE, o formato será feito exatamente como está no arquivo e a chamada falhará se isso violar as \_ \_ funcionalidades do dispositivo.

</dd> <dt>

*Pool* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Membro do tipo [**enumerado D3DPOOL,**](./d3dpool.md) descrevendo a classe de memória na qual a textura deve ser colocada.

</dd> <dt>

*Filtro* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Uma combinação de um ou mais [FILTRO D3DX \_ controlando](d3dx-filter.md) como a imagem é filtrada. Especificar D3DX DEFAULT para esse parâmetro é o equivalente a especificar \_ D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER.

</dd> <dt>

*MipFilter* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Uma combinação de um ou mais [FILTRO D3DX \_ controlando](d3dx-filter.md) como a imagem é filtrada. Especificar D3DX \_ DEFAULT para esse parâmetro é o equivalente a especificar D3DX \_ FILTER \_ BOX. Além disso, use bits 27-31 para especificar o número de níveis de mip a serem ignorados (da parte superior da cadeia mipmap) quando uma textura .dds for carregada na memória; isso permite que você ignore até 32 níveis.

</dd> <dt>

*ColorKey* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

[**Valor D3DCOLOR**](d3dcolor.md) a ser substituído por preto transparente ou 0 para desabilitar a chave de cores. Essa é sempre uma cor ARGB de 32 bits, independentemente do formato de imagem de origem. Alfa é significativo e geralmente deve ser definido como FF para chaves de cores opacas. Portanto, para preto opaco, o valor seria igual a 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***

Ponteiro para uma [**estrutura D3DXIMAGE \_ INFO**](d3dximage-info.md) a ser preenchida com uma descrição dos dados no arquivo de imagem de origem ou **NULL.**

</dd> <dt>

*pPalette* \[ out\]
</dt> <dd>

Tipo: **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***

Ponteiro para uma [**estrutura PALETTEENTRY,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que representa uma paleta de 256 cores a ser preenchida ou **NULL.**

</dd> <dt>

*ppTexture* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***

Endereço de um ponteiro para uma interface [**IDirect3DVolumeTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) representando o objeto de textura criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

A configuração do compilador também determina a versão da função. Se Unicode for definido, a chamada de função será resolvida para D3DXCreateVolumeTextureFromFileExW. Caso contrário, a chamada de função será resolvida para D3DXCreateVolumeTextureFromFileExA porque as cadeias de caracteres ANSI estão sendo usadas.

Essa função dá suporte aos seguintes formatos de arquivo: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm e .tga. Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

As texturas mapeadas automaticamente têm cada nível preenchido com a textura de volume carregada. Ao carregar imagens em texturas com mipmapped, alguns dispositivos não podem ir para uma imagem 1x1 e essa função falhará. Se isso acontecer, as imagens precisarão ser carregadas manualmente.

Ao ignorar níveis de mipmap ao carregar um arquivo .dds, use a macro D3DX SKIP DDS MIP LEVELS para gerar o \_ \_ valor \_ \_ *MipFilter.* Essa macro leva o número de níveis a ignorar e o tipo de filtro e retorna o valor do filtro, que seria passado para o *parâmetro MipFilter.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3DXCreateVolumeTextureFromFile**](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromFileInMemory**](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromFileInMemoryEx**](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromResource**](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromResourceEx**](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
