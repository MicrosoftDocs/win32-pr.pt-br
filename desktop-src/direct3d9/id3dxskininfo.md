---
description: Os aplicativos usam os métodos da interface ID3DXSkinInfo para manipular matrizes Bone, que são usadas para a capa de dados de vértice para animação. Essa interface não está mais estritamente ligada a ID3DXMesh e pode ser usada para aplicar uma capa a qualquer conjunto de dados de vértice.
ms.assetid: 4ccf88b0-2cc7-4e91-a0f2-fb8eea66a3ce
title: Interface ID3DXSkinInfo (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: afb93a0513bef7de1b0815b8b1f50179e2cba41d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798162"
---
# <a name="id3dxskininfo-interface"></a><span data-ttu-id="be9c3-104">Interface ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="be9c3-104">ID3DXSkinInfo interface</span></span>

<span data-ttu-id="be9c3-105">Os aplicativos usam os métodos da interface ID3DXSkinInfo para manipular matrizes Bone, que são usadas para a capa de dados de vértice para animação.</span><span class="sxs-lookup"><span data-stu-id="be9c3-105">Applications use the methods of the ID3DXSkinInfo interface to manipulate bone matrices, which are used to skin vertex data for animation.</span></span> <span data-ttu-id="be9c3-106">Essa interface não está mais estritamente ligada a [**ID3DXMesh**](id3dxmesh.md) e pode ser usada para aplicar uma capa a qualquer conjunto de dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="be9c3-106">This interface is no longer strictly tied to [**ID3DXMesh**](id3dxmesh.md) and can be used to skin any set of vertex data.</span></span>

## <a name="members"></a><span data-ttu-id="be9c3-107">Membros</span><span class="sxs-lookup"><span data-stu-id="be9c3-107">Members</span></span>

<span data-ttu-id="be9c3-108">A interface **ID3DXSkinInfo** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="be9c3-108">The **ID3DXSkinInfo** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="be9c3-109">**ID3DXSkinInfo** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="be9c3-109">**ID3DXSkinInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="be9c3-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="be9c3-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="be9c3-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="be9c3-111">Methods</span></span>

<span data-ttu-id="be9c3-112">A interface **ID3DXSkinInfo** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="be9c3-112">The **ID3DXSkinInfo** interface has these methods.</span></span>



| <span data-ttu-id="be9c3-113">Método</span><span class="sxs-lookup"><span data-stu-id="be9c3-113">Method</span></span>                                                                              | <span data-ttu-id="be9c3-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="be9c3-114">Description</span></span>                                                                                                                                                                                    |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be9c3-115">**8i**</span><span class="sxs-lookup"><span data-stu-id="be9c3-115">**Clone**</span></span>](id3dxskininfo--clone.md)                                               | <span data-ttu-id="be9c3-116">Clona um objeto de informações de capa.</span><span class="sxs-lookup"><span data-stu-id="be9c3-116">Clones a skin info object.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="be9c3-117">**ConvertToBlendedMesh**</span><span class="sxs-lookup"><span data-stu-id="be9c3-117">**ConvertToBlendedMesh**</span></span>](id3dxskininfo--converttoblendedmesh.md)                 | <span data-ttu-id="be9c3-118">Usa uma malha e retorna uma nova malha com pesos de mistura por vértice e uma tabela de combinação de Bone.</span><span class="sxs-lookup"><span data-stu-id="be9c3-118">Takes a mesh and returns a new mesh with per-vertex blend weights and a bone combination table.</span></span> <span data-ttu-id="be9c3-119">A tabela descreve quais Bones afetam quais subconjuntos da malha.</span><span class="sxs-lookup"><span data-stu-id="be9c3-119">The table describes which bones affect which subsets of the mesh.</span></span><br/>                   |
| [<span data-ttu-id="be9c3-120">**ConvertToIndexedBlendedMesh**</span><span class="sxs-lookup"><span data-stu-id="be9c3-120">**ConvertToIndexedBlendedMesh**</span></span>](id3dxskininfo--converttoindexedblendedmesh.md)   | <span data-ttu-id="be9c3-121">Usa uma malha e retorna uma nova malha com pesos de mistura por vértice, índices e uma tabela de combinação de Bone.</span><span class="sxs-lookup"><span data-stu-id="be9c3-121">Takes a mesh and returns a new mesh with per-vertex blend weights, indices, and a bone combination table.</span></span> <span data-ttu-id="be9c3-122">A tabela descreve quais paletas de Bone afetam quais subconjuntos da malha.</span><span class="sxs-lookup"><span data-stu-id="be9c3-122">The table describes which bone palettes affect which subsets of the mesh.</span></span><br/> |
| [<span data-ttu-id="be9c3-123">**FindBoneVertexInfluenceIndex**</span><span class="sxs-lookup"><span data-stu-id="be9c3-123">**FindBoneVertexInfluenceIndex**</span></span>](id3dxskininfo--findbonevertexinfluenceindex.md) | <span data-ttu-id="be9c3-124">Recupera o índice da influência do Bone que afeta um único vértice.</span><span class="sxs-lookup"><span data-stu-id="be9c3-124">Retrieves the index of the bone influence affecting a single vertex.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="be9c3-125">**GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="be9c3-125">**GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)                         | <span data-ttu-id="be9c3-126">Obtém os vértices e os pesos que um Bone influencia.</span><span class="sxs-lookup"><span data-stu-id="be9c3-126">Gets the vertices and weights that a bone influences.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="be9c3-127">**Getbonename**</span><span class="sxs-lookup"><span data-stu-id="be9c3-127">**GetBoneName**</span></span>](id3dxskininfo--getbonename.md)                                   | <span data-ttu-id="be9c3-128">Obtém o nome do Bone, do índice Bone.</span><span class="sxs-lookup"><span data-stu-id="be9c3-128">Gets the bone name, from the bone index.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="be9c3-129">**GetBoneOffsetMatrix**</span><span class="sxs-lookup"><span data-stu-id="be9c3-129">**GetBoneOffsetMatrix**</span></span>](id3dxskininfo--getboneoffsetmatrix.md)                   | <span data-ttu-id="be9c3-130">Obtém a matriz de deslocamento do Bone.</span><span class="sxs-lookup"><span data-stu-id="be9c3-130">Gets the bone offset matrix.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="be9c3-131">**GetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="be9c3-131">**GetBoneVertexInfluence**</span></span>](id3dxskininfo--getbonevertexinfluence.md)             | <span data-ttu-id="be9c3-132">Recupera o fator de mistura e o vértice afetados por uma influência de Bone especificada.</span><span class="sxs-lookup"><span data-stu-id="be9c3-132">Retrieves the blend factor and vertex affected by a specified bone influence.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="be9c3-133">**Getdeclaration**</span><span class="sxs-lookup"><span data-stu-id="be9c3-133">**GetDeclaration**</span></span>](id3dxskininfo--getdeclaration.md)                             | <span data-ttu-id="be9c3-134">Obtém a declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="be9c3-134">Gets the vertex declaration.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="be9c3-135">**GetFVF**</span><span class="sxs-lookup"><span data-stu-id="be9c3-135">**GetFVF**</span></span>](id3dxskininfo--getfvf.md)                                             | <span data-ttu-id="be9c3-136">Obtém o valor de vértice da função fixa.</span><span class="sxs-lookup"><span data-stu-id="be9c3-136">Gets the fixed function vertex value.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="be9c3-137">**GetMaxFaceInfluences**</span><span class="sxs-lookup"><span data-stu-id="be9c3-137">**GetMaxFaceInfluences**</span></span>](id3dxskininfo--getmaxfaceinfluences.md)                 | <span data-ttu-id="be9c3-138">Obtém o número máximo de influências em uma malha de triângulos com o buffer de índice especificado.</span><span class="sxs-lookup"><span data-stu-id="be9c3-138">Gets the maximum face influences in a triangle mesh with the specified index buffer.</span></span><br/>                                                                                                |
| [<span data-ttu-id="be9c3-139">**GetMaxVertexInfluences**</span><span class="sxs-lookup"><span data-stu-id="be9c3-139">**GetMaxVertexInfluences**</span></span>](id3dxskininfo--getmaxvertexinfluences.md)             | <span data-ttu-id="be9c3-140">Obtém o número máximo de influências para qualquer vértice na malha.</span><span class="sxs-lookup"><span data-stu-id="be9c3-140">Gets the maximum number of influences for any vertex in the mesh.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="be9c3-141">**GetMinBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="be9c3-141">**GetMinBoneInfluence**</span></span>](id3dxskininfo--getminboneinfluence.md)                   | <span data-ttu-id="be9c3-142">Obtém a influência mínima do Bone.</span><span class="sxs-lookup"><span data-stu-id="be9c3-142">Gets the minimum bone influence.</span></span> <span data-ttu-id="be9c3-143">Influenciar valores menores do que isso é ignorado.</span><span class="sxs-lookup"><span data-stu-id="be9c3-143">Influence values smaller than this are ignored.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="be9c3-144">**GetNumBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="be9c3-144">**GetNumBoneInfluences**</span></span>](id3dxskininfo--getnumboneinfluences.md)                 | <span data-ttu-id="be9c3-145">Obtém o número de influências para um Bone.</span><span class="sxs-lookup"><span data-stu-id="be9c3-145">Gets the number of influences for a bone.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="be9c3-146">**GetNumBones**</span><span class="sxs-lookup"><span data-stu-id="be9c3-146">**GetNumBones**</span></span>](id3dxskininfo--getnumbones.md)                                   | <span data-ttu-id="be9c3-147">Obtém o número de Bones.</span><span class="sxs-lookup"><span data-stu-id="be9c3-147">Gets the number of bones.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="be9c3-148">**Conseguem**</span><span class="sxs-lookup"><span data-stu-id="be9c3-148">**Remap**</span></span>](id3dxskininfo--remap.md)                                               | <span data-ttu-id="be9c3-149">Atualiza informações de influência de Bone para corresponder os vértices depois que eles são reordenados.</span><span class="sxs-lookup"><span data-stu-id="be9c3-149">Updates bone influence information to match vertices after they are reordered.</span></span> <span data-ttu-id="be9c3-150">Esse método deve ser chamado se o buffer de vértice de destino tiver sido reordenado externamente.</span><span class="sxs-lookup"><span data-stu-id="be9c3-150">This method should be called if the target vertex buffer has been reordered externally.</span></span><br/>              |
| [<span data-ttu-id="be9c3-151">**SetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="be9c3-151">**SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)                         | <span data-ttu-id="be9c3-152">Define o valor de influência para um Bone.</span><span class="sxs-lookup"><span data-stu-id="be9c3-152">Sets the influence value for a bone.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="be9c3-153">**Setbonename**</span><span class="sxs-lookup"><span data-stu-id="be9c3-153">**SetBoneName**</span></span>](id3dxskininfo--setbonename.md)                                   | <span data-ttu-id="be9c3-154">Define o nome do Bone.</span><span class="sxs-lookup"><span data-stu-id="be9c3-154">Sets the bone name.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="be9c3-155">**SetBoneOffsetMatrix**</span><span class="sxs-lookup"><span data-stu-id="be9c3-155">**SetBoneOffsetMatrix**</span></span>](id3dxskininfo--setboneoffsetmatrix.md)                   | <span data-ttu-id="be9c3-156">Define a matriz de deslocamento do Bone.</span><span class="sxs-lookup"><span data-stu-id="be9c3-156">Sets the bone offset matrix.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="be9c3-157">**SetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="be9c3-157">**SetBoneVertexInfluence**</span></span>](id3dxskininfo--setbonevertexinfluence.md)             | <span data-ttu-id="be9c3-158">Define um valor de influência de um Bone em um único vértice.</span><span class="sxs-lookup"><span data-stu-id="be9c3-158">Sets an influence value of a bone on a single vertex.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="be9c3-159">**Setdeclaration**</span><span class="sxs-lookup"><span data-stu-id="be9c3-159">**SetDeclaration**</span></span>](id3dxskininfo--setdeclaration.md)                             | <span data-ttu-id="be9c3-160">Define a declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="be9c3-160">Sets the vertex declaration.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="be9c3-161">**SetFVF**</span><span class="sxs-lookup"><span data-stu-id="be9c3-161">**SetFVF**</span></span>](id3dxskininfo--setfvf.md)                                             | <span data-ttu-id="be9c3-162">Define o tipo de formato de vértice flexível (FVF).</span><span class="sxs-lookup"><span data-stu-id="be9c3-162">Sets the flexible vertex format (FVF) type.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="be9c3-163">**SetMinBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="be9c3-163">**SetMinBoneInfluence**</span></span>](id3dxskininfo--setminboneinfluence.md)                   | <span data-ttu-id="be9c3-164">Define a influência mínima do Bone.</span><span class="sxs-lookup"><span data-stu-id="be9c3-164">Sets the minimum bone influence.</span></span> <span data-ttu-id="be9c3-165">Influenciar valores menores do que isso é ignorado.</span><span class="sxs-lookup"><span data-stu-id="be9c3-165">Influence values smaller than this are ignored.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="be9c3-166">**UpdateSkinnedMesh**</span><span class="sxs-lookup"><span data-stu-id="be9c3-166">**UpdateSkinnedMesh**</span></span>](id3dxskininfo--updateskinnedmesh.md)                       | <span data-ttu-id="be9c3-167">Aplica a procapação de software aos vértices de destino com base nas matrizes atuais.</span><span class="sxs-lookup"><span data-stu-id="be9c3-167">Applies software skinning to the target vertices based on the current matrices.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="be9c3-168">Comentários</span><span class="sxs-lookup"><span data-stu-id="be9c3-168">Remarks</span></span>

<span data-ttu-id="be9c3-169">Crie uma interface **ID3DXSkinInfo** com [**D3DXCreateSkinInfo**](d3dxcreateskininfo.md), [**D3DXCreateSkinInfoFromBlendedMesh**](d3dxcreateskininfofromblendedmesh.md)ou [**D3DXCreateSkinInfoFVF**](d3dxcreateskininfofvf.md).</span><span class="sxs-lookup"><span data-stu-id="be9c3-169">Create a **ID3DXSkinInfo** interface with [**D3DXCreateSkinInfo**](d3dxcreateskininfo.md), [**D3DXCreateSkinInfoFromBlendedMesh**](d3dxcreateskininfofromblendedmesh.md), or [**D3DXCreateSkinInfoFVF**](d3dxcreateskininfofvf.md).</span></span>

<span data-ttu-id="be9c3-170">O tipo LPD3DXSKININFO é definido como um ponteiro para a interface **ID3DXSkinInfo** .</span><span class="sxs-lookup"><span data-stu-id="be9c3-170">The LPD3DXSKININFO type is defined as a pointer to the **ID3DXSkinInfo** interface.</span></span>


```
typedef struct ID3DXSkinInfo *LPD3DXSKININFO;
```



## <a name="requirements"></a><span data-ttu-id="be9c3-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be9c3-171">Requirements</span></span>



| <span data-ttu-id="be9c3-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="be9c3-172">Requirement</span></span> | <span data-ttu-id="be9c3-173">Valor</span><span class="sxs-lookup"><span data-stu-id="be9c3-173">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be9c3-174">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be9c3-174">Header</span></span><br/>  | <dl> <span data-ttu-id="be9c3-175"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="be9c3-175"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="be9c3-176">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="be9c3-176">Library</span></span><br/> | <dl> <span data-ttu-id="be9c3-177"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be9c3-177"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="be9c3-178">Confira também</span><span class="sxs-lookup"><span data-stu-id="be9c3-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be9c3-179">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="be9c3-179">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
