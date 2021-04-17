---
description: Especifica os valores de tolerância para cada componente de vértice ao comparar vértices para determinar se eles são semelhantes o suficiente para serem soldados juntos.
ms.assetid: b28a17bd-5d5b-41b3-86d9-327f5497fc94
title: Estrutura de D3DX10_WELD_EPSILONS (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_WELD_EPSILONS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: c72f63e3ecef1fdb193fcaec9220f9768204d099
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798018"
---
# <a name="d3dx10_weld_epsilons-structure"></a><span data-ttu-id="38b36-103">Estrutura de 13 de \_ solda de D3DX10 \_</span><span class="sxs-lookup"><span data-stu-id="38b36-103">D3DX10\_WELD\_EPSILONS structure</span></span>

<span data-ttu-id="38b36-104">Especifica os valores de tolerância para cada componente de vértice ao comparar vértices para determinar se eles são semelhantes o suficiente para serem soldados juntos.</span><span class="sxs-lookup"><span data-stu-id="38b36-104">Specifies tolerance values for each vertex component when comparing vertices to determine if they are similar enough to be welded together.</span></span>

## <a name="syntax"></a><span data-ttu-id="38b36-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38b36-105">Syntax</span></span>


```C++
typedef struct D3DX10_WELD_EPSILONS {
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
} D3DX10_WELD_EPSILONS, *LPD3DX10_WELD_EPSILONS;
```



## <a name="members"></a><span data-ttu-id="38b36-106">Membros</span><span class="sxs-lookup"><span data-stu-id="38b36-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="38b36-107">**Posição**</span><span class="sxs-lookup"><span data-stu-id="38b36-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="38b36-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38b36-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="38b36-109">Posição</span><span class="sxs-lookup"><span data-stu-id="38b36-109">Position</span></span>

</dd> <dt>

<span data-ttu-id="38b36-110">**BlendWeights**</span><span class="sxs-lookup"><span data-stu-id="38b36-110">**BlendWeights**</span></span>
</dt> <dd>

<span data-ttu-id="38b36-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38b36-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="38b36-112">Peso de mistura</span><span class="sxs-lookup"><span data-stu-id="38b36-112">Blend weight</span></span>

</dd> <dt>

<span data-ttu-id="38b36-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="38b36-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="38b36-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38b36-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="38b36-115">Normal</span><span class="sxs-lookup"><span data-stu-id="38b36-115">Normal</span></span>

</dd> <dt>

<span data-ttu-id="38b36-116">**PSize**</span><span class="sxs-lookup"><span data-stu-id="38b36-116">**PSize**</span></span>
</dt> <dd>

<span data-ttu-id="38b36-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38b36-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="38b36-118">Valor do tamanho do ponto</span><span class="sxs-lookup"><span data-stu-id="38b36-118">Point size value</span></span>

</dd> <dt>

<span data-ttu-id="38b36-119">**Especular**</span><span class="sxs-lookup"><span data-stu-id="38b36-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="38b36-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38b36-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="38b36-121">Valor de iluminação especular</span><span class="sxs-lookup"><span data-stu-id="38b36-121">Specular lighting value</span></span>

</dd> <dt>

<span data-ttu-id="38b36-122">**Difusa**</span><span class="sxs-lookup"><span data-stu-id="38b36-122">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="38b36-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38b36-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="38b36-124">Valor de iluminação difusa</span><span class="sxs-lookup"><span data-stu-id="38b36-124">Diffuse lighting value</span></span>

</dd> <dt>

<span data-ttu-id="38b36-125">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="38b36-125">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="38b36-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38b36-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="38b36-127">Oito coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="38b36-127">Eight texture coordinates</span></span>

</dd> <dt>

<span data-ttu-id="38b36-128">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="38b36-128">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="38b36-129">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38b36-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="38b36-130">Tangente</span><span class="sxs-lookup"><span data-stu-id="38b36-130">Tangent</span></span>

</dd> <dt>

<span data-ttu-id="38b36-131">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="38b36-131">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="38b36-132">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38b36-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="38b36-133">Binormal</span><span class="sxs-lookup"><span data-stu-id="38b36-133">Binormal</span></span>

</dd> <dt>

<span data-ttu-id="38b36-134">**TessFactor**</span><span class="sxs-lookup"><span data-stu-id="38b36-134">**TessFactor**</span></span>
</dt> <dd>

<span data-ttu-id="38b36-135">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38b36-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="38b36-136">Fator de mosaico</span><span class="sxs-lookup"><span data-stu-id="38b36-136">Tessellation factor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38b36-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="38b36-137">Remarks</span></span>

<span data-ttu-id="38b36-138">O tipo LPD3DXWeldEpsilons é definido como um ponteiro para a estrutura D3DXWeldEpsilons.</span><span class="sxs-lookup"><span data-stu-id="38b36-138">The LPD3DXWeldEpsilons type is defined as a pointer to the D3DXWeldEpsilons structure.</span></span>


```
typedef D3DX_WELD_EPSILONS *LPD3DX_WELD_EPSILONS;
```



## <a name="requirements"></a><span data-ttu-id="38b36-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38b36-139">Requirements</span></span>



| <span data-ttu-id="38b36-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="38b36-140">Requirement</span></span> | <span data-ttu-id="38b36-141">Valor</span><span class="sxs-lookup"><span data-stu-id="38b36-141">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="38b36-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="38b36-142">Header</span></span><br/> | <dl> <span data-ttu-id="38b36-143"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="38b36-143"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38b36-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="38b36-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38b36-145">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="38b36-145">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
