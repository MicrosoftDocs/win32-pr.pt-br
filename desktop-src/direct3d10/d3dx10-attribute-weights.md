---
description: Especifica os atributos de peso de malha.
ms.assetid: 554bb8f2-9e92-4e9e-b500-c3cc47d57830
title: Estrutura de D3DX10_ATTRIBUTE_WEIGHTS (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_WEIGHTS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 4f137c1ecc29c184c4dec3995fb0202741ce9f09
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298671"
---
# <a name="d3dx10_attribute_weights-structure"></a><span data-ttu-id="07b7c-103">Estrutura de pesos de \_ atributo D3DX10 \_</span><span class="sxs-lookup"><span data-stu-id="07b7c-103">D3DX10\_ATTRIBUTE\_WEIGHTS structure</span></span>

<span data-ttu-id="07b7c-104">Especifica os atributos de peso de malha.</span><span class="sxs-lookup"><span data-stu-id="07b7c-104">Specifies mesh weight attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="07b7c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07b7c-105">Syntax</span></span>


```C++
typedef struct D3DX10_ATTRIBUTE_WEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DX10_ATTRIBUTE_WEIGHTS, *LPD3DX10_ATTRIBUTE_WEIGHTS;
```



## <a name="members"></a><span data-ttu-id="07b7c-106">Membros</span><span class="sxs-lookup"><span data-stu-id="07b7c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="07b7c-107">**Posição**</span><span class="sxs-lookup"><span data-stu-id="07b7c-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="07b7c-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07b7c-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07b7c-109">Posição.</span><span class="sxs-lookup"><span data-stu-id="07b7c-109">Position.</span></span>

</dd> <dt>

<span data-ttu-id="07b7c-110">**Limite**</span><span class="sxs-lookup"><span data-stu-id="07b7c-110">**Boundary**</span></span>
</dt> <dd>

<span data-ttu-id="07b7c-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07b7c-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07b7c-112">Peso de mistura.</span><span class="sxs-lookup"><span data-stu-id="07b7c-112">Blend weight.</span></span>

</dd> <dt>

<span data-ttu-id="07b7c-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="07b7c-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="07b7c-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07b7c-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07b7c-115">Normal.</span><span class="sxs-lookup"><span data-stu-id="07b7c-115">Normal.</span></span>

</dd> <dt>

<span data-ttu-id="07b7c-116">**Difusa**</span><span class="sxs-lookup"><span data-stu-id="07b7c-116">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="07b7c-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07b7c-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07b7c-118">Valor de iluminação difusa.</span><span class="sxs-lookup"><span data-stu-id="07b7c-118">Diffuse lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="07b7c-119">**Especular**</span><span class="sxs-lookup"><span data-stu-id="07b7c-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="07b7c-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07b7c-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07b7c-121">Valor de iluminação especular.</span><span class="sxs-lookup"><span data-stu-id="07b7c-121">Specular lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="07b7c-122">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="07b7c-122">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="07b7c-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07b7c-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07b7c-124">Oito coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="07b7c-124">Eight texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="07b7c-125">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="07b7c-125">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="07b7c-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07b7c-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07b7c-127">Tangente.</span><span class="sxs-lookup"><span data-stu-id="07b7c-127">Tangent.</span></span>

</dd> <dt>

<span data-ttu-id="07b7c-128">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="07b7c-128">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="07b7c-129">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07b7c-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07b7c-130">Binormal.</span><span class="sxs-lookup"><span data-stu-id="07b7c-130">Binormal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07b7c-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="07b7c-131">Remarks</span></span>

<span data-ttu-id="07b7c-132">Esta estrutura descreve como uma operação de simplificação considerará os dados de vértice ao calcular os custos relativos entre as bordas de recolhimento.</span><span class="sxs-lookup"><span data-stu-id="07b7c-132">This structure describes how a simplification operation will consider vertex data when calculating relative costs between collapsing edges.</span></span> <span data-ttu-id="07b7c-133">Por exemplo, se o campo normal for 0,0, a operação de simplificação irá ignorar o componente normal de vértice ao calcular o erro para o recolhimento.</span><span class="sxs-lookup"><span data-stu-id="07b7c-133">For example, if the Normal field is 0.0, the simplification operation will ignore the vertex normal component when calculating the error for the collapse.</span></span> <span data-ttu-id="07b7c-134">No entanto, se o campo normal for 1,0, a operação de simplificação usará o componente normal de vértice.</span><span class="sxs-lookup"><span data-stu-id="07b7c-134">However, if the Normal field is 1.0, the simplification operation will use the vertex normal component.</span></span> <span data-ttu-id="07b7c-135">Se o campo normal for 2,0, dobrar a quantidade de erros; Se o campo normal for 4,0, o número de erros será quádruplo e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="07b7c-135">If the Normal field is 2.0, double the amount of errors; if the Normal field is 4.0, then quadruple the number of errors, and so on.</span></span>

<span data-ttu-id="07b7c-136">O \_ tipo de pesos do atributo LPD3DX \_ é definido como um ponteiro para a \_ estrutura de pesos do atributo D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="07b7c-136">The LPD3DX\_ATTRIBUTE\_WEIGHTS type is defined as a pointer to the D3DX\_ATTRIBUTE\_WEIGHTS structure.</span></span>


```
    typedef D3DX_ATTRIBUTE_WEIGHTS* LPD3DX_ATTRIBUTE_WEIGHTS;
```



## <a name="requirements"></a><span data-ttu-id="07b7c-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07b7c-137">Requirements</span></span>



| <span data-ttu-id="07b7c-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="07b7c-138">Requirement</span></span> | <span data-ttu-id="07b7c-139">Valor</span><span class="sxs-lookup"><span data-stu-id="07b7c-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="07b7c-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="07b7c-140">Header</span></span><br/> | <dl> <span data-ttu-id="07b7c-141"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="07b7c-141"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07b7c-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="07b7c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07b7c-143">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="07b7c-143">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
