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
# <a name="id3dxtexturegutterhelperresampletex-method"></a><span data-ttu-id="0543b-103">Método ID3DXTextureGutterHelper:: ResampleTex</span><span class="sxs-lookup"><span data-stu-id="0543b-103">ID3DXTextureGutterHelper::ResampleTex method</span></span>

<span data-ttu-id="0543b-104">Reamostrar uma textura na parametrização desta gutterhelper.</span><span class="sxs-lookup"><span data-stu-id="0543b-104">Resamples a texture into this gutterhelper's parameterization.</span></span>

## <a name="syntax"></a><span data-ttu-id="0543b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0543b-105">Syntax</span></span>


```C++
HRESULT ResampleTex(
  [in]  LPDIRECT3DTEXTURE9 pTextureIn,
  [in]  LPD3DXMESH         pMeshIn,
  [in]  D3DDECLUSAGE       Usage,
  [in]  UINT               UsageIndex,
  [out] LPDIRECT3DTEXTURE9 pTextureOut
);
```



## <a name="parameters"></a><span data-ttu-id="0543b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0543b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0543b-107">*pTextureIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0543b-107">*pTextureIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0543b-108">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="0543b-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="0543b-109">Textura que corresponde à parametrização original em pMeshIn.</span><span class="sxs-lookup"><span data-stu-id="0543b-109">Texture that corresponds to the original parameterization in pMeshIn.</span></span> <span data-ttu-id="0543b-110">Essa textura será usada para criar pTextureOut.</span><span class="sxs-lookup"><span data-stu-id="0543b-110">This texture will be used to create pTextureOut.</span></span>

</dd> <dt>

<span data-ttu-id="0543b-111">*pMeshIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0543b-111">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0543b-112">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="0543b-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="0543b-113">Malha que contém o parametrizações original e o novo.</span><span class="sxs-lookup"><span data-stu-id="0543b-113">Mesh containing the original and new parameterizations.</span></span> <span data-ttu-id="0543b-114">É necessário armazenar a nova parametrização no \_ índice 0 do D3DDECLUSAGE TEXCOORD.</span><span class="sxs-lookup"><span data-stu-id="0543b-114">It is required to store the new parameterization in D3DDECLUSAGE\_TEXCOORD index 0.</span></span>

</dd> <dt>

<span data-ttu-id="0543b-115">*Uso* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="0543b-115">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0543b-116">Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="0543b-116">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="0543b-117">Uso de dados de vértice (usado em combinação com UsageIndex) que identifica o componente da declaração de vértice que contém a parametrização original em pMeshIn.</span><span class="sxs-lookup"><span data-stu-id="0543b-117">Vertex data usage (used in combination with UsageIndex) which identifies the component of the vertex declaration that contains the original parameterization in pMeshIn.</span></span> <span data-ttu-id="0543b-118">Consulte [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="0543b-118">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="0543b-119">*UsageIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0543b-119">*UsageIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0543b-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0543b-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0543b-121">Índice baseado em zero (usado em combinação com o uso), que identifica o componente da declaração de vértice que contém a parametrização original em pMeshIn.</span><span class="sxs-lookup"><span data-stu-id="0543b-121">Zero-based index (used in combination with Usage), which identifies the component of the vertex declaration that contains the original parameterization in pMeshIn.</span></span> <span data-ttu-id="0543b-122">A combinação de D3DDECLUSAGE \_ TEXCOORD e índice 0 é necessária para a nova parametrização; qualquer outra combinação de uso/índice pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="0543b-122">The combination of D3DDECLUSAGE\_TEXCOORD and index 0 is required for the new parameterization; any other usage/index combination may be used.</span></span>

</dd> <dt>

<span data-ttu-id="0543b-123">*pTextureOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0543b-123">*pTextureOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0543b-124">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="0543b-124">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="0543b-125">Textura reamostrada.</span><span class="sxs-lookup"><span data-stu-id="0543b-125">Resampled texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0543b-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0543b-126">Return value</span></span>

<span data-ttu-id="0543b-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0543b-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0543b-128">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0543b-128">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0543b-129">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0543b-129">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0543b-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="0543b-130">Remarks</span></span>

<span data-ttu-id="0543b-131">Uma parametrização no caso dessa função é um conjunto de coordenadas de textura que mapeia os triângulos de uma malha para os triângulos em uma textura.</span><span class="sxs-lookup"><span data-stu-id="0543b-131">A parameterization in the case of this function is a set of texture coordinates that maps the triangles of a mesh to the triangles on a texture.</span></span> <span data-ttu-id="0543b-132">A nova parametrização é o conjunto de coordenadas de textura contidas na interface auxiliar da medianiz, e a parametrização original é o conjunto de coordenadas de textura contidas na malha de entrada.</span><span class="sxs-lookup"><span data-stu-id="0543b-132">The new parameterization is the set of texture coordinates contained in the gutter helper interface, and the original parameterization is the set of texture coordinates contained within the input mesh.</span></span>

<span data-ttu-id="0543b-133">Supõe-se que as coordenadas de textura estão entre 0 e 1, inclusive, e a nova parametrização deve ser declarada na declaração de vértice como índice de coordenadas de textura 0.</span><span class="sxs-lookup"><span data-stu-id="0543b-133">It is assumed that texture coordinates are between 0 and 1, inclusive, and the new parameterization must be declared in the vertex declaration as texture coordinate index 0.</span></span> <span data-ttu-id="0543b-134">A textura original e a textura reamostrada devem ter a mesma largura e altura.</span><span class="sxs-lookup"><span data-stu-id="0543b-134">The original texture and the resampled texture must have the same width and height.</span></span>

<span data-ttu-id="0543b-135">Por exemplo, para se preparar para reamostrar uma textura:</span><span class="sxs-lookup"><span data-stu-id="0543b-135">For example, to prepare for resampling a texture:</span></span>

-   <span data-ttu-id="0543b-136">Crie a interface de textura original (pOriginalTex abaixo) usando uma função como [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span><span class="sxs-lookup"><span data-stu-id="0543b-136">Create the original texture interface (pOriginalTex below) using a function like [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span></span>
-   <span data-ttu-id="0543b-137">Crie a nova interface de textura para a textura reamostrada (pResampledTex abaixo).</span><span class="sxs-lookup"><span data-stu-id="0543b-137">Create the new texture interface for the resampled texture (pResampledTex below).</span></span> <span data-ttu-id="0543b-138">O tamanho dessa textura deve corresponder ao tamanho (largura e altura) da textura auxiliar da medianiz.</span><span class="sxs-lookup"><span data-stu-id="0543b-138">The size of this texture must match the size (width and height) of the gutter helper texture.</span></span>
-   <span data-ttu-id="0543b-139">Chame [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) para obter a nova parametrização, conforme mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="0543b-139">Call [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) to obtain the new parameterization as shown here:</span></span>


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



<span data-ttu-id="0543b-140">Um cenário comum pode ser usar UVAtlas para criar um Atlas de textura e, em seguida, usar ResampleTex para reamostrar a textura na nova parametrização.</span><span class="sxs-lookup"><span data-stu-id="0543b-140">One common scenario might be to use UVAtlas to create a texture atlas and then use ResampleTex to resample the texture into the new parameterization.</span></span> <span data-ttu-id="0543b-141">Para obter mais informações sobre os atlass, consulte [usando o UVAtlas (Direct3D 9)](using-uvatlas.md).</span><span class="sxs-lookup"><span data-stu-id="0543b-141">For more information about atlases, see [Using UVAtlas (Direct3D 9)](using-uvatlas.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0543b-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0543b-142">Requirements</span></span>



| <span data-ttu-id="0543b-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="0543b-143">Requirement</span></span> | <span data-ttu-id="0543b-144">Valor</span><span class="sxs-lookup"><span data-stu-id="0543b-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0543b-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0543b-145">Header</span></span><br/>  | <dl> <span data-ttu-id="0543b-146"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0543b-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0543b-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0543b-147">Library</span></span><br/> | <dl> <span data-ttu-id="0543b-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0543b-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0543b-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="0543b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0543b-150">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="0543b-150">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> <dt>

[<span data-ttu-id="0543b-151">**D3DXUVAtlasCreate**</span><span class="sxs-lookup"><span data-stu-id="0543b-151">**D3DXUVAtlasCreate**</span></span>](d3dxuvatlascreate.md)
</dt> </dl>

 

 
