---
description: Define operações a serem executadas em vértices em preparação para limpeza de malha.
ms.assetid: f222acaa-fa82-4591-b7c2-b520cb648ed5
title: Enumeração D3DXCLEANTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCLEANTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: b38578d0f50521def552b8bd6608c2696b405d0f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173045"
---
# <a name="d3dxcleantype-enumeration"></a><span data-ttu-id="385e5-103">Enumeração D3DXCLEANTYPE</span><span class="sxs-lookup"><span data-stu-id="385e5-103">D3DXCLEANTYPE enumeration</span></span>

<span data-ttu-id="385e5-104">Define operações a serem executadas em vértices em preparação para limpeza de malha.</span><span class="sxs-lookup"><span data-stu-id="385e5-104">Defines operations to perform on vertices in preparation for mesh cleaning.</span></span>

## <a name="syntax"></a><span data-ttu-id="385e5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="385e5-105">Syntax</span></span>


```C++
typedef enum D3DXCLEANTYPE { 
  D3DXCLEAN_BACKFACING      = 1,
  D3DXCLEAN_BOWTIES         = 2,
  D3DXCLEAN_SKINNING        = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_OPTIMIZATION    = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_SIMPLIFICATION  = D3DXCLEAN_BACKFACING | D3DXCLEAN_BOWTIES
} D3DXCLEANTYPE, *LPD3DXCLEANTYPE;
```



## <a name="constants"></a><span data-ttu-id="385e5-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="385e5-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="385e5-107"><span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**\_Volta D3DXCLEAN**</span><span class="sxs-lookup"><span data-stu-id="385e5-107"><span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**D3DXCLEAN\_BACKFACING**</span></span>
</dt> <dd>

<span data-ttu-id="385e5-108">Mescle triângulos que compartilham os mesmos índices de vértice, mas que têm normalidades de face apontando para direções opostas (triângulos voltados para o verso).</span><span class="sxs-lookup"><span data-stu-id="385e5-108">Merge triangles that share the same vertex indices but have face normals pointing in opposite directions (back-facing triangles).</span></span> <span data-ttu-id="385e5-109">A menos que os triângulos não sejam divididos adicionando um vértice replicado, os dados de adjacência da malha dos dois triângulos podem entrar em conflito.</span><span class="sxs-lookup"><span data-stu-id="385e5-109">Unless the triangles are not split by adding a replicated vertex, mesh adjacency data from the two triangles may conflict.</span></span>

</dd> <dt>

<span data-ttu-id="385e5-110"><span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**D3DXCLEAN \_ BOWTIES**</span><span class="sxs-lookup"><span data-stu-id="385e5-110"><span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**D3DXCLEAN\_BOWTIES**</span></span>
</dt> <dd>

<span data-ttu-id="385e5-111">Se um vértice for o Apex de dois fãs de triângulo (um bowtie) e operações de malha afetarão um dos ventiladores, dividirá o vértice compartilhado em dois novos vértices.</span><span class="sxs-lookup"><span data-stu-id="385e5-111">If a vertex is the apex of two triangle fans (a bowtie) and mesh operations will affect one of the fans, then split the shared vertex into two new vertices.</span></span> <span data-ttu-id="385e5-112">O bowties pode causar problemas para operações como a simplificação da malha que Remove vértices, porque a remoção de um vértice afeta dois conjuntos distintos de triângulos.</span><span class="sxs-lookup"><span data-stu-id="385e5-112">Bowties can cause problems for operations such as mesh simplification that remove vertices, because removing one vertex affects two distinct sets of triangles.</span></span>

</dd> <dt>

<span data-ttu-id="385e5-113"><span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**D3DXCLEAN de \_ aparência**</span><span class="sxs-lookup"><span data-stu-id="385e5-113"><span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**D3DXCLEAN\_SKINNING**</span></span>
</dt> <dd>

<span data-ttu-id="385e5-114">Use esse sinalizador para evitar loops infinitos durante as operações de malha da configuração de revestimento.</span><span class="sxs-lookup"><span data-stu-id="385e5-114">Use this flag to prevent infinite loops during skinning setup mesh operations.</span></span>

</dd> <dt>

<span data-ttu-id="385e5-115"><span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**Otimização de D3DXCLEAN \_**</span><span class="sxs-lookup"><span data-stu-id="385e5-115"><span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**D3DXCLEAN\_OPTIMIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="385e5-116">Use esse sinalizador para evitar loops infinitos durante operações de otimização de malha.</span><span class="sxs-lookup"><span data-stu-id="385e5-116">Use this flag to prevent infinite loops during mesh optimization operations.</span></span>

</dd> <dt>

<span data-ttu-id="385e5-117"><span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**\_Simplificação de D3DXCLEAN**</span><span class="sxs-lookup"><span data-stu-id="385e5-117"><span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**D3DXCLEAN\_SIMPLIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="385e5-118">Use esse sinalizador para evitar loops infinitos durante operações de simplificação de malha.</span><span class="sxs-lookup"><span data-stu-id="385e5-118">Use this flag to prevent infinite loops during mesh simplification operations.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="385e5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="385e5-119">Requirements</span></span>



| <span data-ttu-id="385e5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="385e5-120">Requirement</span></span> | <span data-ttu-id="385e5-121">Valor</span><span class="sxs-lookup"><span data-stu-id="385e5-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="385e5-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="385e5-122">Header</span></span><br/> | <dl> <span data-ttu-id="385e5-123"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="385e5-123"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="385e5-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="385e5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="385e5-125">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="385e5-125">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




