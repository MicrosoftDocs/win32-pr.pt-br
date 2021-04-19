---
description: Especifica o tipo de otimização de malha a ser executada.
ms.assetid: 32ef227a-b299-47c4-96b8-c0ea7bf549e1
title: Enumeração D3DXMESHOPT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXMESHOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: e7d4f9f4ae36cec74ea86fcb50a194ac66d0add7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105810624"
---
# <a name="d3dxmeshopt-enumeration"></a><span data-ttu-id="ec89b-103">Enumeração D3DXMESHOPT</span><span class="sxs-lookup"><span data-stu-id="ec89b-103">D3DXMESHOPT enumeration</span></span>

<span data-ttu-id="ec89b-104">Especifica o tipo de otimização de malha a ser executada.</span><span class="sxs-lookup"><span data-stu-id="ec89b-104">Specifies the type of mesh optimization to be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec89b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec89b-105">Syntax</span></span>


```C++
enum _D3DXMESHOPT {
  D3DXMESHOPT_COMPACT            = 0x01000000, 
  D3DXMESHOPT_ATTRSORT           = 0x02000000, 
  D3DXMESHOPT_VERTEXCACHE        = 0x04000000, 
  D3DXMESHOPT_STRIPREORDER       = 0x08000000, 
  D3DXMESHOPT_IGNOREVERTS        = 0x10000000, 
  D3DXMESHOPT_DONOTSPLIT         = 0x20000000, 
  D3DXMESHOPT_DEVICEINDEPENDENT  = 0x40000000 

};
```



## <a name="constants"></a><span data-ttu-id="ec89b-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="ec89b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ec89b-107"><span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT \_ Compact**</span><span class="sxs-lookup"><span data-stu-id="ec89b-107"><span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT\_COMPACT**</span></span>
</dt> <dd>

<span data-ttu-id="ec89b-108">Reordena os rostos para remover vértices e faces não utilizados.</span><span class="sxs-lookup"><span data-stu-id="ec89b-108">Reorders faces to remove unused vertices and faces.</span></span>

</dd> <dt>

<span data-ttu-id="ec89b-109"><span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT \_ ATTRSORT**</span><span class="sxs-lookup"><span data-stu-id="ec89b-109"><span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT\_ATTRSORT**</span></span>
</dt> <dd>

<span data-ttu-id="ec89b-110">Reordena os rostos para otimizar para menos alterações de estado de pacote de atributo e ID3DXBaseMesh aprimorada [**::D rawsubset**](id3dxbasemesh--drawsubset.md) desempenho.</span><span class="sxs-lookup"><span data-stu-id="ec89b-110">Reorders faces to optimize for fewer attribute bundle state changes and enhanced [**ID3DXBaseMesh::DrawSubset**](id3dxbasemesh--drawsubset.md) performance.</span></span>

</dd> <dt>

<span data-ttu-id="ec89b-111"><span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT \_ VERTEXCACHE**</span><span class="sxs-lookup"><span data-stu-id="ec89b-111"><span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT\_VERTEXCACHE**</span></span>
</dt> <dd>

<span data-ttu-id="ec89b-112">Reordena as faces para aumentar a taxa de acesso do cache de caches de vértice.</span><span class="sxs-lookup"><span data-stu-id="ec89b-112">Reorders faces to increase the cache hit rate of vertex caches.</span></span>

</dd> <dt>

<span data-ttu-id="ec89b-113"><span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT \_ STRIPREORDER**</span><span class="sxs-lookup"><span data-stu-id="ec89b-113"><span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT\_STRIPREORDER**</span></span>
</dt> <dd>

<span data-ttu-id="ec89b-114">Reordena os rostos para maximizar o comprimento dos triângulos adjacentes.</span><span class="sxs-lookup"><span data-stu-id="ec89b-114">Reorders faces to maximize length of adjacent triangles.</span></span>

</dd> <dt>

<span data-ttu-id="ec89b-115"><span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT \_ IGNOREVERTS**</span><span class="sxs-lookup"><span data-stu-id="ec89b-115"><span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT\_IGNOREVERTS**</span></span>
</dt> <dd>

<span data-ttu-id="ec89b-116">Otimizar apenas as faces; Não Otimize os vértices.</span><span class="sxs-lookup"><span data-stu-id="ec89b-116">Optimize the faces only; do not optimize the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="ec89b-117"><span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT \_ DONOTSPLIT**</span><span class="sxs-lookup"><span data-stu-id="ec89b-117"><span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT\_DONOTSPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="ec89b-118">Enquanto a classificação de atributo, não divida os vértices compartilhados entre os grupos de atributos.</span><span class="sxs-lookup"><span data-stu-id="ec89b-118">While attribute sorting, do not split vertices that are shared between attribute groups.</span></span>

</dd> <dt>

<span data-ttu-id="ec89b-119"><span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT \_ DEVICEINDEPENDENT**</span><span class="sxs-lookup"><span data-stu-id="ec89b-119"><span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT\_DEVICEINDEPENDENT**</span></span>
</dt> <dd>

<span data-ttu-id="ec89b-120">Afeta o tamanho do cache de vértice.</span><span class="sxs-lookup"><span data-stu-id="ec89b-120">Affects the vertex cache size.</span></span> <span data-ttu-id="ec89b-121">O uso desse sinalizador especifica um tamanho de cache de vértice padrão que funciona bem em hardware herdado.</span><span class="sxs-lookup"><span data-stu-id="ec89b-121">Using this flag specifies a default vertex cache size that works well on legacy hardware.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec89b-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec89b-122">Remarks</span></span>

<span data-ttu-id="ec89b-123">Os \_ sinalizadores de otimização D3DXMESHOPT STRIPREORDER e D3DXMESHOPT \_ VERTEXCACHE são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="ec89b-123">The D3DXMESHOPT\_STRIPREORDER and D3DXMESHOPT\_VERTEXCACHE optimization flags are mutually exclusive.</span></span>

<span data-ttu-id="ec89b-124">O \_ sinalizador D3DXMESHOPT SHAREVB foi removido desta enumeração.</span><span class="sxs-lookup"><span data-stu-id="ec89b-124">The D3DXMESHOPT\_SHAREVB flag has been removed from this enumeration.</span></span> <span data-ttu-id="ec89b-125">\_ \_ Em vez disso, use o compartilhamento vb do D3DXMESH, no [**D3DXMESH**](./d3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="ec89b-125">Use D3DXMESH\_VB\_SHARE instead, in [**D3DXMESH**](./d3dxmesh.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec89b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec89b-126">Requirements</span></span>



| <span data-ttu-id="ec89b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec89b-127">Requirement</span></span> | <span data-ttu-id="ec89b-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ec89b-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec89b-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ec89b-129">Header</span></span><br/> | <dl> <span data-ttu-id="ec89b-130"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec89b-130"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec89b-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec89b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec89b-132">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="ec89b-132">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
