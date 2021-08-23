---
description: Cria uma textura de cubo a partir de um arquivo na memória.
ms.assetid: f7e99d5a-5479-4f0b-b040-bb07e7e37666
title: Função D3DXCreateCubeTextureFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8c39e3aa96445ddfd6e2aee9df90c16bf52aee6f70759eb310288276ff8b9531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631546"
---
# <a name="d3dxcreatecubetexturefromfileinmemory-function"></a>Função D3DXCreateCubeTextureFromFileInMemory

Cria uma textura de cubo a partir de um arquivo na memória.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateCubeTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  UINT                   SrcDataSize,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
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

Ponteiro para o arquivo na memória a partir da qual criar o cubemap. Consulte Observações.

</dd> <dt>

*SrcDataSize* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Tamanho do arquivo na memória, em bytes.

</dd> <dt>

*ppCubeTexture* \[ fora\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***

Endereço de um ponteiro para uma interface [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , que representa o objeto de textura do cubo criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DERR \_ não disponível, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, e \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Essa função dá suporte aos seguintes formatos de arquivo: .bmp,. DDS,. dib,. HDR, .jpg,. PFM, .png,. ppm e. tga. Consulte [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).

A função é equivalente a D3DXCreateCubeTextureFromFileInMemoryEx (pDevice, pSrcData, SrcDataSize, D3DX \_ padrão, D3DX \_ padrão, 0, D3DFMT \_ Unknown, D3DPOOL \_ gerenciado, D3DX \_ padrão, D3DX \_ Default, 0, **NULL**, **NULL**, ppCubeTexture).

Observe que um recurso criado com essa função quando chamado de um objeto IDirect3DDevice9 será colocado na classe de memória denotada por D3DPOOL \_ gerenciado. Quando esse método é chamado de um objeto IDirect3DDevice9Ex, o recurso será colocado na classe de memória denotada por D3DPOOL \_ padrão.

Esse método foi projetado para ser usado para carregar arquivos de imagem armazenados como RT \_ RCDATA, que é um recurso definido pelo aplicativo (dados brutos). Caso contrário, esse método falhará.

A filtragem é aplicada automaticamente a uma textura criada usando esse método. A filtragem é equivalente ao D3DX \_ Filter \_ triângulo \| D3DX \_ Filter \_ pontilhado [no \_ filtro D3DX](d3dx-filter.md).

**D3DXCreateCubeTextureFromFileInMemory** usa o formato de arquivo de superfície do DIRECTDRAW (DDS). O editor de textura DirectX (Dxtex.exe) permite que você gere um mapa de cubo de outros formatos de arquivo e salve-o no formato de arquivo DDS. Você pode obter Dxtex.exe e aprender sobre ele no SDK do DirectX. Para obter informações sobre o SDK do DirectX, consulte [onde está o SDK do DirectX?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
