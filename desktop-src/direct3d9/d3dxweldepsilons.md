---
description: Estrutura D3DXWELDEPSILONS – especifica valores de tolerância para cada componente de vértice ao comparar vértices para determinar se eles são semelhantes o suficiente para serem soldados juntos.
ms.assetid: 534903da-ff65-4629-9be9-66c9daed6ef5
title: Estrutura D3DXWELDEPSILONS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWELDEPSILONS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: bb11e6f5481b1adf7cc1bac58edf40d4ac770e92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115494"
---
# <a name="d3dxweldepsilons-structure"></a><span data-ttu-id="40075-103">Estrutura D3DXWELDEPSILONS</span><span class="sxs-lookup"><span data-stu-id="40075-103">D3DXWELDEPSILONS structure</span></span>

<span data-ttu-id="40075-104">Especifica os valores de tolerância para cada componente de vértice ao comparar vértices para determinar se eles são semelhantes o suficiente para serem soldados juntos.</span><span class="sxs-lookup"><span data-stu-id="40075-104">Specifies tolerance values for each vertex component when comparing vertices to determine if they are similar enough to be welded together.</span></span>

## <a name="syntax"></a><span data-ttu-id="40075-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40075-105">Syntax</span></span>


```C++
typedef struct _D3DXWELDEPSILONS {
  FLOAT Position;
  FLOAT BlendWeights;
  FLOAT Normal;
  FLOAT PSize;
  FLOAT Specular;
  FLOAT Diffuse;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
  FLOAT TessFactor;
} D3DXWELDEPSILONS, *LPD3DXWELDEPSILONS;
```



## <a name="members"></a><span data-ttu-id="40075-106">Membros</span><span class="sxs-lookup"><span data-stu-id="40075-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="40075-107">**Posição**</span><span class="sxs-lookup"><span data-stu-id="40075-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="40075-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40075-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="40075-109">Posição</span><span class="sxs-lookup"><span data-stu-id="40075-109">Position</span></span>

</dd> <dt>

<span data-ttu-id="40075-110">**BlendWeights**</span><span class="sxs-lookup"><span data-stu-id="40075-110">**BlendWeights**</span></span>
</dt> <dd>

<span data-ttu-id="40075-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40075-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="40075-112">Peso de mistura</span><span class="sxs-lookup"><span data-stu-id="40075-112">Blend weight</span></span>

</dd> <dt>

<span data-ttu-id="40075-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="40075-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="40075-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40075-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="40075-115">Normal</span><span class="sxs-lookup"><span data-stu-id="40075-115">Normal</span></span>

</dd> <dt>

<span data-ttu-id="40075-116">**PSize**</span><span class="sxs-lookup"><span data-stu-id="40075-116">**PSize**</span></span>
</dt> <dd>

<span data-ttu-id="40075-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40075-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="40075-118">Valor do tamanho do ponto</span><span class="sxs-lookup"><span data-stu-id="40075-118">Point size value</span></span>

</dd> <dt>

<span data-ttu-id="40075-119">**Especular**</span><span class="sxs-lookup"><span data-stu-id="40075-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="40075-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40075-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="40075-121">Valor de iluminação especular</span><span class="sxs-lookup"><span data-stu-id="40075-121">Specular lighting value</span></span>

</dd> <dt>

<span data-ttu-id="40075-122">**Difusa**</span><span class="sxs-lookup"><span data-stu-id="40075-122">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="40075-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40075-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="40075-124">Valor de iluminação difusa</span><span class="sxs-lookup"><span data-stu-id="40075-124">Diffuse lighting value</span></span>

</dd> <dt>

<span data-ttu-id="40075-125">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="40075-125">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="40075-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40075-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="40075-127">Oito coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="40075-127">Eight texture coordinates</span></span>

</dd> <dt>

<span data-ttu-id="40075-128">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="40075-128">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="40075-129">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40075-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="40075-130">Tangente</span><span class="sxs-lookup"><span data-stu-id="40075-130">Tangent</span></span>

</dd> <dt>

<span data-ttu-id="40075-131">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="40075-131">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="40075-132">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40075-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="40075-133">Binormal</span><span class="sxs-lookup"><span data-stu-id="40075-133">Binormal</span></span>

</dd> <dt>

<span data-ttu-id="40075-134">**TessFactor**</span><span class="sxs-lookup"><span data-stu-id="40075-134">**TessFactor**</span></span>
</dt> <dd>

<span data-ttu-id="40075-135">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40075-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="40075-136">Fator de mosaico</span><span class="sxs-lookup"><span data-stu-id="40075-136">Tessellation factor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40075-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="40075-137">Remarks</span></span>

<span data-ttu-id="40075-138">O tipo LPD3DXWELDEPSILONS é definido como um ponteiro para a estrutura **D3DXWELDEPSILONS** .</span><span class="sxs-lookup"><span data-stu-id="40075-138">The LPD3DXWELDEPSILONS type is defined as a pointer to the **D3DXWELDEPSILONS** structure.</span></span>


```
typedef D3DXWELDEPSILONS *LPD3DXWELDEPSILONS;
```



## <a name="requirements"></a><span data-ttu-id="40075-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40075-139">Requirements</span></span>



| <span data-ttu-id="40075-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="40075-140">Requirement</span></span> | <span data-ttu-id="40075-141">Valor</span><span class="sxs-lookup"><span data-stu-id="40075-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40075-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="40075-142">Header</span></span><br/> | <dl> <span data-ttu-id="40075-143"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="40075-143"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40075-144">Consulte também</span><span class="sxs-lookup"><span data-stu-id="40075-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40075-145">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="40075-145">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="40075-146">**D3DXWeldVertices**</span><span class="sxs-lookup"><span data-stu-id="40075-146">**D3DXWeldVertices**</span></span>](d3dxweldvertices.md)
</dt> </dl>

 

 
