---
description: Carrega um volume da memória.
ms.assetid: 9f74fcc0-f935-4466-865b-e798711a1f2f
title: Função D3DXLoadVolumeFromMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d6c3f1bdfe40f19eeb57b4f0d8a38c40a239404
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762389"
---
# <a name="d3dxloadvolumefrommemory-function"></a>Função D3DXLoadVolumeFromMemory

Carrega um volume da memória.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXLoadVolumeFromMemory(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCVOID           pSrcMemory,
  _In_       D3DFORMAT         SrcFormat,
  _In_       UINT              SrcRowPitch,
  _In_       UINT              SrcSlicePitch,
  _In_ const PALETTEENTRY      *pSrcPalette,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDestVolume* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

Ponteiro para uma interface [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) . Especifica o volume de destino, que recebe a imagem.

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

*pSrcMemory* \[ no\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Ponteiro para o canto superior esquerdo do volume de origem na memória.

</dd> <dt>

*SrcFormat* \[ no\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , o formato de pixel do volume de origem.

</dd> <dt>

*SrcRowPitch* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Densidade da imagem de origem, em bytes. Para formatos DXT (formatos de textura compactados), esse número deve representar o tamanho de uma linha de células, em bytes.

</dd> <dt>

*SrcSlicePitch* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Densidade da imagem de origem, em bytes. Para formatos DXT (formatos de textura compactados), esse número deve representar o tamanho de uma fatia de células, em bytes.

</dd> <dt>

*pSrcPalette* \[ no\]
</dt> <dd>

Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , a paleta de origem de 256 cores ou **NULL**.

</dd> <dt>

*pSrcBox* \[ no\]
</dt> <dd>

Tipo: **const [**D3DBOX**](d3dbox.md) \***

Ponteiro para uma estrutura [**D3DBOX**](d3dbox.md) . Especifica a caixa de origem. **NULL** não é um valor válido para este parâmetro.

</dd> <dt>

*Filtrar* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Uma combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md) controlando como a imagem é filtrada. A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação de pontilhado de filtro de D3DX de \_ \_ triângulo \| D3DX \_ \_ .

</dd> <dt>

*COLORKEY* \[ no\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

Valor [**D3DCOLOR**](d3dcolor.md) a ser substituído por preto transparente ou 0 para desabilitar o COLORKEY. Essa é sempre uma cor ARGB de 32 bits, independente do formato de imagem de origem. Alfa é significativo e deve geralmente ser definido como FF para chaves de cor opacas. Portanto, para preto opaco, o valor seria igual a 0xFF000000.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

Gravar em uma superfície de não nível zero da textura do volume não fará com que o retângulo sujo seja atualizado. Se **D3DXLoadVolumeFromMemory** for chamado e a textura ainda não tiver sido suja (isso é improvável em cenários de uso normal), o aplicativo precisa chamar explicitamente [**IDirect3DVolumeTexture9:: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) na textura do volume.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md)
</dt> <dt>

[**D3DXLoadVolumeFromResource**](d3dxloadvolumefromresource.md)
</dt> <dt>

[**D3DXLoadVolumeFromVolume**](d3dxloadvolumefromvolume.md)
</dt> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
