---
description: Estrutura D3DX10_INTERSECT_INFO-descreve uma interseção Ray-triângulo.
ms.assetid: 21658b74-6f1d-4a16-a8b3-0c7bb6edf899
title: Estrutura de D3DX10_INTERSECT_INFO (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_INTERSECT_INFO
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 203daa48e766edd545bf232c4f8d94c4f17b5b2a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105454"
---
# <a name="d3dx10_intersect_info-structure"></a><span data-ttu-id="8d165-103">\_Estrutura de informações de interseção D3DX10 \_</span><span class="sxs-lookup"><span data-stu-id="8d165-103">D3DX10\_INTERSECT\_INFO structure</span></span>

<span data-ttu-id="8d165-104">Descreve uma interseção do Ray-triângulo.</span><span class="sxs-lookup"><span data-stu-id="8d165-104">Describes a ray-triangle intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d165-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d165-105">Syntax</span></span>


```C++
typedef struct D3DX10_INTERSECT_INFO {
  UINT  FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DX10_INTERSECT_INFO, *LPD3DX10_INTERSECT_INFO;
```



## <a name="members"></a><span data-ttu-id="8d165-106">Membros</span><span class="sxs-lookup"><span data-stu-id="8d165-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8d165-107">**FaceIndex**</span><span class="sxs-lookup"><span data-stu-id="8d165-107">**FaceIndex**</span></span>
</dt> <dd>

<span data-ttu-id="8d165-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d165-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8d165-109">Índice do triângulo que atingiu o raio.</span><span class="sxs-lookup"><span data-stu-id="8d165-109">Index of the triangle that hit the ray.</span></span>

</dd> <dt>

<span data-ttu-id="8d165-110">**U**</span><span class="sxs-lookup"><span data-stu-id="8d165-110">**U**</span></span>
</dt> <dd>

<span data-ttu-id="8d165-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d165-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8d165-112">Coordenada barycentric dentro do triângulo em que o Ray intersecciona.</span><span class="sxs-lookup"><span data-stu-id="8d165-112">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="8d165-113">**V**</span><span class="sxs-lookup"><span data-stu-id="8d165-113">**V**</span></span>
</dt> <dd>

<span data-ttu-id="8d165-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d165-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8d165-115">Coordenada barycentric dentro do triângulo em que o Ray intersecciona.</span><span class="sxs-lookup"><span data-stu-id="8d165-115">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="8d165-116">**Expo**</span><span class="sxs-lookup"><span data-stu-id="8d165-116">**Dist**</span></span>
</dt> <dd>

<span data-ttu-id="8d165-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d165-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8d165-118">Distância ao longo do raio onde a interseção ocorreu.</span><span class="sxs-lookup"><span data-stu-id="8d165-118">Distance along the ray where the intersection occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d165-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d165-119">Remarks</span></span>

<span data-ttu-id="8d165-120">As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo.</span><span class="sxs-lookup"><span data-stu-id="8d165-120">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="8d165-121">Para obter uma descrição mais detalhada das coordenadas de barycentric, consulte [Descrição de coordenadas barycentric do MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="8d165-121">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d165-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d165-122">Requirements</span></span>



| <span data-ttu-id="8d165-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d165-123">Requirement</span></span> | <span data-ttu-id="8d165-124">Valor</span><span class="sxs-lookup"><span data-stu-id="8d165-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8d165-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8d165-125">Header</span></span><br/> | <dl> <span data-ttu-id="8d165-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d165-126"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d165-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8d165-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d165-128">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="8d165-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
