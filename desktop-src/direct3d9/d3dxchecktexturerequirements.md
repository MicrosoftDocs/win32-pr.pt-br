---
description: Verifica os parâmetros de criação de textura.
ms.assetid: f8e788f3-02a9-4ee7-b74d-9e781a2fb39f
title: Função D3DXCheckTextureRequirements (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d4fdc0998bfda2144e900c099919bc75c01e8ee3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173046"
---
# <a name="d3dxchecktexturerequirements-function"></a>Função D3DXCheckTextureRequirements

Verifica os parâmetros de criação de textura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCheckTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pWidth,
  _Inout_ UINT              *pHeight,
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

Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura.

</dd> <dt>

*pWidth* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Ponteiro para a largura solicitada em pixels ou **nulo**. Retorna o tamanho corrigido.

</dd> <dt>

*pHeight* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Ponteiro para a altura solicitada em pixels, ou **NULL**. Retorna o tamanho corrigido.

</dd> <dt>

*pNumMipLevels* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Ponteiro para o número de níveis de mipmap solicitados ou **NULL**. Retorna o número corrigido de níveis de mipmap.

</dd> <dt>

*Uso* \[ do no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0 ou [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md). Definir esse sinalizador como D3DUSAGE \_ RENDERTARGET indica que a superfície deve ser usada como um destino de renderização. O recurso pode então ser passado para o parâmetro pNewRenderTarget do método [**SetRenderTarget**](/windows/desktop/api) . Se **D3DUSAGE \_ RENDERTARGET** for especificado, o aplicativo deverá verificar se o dispositivo dá suporte a essa operação chamando [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).

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

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DERR \_ não disponível.

## <a name="remarks"></a>Comentários

Se os parâmetros para essa função forem inválidos, essa função retornará parâmetros corrigidos.

Essa função usa a heurística a seguir ao comparar os requisitos solicitados com os formatos disponíveis:

-   Não escolha um formato que tenha menos canais.
-   Evite formatos [FOURCC](d3dformat.md) e de 24 bits, a menos que solicitado explicitamente.
-   Tente não adicionar novos canais.
-   Tente não alterar o número de bits por canal.
-   Tente evitar a conversão entre tipos de formatos. Por exemplo, evite converter um formato ARGB em um formato de profundidade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
