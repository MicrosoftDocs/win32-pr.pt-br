---
description: Enumeração de D3DX10_MESHOPT-especifica o tipo de otimização de malha a ser executada.
ms.assetid: 20d1da8c-8c3d-4045-9a37-d534a8682716
title: Enumeração de D3DX10_MESHOPT (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESHOPT
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: 7b3085cf9970f2c1f6fe3748cc4db8f4fb2b2a78
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105444"
---
# <a name="d3dx10_meshopt-enumeration"></a><span data-ttu-id="b2075-103">\_Enumeração D3DX10 MESHOPT</span><span class="sxs-lookup"><span data-stu-id="b2075-103">D3DX10\_MESHOPT enumeration</span></span>

<span data-ttu-id="b2075-104">Especifica o tipo de otimização de malha a ser executada.</span><span class="sxs-lookup"><span data-stu-id="b2075-104">Specifies the type of mesh optimization to be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2075-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2075-105">Syntax</span></span>


```C++
typedef enum D3DX10_MESHOPT { 
  D3DX10_MESHOPT_COMPACT             = 0x01000000,
  D3DX10_MESHOPT_ATTR_SORT           = 0x02000000,
  D3DX10_MESHOPT_VERTEX_CACHE        = 0x04000000,
  D3DX10_MESHOPT_STRIP_REORDER       = 0x08000000,
  D3DX10_MESHOPT_IGNORE_VERTS        = 0x10000000,
  D3DX10_MESHOPT_DO_NOT_SPLIT        = 0x20000000,
  D3DX10_MESHOPT_DEVICE_INDEPENDENT  = 0x00400000
} D3DX10_MESHOPT, *LPD3DX10_MESHOPT;
```



## <a name="constants"></a><span data-ttu-id="b2075-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="b2075-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b2075-107"><span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10 \_ MESHOPT \_ Compact**</span><span class="sxs-lookup"><span data-stu-id="b2075-107"><span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10\_MESHOPT\_COMPACT**</span></span>
</dt> <dd>

<span data-ttu-id="b2075-108">Reordena os rostos para remover vértices e faces não utilizados.</span><span class="sxs-lookup"><span data-stu-id="b2075-108">Reorders faces to remove unused vertices and faces.</span></span>

</dd> <dt>

<span data-ttu-id="b2075-109"><span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**\_Classificação D3DX10 MESHOPT \_ attr \_**</span><span class="sxs-lookup"><span data-stu-id="b2075-109"><span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10\_MESHOPT\_ATTR\_SORT**</span></span>
</dt> <dd>

<span data-ttu-id="b2075-110">Reordena os rostos para otimizar para menos alterações de estado de pacote de atributo e desempenho de DrawSubset aprimorado.</span><span class="sxs-lookup"><span data-stu-id="b2075-110">Reorders faces to optimize for fewer attribute bundle state changes and enhanced DrawSubset performance.</span></span>

</dd> <dt>

<span data-ttu-id="b2075-111"><span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**\_Cache de \_ vértice D3DX10 MESHOPT \_**</span><span class="sxs-lookup"><span data-stu-id="b2075-111"><span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**D3DX10\_MESHOPT\_VERTEX\_CACHE**</span></span>
</dt> <dd>

<span data-ttu-id="b2075-112">Reordena as faces para aumentar a taxa de acesso do cache de caches de vértice.</span><span class="sxs-lookup"><span data-stu-id="b2075-112">Reorders faces to increase the cache hit rate of vertex caches.</span></span>

</dd> <dt>

<span data-ttu-id="b2075-113"><span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**\_REordenar D3DX10 MESHOPT \_ strip \_**</span><span class="sxs-lookup"><span data-stu-id="b2075-113"><span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**D3DX10\_MESHOPT\_STRIP\_REORDER**</span></span>
</dt> <dd>

<span data-ttu-id="b2075-114">Reordena os rostos para maximizar o comprimento dos triângulos adjacentes.</span><span class="sxs-lookup"><span data-stu-id="b2075-114">Reorders faces to maximize length of adjacent triangles.</span></span>

</dd> <dt>

<span data-ttu-id="b2075-115"><span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10 \_ MESHOPT \_ ignorar \_ reverte**</span><span class="sxs-lookup"><span data-stu-id="b2075-115"><span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10\_MESHOPT\_IGNORE\_VERTS**</span></span>
</dt> <dd>

<span data-ttu-id="b2075-116">Otimizar apenas as faces; Não Otimize os vértices.</span><span class="sxs-lookup"><span data-stu-id="b2075-116">Optimize the faces only; do not optimize the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="b2075-117"><span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10 \_ MESHOPT \_ \_ não \_ divide**</span><span class="sxs-lookup"><span data-stu-id="b2075-117"><span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10\_MESHOPT\_DO\_NOT\_SPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="b2075-118">Enquanto a classificação de atributo, não divida os vértices compartilhados entre os grupos de atributos.</span><span class="sxs-lookup"><span data-stu-id="b2075-118">While attribute sorting, do not split vertices that are shared between attribute groups.</span></span>

</dd> <dt>

<span data-ttu-id="b2075-119"><span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**D3DX10 \_ MESHOPT \_ dispositivo \_ independente**</span><span class="sxs-lookup"><span data-stu-id="b2075-119"><span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**D3DX10\_MESHOPT\_DEVICE\_INDEPENDENT**</span></span>
</dt> <dd>

<span data-ttu-id="b2075-120">Afeta o tamanho do cache de vértice.</span><span class="sxs-lookup"><span data-stu-id="b2075-120">Affects the vertex cache size.</span></span> <span data-ttu-id="b2075-121">O uso desse sinalizador especifica um tamanho de cache de vértice padrão que funciona bem em hardware herdado.</span><span class="sxs-lookup"><span data-stu-id="b2075-121">Using this flag specifies a default vertex cache size that works well on legacy hardware.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2075-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2075-122">Remarks</span></span>

<span data-ttu-id="b2075-123">Os \_ sinalizadores de otimização D3DXMESHOPT STRIPREORDER e D3DXMESHOPT \_ VERTEXCACHE são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="b2075-123">The D3DXMESHOPT\_STRIPREORDER and D3DXMESHOPT\_VERTEXCACHE optimization flags are mutually exclusive.</span></span>

<span data-ttu-id="b2075-124">O \_ sinalizador D3DXMESHOPT SHAREVB foi removido desta enumeração.</span><span class="sxs-lookup"><span data-stu-id="b2075-124">The D3DXMESHOPT\_SHAREVB flag has been removed from this enumeration.</span></span> <span data-ttu-id="b2075-125">\_ \_ Em vez disso, use o compartilhamento vb do D3DXMESH, no D3DXMESH.</span><span class="sxs-lookup"><span data-stu-id="b2075-125">Use D3DXMESH\_VB\_SHARE instead, in D3DXMESH.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2075-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2075-126">Requirements</span></span>



| <span data-ttu-id="b2075-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2075-127">Requirement</span></span> | <span data-ttu-id="b2075-128">Valor</span><span class="sxs-lookup"><span data-stu-id="b2075-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2075-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b2075-129">Header</span></span><br/> | <dl> <span data-ttu-id="b2075-130"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2075-130"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2075-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b2075-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2075-132">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="b2075-132">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




