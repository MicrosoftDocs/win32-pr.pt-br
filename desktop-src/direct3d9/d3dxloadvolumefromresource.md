---
description: Carrega um volume de um recurso.
ms.assetid: 3fa1243b-5e31-4737-8d3c-08852d6528d9
title: Função D3DXLoadVolumeFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d57ce492db24ac9920662d4de5baed4650dd801
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105760643"
---
# <a name="d3dxloadvolumefromresource-function"></a>Função D3DXLoadVolumeFromResource

Carrega um volume de um recurso.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXLoadVolumeFromResource(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       HMODULE           hSrcModule,
  _In_       LPCSTR            pSrcResource,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDestVolume* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

Ponteiro para uma interface [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) . Especifica o volume de destino.

</dd> <dt>

*pDestPalette* \[ no\]
</dt> <dd>

Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , a paleta de destino de 256 cores ou **NULL**.

</dd> <dt>

*pDestBox* \[ no\]
</dt> <dd>

Tipo: **const [**D3DBOX**](d3dbox.md) \***

Ponteiro para uma estrutura [**D3DBOX**](d3dbox.md) . Especifica a caixa de destino. Defina esse parâmetro como **NULL** para especificar o volume inteiro.

</dd> <dt>

*hSrcModule* \[ no\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Manipule o módulo no qual o recurso está localizado ou **nulo** para o módulo associado à imagem que o sistema operacional usou para criar o processo atual.

</dd> <dt>

*pSrcResource* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo da imagem de origem. Se UNICODE ou \_ Unicode estiverem definidos, esse tipo de parâmetro será LPCWSTR, caso contrário, o tipo será LPCSTR.

</dd> <dt>

*pSrcBox* \[ no\]
</dt> <dd>

Tipo: **const [**D3DBOX**](d3dbox.md) \***

Ponteiro para uma estrutura [**D3DBOX**](d3dbox.md) . Especifica a caixa de origem. Defina esse parâmetro como **NULL** para especificar o volume inteiro.

</dd> <dt>

*Filtrar* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md), controlando como a imagem é filtrada. A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação de pontilhado de filtro de D3DX de \_ \_ triângulo \| D3DX \_ \_ .

</dd> <dt>

*COLORKEY* \[ no\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

Valor [**D3DCOLOR**](d3dcolor.md) a ser substituído por preto transparente ou 0 para desabilitar o COLORKEY. Essa é sempre uma cor ARGB de 32 bits, independente do formato de imagem de origem. Alfa é significativo e deve geralmente ser definido como FF para chaves de cor opacas. Portanto, para preto opaco, o valor seria igual a 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ no\]
</dt> <dd>

Tipo: **[ **\_ informações de D3DXIMAGE**](d3dximage-info.md)\***

Ponteiro para uma estrutura de [**\_ informações de D3DXIMAGE**](d3dximage-info.md) a ser preenchida com uma descrição dos dados no arquivo de imagem de origem, ou **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

O recurso que está sendo carregado deve ser um recurso de bitmap ( \_ bitmap RT).

Essa função manipula a conversão de e para formatos de textura compactados.

Gravar em uma superfície de não nível zero da textura do volume não fará com que o retângulo sujo seja atualizado. Se [**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md) for chamado e a textura ainda não tiver sido suja (isso é improvável em cenários de uso normal), o aplicativo precisa chamar explicitamente [**IDirect3DVolumeTexture9:: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) na textura do volume.

Essa função dá suporte a cadeias de caracteres Unicode e ANSI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md)
</dt> <dt>

[**D3DXLoadVolumeFromFileInMemory**](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[**D3DXLoadVolumeFromMemory**](d3dxloadvolumefrommemory.md)
</dt> <dt>

[**D3DXLoadVolumeFromVolume**](d3dxloadvolumefromvolume.md)
</dt> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
