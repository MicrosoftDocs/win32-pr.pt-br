---
description: Estrutura D3DXINTERSECTINFO-descreve uma interseção de Ray-triângulo.
ms.assetid: b6f50fc0-2c8a-4efa-a144-bd0851f8b0ca
title: Estrutura D3DXINTERSECTINFO (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXINTERSECTINFO
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: f4a63c7f4a479bfbe9dcb49f485ce0acb8db6486
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098284"
---
# <a name="d3dxintersectinfo-structure"></a><span data-ttu-id="c8dad-103">Estrutura D3DXINTERSECTINFO</span><span class="sxs-lookup"><span data-stu-id="c8dad-103">D3DXINTERSECTINFO structure</span></span>

<span data-ttu-id="c8dad-104">Descreve uma interseção do Ray-triângulo.</span><span class="sxs-lookup"><span data-stu-id="c8dad-104">Describes a ray-triangle intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8dad-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8dad-105">Syntax</span></span>


```C++
typedef struct D3DXINTERSECTINFO {
  DWORD FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DXINTERSECTINFO, *LPD3DXINTERSECTINFO;
```



## <a name="members"></a><span data-ttu-id="c8dad-106">Membros</span><span class="sxs-lookup"><span data-stu-id="c8dad-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c8dad-107">**FaceIndex**</span><span class="sxs-lookup"><span data-stu-id="c8dad-107">**FaceIndex**</span></span>
</dt> <dd>

<span data-ttu-id="c8dad-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8dad-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c8dad-109">Índice do triângulo que atingiu o raio.</span><span class="sxs-lookup"><span data-stu-id="c8dad-109">Index of the triangle that hit the ray.</span></span>

</dd> <dt>

<span data-ttu-id="c8dad-110">**U**</span><span class="sxs-lookup"><span data-stu-id="c8dad-110">**U**</span></span>
</dt> <dd>

<span data-ttu-id="c8dad-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8dad-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c8dad-112">Coordenada barycentric dentro do triângulo em que o Ray intersecciona.</span><span class="sxs-lookup"><span data-stu-id="c8dad-112">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="c8dad-113">**V**</span><span class="sxs-lookup"><span data-stu-id="c8dad-113">**V**</span></span>
</dt> <dd>

<span data-ttu-id="c8dad-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8dad-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c8dad-115">Coordenada barycentric dentro do triângulo em que o Ray intersecciona.</span><span class="sxs-lookup"><span data-stu-id="c8dad-115">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="c8dad-116">**Expo**</span><span class="sxs-lookup"><span data-stu-id="c8dad-116">**Dist**</span></span>
</dt> <dd>

<span data-ttu-id="c8dad-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8dad-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c8dad-118">Distância ao longo do raio onde a interseção ocorreu.</span><span class="sxs-lookup"><span data-stu-id="c8dad-118">Distance along the ray where the intersection occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8dad-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8dad-119">Remarks</span></span>

<span data-ttu-id="c8dad-120">As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo.</span><span class="sxs-lookup"><span data-stu-id="c8dad-120">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="c8dad-121">Para obter uma descrição mais detalhada das coordenadas de barycentric, consulte [Descrição de coordenadas barycentric do MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="c8dad-121">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8dad-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8dad-122">Requirements</span></span>



| <span data-ttu-id="c8dad-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8dad-123">Requirement</span></span> | <span data-ttu-id="c8dad-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c8dad-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8dad-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c8dad-125">Header</span></span><br/> | <dl> <span data-ttu-id="c8dad-126"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8dad-126"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8dad-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c8dad-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8dad-128">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="c8dad-128">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
