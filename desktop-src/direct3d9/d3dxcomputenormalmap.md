---
description: Converte um mapa de altura em um mapa normal. Os componentes (x, y, z) de cada normal são mapeados para os canais (r, g, b) da textura de saída.
ms.assetid: ed9053c0-b1df-4f74-bdee-627c0f60d942
title: Função D3DXComputeNormalMap (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormalMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e22418f5a023dbe70fee8ea0fba8a449abbcc8d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105814444"
---
# <a name="d3dxcomputenormalmap-function"></a>Função D3DXComputeNormalMap

Converte um mapa de altura em um mapa normal. Os componentes (x, y, z) de cada normal são mapeados para os canais (r, g, b) da textura de saída.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXComputeNormalMap(
  _Out_       LPDIRECT3DTEXTURE9 pTexture,
  _In_        LPDIRECT3DTEXTURE9 pSrcTexture,
  _In_  const PALETTEENTRY       *pSrcPalette,
  _In_        DWORD              Flags,
  _In_        DWORD              Channel,
  _In_        FLOAT              Amplitude
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTexture* \[ fora\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , representando a textura de destino.

</dd> <dt>

*pSrcTexture* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , representando a textura de mapa de altura de origem.

</dd> <dt>

*pSrcPalette* \[ no\]
</dt> <dd>

Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Ponteiro para um tipo [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que contém a paleta de origem de 256 cores ou **NULL**.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Um ou mais sinalizadores [D3DX \_ NormalMap](d3dx-normalmap.md) que controlam a geração de mapas normais.

</dd> <dt>

*Canal* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Um sinalizador de [ \_ canal D3DX](d3dx-channel.md) especificando a fonte de informações de altura.

</dd> <dt>

*Amplitude* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Multiplicador de valor constante que aumenta (ou diminui) os valores no mapa normal. Valores mais altos geralmente tornam os choques mais visíveis, os valores mais baixos geralmente tornam os choques menos visíveis.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser o seguinte valor: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Esse método computa o normal usando a diferença central com um tamanho de kernel de 3x3. O denominador diferencial central usado é 2,0. Os canais RGB no destino contêm componentes com tendência (x, y, z) do normal.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
