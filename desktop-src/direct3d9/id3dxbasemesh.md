---
description: Os aplicativos usam os métodos da interface ID3DXBaseMesh para manipular e consultar malha e objetos de malha progressiva.
ms.assetid: ec4ccd77-e370-470c-9325-3d794a8f7f16
title: Interface ID3DXBaseMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 58029639852b30f5de357bb2643583615c45485c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298655"
---
# <a name="id3dxbasemesh-interface"></a><span data-ttu-id="00567-103">Interface ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="00567-103">ID3DXBaseMesh interface</span></span>

<span data-ttu-id="00567-104">Os aplicativos usam os métodos da interface **ID3DXBaseMesh** para manipular e consultar malha e objetos de malha progressiva.</span><span class="sxs-lookup"><span data-stu-id="00567-104">Applications use the methods of the **ID3DXBaseMesh** interface to manipulate and query mesh and progressive mesh objects.</span></span>

## <a name="members"></a><span data-ttu-id="00567-105">Membros</span><span class="sxs-lookup"><span data-stu-id="00567-105">Members</span></span>

<span data-ttu-id="00567-106">A interface **ID3DXBaseMesh** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="00567-106">The **ID3DXBaseMesh** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="00567-107">**ID3DXBaseMesh** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="00567-107">**ID3DXBaseMesh** also has these types of members:</span></span>

-   [<span data-ttu-id="00567-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="00567-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="00567-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="00567-109">Methods</span></span>

<span data-ttu-id="00567-110">A interface **ID3DXBaseMesh** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="00567-110">The **ID3DXBaseMesh** interface has these methods.</span></span>



| <span data-ttu-id="00567-111">Método</span><span class="sxs-lookup"><span data-stu-id="00567-111">Method</span></span>                                                                            | <span data-ttu-id="00567-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="00567-112">Description</span></span>                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00567-113">**CloneMesh**</span><span class="sxs-lookup"><span data-stu-id="00567-113">**CloneMesh**</span></span>](id3dxbasemesh--clonemesh.md)                                     | <span data-ttu-id="00567-114">Clona uma malha usando um Declarador.</span><span class="sxs-lookup"><span data-stu-id="00567-114">Clones a mesh using a declarator.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="00567-115">**CloneMeshFVF**</span><span class="sxs-lookup"><span data-stu-id="00567-115">**CloneMeshFVF**</span></span>](id3dxbasemesh--clonemeshfvf.md)                               | <span data-ttu-id="00567-116">Clona uma malha usando um código de formato de vértice flexível (FVF).</span><span class="sxs-lookup"><span data-stu-id="00567-116">Clones a mesh using a flexible vertex format (FVF) code.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="00567-117">**ConvertAdjacencyToPointReps**</span><span class="sxs-lookup"><span data-stu-id="00567-117">**ConvertAdjacencyToPointReps**</span></span>](id3dxbasemesh--convertadjacencytopointreps.md) | <span data-ttu-id="00567-118">Converte informações de adjacência de malha em uma matriz de representantes de ponto.</span><span class="sxs-lookup"><span data-stu-id="00567-118">Converts mesh adjacency information to an array of point representatives.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="00567-119">**ConvertPointRepsToAdjacency**</span><span class="sxs-lookup"><span data-stu-id="00567-119">**ConvertPointRepsToAdjacency**</span></span>](id3dxbasemesh--convertpointrepstoadjacency.md) | <span data-ttu-id="00567-120">Converte dados representativos de ponto em informações de adjacência de malha.</span><span class="sxs-lookup"><span data-stu-id="00567-120">Converts point representative data to mesh adjacency information.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="00567-121">**DrawSubset**</span><span class="sxs-lookup"><span data-stu-id="00567-121">**DrawSubset**</span></span>](id3dxbasemesh--drawsubset.md)                                   | <span data-ttu-id="00567-122">Desenha um subconjunto de uma malha.</span><span class="sxs-lookup"><span data-stu-id="00567-122">Draws a subset of a mesh.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="00567-123">**GenerateAdjacency**</span><span class="sxs-lookup"><span data-stu-id="00567-123">**GenerateAdjacency**</span></span>](id3dxbasemesh--generateadjacency.md)                     | <span data-ttu-id="00567-124">Gere uma lista de bordas de malha, bem como uma lista de faces que compartilham cada borda.</span><span class="sxs-lookup"><span data-stu-id="00567-124">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="00567-125">**Getattributetable**</span><span class="sxs-lookup"><span data-stu-id="00567-125">**GetAttributeTable**</span></span>](id3dxbasemesh--getattributetable.md)                     | <span data-ttu-id="00567-126">Recupera uma tabela de atributos para uma malha ou o número de entradas armazenadas em uma tabela de atributos para uma malha.</span><span class="sxs-lookup"><span data-stu-id="00567-126">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span><br/>                                                                                          |
| [<span data-ttu-id="00567-127">**Getdeclaration**</span><span class="sxs-lookup"><span data-stu-id="00567-127">**GetDeclaration**</span></span>](id3dxbasemesh--getdeclaration.md)                           | <span data-ttu-id="00567-128">Recupera uma declaração que descreve os vértices na malha.</span><span class="sxs-lookup"><span data-stu-id="00567-128">Retrieves a declaration describing the vertices in the mesh.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="00567-129">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="00567-129">**GetDevice**</span></span>](id3dxbasemesh--getdevice.md)                                     | <span data-ttu-id="00567-130">Recupera o dispositivo associado à malha.</span><span class="sxs-lookup"><span data-stu-id="00567-130">Retrieves the device associated with the mesh.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="00567-131">**GetFVF**</span><span class="sxs-lookup"><span data-stu-id="00567-131">**GetFVF**</span></span>](id3dxbasemesh--getfvf.md)                                           | <span data-ttu-id="00567-132">Obtém o valor de vértice da função fixa.</span><span class="sxs-lookup"><span data-stu-id="00567-132">Gets the fixed function vertex value.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="00567-133">**GetIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="00567-133">**GetIndexBuffer**</span></span>](id3dxbasemesh--getindexbuffer.md)                           | <span data-ttu-id="00567-134">Recupera os dados em um buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="00567-134">Retrieves the data in an index buffer.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="00567-135">**GetNumBytesPerVertex**</span><span class="sxs-lookup"><span data-stu-id="00567-135">**GetNumBytesPerVertex**</span></span>](id3dxbasemesh--getnumbytespervertex.md)               | <span data-ttu-id="00567-136">Obtém o número de bytes por vértice.</span><span class="sxs-lookup"><span data-stu-id="00567-136">Gets the number of bytes per vertex.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="00567-137">**GetNumFaces**</span><span class="sxs-lookup"><span data-stu-id="00567-137">**GetNumFaces**</span></span>](id3dxbasemesh--getnumfaces.md)                                 | <span data-ttu-id="00567-138">Recupera o número de faces na malha.</span><span class="sxs-lookup"><span data-stu-id="00567-138">Retrieves the number of faces in the mesh.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="00567-139">**GetNumVertices**</span><span class="sxs-lookup"><span data-stu-id="00567-139">**GetNumVertices**</span></span>](id3dxbasemesh--getnumvertices.md)                           | <span data-ttu-id="00567-140">Recupera o número de vértices na malha.</span><span class="sxs-lookup"><span data-stu-id="00567-140">Retrieves the number of vertices in the mesh.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="00567-141">**Getoptions**</span><span class="sxs-lookup"><span data-stu-id="00567-141">**GetOptions**</span></span>](id3dxbasemesh--getoptions.md)                                   | <span data-ttu-id="00567-142">Recupera as opções de malha habilitadas para esta malha no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="00567-142">Retrieves the mesh options enabled for this mesh at creation time.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="00567-143">**GetVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="00567-143">**GetVertexBuffer**</span></span>](id3dxbasemesh--getvertexbuffer.md)                         | <span data-ttu-id="00567-144">Recupera o buffer de vértice associado à malha.</span><span class="sxs-lookup"><span data-stu-id="00567-144">Retrieves the vertex buffer associated with the mesh.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="00567-145">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="00567-145">**LockIndexBuffer**</span></span>](id3dxbasemesh--lockindexbuffer.md)                         | <span data-ttu-id="00567-146">Bloqueia um buffer de índice e Obtém um ponteiro para a memória do buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="00567-146">Locks an index buffer and obtains a pointer to the index buffer memory.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="00567-147">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="00567-147">**LockVertexBuffer**</span></span>](id3dxbasemesh--lockvertexbuffer.md)                       | <span data-ttu-id="00567-148">Bloqueia um buffer de vértice e Obtém um ponteiro para a memória de buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="00567-148">Locks a vertex buffer and obtains a pointer to the vertex buffer memory.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="00567-149">**UnlockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="00567-149">**UnlockIndexBuffer**</span></span>](id3dxbasemesh--unlockindexbuffer.md)                     | <span data-ttu-id="00567-150">Desbloqueia um buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="00567-150">Unlocks an index buffer.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="00567-151">**UnlockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="00567-151">**UnlockVertexBuffer**</span></span>](id3dxbasemesh--unlockvertexbuffer.md)                   | <span data-ttu-id="00567-152">Desbloqueia um buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="00567-152">Unlocks a vertex buffer.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="00567-153">**UpdateSemantics**</span><span class="sxs-lookup"><span data-stu-id="00567-153">**UpdateSemantics**</span></span>](id3dxbasemesh--updatesemantics.md)                         | <span data-ttu-id="00567-154">Esse método permite que o usuário altere a declaração de malha sem alterar o layout de dados do buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="00567-154">This method allows the user to change the mesh declaration without changing the data layout of the vertex buffer.</span></span> <span data-ttu-id="00567-155">A chamada será válida somente se os formatos de declaração antigo e novo tiverem o mesmo tamanho de vértice.</span><span class="sxs-lookup"><span data-stu-id="00567-155">The call is valid only if the old and new declaration formats have the same vertex size.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="00567-156">Comentários</span><span class="sxs-lookup"><span data-stu-id="00567-156">Remarks</span></span>

<span data-ttu-id="00567-157">Uma malha é um objeto composto por um conjunto de rostos Polygons.</span><span class="sxs-lookup"><span data-stu-id="00567-157">A mesh is an object made up of a set of polygonal faces.</span></span> <span data-ttu-id="00567-158">Uma malha define um conjunto de vértices e um conjunto de faces (as faces são definidas em termos de vértices e normais da malha).</span><span class="sxs-lookup"><span data-stu-id="00567-158">A mesh defines a set of vertices and a set of faces (the faces are defined in terms of the vertices and normals of the mesh).</span></span>

<span data-ttu-id="00567-159">O tipo LPD3DXBASEMESH é definido como um ponteiro para a interface **ID3DXBaseMesh** .</span><span class="sxs-lookup"><span data-stu-id="00567-159">The LPD3DXBASEMESH type is defined as a pointer to the **ID3DXBaseMesh** interface.</span></span>


```
typedef struct ID3DXBaseMesh *LPD3DXBASEMESH;
```



## <a name="requirements"></a><span data-ttu-id="00567-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00567-160">Requirements</span></span>



| <span data-ttu-id="00567-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="00567-161">Requirement</span></span> | <span data-ttu-id="00567-162">Valor</span><span class="sxs-lookup"><span data-stu-id="00567-162">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00567-163">parâmetro</span><span class="sxs-lookup"><span data-stu-id="00567-163">Header</span></span><br/>  | <dl> <span data-ttu-id="00567-164"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="00567-164"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="00567-165">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="00567-165">Library</span></span><br/> | <dl> <span data-ttu-id="00567-166"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00567-166"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="00567-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="00567-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00567-168">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="00567-168">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
