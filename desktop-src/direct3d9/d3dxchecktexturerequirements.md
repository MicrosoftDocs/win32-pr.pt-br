---
description: Verifica os parâmetros de criação de textura.
ms.assetid: f8e788f3-02a9-4ee7-b74d-9e781a2fb39f
title: Função D3DXCheckTextureRequirements (D3dx9tex.h)
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
ms.openlocfilehash: 4c7166f981c0351054a2a6c359127a4ce1959b45a6e71c44db9e2546825bc5f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496096"
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

*pDevice* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa o dispositivo a ser associado à textura.

</dd> <dt>

*pWidth* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Ponteiro para a largura solicitada em pixels ou **NULL.** Retorna o tamanho corrigido.

</dd> <dt>

*pHeight* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Ponteiro para a altura solicitada em pixels ou **NULL.** Retorna o tamanho corrigido.

</dd> <dt>

*pNumMipLevels* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Ponteiro para o número de níveis de mipmap solicitados ou **NULL.** Retorna o número corrigido de níveis de mipmap.

</dd> <dt>

*Uso* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0 ou [**D3DUSAGE \_ RENDERTARGET.**](d3dusage.md) Definir esse sinalizador como D3DUSAGE RENDERTARGET indica que a superfície \_ deve ser usada como um destino de renderização. O recurso pode ser passado para o parâmetro pNewRenderTarget do [**método SetRenderTarget.**](/windows/desktop/api) Se **D3DUSAGE \_ RENDERTARGET** for especificado, o aplicativo deverá verificar se o dispositivo dá suporte a essa operação chamando [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).

</dd> <dt>

*pFormat* \[ in, out\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)\***

Ponteiro para um membro do tipo enumerado [D3DFORMAT.](d3dformat.md) Especifica o formato de pixel desejado ou **NULL.** Retorna o formato corrigido.

</dd> <dt>

*Pool* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Membro do tipo [**enumerado D3DPOOL,**](./d3dpool.md) descrevendo a classe de memória na qual a textura deve ser colocada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE.

## <a name="remarks"></a>Comentários

Se os parâmetros para essa função são inválidos, essa função retorna parâmetros corrigidos.

Essa função usa a seguinte heurística ao comparar os requisitos solicitados em relação aos formatos disponíveis:

-   Não escolha um formato que tenha menos canais.
-   Evite [formatos FOURCC](d3dformat.md) e de 24 bits, a menos que explicitamente solicitado.
-   Tente não adicionar novos canais.
-   Tente não alterar o número de bits por canal.
-   Tente evitar a conversão entre tipos de formatos. Por exemplo, evite converter um formato ARGB em um formato de profundidade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
