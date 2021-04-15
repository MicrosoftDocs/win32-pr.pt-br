---
description: Meça o desempenho da taxa de acesso ao cache para texturas e vértices indexados.
ms.assetid: 70bc4e93-0a34-485b-bdcc-028c24b52f62
title: Estrutura de D3DDEVINFO_D3D9CACHEUTILIZATION (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9CACHEUTILIZATION
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 94f77549d0ea2a9c59d7de8367a6133085cc2771
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506465"
---
# <a name="d3ddevinfo_d3d9cacheutilization-structure"></a><span data-ttu-id="7d074-103">\_Estrutura D3DDEVINFO D3D9CACHEUTILIZATION</span><span class="sxs-lookup"><span data-stu-id="7d074-103">D3DDEVINFO\_D3D9CACHEUTILIZATION structure</span></span>

<span data-ttu-id="7d074-104">Meça o desempenho da taxa de acesso ao cache para texturas e vértices indexados.</span><span class="sxs-lookup"><span data-stu-id="7d074-104">Measure the cache hit rate performance for textures and indexed vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d074-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7d074-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9CACHEUTILIZATION {
  FLOAT TextureCacheHitRate;
  FLOAT PostTransformVertexCacheHitRate;
} D3DDEVINFO_D3D9CACHEUTILIZATION, *LPD3DDEVINFO_D3D9CACHEUTILIZATION;
```



## <a name="members"></a><span data-ttu-id="7d074-106">Membros</span><span class="sxs-lookup"><span data-stu-id="7d074-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7d074-107">**TextureCacheHitRate**</span><span class="sxs-lookup"><span data-stu-id="7d074-107">**TextureCacheHitRate**</span></span>
</dt> <dd>

<span data-ttu-id="7d074-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7d074-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7d074-109">A taxa de sucesso para localizar uma textura no cache de textura.</span><span class="sxs-lookup"><span data-stu-id="7d074-109">The hit rate for finding a texture in the texture cache.</span></span> <span data-ttu-id="7d074-110">Isso pressupõe que haja um cache de textura.</span><span class="sxs-lookup"><span data-stu-id="7d074-110">This assumes there is a texture cache.</span></span> <span data-ttu-id="7d074-111">Aumentar a tendência de nível de detalhe para usar a textura mais detalhada, usar muitas texturas grandes ou produzir um padrão de acesso de textura quase aleatória em texturas grandes com código de sombreador personalizado pode afetar drasticamente a taxa de sucesso do cache de textura.</span><span class="sxs-lookup"><span data-stu-id="7d074-111">Increasing the level-of-detail bias to use the most detailed texture, using many large textures, or producing a near random texture access pattern on large textures with custom shader code can dramatically affect the texture cache hit rate.</span></span>

</dd> <dt>

<span data-ttu-id="7d074-112">**PostTransformVertexCacheHitRate**</span><span class="sxs-lookup"><span data-stu-id="7d074-112">**PostTransformVertexCacheHitRate**</span></span>
</dt> <dd>

<span data-ttu-id="7d074-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7d074-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7d074-114">A taxa de sucesso para localizar vértices transformados no cache de vértice.</span><span class="sxs-lookup"><span data-stu-id="7d074-114">The hit rate for finding transformed vertices in the vertex cache.</span></span> <span data-ttu-id="7d074-115">A GPU é projetada para transformar vértices indexados e pode armazená-los em um cache de vértice.</span><span class="sxs-lookup"><span data-stu-id="7d074-115">The GPU is designed to transform indexed vertices and may store them in a vertex cache.</span></span> <span data-ttu-id="7d074-116">Se você estiver usando malhas, [**D3DXOptimizeFaces**](d3dxoptimizefaces.md) ou [**D3DXOptimizeVertices**](d3dxoptimizevertices.md) poderá resultar em melhor utilização de cache de vértice.</span><span class="sxs-lookup"><span data-stu-id="7d074-116">If you are using meshes, [**D3DXOptimizeFaces**](d3dxoptimizefaces.md) or [**D3DXOptimizeVertices**](d3dxoptimizevertices.md) may result in better vertex cache utilization.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d074-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d074-117">Remarks</span></span>

<span data-ttu-id="7d074-118">Um cache eficiente é geralmente mais próximo de uma taxa de impacto de 90% e um cache ineficiente geralmente é mais próximo de uma taxa de impacto de 10% (embora uma porcentagem baixa não seja necessariamente um problema).</span><span class="sxs-lookup"><span data-stu-id="7d074-118">An efficient cache is typically closer to a 90 percent hit rate, and an inefficient cache is typically closer to a 10 percent hit rate (although a low percentage is not necessarily a problem).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d074-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d074-119">Requirements</span></span>



| <span data-ttu-id="7d074-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d074-120">Requirement</span></span> | <span data-ttu-id="7d074-121">Valor</span><span class="sxs-lookup"><span data-stu-id="7d074-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d074-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7d074-122">Header</span></span><br/> | <dl> <span data-ttu-id="7d074-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d074-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d074-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d074-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d074-125">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="7d074-125">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="7d074-126">**GetData**</span><span class="sxs-lookup"><span data-stu-id="7d074-126">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
