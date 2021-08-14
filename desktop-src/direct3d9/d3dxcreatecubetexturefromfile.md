---
description: Cria uma textura de cubo de um arquivo.
ms.assetid: 7ff3b051-568c-4c77-b8a6-b626ba156eb1
title: Função D3DXCreateCubeTextureFromFile (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e25b6692fc22eed1695b1d60b019a595826de15af87e4ca70f2610a621abc532
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279886"
---
# <a name="d3dxcreatecubetexturefromfile-function"></a>Função D3DXCreateCubeTextureFromFile

Cria uma textura de cubo de um arquivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateCubeTextureFromFile(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCTSTR                pSrcFile,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa o dispositivo a ser associado à textura do cubo.

</dd> <dt>

*pSrcFile* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados de cadeia de caracteres será resolvido para LPCSTR. Consulte Observações.

</dd> <dt>

*ppCubeTexture* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***

Endereço de um ponteiro para uma interface [**IDirect3DCubeTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) que representa o objeto de textura do cubo criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

A configuração do compilador também determina a versão da função. Se Unicode for definido, a chamada de função será resolvida para **D3DXCreateCubeTextureFromFileW.** Caso contrário, a chamada de função será resolvida para **D3DXCreateCubeTextureFromFileA** porque as cadeias de caracteres ANSI estão sendo usadas.

A função é equivalente a D3DXCreateCubeTextureFromFileEx(pDevice, pSrcFile, D3DX \_ DEFAULT, D3DX \_ DEFAULT, 0, D3DFMT \_ UNKNOWN, D3DPOOL \_ MANAGED, D3DX \_ DEFAULT, D3DX \_ DEFAULT, 0, **NULL,** **NULL**, ppCubeTexture).

Essa função dá suporte aos seguintes formatos de arquivo: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm e .tga. Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Observe que um recurso criado com essa função quando chamado de um objeto IDirect3DDevice9 será colocado na classe de memória anotada por D3DPOOL \_ MANAGED. Quando esse método é chamado de um objeto IDirect3DDevice9Ex, o recurso será colocado na classe de memória anotada por D3DPOOL \_ DEFAULT.

A filtragem é aplicada automaticamente a uma textura criada usando esse método. A filtragem é equivalente a D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER em [D3DX \_ FILTER](d3dx-filter.md).

**D3DXCreateCubeTextureFromFile** usa o formato de arquivo DDS (superfície DirectDraw). O Editor de Textura do DirectX (Dxtex.exe) permite que você gere um mapa de cubo de outros formatos de arquivo e salve-o no formato de arquivo DDS. Você pode obter Dxtex.exe e saber mais sobre ele no SDK do DirectX. Para obter informações sobre o SDK do DirectX, consulte [Onde está o SDK do DirectX?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3DXCreateCubeTextureFromFileEx**](d3dxcreatecubetexturefromfileex.md)
</dt> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
