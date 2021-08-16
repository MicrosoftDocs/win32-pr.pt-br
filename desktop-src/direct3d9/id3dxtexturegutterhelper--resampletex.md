---
description: Resampla uma textura na parametrização desse mediador.
ms.assetid: a5ace0e4-2e89-471b-bdfb-67d5e85c6f46
title: Método ID3DXTextureGutterHelper::ResampleTex (D3DX9Mesh.h)
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
ms.openlocfilehash: f7d3afe8155eb33a37b30abcfc96aae83c0a96461c1ee2dd6118a671701cfed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800315"
---
# <a name="id3dxtexturegutterhelperresampletex-method"></a>Método ID3DXTextureGutterHelper::ResampleTex

Resampla uma textura na parametrização desse mediador.

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

*pTextureIn* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Textura que corresponde à parametrização original em pMeshIn. Essa textura será usada para criar pTextureOut.

</dd> <dt>

*pMeshIn* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Malha que contém as parametrizações originais e novas. É necessário armazenar a nova parametrização no índice 0 de D3DDECLUSAGE \_ TEXCOORD.

</dd> <dt>

*Uso* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Uso de dados de vértice (usado em combinação com UsageIndex) que identifica o componente da declaração de vértice que contém a parametrização original em pMeshIn. Consulte [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*UsageIndex* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice baseado em zero (usado em combinação com Uso), que identifica o componente da declaração de vértice que contém a parametrização original em pMeshIn. A combinação de D3DDECLUSAGE TEXCOORD e o índice 0 é necessária para a nova parametrização; qualquer outra combinação \_ de uso/índice pode ser usada.

</dd> <dt>

*pTextureOut* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Textura resamplada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Uma parametrização no caso dessa função é um conjunto de coordenadas de textura que mapeia os triângulos de uma malha para os triângulos em uma textura. A nova parametrização é o conjunto de coordenadas de textura contidas na interface auxiliar de medianiz e a parametrização original é o conjunto de coordenadas de textura contidas na malha de entrada.

Supõe-se que as coordenadas de textura estão entre 0 e 1, inclusive, e a nova parametrização deve ser declarada na declaração de vértice como índice de coordenada de textura 0. A textura original e a textura resampled devem ter a mesma largura e altura.

Por exemplo, para se preparar para a resampling de uma textura:

-   Crie a interface de textura original (pOriginalTex abaixo) usando uma função como [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).
-   Crie a nova interface de textura para a textura resampled (pResampledTex abaixo). O tamanho dessa textura deve corresponder ao tamanho (largura e altura) da textura auxiliar da media mediana.
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



Um cenário comum pode ser usar UVAtlas para criar um atlas de textura e, em seguida, usar ResampleTex para resampler a textura na nova parametrização. Para obter mais informações sobre atlases, [consulte Usando UVAtlas (Direct3D 9)](using-uvatlas.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> <dt>

[**D3DXUVAtlasCriar**](d3dxuvatlascreate.md)
</dt> </dl>

 

 
