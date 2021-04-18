---
description: Especifica os atributos de peso de malha.
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
ms.openlocfilehash: 49725e410fb700c7ecb93fd56a8db367d7f982a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793980"
---
# <a name="d3dxattributeweights-structure"></a><span data-ttu-id="d39e2-103">Estrutura D3DXATTRIBUTEWEIGHTS</span><span class="sxs-lookup"><span data-stu-id="d39e2-103">D3DXATTRIBUTEWEIGHTS structure</span></span>

<span data-ttu-id="d39e2-104">Especifica os atributos de peso de malha.</span><span class="sxs-lookup"><span data-stu-id="d39e2-104">Specifies mesh weight attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d39e2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d39e2-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="d39e2-106">Membros</span><span class="sxs-lookup"><span data-stu-id="d39e2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d39e2-107">**Posição**</span><span class="sxs-lookup"><span data-stu-id="d39e2-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="d39e2-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d39e2-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d39e2-109">Posição.</span><span class="sxs-lookup"><span data-stu-id="d39e2-109">Position.</span></span>

</dd> <dt>

<span data-ttu-id="d39e2-110">**Limite**</span><span class="sxs-lookup"><span data-stu-id="d39e2-110">**Boundary**</span></span>
</dt> <dd>

<span data-ttu-id="d39e2-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d39e2-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d39e2-112">Peso de mistura.</span><span class="sxs-lookup"><span data-stu-id="d39e2-112">Blend weight.</span></span>

</dd> <dt>

<span data-ttu-id="d39e2-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="d39e2-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="d39e2-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d39e2-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d39e2-115">Normal.</span><span class="sxs-lookup"><span data-stu-id="d39e2-115">Normal.</span></span>

</dd> <dt>

<span data-ttu-id="d39e2-116">**Difusa**</span><span class="sxs-lookup"><span data-stu-id="d39e2-116">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="d39e2-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d39e2-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d39e2-118">Valor de iluminação difusa.</span><span class="sxs-lookup"><span data-stu-id="d39e2-118">Diffuse lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="d39e2-119">**Especular**</span><span class="sxs-lookup"><span data-stu-id="d39e2-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="d39e2-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d39e2-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d39e2-121">Valor de iluminação especular.</span><span class="sxs-lookup"><span data-stu-id="d39e2-121">Specular lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="d39e2-122">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="d39e2-122">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="d39e2-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d39e2-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d39e2-124">Oito coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="d39e2-124">Eight texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="d39e2-125">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="d39e2-125">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="d39e2-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d39e2-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d39e2-127">Tangente.</span><span class="sxs-lookup"><span data-stu-id="d39e2-127">Tangent.</span></span>

</dd> <dt>

<span data-ttu-id="d39e2-128">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="d39e2-128">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="d39e2-129">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d39e2-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d39e2-130">Binormal.</span><span class="sxs-lookup"><span data-stu-id="d39e2-130">Binormal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d39e2-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="d39e2-131">Remarks</span></span>

<span data-ttu-id="d39e2-132">Esta estrutura descreve como uma operação de simplificação considerará os dados de vértice ao calcular os custos relativos entre as bordas de recolhimento.</span><span class="sxs-lookup"><span data-stu-id="d39e2-132">This structure describes how a simplification operation will consider vertex data when calculating relative costs between collapsing edges.</span></span> <span data-ttu-id="d39e2-133">Por exemplo, se o campo normal for 0,0, a operação de simplificação irá ignorar o componente normal de vértice ao calcular o erro para o recolhimento.</span><span class="sxs-lookup"><span data-stu-id="d39e2-133">For example, if the Normal field is 0.0, the simplification operation will ignore the vertex normal component when calculating the error for the collapse.</span></span> <span data-ttu-id="d39e2-134">No entanto, se o campo normal for 1,0, a operação de simplificação usará o componente normal de vértice.</span><span class="sxs-lookup"><span data-stu-id="d39e2-134">However, if the Normal field is 1.0, the simplification operation will use the vertex normal component.</span></span> <span data-ttu-id="d39e2-135">Se o campo normal for 2,0, dobrar a quantidade de erros; Se o campo normal for 4,0, o número de erros será quádruplo e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d39e2-135">If the Normal field is 2.0, double the amount of errors; if the Normal field is 4.0, then quadruple the number of errors, and so on.</span></span>

<span data-ttu-id="d39e2-136">O tipo LPD3DXATTRIBUTEWEIGHTS é definido como um ponteiro para a estrutura **D3DXATTRIBUTEWEIGHTS** .</span><span class="sxs-lookup"><span data-stu-id="d39e2-136">The LPD3DXATTRIBUTEWEIGHTS type is defined as a pointer to the **D3DXATTRIBUTEWEIGHTS** structure.</span></span>


```
    
    typedef D3DXATTRIBUTEWEIGHTS* LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="requirements"></a><span data-ttu-id="d39e2-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d39e2-137">Requirements</span></span>



| <span data-ttu-id="d39e2-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="d39e2-138">Requirement</span></span> | <span data-ttu-id="d39e2-139">Valor</span><span class="sxs-lookup"><span data-stu-id="d39e2-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d39e2-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d39e2-140">Header</span></span><br/> | <dl> <span data-ttu-id="d39e2-141"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d39e2-141"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d39e2-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="d39e2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d39e2-143">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="d39e2-143">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="d39e2-144">**D3DXSimplifyMesh**</span><span class="sxs-lookup"><span data-stu-id="d39e2-144">**D3DXSimplifyMesh**</span></span>](d3dxsimplifymesh.md)
</dt> </dl>

 

 
