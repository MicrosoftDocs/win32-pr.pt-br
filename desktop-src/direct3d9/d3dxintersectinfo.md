---
description: Descreve uma interseção do Ray-triângulo.
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
ms.openlocfilehash: 31a98e9a7095e81e962b2996dedb9bdf5871533d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105782626"
---
# <a name="d3dxintersectinfo-structure"></a><span data-ttu-id="ab225-103">Estrutura D3DXINTERSECTINFO</span><span class="sxs-lookup"><span data-stu-id="ab225-103">D3DXINTERSECTINFO structure</span></span>

<span data-ttu-id="ab225-104">Descreve uma interseção do Ray-triângulo.</span><span class="sxs-lookup"><span data-stu-id="ab225-104">Describes a ray-triangle intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab225-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab225-105">Syntax</span></span>


```C++
typedef struct D3DXINTERSECTINFO {
  DWORD FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DXINTERSECTINFO, *LPD3DXINTERSECTINFO;
```



## <a name="members"></a><span data-ttu-id="ab225-106">Membros</span><span class="sxs-lookup"><span data-stu-id="ab225-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ab225-107">**FaceIndex**</span><span class="sxs-lookup"><span data-stu-id="ab225-107">**FaceIndex**</span></span>
</dt> <dd>

<span data-ttu-id="ab225-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab225-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ab225-109">Índice do triângulo que atingiu o raio.</span><span class="sxs-lookup"><span data-stu-id="ab225-109">Index of the triangle that hit the ray.</span></span>

</dd> <dt>

<span data-ttu-id="ab225-110">**U**</span><span class="sxs-lookup"><span data-stu-id="ab225-110">**U**</span></span>
</dt> <dd>

<span data-ttu-id="ab225-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab225-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ab225-112">Coordenada barycentric dentro do triângulo em que o Ray intersecciona.</span><span class="sxs-lookup"><span data-stu-id="ab225-112">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="ab225-113">**V**</span><span class="sxs-lookup"><span data-stu-id="ab225-113">**V**</span></span>
</dt> <dd>

<span data-ttu-id="ab225-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab225-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ab225-115">Coordenada barycentric dentro do triângulo em que o Ray intersecciona.</span><span class="sxs-lookup"><span data-stu-id="ab225-115">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="ab225-116">**Expo**</span><span class="sxs-lookup"><span data-stu-id="ab225-116">**Dist**</span></span>
</dt> <dd>

<span data-ttu-id="ab225-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab225-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ab225-118">Distância ao longo do raio onde a interseção ocorreu.</span><span class="sxs-lookup"><span data-stu-id="ab225-118">Distance along the ray where the intersection occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab225-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab225-119">Remarks</span></span>

<span data-ttu-id="ab225-120">As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo.</span><span class="sxs-lookup"><span data-stu-id="ab225-120">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="ab225-121">Para obter uma descrição mais detalhada das coordenadas de barycentric, consulte [Descrição de coordenadas barycentric do MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="ab225-121">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab225-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab225-122">Requirements</span></span>



| <span data-ttu-id="ab225-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab225-123">Requirement</span></span> | <span data-ttu-id="ab225-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ab225-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab225-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ab225-125">Header</span></span><br/> | <dl> <span data-ttu-id="ab225-126"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab225-126"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab225-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab225-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab225-128">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="ab225-128">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
