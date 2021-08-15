---
description: Cria um objeto ID3DXTextureGutterHelper de uma malha de entrada e dados de textura.
ms.assetid: 1696fc3d-5b35-48cc-a79b-c0d4ed44e420
title: Função D3DXCreateTextureGutterHelper (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureGutterHelper
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e62f89911199497abfd905376f272121c6c5a9996ec5685e556453bc378e65e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045134"
---
# <a name="d3dxcreatetexturegutterhelper-function"></a>Função D3DXCreateTextureGutterHelper

Cria um [**objeto ID3DXTextureGutterHelper de**](id3dxtexturegutterhelper.md) uma malha de entrada e dados de textura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateTextureGutterHelper(
  _In_    UINT                      Width,
  _In_    UINT                      Height,
  _In_    LPD3DXMESH                pMesh,
  _In_    FLOAT                     GutterSize,
  _Inout_ LPD3DXTEXTUREGUTTERHELPER *ppBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Largura* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Largura da textura, em pixels.

</dd> <dt>

*Altura* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Altura da textura, em pixels.

</dd> <dt>

*pMesh* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ponteiro para um objeto [**de malha ID3DXMesh**](id3dxmesh.md) de entrada.

</dd> <dt>

*MedianizesSize* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Número de texels pelos quais a textura deve ser super amostrada e criar a região da media mediana. Deve ser pelo menos 1.

</dd> <dt>

*ppBuffer* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)\***

Ponteiro para um [**objeto ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) a ser criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será S \_ OK. Se a função falhar, o valor de retorno poderá ser um destes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Use [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) para transformar uma cena em novas coordenadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de transferência de Radiance pré-comutadas](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
