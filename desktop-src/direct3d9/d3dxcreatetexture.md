---
description: Cria uma textura vazia, ajustando os parâmetros de chamada conforme necessário.
ms.assetid: ea028aa9-4f37-4625-9e07-9072ec1a61d0
title: Função D3DXCreateTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ecbd5cbb94355af9c1e51e6c7e8fc31a862b03be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506482"
---
# <a name="d3dxcreatetexture-function"></a>Função D3DXCreateTexture

Cria uma textura vazia, ajustando os parâmetros de chamada conforme necessário.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateTexture(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  UINT               Width,
  _In_  UINT               Height,
  _In_  UINT               MipLevels,
  _In_  DWORD              Usage,
  _In_  D3DFORMAT          Format,
  _In_  D3DPOOL            Pool,
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

*Largura* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Largura em pixels. Se esse valor for 0, será usado um valor de 1. Consulte Observações.

</dd> <dt>

*Altura* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Altura em pixels. Se esse valor for 0, será usado um valor de 1. Consulte Observações.

</dd> <dt>

*MipLevels* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de níveis de MIP solicitados. Se esse valor for zero ou D3DX \_ padrão, uma cadeia de mipmap completa será criada.

</dd> <dt>

*Uso* \[ do no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0, [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)ou **D3DUSAGE \_ Dynamic**. Definir esse sinalizador como **D3DUSAGE \_ RENDERTARGET** indica que a superfície deve ser usada como um destino de renderização chamando o método [**SetRenderTarget**](/windows/desktop/api) . Se **D3DUSAGE \_ RENDERTARGET** ou **D3DUSAGE \_ Dynamic** for especificado, o aplicativo deverá verificar se o dispositivo dá suporte a essa operação chamando [**CheckDeviceFormat**](/windows/desktop/api). Para obter mais informações sobre como usar texturas dinâmicas, consulte [usando texturas dinâmicas](performance-optimizations.md).

</dd> <dt>

*Formato* \[ no\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato de pixel solicitado para a textura. A textura retornada pode ser de um formato diferente daquele especificado, se o dispositivo não oferecer suporte ao formato solicitado. Os aplicativos devem verificar o formato da textura retornada para ver se ele corresponde ao formato solicitado.

</dd> <dt>

*Pool* \[ de no\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , que descreve a classe de memória na qual a textura deve ser colocada.

</dd> <dt>

*ppTexture* \[ fora\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Endereço de um ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , que representa o objeto de textura criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DERR \_ não disponível, D3DERR \_ OUTOFVIDEOMEMORY, e \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Internamente, o D3DXCreateTexture usa [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) para ajustar os parâmetros de chamada. Portanto, as chamadas para D3DXCreateTexture geralmente terão êxito onde as chamadas para [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) falharão.

Se a altura e a largura forem definidas como [D3DX \_ padrão](other-d3dx-constants.md), um valor de 256 será usado para ambos os parâmetros. Se a altura ou a largura for definida como D3DX \_ padrão e o outro parâmetro for definido como um valor numérico, a textura será quadrada com a altura e a largura iguais ao valor numérico.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
