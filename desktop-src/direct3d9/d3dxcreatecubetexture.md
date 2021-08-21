---
description: Cria uma textura de cubo vazia, ajustando os parâmetros de chamada conforme necessário.
ms.assetid: 96cf3fc1-9efc-4b97-a082-2956386145c7
title: Função D3DXCreateCubeTexture (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 86518a98f9ac78c4c6410d6ff5aa76640dbd04c0d5e50158e4432b7fa5ab79ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045194"
---
# <a name="d3dxcreatecubetexture-function"></a>Função D3DXCreateCubeTexture

Cria uma textura de cubo vazia, ajustando os parâmetros de chamada conforme necessário.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateCubeTexture(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  UINT                   Size,
  _In_  UINT                   MipLevels,
  _In_  DWORD                  Usage,
  _In_  D3DFORMAT              Format,
  _In_  D3DPOOL                Pool,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa o dispositivo a ser associado à textura.

</dd> <dt>

*Tamanho* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Largura e altura da textura do cubo, em pixels. Por exemplo, se a textura do cubo for um cubo de 8 pixels por 8 pixels, o valor desse parâmetro deverá ser 8.

</dd> <dt>

*MipLevels* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de níveis de mip solicitados. Se esse valor for zero ou D3DX \_ DEFAULT, uma cadeia de mipmap completa será criada.

</dd> <dt>

*Uso* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0, D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ DYNAMIC. Definir esse sinalizador como D3DUSAGE RENDERTARGET indica que a superfície \_ deve ser usada como um destino de renderização. O recurso pode ser passado para o parâmetro *pNewRenderTarget* do [**método SetRenderTarget.**](/windows/desktop/api) Se D3DUSAGE RENDERTARGET for especificado, o aplicativo deverá verificar se o dispositivo dá suporte a essa operação chamando \_ [**CheckDeviceFormat**](/windows/desktop/api). Para obter mais informações sobre como usar texturas dinâmicas, consulte [Usando texturas dinâmicas.](performance-optimizations.md)

</dd> <dt>

*Formato* \[ Em\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Membro do tipo [enumerado D3DFORMAT,](d3dformat.md) descrevendo o formato de pixel solicitado para a textura do cubo. A textura do cubo retornada pode ter um formato diferente do especificado por *Formatar*. Os aplicativos devem verificar o formato da textura do cubo retornada.

</dd> <dt>

*Pool* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Membro do tipo [**enumerado D3DPOOL,**](./d3dpool.md) que descreve a classe de memória na qual a textura do cubo deve ser colocada.

</dd> <dt>

*ppCubeTexture* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***

Endereço de um ponteiro para uma interface [**IDirect3DCubeTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) que representa o objeto de textura do cubo criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Texturas de cubo diferem de outras superfícies, já que são coleções de superfícies.

Internamente, D3DXCreateCubeTexture usa [**D3DXCheckCubeTextureRequirements**](d3dxcheckcubetexturerequirements.md) para ajustar os parâmetros de chamada. Portanto, as chamadas para D3DXCreateCubeTexture geralmente terão êxito em que as chamadas para [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) falhariam.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
