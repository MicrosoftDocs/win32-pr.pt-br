---
description: A interface ID3DXTextureGutterHelper é usada para criar e gerenciar regiões de medianiz em uma textura. As regiões da medianiz separam texturas e permitem a interpolação bilinear para evitar a renderização de artefatos em limites de textura.
ms.assetid: 097e27bf-a1a6-4e7e-bdad-33015b50f91f
title: Interface ID3DXTextureGutterHelper (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ece03e14da490bd6d6f5aef69f9457939bc8bab7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298772"
---
# <a name="id3dxtexturegutterhelper-interface"></a><span data-ttu-id="a4863-104">Interface ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="a4863-104">ID3DXTextureGutterHelper interface</span></span>

<span data-ttu-id="a4863-105">A interface ID3DXTextureGutterHelper é usada para criar e gerenciar regiões de medianiz em uma textura.</span><span class="sxs-lookup"><span data-stu-id="a4863-105">The ID3DXTextureGutterHelper interface is used to build and manage gutter regions in a texture.</span></span> <span data-ttu-id="a4863-106">As regiões da medianiz separam texturas e permitem a interpolação bilinear para evitar a renderização de artefatos em limites de textura.</span><span class="sxs-lookup"><span data-stu-id="a4863-106">Gutter regions separate textures and allow for bilinear interpolation to avoid rendering artifacts at texture boundaries.</span></span>

<span data-ttu-id="a4863-107">O Get... os métodos fornecem acesso às estruturas de dados usadas pela aplicação... maneiras.</span><span class="sxs-lookup"><span data-stu-id="a4863-107">The Get... methods provide access to the data structures used by the Apply... methods.</span></span>

## <a name="members"></a><span data-ttu-id="a4863-108">Membros</span><span class="sxs-lookup"><span data-stu-id="a4863-108">Members</span></span>

<span data-ttu-id="a4863-109">A interface **ID3DXTextureGutterHelper** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a4863-109">The **ID3DXTextureGutterHelper** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a4863-110">**ID3DXTextureGutterHelper** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a4863-110">**ID3DXTextureGutterHelper** also has these types of members:</span></span>

-   [<span data-ttu-id="a4863-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="a4863-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a4863-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="a4863-112">Methods</span></span>

<span data-ttu-id="a4863-113">A interface **ID3DXTextureGutterHelper** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a4863-113">The **ID3DXTextureGutterHelper** interface has these methods.</span></span>



| <span data-ttu-id="a4863-114">Método</span><span class="sxs-lookup"><span data-stu-id="a4863-114">Method</span></span>                                                                   | <span data-ttu-id="a4863-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4863-115">Description</span></span>                                                                                            |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4863-116">**ApplyGuttersFloat**</span><span class="sxs-lookup"><span data-stu-id="a4863-116">**ApplyGuttersFloat**</span></span>](id3dxtexturegutterhelper--applyguttersfloat.md) | <span data-ttu-id="a4863-117">Aplica medianizes a um buffer de textura flutuante.</span><span class="sxs-lookup"><span data-stu-id="a4863-117">Applies gutters to a FLOAT texture buffer.</span></span><br/>                                                  |
| [<span data-ttu-id="a4863-118">**ApplyGuttersPRT**</span><span class="sxs-lookup"><span data-stu-id="a4863-118">**ApplyGuttersPRT**</span></span>](id3dxtexturegutterhelper--applyguttersprt.md)     | <span data-ttu-id="a4863-119">Aplica medianizes a um objeto de buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="a4863-119">Applies gutters to an [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer object.</span></span><br/>               |
| [<span data-ttu-id="a4863-120">**ApplyGuttersTex**</span><span class="sxs-lookup"><span data-stu-id="a4863-120">**ApplyGuttersTex**</span></span>](id3dxtexturegutterhelper--applygutterstex.md)     | <span data-ttu-id="a4863-121">Aplica medianizes a um objeto de textura [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="a4863-121">Applies gutters to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object.</span></span><br/>        |
| [<span data-ttu-id="a4863-122">**GetBaryMap**</span><span class="sxs-lookup"><span data-stu-id="a4863-122">**GetBaryMap**</span></span>](id3dxtexturegutterhelper--getbarymap.md)               | <span data-ttu-id="a4863-123">Recupera as coordenadas Texel barycentric.</span><span class="sxs-lookup"><span data-stu-id="a4863-123">Retrieves texel barycentric coordinates.</span></span><br/>                                                    |
| [<span data-ttu-id="a4863-124">**GetFaceMap**</span><span class="sxs-lookup"><span data-stu-id="a4863-124">**GetFaceMap**</span></span>](id3dxtexturegutterhelper--getfacemap.md)               | <span data-ttu-id="a4863-125">Recupera o índice do tipo de malha ao qual cada Texel pertence.</span><span class="sxs-lookup"><span data-stu-id="a4863-125">Retrieves the index of the mesh face to which each texel belongs.</span></span><br/>                           |
| [<span data-ttu-id="a4863-126">**GetGutterMap**</span><span class="sxs-lookup"><span data-stu-id="a4863-126">**GetGutterMap**</span></span>](id3dxtexturegutterhelper--getguttermap.md)           | <span data-ttu-id="a4863-127">Recebe um valor de classe Texel que indica a classe Texel de acordo com o local de cada Texel.</span><span class="sxs-lookup"><span data-stu-id="a4863-127">Receives a texel class value that indicates texel class according to each texel's location.</span></span><br/> |
| [<span data-ttu-id="a4863-128">**GetHeight**</span><span class="sxs-lookup"><span data-stu-id="a4863-128">**GetHeight**</span></span>](id3dxtexturegutterhelper--getheight.md)                 | <span data-ttu-id="a4863-129">Recupera a altura da textura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="a4863-129">Retrieves the height of the texture, in pixels.</span></span><br/>                                             |
| [<span data-ttu-id="a4863-130">**GetTexelMap**</span><span class="sxs-lookup"><span data-stu-id="a4863-130">**GetTexelMap**</span></span>](id3dxtexturegutterhelper--gettexelmap.md)             | <span data-ttu-id="a4863-131">Recupera as coordenadas de textura (u, v) de cada Texel.</span><span class="sxs-lookup"><span data-stu-id="a4863-131">Retrieves the (u, v) texture coordinates of each texel.</span></span><br/>                                     |
| [<span data-ttu-id="a4863-132">**GetWidth**</span><span class="sxs-lookup"><span data-stu-id="a4863-132">**GetWidth**</span></span>](id3dxtexturegutterhelper--getwidth.md)                   | <span data-ttu-id="a4863-133">Recupera a largura da textura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="a4863-133">Retrieves the width of the texture, in pixels.</span></span><br/>                                              |
| [<span data-ttu-id="a4863-134">**ResampleTex**</span><span class="sxs-lookup"><span data-stu-id="a4863-134">**ResampleTex**</span></span>](id3dxtexturegutterhelper--resampletex.md)             | <span data-ttu-id="a4863-135">Reamostrar uma textura na parametrização desta gutterhelper.</span><span class="sxs-lookup"><span data-stu-id="a4863-135">Resamples a texture into this gutterhelper's parameterization.</span></span><br/>                              |
| [<span data-ttu-id="a4863-136">**SetBaryMap**</span><span class="sxs-lookup"><span data-stu-id="a4863-136">**SetBaryMap**</span></span>](id3dxtexturegutterhelper--setbarymap.md)               | <span data-ttu-id="a4863-137">Define as coordenadas Texel barycentric.</span><span class="sxs-lookup"><span data-stu-id="a4863-137">Sets texel barycentric coordinates.</span></span><br/>                                                         |
| [<span data-ttu-id="a4863-138">**SetFaceMap**</span><span class="sxs-lookup"><span data-stu-id="a4863-138">**SetFaceMap**</span></span>](id3dxtexturegutterhelper--setfacemap.md)               | <span data-ttu-id="a4863-139">Define o índice do tipo de malha ao qual cada Texel pertence.</span><span class="sxs-lookup"><span data-stu-id="a4863-139">Sets the index of the mesh face to which each texel belongs.</span></span><br/>                                |
| [<span data-ttu-id="a4863-140">**SetGutterMap**</span><span class="sxs-lookup"><span data-stu-id="a4863-140">**SetGutterMap**</span></span>](id3dxtexturegutterhelper--setguttermap.md)           | <span data-ttu-id="a4863-141">Define um valor de classe Texel que indica a classe Texel de acordo com o local de cada Texel.</span><span class="sxs-lookup"><span data-stu-id="a4863-141">Sets a texel class value that indicates texel class according to each texel's location.</span></span><br/>     |
| [<span data-ttu-id="a4863-142">**SetTexelMap**</span><span class="sxs-lookup"><span data-stu-id="a4863-142">**SetTexelMap**</span></span>](id3dxtexturegutterhelper--settexelmap.md)             | <span data-ttu-id="a4863-143">Define as coordenadas de textura (u, v) de cada Texel.</span><span class="sxs-lookup"><span data-stu-id="a4863-143">Sets the (u, v) texture coordinates of each texel.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="a4863-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4863-144">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a4863-145">Quando usado com PRT (transferência de radiante de computação), essa interface requer uma parametrização exclusiva do modelo.</span><span class="sxs-lookup"><span data-stu-id="a4863-145">When used with precomputed radiance transfer (PRT), this interface requires a unique parameterization of the model.</span></span> <span data-ttu-id="a4863-146">Cada Texel deve corresponder a um único ponto na superfície do modelo e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="a4863-146">Every texel must correspond to a single point on the surface of the model and vice-versa.</span></span> <span data-ttu-id="a4863-147">Se o modelo incluir várias texturas, ele deverá ser dividido em partes separadas que contêm um objeto auxiliar de medianiz por textura.</span><span class="sxs-lookup"><span data-stu-id="a4863-147">If the model includes multiple textures, it must be split into separate pieces that each contain one gutter helper object per texture.</span></span>

 

<span data-ttu-id="a4863-148">Essa interface pode ser usada para gerar um mapa no espaço de textura no qual cada Texel está em uma das quatro classes.</span><span class="sxs-lookup"><span data-stu-id="a4863-148">This interface can be used to generate a map in texture space in which each texel is in one of four classes.</span></span>



| <span data-ttu-id="a4863-149">Classe Texel</span><span class="sxs-lookup"><span data-stu-id="a4863-149">Texel Class</span></span> | <span data-ttu-id="a4863-150">Local Texel</span><span class="sxs-lookup"><span data-stu-id="a4863-150">Texel Location</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4863-151">0</span><span class="sxs-lookup"><span data-stu-id="a4863-151">0</span></span>           | <span data-ttu-id="a4863-152">Ponto inválido; Texel não será usado.</span><span class="sxs-lookup"><span data-stu-id="a4863-152">Invalid point; texel will not be used.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a4863-153">1</span><span class="sxs-lookup"><span data-stu-id="a4863-153">1</span></span>           | <span data-ttu-id="a4863-154">Triângulo interno.</span><span class="sxs-lookup"><span data-stu-id="a4863-154">Inside triangle.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="a4863-155">2</span><span class="sxs-lookup"><span data-stu-id="a4863-155">2</span></span>           | <span data-ttu-id="a4863-156">Dentro da medianiz.</span><span class="sxs-lookup"><span data-stu-id="a4863-156">Inside gutter.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="a4863-157">4</span><span class="sxs-lookup"><span data-stu-id="a4863-157">4</span></span>           | <span data-ttu-id="a4863-158">Na medianiz; Texel será avaliado como um exemplo completo nos métodos [**ID3DXTextureGutterHelper:: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)ou [**ID3DXTextureGutterHelper:: ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) .</span><span class="sxs-lookup"><span data-stu-id="a4863-158">Inside gutter; texel will be evaluated as a full sample in the [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md), or [**ID3DXTextureGutterHelper::ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) methods.</span></span> |



 

<span data-ttu-id="a4863-159">Para as classes 1 e 2, um Texel é armazenado com a face à qual ele pertence, juntamente com as coordenadas barycentric dos dois primeiros vértices dessa face.</span><span class="sxs-lookup"><span data-stu-id="a4863-159">For classes 1 and 2, a texel is stored with the face it belongs to, along with barycentric coordinates of the first two vertices of that face.</span></span> <span data-ttu-id="a4863-160">Os vértices da medianiz são atribuídos à borda mais próxima no espaço de textura.</span><span class="sxs-lookup"><span data-stu-id="a4863-160">Gutter vertices are assigned to the closest edge in texture space.</span></span>

<span data-ttu-id="a4863-161">Não há nenhuma classe de Texel 3.</span><span class="sxs-lookup"><span data-stu-id="a4863-161">There is no texel class 3.</span></span>

<span data-ttu-id="a4863-162">A interface **ID3DXTextureGutterHelper** é obtida chamando a função [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) .</span><span class="sxs-lookup"><span data-stu-id="a4863-162">The **ID3DXTextureGutterHelper** interface is obtained by calling the [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) function.</span></span>

<span data-ttu-id="a4863-163">O tipo LPD3DXTEXTUREGUTTERHELPER é definido como um ponteiro para a interface **ID3DXTextureGutterHelper** .</span><span class="sxs-lookup"><span data-stu-id="a4863-163">The LPD3DXTEXTUREGUTTERHELPER type is defined as a pointer to the **ID3DXTextureGutterHelper** interface.</span></span>


```
typedef interface ID3DXTextureGutterHelper ID3DXTextureGutterHelper;
typedef interface ID3DXTextureGutterHelper *LPD3DXTEXTUREGUTTERHELPER;
```



## <a name="requirements"></a><span data-ttu-id="a4863-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4863-164">Requirements</span></span>



| <span data-ttu-id="a4863-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4863-165">Requirement</span></span> | <span data-ttu-id="a4863-166">Valor</span><span class="sxs-lookup"><span data-stu-id="a4863-166">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4863-167">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a4863-167">Header</span></span><br/>  | <dl> <span data-ttu-id="a4863-168"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4863-168"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a4863-169">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a4863-169">Library</span></span><br/> | <dl> <span data-ttu-id="a4863-170"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4863-170"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a4863-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4863-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4863-172">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="a4863-172">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
