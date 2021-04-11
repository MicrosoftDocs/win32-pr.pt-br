---
description: Reamostrar uma textura na parametrização desta gutterhelper.
ms.assetid: a5ace0e4-2e89-471b-bdfb-67d5e85c6f46
title: 'Método ID3DXTextureGutterHelper:: ResampleTex (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ResampleTex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ad8b4cefe0b368cbf81de4ddc030f32cda8fb17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173120"
---
# <a name="id3dxtexturegutterhelperresampletex-method"></a>Método ID3DXTextureGutterHelper:: ResampleTex

Reamostrar uma textura na parametrização desta gutterhelper.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ResampleTex(
  [in]  LPDIRECT3DTEXTURE9 pTextureIn,
  [in]  LPD3DXMESH         pMeshIn,
  [in]  D3DDECLUSAGE       Usage,
  [in]  UINT               UsageIndex,
  [out] LPDIRECT3DTEXTURE9 pTextureOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTextureIn* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Textura que corresponde à parametrização original em pMeshIn. Essa textura será usada para criar pTextureOut.

</dd> <dt>

*pMeshIn* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Malha que contém o parametrizações original e o novo. É necessário armazenar a nova parametrização no \_ índice 0 do D3DDECLUSAGE TEXCOORD.

</dd> <dt>

*Uso* \[ do no\]
</dt> <dd>

Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Uso de dados de vértice (usado em combinação com UsageIndex) que identifica o componente da declaração de vértice que contém a parametrização original em pMeshIn. Consulte [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*UsageIndex* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice baseado em zero (usado em combinação com o uso), que identifica o componente da declaração de vértice que contém a parametrização original em pMeshIn. A combinação de D3DDECLUSAGE \_ TEXCOORD e índice 0 é necessária para a nova parametrização; qualquer outra combinação de uso/índice pode ser usada.

</dd> <dt>

*pTextureOut* \[ fora\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Textura reamostrada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Uma parametrização no caso dessa função é um conjunto de coordenadas de textura que mapeia os triângulos de uma malha para os triângulos em uma textura. A nova parametrização é o conjunto de coordenadas de textura contidas na interface auxiliar da medianiz, e a parametrização original é o conjunto de coordenadas de textura contidas na malha de entrada.

Supõe-se que as coordenadas de textura estão entre 0 e 1, inclusive, e a nova parametrização deve ser declarada na declaração de vértice como índice de coordenadas de textura 0. A textura original e a textura reamostrada devem ter a mesma largura e altura.

Por exemplo, para se preparar para reamostrar uma textura:

-   Crie a interface de textura original (pOriginalTex abaixo) usando uma função como [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).
-   Crie a nova interface de textura para a textura reamostrada (pResampledTex abaixo). O tamanho dessa textura deve corresponder ao tamanho (largura e altura) da textura auxiliar da medianiz.
-   Chame [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) para obter a nova parametrização, conforme mostrado aqui:


```
// Given:
// pMesh points to a mesh that contains the original and new texture coordinates
ID3DXTextureGutterHelper * pGutterHelper;
    
// Mesh vertex declaration
D3DVERTEXELEMENT9 decl[] = {
    {0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0},
    // contains new set of texcoords
    {0, 24, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0}, 
    // contains original set of texcoords
    {0, 32, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1}, 
    D3DDECL_END()
};
    
// Create a gutter helper with the new parameterization
hr = D3DXCreateTextureGutterHelper(width, height, pMesh, 1, &pGutterHelper);  
    
// Resample the texture
hr = pGutterHelper->ResampleTex(pOriginalTex, pMesh, D3DDECLUSAGE_TEXCOORD, 
           1, pResampledTex); 
    
// Release the gutter helper interface when done with it
```



Um cenário comum pode ser usar UVAtlas para criar um Atlas de textura e, em seguida, usar ResampleTex para reamostrar a textura na nova parametrização. Para obter mais informações sobre os atlass, consulte [usando o UVAtlas (Direct3D 9)](using-uvatlas.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> <dt>

[**D3DXUVAtlasCreate**](d3dxuvatlascreate.md)
</dt> </dl>

 

 
