---
description: Estrutura D3DXATTRIBUTEWEIGHTS-especifica os atributos de peso de malha.
ms.assetid: 8901a0fe-e38a-4045-8e8d-584be2620cc3
title: Estrutura D3DXATTRIBUTEWEIGHTS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTEWEIGHTS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 7a833d2a58db0f434f836126926e461cd2ee3ea0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115964"
---
# <a name="d3dxattributeweights-structure"></a><span data-ttu-id="e74e0-103">Estrutura D3DXATTRIBUTEWEIGHTS</span><span class="sxs-lookup"><span data-stu-id="e74e0-103">D3DXATTRIBUTEWEIGHTS structure</span></span>

<span data-ttu-id="e74e0-104">Especifica os atributos de peso de malha.</span><span class="sxs-lookup"><span data-stu-id="e74e0-104">Specifies mesh weight attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="e74e0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e74e0-105">Syntax</span></span>


```C++
typedef struct D3DXATTRIBUTEWEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DXATTRIBUTEWEIGHTS, *LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="members"></a><span data-ttu-id="e74e0-106">Membros</span><span class="sxs-lookup"><span data-stu-id="e74e0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e74e0-107">**Posição**</span><span class="sxs-lookup"><span data-stu-id="e74e0-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="e74e0-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e74e0-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e74e0-109">Posição.</span><span class="sxs-lookup"><span data-stu-id="e74e0-109">Position.</span></span>

</dd> <dt>

<span data-ttu-id="e74e0-110">**Limite**</span><span class="sxs-lookup"><span data-stu-id="e74e0-110">**Boundary**</span></span>
</dt> <dd>

<span data-ttu-id="e74e0-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e74e0-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e74e0-112">Peso de mistura.</span><span class="sxs-lookup"><span data-stu-id="e74e0-112">Blend weight.</span></span>

</dd> <dt>

<span data-ttu-id="e74e0-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="e74e0-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="e74e0-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e74e0-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e74e0-115">Normal.</span><span class="sxs-lookup"><span data-stu-id="e74e0-115">Normal.</span></span>

</dd> <dt>

<span data-ttu-id="e74e0-116">**Difusa**</span><span class="sxs-lookup"><span data-stu-id="e74e0-116">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="e74e0-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e74e0-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e74e0-118">Valor de iluminação difusa.</span><span class="sxs-lookup"><span data-stu-id="e74e0-118">Diffuse lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="e74e0-119">**Especular**</span><span class="sxs-lookup"><span data-stu-id="e74e0-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="e74e0-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e74e0-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e74e0-121">Valor de iluminação especular.</span><span class="sxs-lookup"><span data-stu-id="e74e0-121">Specular lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="e74e0-122">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="e74e0-122">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="e74e0-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e74e0-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e74e0-124">Oito coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="e74e0-124">Eight texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="e74e0-125">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="e74e0-125">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="e74e0-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e74e0-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e74e0-127">Tangente.</span><span class="sxs-lookup"><span data-stu-id="e74e0-127">Tangent.</span></span>

</dd> <dt>

<span data-ttu-id="e74e0-128">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="e74e0-128">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="e74e0-129">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e74e0-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e74e0-130">Binormal.</span><span class="sxs-lookup"><span data-stu-id="e74e0-130">Binormal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e74e0-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="e74e0-131">Remarks</span></span>

<span data-ttu-id="e74e0-132">Esta estrutura descreve como uma operação de simplificação considerará os dados de vértice ao calcular os custos relativos entre as bordas de recolhimento.</span><span class="sxs-lookup"><span data-stu-id="e74e0-132">This structure describes how a simplification operation will consider vertex data when calculating relative costs between collapsing edges.</span></span> <span data-ttu-id="e74e0-133">Por exemplo, se o campo normal for 0,0, a operação de simplificação irá ignorar o componente normal de vértice ao calcular o erro para o recolhimento.</span><span class="sxs-lookup"><span data-stu-id="e74e0-133">For example, if the Normal field is 0.0, the simplification operation will ignore the vertex normal component when calculating the error for the collapse.</span></span> <span data-ttu-id="e74e0-134">No entanto, se o campo normal for 1,0, a operação de simplificação usará o componente normal de vértice.</span><span class="sxs-lookup"><span data-stu-id="e74e0-134">However, if the Normal field is 1.0, the simplification operation will use the vertex normal component.</span></span> <span data-ttu-id="e74e0-135">Se o campo normal for 2,0, dobrar a quantidade de erros; Se o campo normal for 4,0, o número de erros será quádruplo e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="e74e0-135">If the Normal field is 2.0, double the amount of errors; if the Normal field is 4.0, then quadruple the number of errors, and so on.</span></span>

<span data-ttu-id="e74e0-136">O tipo LPD3DXATTRIBUTEWEIGHTS é definido como um ponteiro para a estrutura **D3DXATTRIBUTEWEIGHTS** .</span><span class="sxs-lookup"><span data-stu-id="e74e0-136">The LPD3DXATTRIBUTEWEIGHTS type is defined as a pointer to the **D3DXATTRIBUTEWEIGHTS** structure.</span></span>


```
    
    typedef D3DXATTRIBUTEWEIGHTS* LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="requirements"></a><span data-ttu-id="e74e0-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e74e0-137">Requirements</span></span>



| <span data-ttu-id="e74e0-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="e74e0-138">Requirement</span></span> | <span data-ttu-id="e74e0-139">Valor</span><span class="sxs-lookup"><span data-stu-id="e74e0-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e74e0-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e74e0-140">Header</span></span><br/> | <dl> <span data-ttu-id="e74e0-141"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e74e0-141"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e74e0-142">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e74e0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e74e0-143">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="e74e0-143">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="e74e0-144">**D3DXSimplifyMesh**</span><span class="sxs-lookup"><span data-stu-id="e74e0-144">**D3DXSimplifyMesh**</span></span>](d3dxsimplifymesh.md)
</dt> </dl>

 

 
