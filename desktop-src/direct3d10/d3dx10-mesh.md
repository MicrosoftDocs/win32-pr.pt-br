---
description: Sinalizadores usados para especificar as opções de criação para uma malha.
ms.assetid: 1a5a6b3f-34f4-4338-9ffe-8f95f6f0c385
title: Enumeração de D3DX10_MESH (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESH
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: c2387024512a42c0a9e06ac1818b0282121cd0eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105786959"
---
# <a name="d3dx10_mesh-enumeration"></a><span data-ttu-id="db796-103">\_Enumeração de malha D3DX10</span><span class="sxs-lookup"><span data-stu-id="db796-103">D3DX10\_MESH enumeration</span></span>

<span data-ttu-id="db796-104">Sinalizadores usados para especificar as opções de criação para uma malha.</span><span class="sxs-lookup"><span data-stu-id="db796-104">Flags used to specify creation options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="db796-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db796-105">Syntax</span></span>


```C++
typedef enum D3DX10_MESH { 
  D3DX10_MESH_32_BIT        = 0x001,
  D3DX10_MESH_GS_ADJACENCY  = 0x004
} D3DX10_MESH, *LPD3DX10_MESH;
```



## <a name="constants"></a><span data-ttu-id="db796-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="db796-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="db796-107"><span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10 de \_ malha de \_ 32 \_ bits**</span><span class="sxs-lookup"><span data-stu-id="db796-107"><span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10\_MESH\_32\_BIT**</span></span>
</dt> <dd>

<span data-ttu-id="db796-108">A malha tem índices de 32 bits em vez de índices de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="db796-108">The mesh has 32-bit indices instead of 16-bit indices.</span></span> <span data-ttu-id="db796-109">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="db796-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="db796-110"><span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**\_Adjacência da malha D3DX10 \_ GS \_**</span><span class="sxs-lookup"><span data-stu-id="db796-110"><span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**D3DX10\_MESH\_GS\_ADJACENCY**</span></span>
</dt> <dd>

<span data-ttu-id="db796-111">Sinaliza que a malha contém dados de adjacência do sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="db796-111">Signals that the mesh contains geometry shader adjacency data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db796-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="db796-112">Remarks</span></span>

<span data-ttu-id="db796-113">Uma malha de 32 bits (D3DXMESH \_ 32bit) pode teoricamente dar suporte a (2 ³ ²)-1 rostos e vértices.</span><span class="sxs-lookup"><span data-stu-id="db796-113">A 32-bit mesh (D3DXMESH\_32BIT) can theoretically support (2³²)-1 faces and vertices.</span></span> <span data-ttu-id="db796-114">No entanto, a alocação de memória para uma malha grande em um sistema operacional de 32 bits não é prática.</span><span class="sxs-lookup"><span data-stu-id="db796-114">However, allocating memory for a mesh that large on a 32-bit operating system is not practical.</span></span>

## <a name="requirements"></a><span data-ttu-id="db796-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db796-115">Requirements</span></span>



| <span data-ttu-id="db796-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="db796-116">Requirement</span></span> | <span data-ttu-id="db796-117">Valor</span><span class="sxs-lookup"><span data-stu-id="db796-117">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db796-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="db796-118">Header</span></span><br/> | <dl> <span data-ttu-id="db796-119"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="db796-119"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db796-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="db796-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db796-121">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="db796-121">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




