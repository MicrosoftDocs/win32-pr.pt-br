---
description: Cria uma textura a partir de um recurso.
ms.assetid: 7c841f21-5565-4923-a2fe-bbd618616f87
title: Função D3DXCreateTextureFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4ce9101caed2a60dc3be7fe0039a1e391423f1fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837931"
---
# <a name="d3dxcreatetexturefromresource-function"></a>Função D3DXCreateTextureFromResource

Cria uma textura a partir de um recurso.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateTextureFromResource(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  HMODULE            hSrcModule,
  _In_  LPCTSTR            pSrcResource,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura.

</dd> <dt>

*hSrcModule* \[ no\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Manipule o módulo no qual o recurso está localizado ou **nulo** para o módulo associado à imagem que o sistema operacional usou para criar o processo atual.

</dd> <dt>

*pSrcResource* \[ no\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Ponteiro para uma cadeia de caracteres que especifica o nome do recurso. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados String será resolvido para LPCSTR. Consulte Observações.

</dd> <dt>

*ppTexture* \[ fora\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Endereço de um ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , que representa o objeto de textura criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ não disponível, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, e \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

A configuração do compilador também determina a versão da função. Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateTextureFromResourceW. Caso contrário, a chamada de função é resolvida como D3DXCreateTextureFromResourceA porque as cadeias de caracteres ANSI estão sendo usadas.

A função é equivalente a D3DXCreateTextureFromResourceEx (pDevice, hSrcModule, pSrcResource, D3DX \_ padrão, D3DX padrão \_ , D3DX padrão \_ , 0, D3DFMT \_ Unknown, D3DPOOL \_ gerenciado, D3DX \_ padrão, D3DX \_ Default, 0, **NULL**, **null**, ppTexture).

O recurso que está sendo carregado deve ser do tipo \_ bitmap RT ou RT \_ RCDATA. O tipo de recurso RT \_ RCDATA é usado para carregar formatos diferentes de bitmaps (como. tga,. jpg e. DDS).

Essa função dá suporte aos seguintes formatos de arquivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm e. tga. Consulte [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).

Observe que um recurso criado com essa função quando chamado de um objeto IDirect3DDevice9 será colocado na classe de memória denotada por D3DPOOL \_ gerenciado. Quando esse método é chamado de um objeto IDirect3DDevice9Ex, o recurso será colocado na classe de memória denotada por D3DPOOL \_ padrão.

A filtragem é aplicada automaticamente a uma textura criada usando esse método. A filtragem é equivalente ao D3DX \_ Filter \_ triângulo \| D3DX \_ Filter \_ pontilhado [no \_ filtro D3DX](d3dx-filter.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3DXCreateTextureFromResourceEx**](d3dxcreatetexturefromresourceex.md)
</dt> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
