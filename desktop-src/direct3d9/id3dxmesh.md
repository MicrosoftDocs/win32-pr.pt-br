---
description: Os aplicativos usam os métodos da interface ID3DXMesh para manipular objetos de malha.
ms.assetid: f571fe0b-3f0c-43c9-809c-d1e14f85b720
title: Interface ID3DXMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c2a677edba4bad5e908b6dd69aa21a467b2a245
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298792"
---
# <a name="id3dxmesh-interface"></a><span data-ttu-id="20c8a-103">Interface ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="20c8a-103">ID3DXMesh interface</span></span>

<span data-ttu-id="20c8a-104">Os aplicativos usam os métodos da interface ID3DXMesh para manipular objetos de malha.</span><span class="sxs-lookup"><span data-stu-id="20c8a-104">Applications use the methods of the ID3DXMesh interface to manipulate mesh objects.</span></span>

## <a name="members"></a><span data-ttu-id="20c8a-105">Membros</span><span class="sxs-lookup"><span data-stu-id="20c8a-105">Members</span></span>

<span data-ttu-id="20c8a-106">A interface **ID3DXMesh** herda de [**ID3DXBaseMesh**](id3dxbasemesh.md).</span><span class="sxs-lookup"><span data-stu-id="20c8a-106">The **ID3DXMesh** interface inherits from [**ID3DXBaseMesh**](id3dxbasemesh.md).</span></span> <span data-ttu-id="20c8a-107">**ID3DXMesh** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="20c8a-107">**ID3DXMesh** also has these types of members:</span></span>

-   [<span data-ttu-id="20c8a-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="20c8a-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="20c8a-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="20c8a-109">Methods</span></span>

<span data-ttu-id="20c8a-110">A interface **ID3DXMesh** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="20c8a-110">The **ID3DXMesh** interface has these methods.</span></span>



| <span data-ttu-id="20c8a-111">Método</span><span class="sxs-lookup"><span data-stu-id="20c8a-111">Method</span></span>                                                            | <span data-ttu-id="20c8a-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="20c8a-112">Description</span></span>                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20c8a-113">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="20c8a-113">**LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)     | <span data-ttu-id="20c8a-114">Bloqueia o buffer de malha que contém os dados de atributo de malha e retorna um ponteiro para ele.</span><span class="sxs-lookup"><span data-stu-id="20c8a-114">Locks the mesh buffer that contains the mesh attribute data, and returns a pointer to it.</span></span><br/>                                   |
| [<span data-ttu-id="20c8a-115">**Otimizar**</span><span class="sxs-lookup"><span data-stu-id="20c8a-115">**Optimize**</span></span>](id3dxmesh--optimize.md)                           | <span data-ttu-id="20c8a-116">Gera uma nova malha com faces e vértices reordenados para otimizar o desempenho do desenho.</span><span class="sxs-lookup"><span data-stu-id="20c8a-116">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span><br/>                                     |
| [<span data-ttu-id="20c8a-117">**OptimizeInplace**</span><span class="sxs-lookup"><span data-stu-id="20c8a-117">**OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)             | <span data-ttu-id="20c8a-118">Gera uma malha com faces e vértices reordenados para otimizar o desempenho do desenho.</span><span class="sxs-lookup"><span data-stu-id="20c8a-118">Generates a mesh with reordered faces and vertices to optimize drawing performance.</span></span> <span data-ttu-id="20c8a-119">Esse método reordena a malha existente.</span><span class="sxs-lookup"><span data-stu-id="20c8a-119">This method reorders the existing mesh.</span></span><br/> |
| [<span data-ttu-id="20c8a-120">**SetAttributeTable**</span><span class="sxs-lookup"><span data-stu-id="20c8a-120">**SetAttributeTable**</span></span>](id3dxmesh--setattributetable.md)         | <span data-ttu-id="20c8a-121">Define a tabela de atributos para uma malha e o número de entradas armazenadas na tabela.</span><span class="sxs-lookup"><span data-stu-id="20c8a-121">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span><br/>                                          |
| [<span data-ttu-id="20c8a-122">**UnlockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="20c8a-122">**UnlockAttributeBuffer**</span></span>](id3dxmesh--unlockattributebuffer.md) | <span data-ttu-id="20c8a-123">Desbloqueia um buffer de atributo.</span><span class="sxs-lookup"><span data-stu-id="20c8a-123">Unlocks an attribute buffer.</span></span><br/>                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="20c8a-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="20c8a-124">Remarks</span></span>

<span data-ttu-id="20c8a-125">Para obter a interface **ID3DXMesh** , chame a função [**D3DXCreateMesh**](d3dxcreatemesh.md) ou [**D3DXCreateMeshFVF**](d3dxcreatemeshfvf.md) .</span><span class="sxs-lookup"><span data-stu-id="20c8a-125">To obtain the **ID3DXMesh** interface, call either the [**D3DXCreateMesh**](d3dxcreatemesh.md) or [**D3DXCreateMeshFVF**](d3dxcreatemeshfvf.md) function.</span></span>

<span data-ttu-id="20c8a-126">Essa interface herda a funcionalidade adicional da interface [**ID3DXBaseMesh**](id3dxbasemesh.md) .</span><span class="sxs-lookup"><span data-stu-id="20c8a-126">This interface inherits additional functionality from the [**ID3DXBaseMesh**](id3dxbasemesh.md) interface.</span></span>

<span data-ttu-id="20c8a-127">O tipo LPD3DXMESH é definido como um ponteiro para a interface **ID3DXMesh** .</span><span class="sxs-lookup"><span data-stu-id="20c8a-127">The LPD3DXMESH type is defined as a pointer to the **ID3DXMesh** interface.</span></span>


```
typedef struct ID3DXMesh *LPD3DXMESH;
```



## <a name="requirements"></a><span data-ttu-id="20c8a-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20c8a-128">Requirements</span></span>



| <span data-ttu-id="20c8a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="20c8a-129">Requirement</span></span> | <span data-ttu-id="20c8a-130">Valor</span><span class="sxs-lookup"><span data-stu-id="20c8a-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="20c8a-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="20c8a-131">Header</span></span><br/>  | <dl> <span data-ttu-id="20c8a-132"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="20c8a-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="20c8a-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="20c8a-133">Library</span></span><br/> | <dl> <span data-ttu-id="20c8a-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20c8a-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="20c8a-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="20c8a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20c8a-136">**ID3DXBaseMesh**</span><span class="sxs-lookup"><span data-stu-id="20c8a-136">**ID3DXBaseMesh**</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="20c8a-137">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="20c8a-137">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="20c8a-138">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="20c8a-138">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




