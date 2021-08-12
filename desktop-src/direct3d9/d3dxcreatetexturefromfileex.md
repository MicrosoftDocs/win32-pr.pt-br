---
description: Cria uma textura de um arquivo. Essa é uma função mais avançada do que D3DXCreateTextureFromFile.
ms.assetid: 820bbd77-98af-4051-a22e-825fa4dd87d8
title: Função D3DXCreateTextureFromFileEx (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d5964f7f466dac135d08958ef66c12a1dfe2e61a19180eb45072c5489f9f4a64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299241"
---
# <a name="d3dxcreatetexturefromfileex-function"></a>Função D3DXCreateTextureFromFileEx

Cria uma textura de um arquivo. Essa é uma função mais avançada do que [**D3DXCreateTextureFromFile.**](d3dxcreatetexturefromfile.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateTextureFromFileEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    LPCTSTR            pSrcFile,
  _In_    UINT               Width,
  _In_    UINT               Height,
  _In_    UINT               MipLevels,
  _In_    DWORD              Usage,
  _In_    D3DFORMAT          Format,
  _In_    D3DPOOL            Pool,
  _In_    DWORD              Filter,
  _In_    DWORD              MipFilter,
  _In_    D3DCOLOR           ColorKey,
  _Inout_ D3DXIMAGE_INFO     *pSrcInfo,
  _Out_   PALETTEENTRY       *pPalette,
  _Out_   LPDIRECT3DTEXTURE9 *ppTexture
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

Largura em pixels. Se esse valor for zero ou D3DX DEFAULT, as dimensões serão retiradas do arquivo e arredondadas para uma \_ potência de dois. Se o dispositivo for compatível com a não potência de duas texturas e [D3DX \_ DEFAULT \_ NONPOW2](other-d3dx-constants.md) for especificado, o tamanho não será arredondado.

</dd> <dt>

*Altura* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Altura, em pixels. Se esse valor for zero ou D3DX DEFAULT, as dimensões serão retiradas do arquivo e arredondadas para uma \_ potência de dois. Se o dispositivo for compatível com a não potência de duas texturas e [D3DX \_ DEFAULT \_ NONPOW2](other-d3dx-constants.md) for sepcified, o tamanho não será arredondado.

</dd> <dt>

*MipLevels* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de níveis de mip solicitados. Se esse valor for zero ou D3DX \_ DEFAULT, uma cadeia de mipmap completa será criada. Se D3DX FROM FILE, o tamanho será tirado exatamente como está no arquivo e a chamada falhará se isso violar as \_ \_ funcionalidades do dispositivo.

</dd> <dt>

*Uso* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0, [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)ou **D3DUSAGE \_ DYNAMIC.** Definir esse sinalizador como **D3DUSAGE \_ RENDERTARGET** indica que a superfície deve ser usada como um destino de renderização. O recurso pode ser passado para o parâmetro *pNewRenderTarget* do [**método SetRenderTarget.**](/windows/desktop/api) Se **D3DUSAGE \_ RENDERTARGET** ou **D3DUSAGE \_ DYNAMIC** for especificado, o *pool* deverá ser definido como D3DPOOL DEFAULT e o aplicativo deverá verificar se o dispositivo dá suporte a essa operação chamando \_ [**CheckDeviceFormat**](/windows/desktop/api). **D3DUSAGE \_ DYNAMIC** indica que a superfície deve ser tratada dinamicamente. Consulte [Usando texturas dinâmicas](performance-optimizations.md).

</dd> <dt>

*Formato* \[ Em\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Membro do tipo [enumerado D3DFORMAT,](d3dformat.md) que descreve o formato de pixel solicitado para a textura. A textura retornada pode ter um formato diferente do especificado por *Formatar*. Os aplicativos devem verificar o formato da textura retornada. Se D3DFMT \_ UNKNOWN, o formato será retirado do arquivo. Se D3DFMT FROM FILE, o formato será feito exatamente como está no arquivo e a chamada falhará se isso violar as \_ \_ funcionalidades do dispositivo.

</dd> <dt>

*Pool* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Membro do tipo [**enumerado D3DPOOL,**](./d3dpool.md) descrevendo a classe de memória na qual a textura deve ser colocada.

</dd> <dt>

*Filtro* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Uma combinação de uma ou mais constantes [D3DX \_ FILTER](d3dx-filter.md) controlando como a imagem é filtrada. Especificar [D3DX \_ DEFAULT](other-d3dx-constants.md) para esse parâmetro é o equivalente a especificar D3DX \_ FILTER TRIANGLE \_ \| D3DX \_ FILTER \_ DITHER.

</dd> <dt>

*MipFilter* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Uma combinação de uma ou mais constantes [D3DX \_ FILTER](d3dx-filter.md) controlando como a imagem é filtrada. Especificar D3DX \_ DEFAULT para esse parâmetro é o equivalente a especificar D3DX \_ FILTER \_ BOX. Além disso, use bits 27-31 para especificar o número de níveis de mip a serem ignorados (da parte superior da cadeia mipmap) quando uma textura .dds for carregada na memória; isso permite que você ignore até 32 níveis.

</dd> <dt>

*ColorKey* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

[**Valor D3DCOLOR**](d3dcolor.md) a ser substituído por preto transparente ou 0 para desabilitar a chave de cor. Essa é sempre uma cor ARGB de 32 bits, independentemente do formato de imagem de origem. Alfa é significativo e geralmente deve ser definido como FF para chaves de cores opacas. Portanto, para preto opaco, o valor seria igual a 0xFF000000.

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

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Endereço de um ponteiro para uma interface [**IDirect3DTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa o objeto de textura criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

A configuração do compilador também determina a versão da função. Se Unicode for definido, a chamada de função será resolvida para D3DXCreateTextureFromFileExW. Caso contrário, a chamada de função será resolvida para D3DXCreateTextureFromFileExA porque as cadeias de caracteres ANSI estão sendo usadas.

Use [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) para determinar se o dispositivo pode dar suporte à textura considerando o estado atual.

Essa função dá suporte aos seguintes formatos de arquivo: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm e .tga. Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

As texturas mapeadas automaticamente têm cada nível preenchido com a textura carregada. Ao carregar imagens em texturas com mipmapped, alguns dispositivos não podem ir para uma imagem 1x1 e essa função falhará. Se isso acontecer, as imagens precisarão ser carregadas manualmente.

Para ter o melhor desempenho ao usar **D3DXCreateTextureFromFileEx:**

1.  Fazer a conversão de formato e dimensionamento de imagem em tempo de carregamento pode ser lento. Armazene imagens no formato e na resolução que serão usadas. Se o hardware de destino exigir potência de duas dimensões, crie e armazene imagens usando a potência de duas dimensões.
2.  Para a criação de imagem mipmap em tempo de carregamento, filtre usando [D3DX \_ FILTER \_ BOX](d3dx-filter.md). Um filtro de caixa é muito mais rápido do que outros tipos de filtro, como D3DX \_ FILTER \_ TRIANGLE.
3.  Considere o uso de arquivos DDS. Como os arquivos DDS podem ser usados para representar qualquer formato de textura direct3D 9, eles são muito fáceis de ler para o D3DX. Além disso, eles podem armazenar mipmaps, de modo que qualquer algoritmo de geração de mipmap possa ser usado para a autor das imagens.

Ao ignorar níveis de mipmap ao carregar um arquivo .dds, use a macro D3DX SKIP DDS MIP LEVELS para gerar o \_ \_ valor \_ \_ MipFilter. Essa macro leva o número de níveis a ignorar e o tipo de filtro e retorna o valor do filtro, que seria passado para o parâmetro MipFilter.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)
</dt> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
