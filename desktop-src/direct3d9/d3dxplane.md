---
description: Descreve um plano.
ms.assetid: ffca4650-9788-4559-8f6b-a4e5db29ce55
title: Estrutura D3DXPLANE (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 260f9555313aea3443f0728f2b50189228429803
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812076"
---
# <a name="d3dxplane-structure-d3dx9mathh"></a><span data-ttu-id="be294-103">Estrutura D3DXPLANE (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="be294-103">D3DXPLANE structure (D3dx9math.h)</span></span>

<span data-ttu-id="be294-104">Descreve um plano.</span><span class="sxs-lookup"><span data-stu-id="be294-104">Describes a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="be294-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be294-105">Syntax</span></span>


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a><span data-ttu-id="be294-106">Membros</span><span class="sxs-lookup"><span data-stu-id="be294-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="be294-107">**um**</span><span class="sxs-lookup"><span data-stu-id="be294-107">**a**</span></span>
</dt> <dd>

<span data-ttu-id="be294-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be294-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="be294-109">O coeficiente de recorte na equação do plano geral.</span><span class="sxs-lookup"><span data-stu-id="be294-109">The a coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="be294-110">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="be294-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="be294-111">**b**</span><span class="sxs-lookup"><span data-stu-id="be294-111">**b**</span></span>
</dt> <dd>

<span data-ttu-id="be294-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be294-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="be294-113">O coeficiente b do plano de recorte na equação do plano geral.</span><span class="sxs-lookup"><span data-stu-id="be294-113">The b coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="be294-114">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="be294-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="be294-115">**c**</span><span class="sxs-lookup"><span data-stu-id="be294-115">**c**</span></span>
</dt> <dd>

<span data-ttu-id="be294-116">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be294-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="be294-117">O coeficiente de c do plano de recorte na equação do plano geral.</span><span class="sxs-lookup"><span data-stu-id="be294-117">The c coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="be294-118">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="be294-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="be294-119">**d**</span><span class="sxs-lookup"><span data-stu-id="be294-119">**d**</span></span>
</dt> <dd>

<span data-ttu-id="be294-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be294-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="be294-121">O coeficiente d do plano de recorte na equação do plano geral.</span><span class="sxs-lookup"><span data-stu-id="be294-121">The d coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="be294-122">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="be294-122">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be294-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="be294-123">Remarks</span></span>

<span data-ttu-id="be294-124">Os membros da estrutura **D3DXPLANE** assumem a forma da equação de plano geral.</span><span class="sxs-lookup"><span data-stu-id="be294-124">The members of the **D3DXPLANE** structure take the form of the general plane equation.</span></span> <span data-ttu-id="be294-125">Eles se enquadram na equação do plano geral para que **um** x + **b** y + **c** z + **d** w = 0.</span><span class="sxs-lookup"><span data-stu-id="be294-125">They fit into the general plane equation so that **a** x + **b** y + **c** z + **d** w = 0.</span></span>

<span data-ttu-id="be294-126">Os programadores de C++ podem aproveitar a sobrecarga de operador e a conversão de tipos com as [**extensões D3DXPLANE**](d3dxplane-extensions.md) que implementam construtores sobrecarregados e operadores de atribuição, unários e binários (incluindo igualdade).</span><span class="sxs-lookup"><span data-stu-id="be294-126">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXPLANE Extensions**](d3dxplane-extensions.md) which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="be294-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be294-127">Requirements</span></span>



| <span data-ttu-id="be294-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="be294-128">Requirement</span></span> | <span data-ttu-id="be294-129">Valor</span><span class="sxs-lookup"><span data-stu-id="be294-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be294-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be294-130">Header</span></span><br/> | <dl> <span data-ttu-id="be294-131"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="be294-131"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be294-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="be294-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be294-133">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="be294-133">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
