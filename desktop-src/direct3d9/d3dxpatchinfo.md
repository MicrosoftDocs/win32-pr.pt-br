---
description: Estrutura que contém os atributos de uma malha de patch.
ms.assetid: aaea69c9-2d33-46e8-bc26-95daf65abf50
title: Estrutura D3DXPATCHINFO (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHINFO
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 8628cc27a0223580aa1f8072750f4c31a176533e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298478"
---
# <a name="d3dxpatchinfo-structure"></a><span data-ttu-id="71c98-103">Estrutura D3DXPATCHINFO</span><span class="sxs-lookup"><span data-stu-id="71c98-103">D3DXPATCHINFO structure</span></span>

<span data-ttu-id="71c98-104">Estrutura que contém os atributos de uma malha de patch.</span><span class="sxs-lookup"><span data-stu-id="71c98-104">Structure that contains the attributes of a patch mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="71c98-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71c98-105">Syntax</span></span>


```C++
typedef struct D3DXPATCHINFO {
  D3DXPATCHMESHTYPE PatchType;
  D3DDEGREETYPE     Degree;
  D3DBASISTYPE      Basis;
} D3DXPATCHINFO, *LPD3DXPATCHINFO;
```



## <a name="members"></a><span data-ttu-id="71c98-106">Membros</span><span class="sxs-lookup"><span data-stu-id="71c98-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="71c98-107">**Patchtype**</span><span class="sxs-lookup"><span data-stu-id="71c98-107">**PatchType**</span></span>
</dt> <dd>

<span data-ttu-id="71c98-108">Tipo: **[ **D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md)**</span><span class="sxs-lookup"><span data-stu-id="71c98-108">Type: **[**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="71c98-109">O tipo de patch.</span><span class="sxs-lookup"><span data-stu-id="71c98-109">The patch type.</span></span> <span data-ttu-id="71c98-110">Para obter informações sobre tipos de patch, consulte [**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md).</span><span class="sxs-lookup"><span data-stu-id="71c98-110">For information about patch types, see [**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md).</span></span>

</dd> <dt>

<span data-ttu-id="71c98-111">**Grau**</span><span class="sxs-lookup"><span data-stu-id="71c98-111">**Degree**</span></span>
</dt> <dd>

<span data-ttu-id="71c98-112">Tipo: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**</span><span class="sxs-lookup"><span data-stu-id="71c98-112">Type: **[**D3DDEGREETYPE**](./d3ddegreetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="71c98-113">Grau das curvas usadas para construir o patch.</span><span class="sxs-lookup"><span data-stu-id="71c98-113">Degree of the curves used to construct the patch.</span></span> <span data-ttu-id="71c98-114">Para obter informações sobre os graus com suporte, consulte [**D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="71c98-114">For information about the degrees supported, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="71c98-115">**Base**</span><span class="sxs-lookup"><span data-stu-id="71c98-115">**Basis**</span></span>
</dt> <dd>

<span data-ttu-id="71c98-116">Tipo: **[ **D3DBASISTYPE**](./d3dbasistype.md)**</span><span class="sxs-lookup"><span data-stu-id="71c98-116">Type: **[**D3DBASISTYPE**](./d3dbasistype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="71c98-117">Tipo de curva usado para construir o patch.</span><span class="sxs-lookup"><span data-stu-id="71c98-117">Type of curve used to construct the patch.</span></span> <span data-ttu-id="71c98-118">Para obter informações sobre os tipos de base com suporte, consulte [**D3DBASISTYPE**](./d3dbasistype.md).</span><span class="sxs-lookup"><span data-stu-id="71c98-118">For information about the basis types supported, see [**D3DBASISTYPE**](./d3dbasistype.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="71c98-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="71c98-119">Remarks</span></span>

<span data-ttu-id="71c98-120">Uma malha é um conjunto de faces, cada uma delas é descrita por um polígono simples.</span><span class="sxs-lookup"><span data-stu-id="71c98-120">A mesh is a set of faces, each of which is described by a simple polygon.</span></span> <span data-ttu-id="71c98-121">Os objetos podem ser criados Conectando várias malhas juntas.</span><span class="sxs-lookup"><span data-stu-id="71c98-121">Objects can be created by connecting several meshes together.</span></span> <span data-ttu-id="71c98-122">Uma malha de patch é construída A partir de patches.</span><span class="sxs-lookup"><span data-stu-id="71c98-122">A patch mesh is constructed from patches.</span></span> <span data-ttu-id="71c98-123">Um patch é uma parte com quatro lados da geometria construída com base nas curvas.</span><span class="sxs-lookup"><span data-stu-id="71c98-123">A patch is a four-sided piece of geometry constructed from curves.</span></span> <span data-ttu-id="71c98-124">O tipo de curva usado e a ordem da curva podem ser variados para que a superfície do patch caiba quase qualquer forma de superfície.</span><span class="sxs-lookup"><span data-stu-id="71c98-124">The type of curve used and the order of the curve can be varied so that the patch surface will fit almost any surface shape.</span></span>

<span data-ttu-id="71c98-125">Há suporte para os seguintes tipos de combinações de patch:</span><span class="sxs-lookup"><span data-stu-id="71c98-125">The following types of patch combinations are supported:</span></span>



| <span data-ttu-id="71c98-126">Tipo de patch</span><span class="sxs-lookup"><span data-stu-id="71c98-126">Patch Type</span></span> | <span data-ttu-id="71c98-127">Base</span><span class="sxs-lookup"><span data-stu-id="71c98-127">Basis</span></span>       | <span data-ttu-id="71c98-128">Grau</span><span class="sxs-lookup"><span data-stu-id="71c98-128">Degree</span></span> |
|------------|-------------|--------|
| <span data-ttu-id="71c98-129">Retângulo</span><span class="sxs-lookup"><span data-stu-id="71c98-129">Rectangle</span></span>  | <span data-ttu-id="71c98-130">Bézier</span><span class="sxs-lookup"><span data-stu-id="71c98-130">Bezier</span></span>      | <span data-ttu-id="71c98-131">2, 3, 5</span><span class="sxs-lookup"><span data-stu-id="71c98-131">2,3,5</span></span>  |
| <span data-ttu-id="71c98-132">Retângulo</span><span class="sxs-lookup"><span data-stu-id="71c98-132">Rectangle</span></span>  | <span data-ttu-id="71c98-133">B-spline</span><span class="sxs-lookup"><span data-stu-id="71c98-133">B-Spline</span></span>    | <span data-ttu-id="71c98-134">2, 3, 5</span><span class="sxs-lookup"><span data-stu-id="71c98-134">2,3,5</span></span>  |
| <span data-ttu-id="71c98-135">Retângulo</span><span class="sxs-lookup"><span data-stu-id="71c98-135">Rectangle</span></span>  | <span data-ttu-id="71c98-136">Catmull-Rom</span><span class="sxs-lookup"><span data-stu-id="71c98-136">Catmull-Rom</span></span> | <span data-ttu-id="71c98-137">3</span><span class="sxs-lookup"><span data-stu-id="71c98-137">3</span></span>      |
| <span data-ttu-id="71c98-138">Triangle</span><span class="sxs-lookup"><span data-stu-id="71c98-138">Triangle</span></span>   | <span data-ttu-id="71c98-139">Bézier</span><span class="sxs-lookup"><span data-stu-id="71c98-139">Bezier</span></span>      | <span data-ttu-id="71c98-140">2, 3, 5</span><span class="sxs-lookup"><span data-stu-id="71c98-140">2,3,5</span></span>  |
| <span data-ttu-id="71c98-141">N-patch</span><span class="sxs-lookup"><span data-stu-id="71c98-141">N-patch</span></span>    | <span data-ttu-id="71c98-142">N/D</span><span class="sxs-lookup"><span data-stu-id="71c98-142">N/A</span></span>         | <span data-ttu-id="71c98-143">3</span><span class="sxs-lookup"><span data-stu-id="71c98-143">3</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="71c98-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71c98-144">Requirements</span></span>



| <span data-ttu-id="71c98-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="71c98-145">Requirement</span></span> | <span data-ttu-id="71c98-146">Valor</span><span class="sxs-lookup"><span data-stu-id="71c98-146">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="71c98-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="71c98-147">Header</span></span><br/> | <dl> <span data-ttu-id="71c98-148"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="71c98-148"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71c98-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="71c98-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71c98-150">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="71c98-150">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="71c98-151">**Informações de D3DRECTPATCH \_**</span><span class="sxs-lookup"><span data-stu-id="71c98-151">**D3DRECTPATCH\_INFO**</span></span>](d3drectpatch-info.md)
</dt> <dt>

[<span data-ttu-id="71c98-152">**Informações de D3DTRIPATCH \_**</span><span class="sxs-lookup"><span data-stu-id="71c98-152">**D3DTRIPATCH\_INFO**</span></span>](d3dtripatch-info.md)
</dt> <dt>

[<span data-ttu-id="71c98-153">**D3DXCreatePatchMesh**</span><span class="sxs-lookup"><span data-stu-id="71c98-153">**D3DXCreatePatchMesh**</span></span>](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 
