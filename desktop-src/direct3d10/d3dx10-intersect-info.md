---
description: Descreve uma interseção do Ray-triângulo.
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
ms.openlocfilehash: 87490e734299cba57952bb43d1ee4ffad8e014c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664027"
---
# <a name="d3dx10_intersect_info-structure"></a><span data-ttu-id="defe7-103">\_Estrutura de informações de interseção D3DX10 \_</span><span class="sxs-lookup"><span data-stu-id="defe7-103">D3DX10\_INTERSECT\_INFO structure</span></span>

<span data-ttu-id="defe7-104">Descreve uma interseção do Ray-triângulo.</span><span class="sxs-lookup"><span data-stu-id="defe7-104">Describes a ray-triangle intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="defe7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="defe7-105">Syntax</span></span>


```C++
typedef struct D3DX10_INTERSECT_INFO {
  UINT  FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DX10_INTERSECT_INFO, *LPD3DX10_INTERSECT_INFO;
```



## <a name="members"></a><span data-ttu-id="defe7-106">Membros</span><span class="sxs-lookup"><span data-stu-id="defe7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="defe7-107">**FaceIndex**</span><span class="sxs-lookup"><span data-stu-id="defe7-107">**FaceIndex**</span></span>
</dt> <dd>

<span data-ttu-id="defe7-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="defe7-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="defe7-109">Índice do triângulo que atingiu o raio.</span><span class="sxs-lookup"><span data-stu-id="defe7-109">Index of the triangle that hit the ray.</span></span>

</dd> <dt>

<span data-ttu-id="defe7-110">**U**</span><span class="sxs-lookup"><span data-stu-id="defe7-110">**U**</span></span>
</dt> <dd>

<span data-ttu-id="defe7-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="defe7-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="defe7-112">Coordenada barycentric dentro do triângulo em que o Ray intersecciona.</span><span class="sxs-lookup"><span data-stu-id="defe7-112">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="defe7-113">**V**</span><span class="sxs-lookup"><span data-stu-id="defe7-113">**V**</span></span>
</dt> <dd>

<span data-ttu-id="defe7-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="defe7-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="defe7-115">Coordenada barycentric dentro do triângulo em que o Ray intersecciona.</span><span class="sxs-lookup"><span data-stu-id="defe7-115">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="defe7-116">**Expo**</span><span class="sxs-lookup"><span data-stu-id="defe7-116">**Dist**</span></span>
</dt> <dd>

<span data-ttu-id="defe7-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="defe7-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="defe7-118">Distância ao longo do raio onde a interseção ocorreu.</span><span class="sxs-lookup"><span data-stu-id="defe7-118">Distance along the ray where the intersection occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="defe7-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="defe7-119">Remarks</span></span>

<span data-ttu-id="defe7-120">As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo.</span><span class="sxs-lookup"><span data-stu-id="defe7-120">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="defe7-121">Para obter uma descrição mais detalhada das coordenadas de barycentric, consulte [Descrição de coordenadas barycentric do MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="defe7-121">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="defe7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="defe7-122">Requirements</span></span>



| <span data-ttu-id="defe7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="defe7-123">Requirement</span></span> | <span data-ttu-id="defe7-124">Valor</span><span class="sxs-lookup"><span data-stu-id="defe7-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="defe7-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="defe7-125">Header</span></span><br/> | <dl> <span data-ttu-id="defe7-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="defe7-126"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="defe7-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="defe7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="defe7-128">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="defe7-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
