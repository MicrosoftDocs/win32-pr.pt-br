---
description: Cria uma textura de cubo a partir de um arquivo na memória. Essa é uma função mais avançada do que D3DXCreateCubeTextureFromFileInMemory.
ms.assetid: 598016eb-9ea9-4dca-a297-5708a957da6a
title: Função D3DXCreateCubeTextureFromFileInMemoryEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7813d4532bbde18a5fc7fd7d1d090dc72eccd61f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012160"
---
# <a name="d3dxcreatecubetexturefromfileinmemoryex-function"></a>Função D3DXCreateCubeTextureFromFileInMemoryEx

Cria uma textura de cubo a partir de um arquivo na memória. Essa é uma função mais avançada do que [**D3DXCreateCubeTextureFromFileInMemory**](d3dxcreatecubetexturefromfileinmemory.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateCubeTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9      pDevice,
  _In_    LPCVOID                pSrcData,
  _In_    UINT                   SrcDataSize,
  _In_    UINT                   Size,
  _In_    UINT                   MipLevels,
  _In_    DWORD                  Usage,
  _In_    D3DFORMAT              Format,
  _In_    D3DPOOL                Pool,
  _In_    DWORD                  Filter,
  _In_    DWORD                  MipFilter,
  _In_    D3DCOLOR               ColorKey,
  _Inout_ D3DXIMAGE_INFO         *pSrcInfo,
  _Out_   PALETTEENTRY           *pPalette,
  _Out_   LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura do cubo.

</dd> <dt>

*pSrcData* \[ no\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Ponteiro para o arquivo na memória a partir da qual criar a textura do cubo. Consulte Observações.

</dd> <dt>

*SrcDataSize* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Tamanho do arquivo na memória, em bytes.

</dd> <dt>

*Tamanho* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Largura (ou altura) em pixels. Se esse valor for zero ou D3DX \_ padrão, as dimensões serão obtidas do arquivo.

</dd> <dt>

*MipLevels* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de níveis de MIP solicitados. Se esse valor for zero ou D3DX \_ padrão, uma cadeia de mipmap completa será criada.

</dd> <dt>

*Uso* \[ do no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0, D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ Dynamic. Definir esse sinalizador como D3DUSAGE \_ RENDERTARGET indica que a superfície deve ser usada como um destino de renderização. O recurso pode então ser passado para o parâmetro *pNewRenderTarget* do método [**SetRenderTarget**](/windows/desktop/api) . Se D3DUSAGE \_ RENDERTARGET for especificado, o aplicativo deverá verificar se o dispositivo dá suporte a essa operação [**chamando CheckDeviceFormat**](/windows/desktop/api). Para obter mais informações sobre como usar texturas dinâmicas, consulte [usando texturas dinâmicas](performance-optimizations.md).

</dd> <dt>

*Formato* \[ no\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato de pixel solicitado para a textura do cubo. A textura retornada pode ter um formato diferente daquele especificado pelo *formato*. Os aplicativos devem verificar o formato da textura retornada. Se [D3DFMT \_ desconhecido](other-d3dx-constants.md), o formato será extraído do arquivo. Se D3DFMT \_ do \_ arquivo, o formato será levado exatamente como está no arquivo e a chamada falhará se isso violar os recursos do dispositivo.

</dd> <dt>

*Pool* \[ de no\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , que descreve a classe de memória na qual a textura do cubo deve ser colocada.

</dd> <dt>

*Filtrar* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Uma combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md) controlando como a imagem é filtrada. A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação de pontilhado de filtro de D3DX de \_ \_ triângulo \| D3DX \_ \_ .

</dd> <dt>

*MipFilter* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Uma combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md) controlando como a imagem é filtrada. A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação da \_ caixa de filtro D3DX \_ . Além disso, use o bits 27-31 para especificar o número de níveis MIP a serem ignorados (da parte superior da cadeia mipmap) quando uma textura. DDS for carregada na memória; Isso permite que você pule até 32 níveis.

</dd> <dt>

*COLORKEY* \[ no\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

Valor [**D3DCOLOR**](d3dcolor.md) a ser substituído por preto transparente ou 0 para desabilitar o COLORKEY. Essa é sempre uma cor ARGB de 32 bits, independente do formato de imagem de origem. Alfa é significativo e normalmente deve ser definido como FF para chaves de cor opacas. Portanto, para preto opaco, o valor seria igual a 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **\_ informações de D3DXIMAGE**](d3dximage-info.md)\***

Ponteiro para uma estrutura de [**\_ informações de D3DXIMAGE**](d3dximage-info.md) a ser preenchida com uma descrição dos dados no arquivo de imagem de origem, ou **NULL**.

</dd> <dt>

*pPalette* \[ fora\]
</dt> <dd>

Tipo: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***

Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , representando uma paleta de cor de 256 para preencher ou **NULL**. Consulte Observações.

</dd> <dt>

*ppCubeTexture* \[ fora\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***

Endereço de um ponteiro para uma interface [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , que representa o objeto de textura do cubo criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DERR \_ não disponível, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, e \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Essa função dá suporte aos seguintes formatos de arquivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm e. tga. Consulte [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).

Texturas de cubos diferem de outras superfícies em que são coleções de superfícies. Para chamar [**SetRenderTarget**](/windows/desktop/api) com uma textura de cubo, você deve selecionar uma face individual usando [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) e passar a superfície resultante para **SetRenderTarget** .

Esse método foi projetado para ser usado para carregar arquivos de imagem armazenados como RT \_ RCDATA, que é um recurso definido pelo aplicativo (dados brutos). Caso contrário, esse método falhará.

Para obter detalhes sobre o [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), consulte o SDK da plataforma. Observe que, a partir do DirectX 8,0, o membro peFlags da estrutura **PaletteEntry** não funciona conforme documentado no SDK da plataforma. O membro peFlags agora é o canal alfa para formatos de palettized de 8 bits.

**D3DXCreateCubeTextureFromFileInMemoryEx** usa o formato de arquivo de superfície do DIRECTDRAW (DDS). O editor de textura DirectX (Dxtex.exe) permite que você gere um mapa de cubo de outros formatos de arquivo e salve-o no formato de arquivo DDS. Você pode obter Dxtex.exe e aprender sobre ele no SDK do DirectX. Para obter informações sobre o SDK do DirectX, consulte [onde está o SDK do DirectX?](../directx-sdk--august-2009-.md).

Ao ignorar os níveis de mipmap ao carregar um arquivo. DDS, use a \_ \_ macro D3DX \_ ignorar \_ os níveis de MIP do DDS para gerar o valor de MipFilter. Essa macro usa o número de níveis a serem ignorados e o tipo de filtro e retorna o valor do filtro, que seria passado para o parâmetro MipFilter.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
