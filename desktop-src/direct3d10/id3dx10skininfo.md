---
description: O ID3DX10SkinInfo permite otimizar, processar e definir manualmente a relação entre os Bones e os vértices em suas malhas (consulte a animação estrutural na Wikipédia).
ms.assetid: bea0fe71-c201-45c6-8036-d0d76d5851fd
title: Interface ID3DX10SkinInfo (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3216765ab9ef2ba9f2b0883c31a878a7eae6861f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298635"
---
# <a name="id3dx10skininfo-interface"></a><span data-ttu-id="cf976-103">Interface ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="cf976-103">ID3DX10SkinInfo interface</span></span>

<span data-ttu-id="cf976-104">O ID3DX10SkinInfo permite otimizar, processar e definir manualmente a relação entre os Bones e os vértices em suas malhas (consulte a [animação estrutural na Wikipédia](https://en.wikipedia.org/wiki/Skeletal_animation)).</span><span class="sxs-lookup"><span data-stu-id="cf976-104">ID3DX10SkinInfo allows you to optimize, process, and manually set the relationship between bones and vertices in your meshes (see [Skeletal Animation on Wikipedia](https://en.wikipedia.org/wiki/Skeletal_animation)).</span></span> <span data-ttu-id="cf976-105">Ele é mais útil para fazer arquivos. x exportados por aplicativos DCC (como 3DS Max e Maya) mais amigáveis para hardware e para melhorar a velocidade de renderização de suas malhas subcapadas no modo de processamento de software.</span><span class="sxs-lookup"><span data-stu-id="cf976-105">It is most useful for making .x files exported by DCC Apps (such as 3DS Max and Maya) more hardware-friendly, and for improving the render speed of your skinned meshes in software render mode.</span></span>

## <a name="members"></a><span data-ttu-id="cf976-106">Membros</span><span class="sxs-lookup"><span data-stu-id="cf976-106">Members</span></span>

<span data-ttu-id="cf976-107">A interface **ID3DX10SkinInfo** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cf976-107">The **ID3DX10SkinInfo** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cf976-108">**ID3DX10SkinInfo** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cf976-108">**ID3DX10SkinInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="cf976-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="cf976-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cf976-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="cf976-110">Methods</span></span>

<span data-ttu-id="cf976-111">A interface **ID3DX10SkinInfo** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="cf976-111">The **ID3DX10SkinInfo** interface has these methods.</span></span>



| <span data-ttu-id="cf976-112">Método</span><span class="sxs-lookup"><span data-stu-id="cf976-112">Method</span></span>                                                                   | <span data-ttu-id="cf976-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf976-113">Description</span></span>                                                                                                                        |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf976-114">**AddBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="cf976-114">**AddBoneInfluences**</span></span>](id3dx10skininfo-addboneinfluences.md)           | <span data-ttu-id="cf976-115">Habilite um Bone existente para influenciar um grupo de vértices e definir quanto influência o Bone tem em cada vértice.</span><span class="sxs-lookup"><span data-stu-id="cf976-115">Enable an existing bone to influence a group of vertices and define how much influence the bone has on each vertex.</span></span><br/>     |
| [<span data-ttu-id="cf976-116">**Addbones**</span><span class="sxs-lookup"><span data-stu-id="cf976-116">**AddBones**</span></span>](id3dx10skininfo-addbones.md)                             | <span data-ttu-id="cf976-117">Aloque espaço para mais Bones.</span><span class="sxs-lookup"><span data-stu-id="cf976-117">Allocate space for more bones.</span></span><br/>                                                                                          |
| [<span data-ttu-id="cf976-118">**Addvértices**</span><span class="sxs-lookup"><span data-stu-id="cf976-118">**AddVertices**</span></span>](id3dx10skininfo-addvertices.md)                       | <span data-ttu-id="cf976-119">Aloque espaço para vértices adicionais.</span><span class="sxs-lookup"><span data-stu-id="cf976-119">Allocate space for additional vertices.</span></span><br/>                                                                                 |
| [<span data-ttu-id="cf976-120">**ClearBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="cf976-120">**ClearBoneInfluences**</span></span>](id3dx10skininfo-clearboneinfluences.md)       | <span data-ttu-id="cf976-121">Desmarque a lista de vértices de um Bone que ele influencia.</span><span class="sxs-lookup"><span data-stu-id="cf976-121">Clear a bone's list of vertices that it influences.</span></span><br/>                                                                     |
| [<span data-ttu-id="cf976-122">**Compacto**</span><span class="sxs-lookup"><span data-stu-id="cf976-122">**Compact**</span></span>](id3dx10skininfo-compact.md)                               | <span data-ttu-id="cf976-123">Limitar o número de Bones que podem influenciar um vértice e/ou limitar a quantidade de influência que um Bone pode ter em um vértice.</span><span class="sxs-lookup"><span data-stu-id="cf976-123">Limit the number of bones that can influence a vertex and/or limit the amount of influence a bone can have on a vertex.</span></span><br/> |
| [<span data-ttu-id="cf976-124">**DoSoftwareSkinning**</span><span class="sxs-lookup"><span data-stu-id="cf976-124">**DoSoftwareSkinning**</span></span>](id3dx10skininfo-dosoftwareskinning.md)         | <span data-ttu-id="cf976-125">Faça a subaparência do software em uma matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="cf976-125">Do software skinning on an array of vertices.</span></span><br/>                                                                           |
| [<span data-ttu-id="cf976-126">**FindBoneInfluenceIndex**</span><span class="sxs-lookup"><span data-stu-id="cf976-126">**FindBoneInfluenceIndex**</span></span>](id3dx10skininfo-findboneinfluenceindex.md) | <span data-ttu-id="cf976-127">Localize o índice que indica onde um determinado vértice está em uma determinada lista de vértices influenciados.</span><span class="sxs-lookup"><span data-stu-id="cf976-127">Find the index that indicates where a given vertex is in a given bone's list of influenced vertices.</span></span><br/>                    |
| [<span data-ttu-id="cf976-128">**GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="cf976-128">**GetBoneInfluence**</span></span>](id3dx10skininfo-getboneinfluence.md)             | <span data-ttu-id="cf976-129">Obter a quantidade de influência que um determinado Bone tem sobre um determinado vértice.</span><span class="sxs-lookup"><span data-stu-id="cf976-129">Get the amount of influence a given bone has over a given vertex.</span></span><br/>                                                       |
| [<span data-ttu-id="cf976-130">**GetBoneInfluenceCount**</span><span class="sxs-lookup"><span data-stu-id="cf976-130">**GetBoneInfluenceCount**</span></span>](id3dx10skininfo-getboneinfluencecount.md)   | <span data-ttu-id="cf976-131">Obter o número de vértices que um determinado Bone influencia.</span><span class="sxs-lookup"><span data-stu-id="cf976-131">Get the number of vertices that a given bone influences.</span></span><br/>                                                                |
| [<span data-ttu-id="cf976-132">**GetBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="cf976-132">**GetBoneInfluences**</span></span>](id3dx10skininfo-getboneinfluences.md)           | <span data-ttu-id="cf976-133">Obtenha uma lista de vértices que um determinado Bone influencia e uma lista da quantidade de influência que o Bone tem em cada vértice.</span><span class="sxs-lookup"><span data-stu-id="cf976-133">Get a list of vertices that a given bone influences and a list of the amount of influence that bone has on each vertex.</span></span><br/> |
| [<span data-ttu-id="cf976-134">**GetMaxBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="cf976-134">**GetMaxBoneInfluences**</span></span>](id3dx10skininfo-getmaxboneinfluences.md)     | <span data-ttu-id="cf976-135">Obter o número de vértices que um Bone pode influenciar de uma influência.</span><span class="sxs-lookup"><span data-stu-id="cf976-135">Get the number of vertices a bone can maximally influence.</span></span><br/>                                                              |
| [<span data-ttu-id="cf976-136">**GetNumBones**</span><span class="sxs-lookup"><span data-stu-id="cf976-136">**GetNumBones**</span></span>](id3dx10skininfo-getnumbones.md)                       | <span data-ttu-id="cf976-137">Obtenha o número de Bones em ID3DX10SkinInfo.</span><span class="sxs-lookup"><span data-stu-id="cf976-137">Get the number of bones in ID3DX10SkinInfo.</span></span><br/>                                                                             |
| [<span data-ttu-id="cf976-138">**GetNumVertices**</span><span class="sxs-lookup"><span data-stu-id="cf976-138">**GetNumVertices**</span></span>](id3dx10skininfo-getnumvertices.md)                 | <span data-ttu-id="cf976-139">Obtenha o número de vértices em ID3DX10SkinInfo.</span><span class="sxs-lookup"><span data-stu-id="cf976-139">Get the number of vertices in ID3DX10SkinInfo.</span></span><br/>                                                                          |
| [<span data-ttu-id="cf976-140">**RemapBones**</span><span class="sxs-lookup"><span data-stu-id="cf976-140">**RemapBones**</span></span>](id3dx10skininfo-remapbones.md)                         | <span data-ttu-id="cf976-141">Altere quais Bones influenciam quais vértices.</span><span class="sxs-lookup"><span data-stu-id="cf976-141">Change which bones influence which vertices.</span></span><br/>                                                                            |
| [<span data-ttu-id="cf976-142">**RemapVertices**</span><span class="sxs-lookup"><span data-stu-id="cf976-142">**RemapVertices**</span></span>](id3dx10skininfo-remapvertices.md)                   | <span data-ttu-id="cf976-143">Altere quais vértices são influenciados por quais Bones.</span><span class="sxs-lookup"><span data-stu-id="cf976-143">Change which vertices are influenced by which bones.</span></span><br/>                                                                    |
| [<span data-ttu-id="cf976-144">**RemoveBone**</span><span class="sxs-lookup"><span data-stu-id="cf976-144">**RemoveBone**</span></span>](id3dx10skininfo-removebone.md)                         | <span data-ttu-id="cf976-145">Remover um Bone.</span><span class="sxs-lookup"><span data-stu-id="cf976-145">Remove a bone.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="cf976-146">**SetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="cf976-146">**SetBoneInfluence**</span></span>](id3dx10skininfo-setboneinfluence.md)             | <span data-ttu-id="cf976-147">Defina a quantidade de influência que um determinado Bone tem sobre um determinado vértice.</span><span class="sxs-lookup"><span data-stu-id="cf976-147">Set the amount of influence a given bone has over a given vertex.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="cf976-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf976-148">Remarks</span></span>

<span data-ttu-id="cf976-149">Crie uma interface ID3DX10SkinInfo com [**D3DX10CreateSkinInfo**](d3d10-d3dx10createskininfo.md), **D3DX10CreateSkinInfoFromBlendedMesh** ou **D3DX10CreateSkinInfoFVF**.</span><span class="sxs-lookup"><span data-stu-id="cf976-149">Create a ID3DX10SkinInfo interface with [**D3DX10CreateSkinInfo**](d3d10-d3dx10createskininfo.md), **D3DX10CreateSkinInfoFromBlendedMesh**, or **D3DX10CreateSkinInfoFVF**.</span></span>

<span data-ttu-id="cf976-150">O tipo LPD3DX10SKININFO é definido como um ponteiro para a interface **ID3DX10SkinInfo** .</span><span class="sxs-lookup"><span data-stu-id="cf976-150">The LPD3DX10SKININFO type is defined as a pointer to the **ID3DX10SkinInfo** interface.</span></span>


```
typedef struct ID3DX10SkinInfo *LPD3DX10SKININFO;
```



## <a name="requirements"></a><span data-ttu-id="cf976-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf976-151">Requirements</span></span>



| <span data-ttu-id="cf976-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf976-152">Requirement</span></span> | <span data-ttu-id="cf976-153">Valor</span><span class="sxs-lookup"><span data-stu-id="cf976-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf976-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cf976-154">Header</span></span><br/>  | <dl> <span data-ttu-id="cf976-155"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf976-155"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="cf976-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cf976-156">Library</span></span><br/> | <dl> <span data-ttu-id="cf976-157"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf976-157"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf976-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf976-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf976-159">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="cf976-159">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
