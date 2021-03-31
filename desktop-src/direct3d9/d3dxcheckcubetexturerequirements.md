---
description: Verifica os parâmetros de criação de textura de cubo.
ms.assetid: 56ced947-1142-4d05-95e3-ca6a26b147d4
title: Função D3DXCheckCubeTextureRequirements (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckCubeTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f800617920c5d79361b5e6da291fd88b5b963b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664106"
---
# <a name="d3dxcheckcubetexturerequirements-function"></a>Função D3DXCheckCubeTextureRequirements

Verifica os parâmetros de criação de textura de cubo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCheckCubeTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pSize,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura do cubo.

</dd> <dt>

*psize* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Ponteiro para a largura e a altura solicitadas em pixels, ou **NULL**. Retorna o tamanho corrigido.

</dd> <dt>

*pNumMipLevels* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Aponta para o número de níveis de mipmap solicitados ou **NULL**. Retorna o número corrigido de níveis de mipmap.

</dd> <dt>

*Uso* \[ do no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0 ou D3DUSAGE \_ RENDERTARGET. Definir esse sinalizador como D3DUSAGE \_ RENDERTARGET indica que a superfície deve ser usada como um destino de renderização. O recurso pode então ser passado para o parâmetro pNewRenderTarget do método [**SetRenderTarget**](/windows/desktop/api) . Se D3DUSAGE \_ RENDERTARGET for especificado, o aplicativo deverá verificar se o dispositivo dá suporte a essa operação [**chamando CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).

</dd> <dt>

*pFormat* \[ entrada, saída\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)\***

Ponteiro para um membro do tipo enumerado [D3DFORMAT](d3dformat.md) . Especifica o formato de pixel desejado ou **nulo**. Retorna o formato corrigido.

</dd> <dt>

*Pool* \[ de no\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , que descreve a classe de memória na qual a textura deve ser colocada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ não disponível, D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Se os parâmetros para essa função forem inválidos, essa função retornará parâmetros corrigidos.

Texturas de cubos diferem de outras superfícies em que são coleções de superfícies. Para chamar [**SetRenderTarget**](/windows/desktop/api) com uma textura de cubo, você deve selecionar uma face individual usando [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) e passar a superfície resultante para **SetRenderTarget**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
