---
description: Essa interface encapsula a funcionalidade de malha de patch.
ms.assetid: c70c0fe0-b695-4ad9-b0c6-7854cf8f7593
title: Interface ID3DXPatchMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f1f13e6abe3a164e8027ddcb6bb33e9f0ca618fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298691"
---
# <a name="id3dxpatchmesh-interface"></a><span data-ttu-id="8c2bf-103">Interface ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="8c2bf-103">ID3DXPatchMesh interface</span></span>

<span data-ttu-id="8c2bf-104">Essa interface encapsula a funcionalidade de malha de patch.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-104">This interface encapsulates patch mesh functionality.</span></span>

## <a name="members"></a><span data-ttu-id="8c2bf-105">Membros</span><span class="sxs-lookup"><span data-stu-id="8c2bf-105">Members</span></span>

<span data-ttu-id="8c2bf-106">A interface **ID3DXPatchMesh** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8c2bf-106">The **ID3DXPatchMesh** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8c2bf-107">**ID3DXPatchMesh** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8c2bf-107">**ID3DXPatchMesh** also has these types of members:</span></span>

-   [<span data-ttu-id="8c2bf-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="8c2bf-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8c2bf-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="8c2bf-109">Methods</span></span>

<span data-ttu-id="8c2bf-110">A interface **ID3DXPatchMesh** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-110">The **ID3DXPatchMesh** interface has these methods.</span></span>



| <span data-ttu-id="8c2bf-111">Método</span><span class="sxs-lookup"><span data-stu-id="8c2bf-111">Method</span></span>                                                                           | <span data-ttu-id="8c2bf-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="8c2bf-112">Description</span></span>                                                                                     |
|:---------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c2bf-113">**CloneMesh**</span><span class="sxs-lookup"><span data-stu-id="8c2bf-113">**CloneMesh**</span></span>](id3dxpatchmesh--clonemesh.md)                                   | <span data-ttu-id="8c2bf-114">Cria uma nova malha de patch com a declaração de vértice especificada.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-114">Creates a new patch mesh with the specified vertex declaration.</span></span><br/>                      |
| [<span data-ttu-id="8c2bf-115">**GenerateAdjacency**</span><span class="sxs-lookup"><span data-stu-id="8c2bf-115">**GenerateAdjacency**</span></span>](id3dxpatchmesh--generateadjacency.md)                   | <span data-ttu-id="8c2bf-116">Gere uma lista de bordas de malha e os patches que compartilham cada borda.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-116">Generate a list of mesh edges and the patches that share each edge.</span></span><br/>                  |
| [<span data-ttu-id="8c2bf-117">**GetControlVerticesPerPatch**</span><span class="sxs-lookup"><span data-stu-id="8c2bf-117">**GetControlVerticesPerPatch**</span></span>](id3dxpatchmesh--getcontrolverticesperpatch.md) | <span data-ttu-id="8c2bf-118">Obtém o número de vértices de controle por patch.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-118">Gets the number of control vertices per patch.</span></span><br/>                                       |
| [<span data-ttu-id="8c2bf-119">**Getdeclaration**</span><span class="sxs-lookup"><span data-stu-id="8c2bf-119">**GetDeclaration**</span></span>](id3dxpatchmesh--getdeclaration.md)                         | <span data-ttu-id="8c2bf-120">Obtém a declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-120">Gets the vertex declaration.</span></span><br/>                                                         |
| [<span data-ttu-id="8c2bf-121">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="8c2bf-121">**GetDevice**</span></span>](id3dxpatchmesh--getdevice.md)                                   | <span data-ttu-id="8c2bf-122">Obtém o dispositivo que criou a malha.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-122">Gets the device that created the mesh.</span></span><br/>                                               |
| [<span data-ttu-id="8c2bf-123">**GetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="8c2bf-123">**GetDisplaceParam**</span></span>](id3dxpatchmesh--getdisplaceparam.md)                     | <span data-ttu-id="8c2bf-124">Obtém os parâmetros de deslocamento da geometria de malha.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-124">Gets mesh geometry displacement parameters.</span></span><br/>                                          |
| [<span data-ttu-id="8c2bf-125">**GetIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="8c2bf-125">**GetIndexBuffer**</span></span>](id3dxpatchmesh--getindexbuffer.md)                         | <span data-ttu-id="8c2bf-126">Obtém o buffer do índice de malha.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-126">Gets the mesh index buffer.</span></span><br/>                                                          |
| [<span data-ttu-id="8c2bf-127">**GetNumPatches**</span><span class="sxs-lookup"><span data-stu-id="8c2bf-127">**GetNumPatches**</span></span>](id3dxpatchmesh--getnumpatches.md)                           | <span data-ttu-id="8c2bf-128">Obtém o número de patches na malha.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-128">Gets the number of patches in the mesh.</span></span><br/>                                              |
| [<span data-ttu-id="8c2bf-129">**GetNumVertices**</span><span class="sxs-lookup"><span data-stu-id="8c2bf-129">**GetNumVertices**</span></span>](id3dxpatchmesh--getnumvertices.md)                         | <span data-ttu-id="8c2bf-130">Obtém o número de vértices na malha.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-130">Gets the number of vertices in the mesh.</span></span><br/>                                             |
| [<span data-ttu-id="8c2bf-131">**Getoptions**</span><span class="sxs-lookup"><span data-stu-id="8c2bf-131">**GetOptions**</span></span>](id3dxpatchmesh--getoptions.md)                                 | <span data-ttu-id="8c2bf-132">Obtém o tipo de patch.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-132">Gets the type of patch.</span></span><br/>                                                              |
| [<span data-ttu-id="8c2bf-133">**GetPatchInfo**</span><span class="sxs-lookup"><span data-stu-id="8c2bf-133">**GetPatchInfo**</span></span>](id3dxpatchmesh--getpatchinfo.md)                             | <span data-ttu-id="8c2bf-134">Obtém os atributos do patch.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-134">Gets the attributes of the patch.</span></span><br/>                                                    |
| [<span data-ttu-id="8c2bf-135">**GetTessSize**</span><span class="sxs-lookup"><span data-stu-id="8c2bf-135">**GetTessSize**</span></span>](id3dxpatchmesh--gettesssize.md)                               | <span data-ttu-id="8c2bf-136">Obtém o tamanho da malha mosaico, dado um nível de mosaico.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-136">Gets the size of the tessellated mesh, given a tessellation level.</span></span><br/>                   |
| [<span data-ttu-id="8c2bf-137">**GetVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="8c2bf-137">**GetVertexBuffer**</span></span>](id3dxpatchmesh--getvertexbuffer.md)                       | <span data-ttu-id="8c2bf-138">Obtém o buffer de vértice de malha.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-138">Gets the mesh vertex buffer.</span></span><br/>                                                         |
| [<span data-ttu-id="8c2bf-139">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="8c2bf-139">**LockAttributeBuffer**</span></span>](id3dxpatchmesh--lockattributebuffer.md)               | <span data-ttu-id="8c2bf-140">Bloqueia o buffer de atributo.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-140">Locks the attribute buffer.</span></span><br/>                                                          |
| [<span data-ttu-id="8c2bf-141">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="8c2bf-141">**LockIndexBuffer**</span></span>](id3dxpatchmesh--lockindexbuffer.md)                       | <span data-ttu-id="8c2bf-142">Bloquear o buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-142">Lock the index buffer.</span></span><br/>                                                               |
| [<span data-ttu-id="8c2bf-143">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="8c2bf-143">**LockVertexBuffer**</span></span>](id3dxpatchmesh--lockvertexbuffer.md)                     | <span data-ttu-id="8c2bf-144">Bloquear o buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-144">Lock the vertex buffer.</span></span><br/>                                                              |
| [<span data-ttu-id="8c2bf-145">**Otimizar**</span><span class="sxs-lookup"><span data-stu-id="8c2bf-145">**Optimize**</span></span>](id3dxpatchmesh--optimize.md)                                     | <span data-ttu-id="8c2bf-146">Otimiza a malha de patches para mosaico eficiente.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-146">Optimizes the patch mesh for efficient tessellation.</span></span><br/>                                 |
| [<span data-ttu-id="8c2bf-147">**SetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="8c2bf-147">**SetDisplaceParam**</span></span>](id3dxpatchmesh--setdisplaceparam.md)                     | <span data-ttu-id="8c2bf-148">Define os parâmetros de deslocamento de geometria de malha.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-148">Sets mesh geometry displacement parameters.</span></span><br/>                                          |
| [<span data-ttu-id="8c2bf-149">**Incluí**</span><span class="sxs-lookup"><span data-stu-id="8c2bf-149">**Tessellate**</span></span>](id3dxpatchmesh--tessellate.md)                                 | <span data-ttu-id="8c2bf-150">Executa mosaico uniforme com base no nível de mosaico.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-150">Performs uniform tessellation based on the tessellation level.</span></span><br/>                       |
| [<span data-ttu-id="8c2bf-151">**TessellateAdaptive**</span><span class="sxs-lookup"><span data-stu-id="8c2bf-151">**TessellateAdaptive**</span></span>](id3dxpatchmesh--tessellateadaptive.md)                 | <span data-ttu-id="8c2bf-152">Executa mosaico adaptável com base no critério de mosaico adaptável baseado em z.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-152">Performs adaptive tessellation based on the z-based adaptive tessellation criterion.</span></span><br/> |
| [<span data-ttu-id="8c2bf-153">**UnlockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="8c2bf-153">**UnlockAttributeBuffer**</span></span>](id3dxpatchmesh--unlockattributebuffer.md)           | <span data-ttu-id="8c2bf-154">Desbloqueie o buffer de atributo.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-154">Unlock the attribute buffer.</span></span><br/>                                                         |
| [<span data-ttu-id="8c2bf-155">**UnlockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="8c2bf-155">**UnlockIndexBuffer**</span></span>](id3dxpatchmesh--unlockindexbuffer.md)                   | <span data-ttu-id="8c2bf-156">Desbloqueie o buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-156">Unlock the index buffer.</span></span><br/>                                                             |
| [<span data-ttu-id="8c2bf-157">**UnlockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="8c2bf-157">**UnlockVertexBuffer**</span></span>](id3dxpatchmesh--unlockvertexbuffer.md)                 | <span data-ttu-id="8c2bf-158">Desbloqueie o buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-158">Unlock the vertex buffer.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="8c2bf-159">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c2bf-159">Remarks</span></span>

<span data-ttu-id="8c2bf-160">Uma malha de patch é uma malha que consiste em uma série de patches.</span><span class="sxs-lookup"><span data-stu-id="8c2bf-160">A patch mesh is a mesh that consists of a series of patches.</span></span>

<span data-ttu-id="8c2bf-161">Para obter a interface **ID3DXPatchMesh** , chame a função [**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="8c2bf-161">To obtain the **ID3DXPatchMesh** interface, call the [**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md) function.</span></span>

<span data-ttu-id="8c2bf-162">O tipo LPD3DXPATCHMESH é definido como um ponteiro para a interface **ID3DXPatchMesh** , da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="8c2bf-162">The LPD3DXPATCHMESH type is defined as a pointer to the **ID3DXPatchMesh** interface, as follows:</span></span>


```
typedef struct ID3DXPatchMesh *LPD3DXPATCHMESH;
```



## <a name="requirements"></a><span data-ttu-id="8c2bf-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c2bf-163">Requirements</span></span>



| <span data-ttu-id="8c2bf-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c2bf-164">Requirement</span></span> | <span data-ttu-id="8c2bf-165">Valor</span><span class="sxs-lookup"><span data-stu-id="8c2bf-165">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c2bf-166">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8c2bf-166">Header</span></span><br/>  | <dl> <span data-ttu-id="8c2bf-167"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c2bf-167"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8c2bf-168">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8c2bf-168">Library</span></span><br/> | <dl> <span data-ttu-id="8c2bf-169"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c2bf-169"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8c2bf-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c2bf-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c2bf-171">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="8c2bf-171">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="8c2bf-172">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="8c2bf-172">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
