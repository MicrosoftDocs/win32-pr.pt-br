---
description: Cria uma textura de cubo de um recurso especificado por uma cadeia de caracteres. Essa é uma função mais avançada do que D3DXCreateCubeTextureFromResource.
ms.assetid: 4d263386-8270-4967-8ef5-e9ac69e502a5
title: Função D3DXCreateCubeTextureFromResourceEx (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8548863f7c35ff3d56fd83287cf1c3628bb1a9ff89d8ad34346530063c494c99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857296"
---
# <a name="d3dxcreatecubetexturefromresourceex-function"></a>Função D3DXCreateCubeTextureFromResourceEx

Cria uma textura de cubo de um recurso especificado por uma cadeia de caracteres. Essa é uma função mais avançada do [**que D3DXCreateCubeTextureFromResource**](d3dxcreatecubetexturefromresource.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateCubeTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9      pDevice,
  _In_    HMODULE                hSrcModule,
  _In_    LPCTSTR                pSrcResource,
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

*pDevice* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa o dispositivo a ser associado à textura do cubo.

</dd> <dt>

*hSrcModule* \[ Em\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Manipular para o módulo em que o recurso está localizado ou **NULL** para o módulo associado à imagem que o sistema operacional usou para criar o processo atual.

</dd> <dt>

*pSrcResource* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Ponteiro para uma cadeia de caracteres que especifica o nome do recurso. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados de cadeia de caracteres será resolvido para LPCSTR. Consulte Observações.

</dd> <dt>

*Tamanho* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Largura e altura da textura do cubo, em pixels. Por exemplo, se a textura do cubo for um cubo de 8 pixels por 8 pixels, o valor desse parâmetro deverá ser 8. Se esse valor for 0 ou D3DX \_ DEFAULT, as dimensões serão retiradas do arquivo.

</dd> <dt>

*MipLevels* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de níveis de mip solicitados. Se esse valor for zero ou D3DX \_ DEFAULT, uma cadeia de mipmap completa será criada.

</dd> <dt>

*Uso* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0 ou D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ DYNAMIC. Definir esse sinalizador como D3DUSAGE RENDERTARGET indica que a superfície \_ deve ser usada como um destino de renderização. O recurso pode ser passado para o parâmetro *pNewRenderTarget* do [**método SetRenderTarget.**](/windows/desktop/api) Se D3DUSAGE RENDERTARGET for especificado, o aplicativo deverá verificar se o dispositivo dá suporte a essa operação chamando \_ [**CheckDeviceFormat**](/windows/desktop/api). D3DUSAGE \_ DYNAMIC indica que a superfície deve ser tratada dinamicamente. Para obter mais informações sobre como usar texturas dinâmicas, consulte [Usando texturas dinâmicas.](performance-optimizations.md)

</dd> <dt>

*Formato* \[ Em\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Membro do tipo [enumerado D3DFORMAT,](d3dformat.md) descrevendo o formato de pixel solicitado para a textura do cubo. A textura do cubo retornada pode ter um formato diferente do especificado por *Formatar*. Os aplicativos devem verificar o formato da textura do cubo retornada. Se [D3DFMT \_ UNKNOWN](other-d3dx-constants.md), o formato será retirado do arquivo. Se D3DFMT FROM FILE, o formato será feito exatamente como está no arquivo e a chamada falhará se isso violar as \_ \_ funcionalidades do dispositivo.

</dd> <dt>

*Pool* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Membro do tipo [**enumerado D3DPOOL,**](./d3dpool.md) que descreve a classe de memória na qual a textura do cubo deve ser colocada.

</dd> <dt>

*Filtro* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Uma combinação de um ou mais [FILTRO D3DX \_ ](d3dx-filter.md), controlando como a imagem é filtrada. Especificar D3DX DEFAULT para esse parâmetro é o equivalente a especificar \_ D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER.

</dd> <dt>

*MipFilter* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Uma combinação de um ou mais [FILTRO D3DX \_ controlando](d3dx-filter.md) como a imagem é filtrada. Especificar D3DX \_ DEFAULT para esse parâmetro é o equivalente a especificar D3DX \_ FILTER \_ BOX.

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

Ponteiro para uma [**estrutura PALETTEENTRY,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que representa uma paleta de 256 cores para preencher ou **NULL.**

</dd> <dt>

*ppCubeTexture* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***

Endereço de um ponteiro para uma interface [**IDirect3DCubeTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) que representa o objeto de textura do cubo criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

A configuração do compilador determina a versão da função. Se Unicode for definido, a chamada de função será resolvida para **D3DXCreateCubeTextureFromResourceExW.** Caso contrário, a chamada de função será resolvida para **D3DXCreateCubeTextureFromResourceExA** porque as cadeias de caracteres ANSI estão sendo usadas.

Essa função dá suporte aos seguintes formatos de arquivo: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm e .tga. Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Texturas de cubo diferem de outras superfícies, já que são coleções de superfícies. Para chamar [**SetRenderTarget com**](/windows/desktop/api) uma textura de cubo, você deve selecionar um rosto individual usando [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) e passar a superfície resultante para **SetRenderTarget**.

**D3DXCreateCubeTextureFromResourceEx** usa o formato de arquivo DDS (DirectDraw Surface). O Editor de Textura directX (Dxtex.exe) permite que você gere um mapa de cubo de outros formatos de arquivo e salve-o no formato de arquivo DDS. Você pode obter Dxtex.exe e saber mais sobre ele no SDK do DirectX. Para obter informações sobre o SDK do DirectX, consulte [Onde está o SDK do DirectX?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3DXCreateCubeTextureFromResource**](d3dxcreatecubetexturefromresource.md)
</dt> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
