---
description: Estrutura D3DXPLANE (D3DX10Math. h) – descreve um plano.
ms.assetid: c6da7343-a4f3-4cac-855b-14bd70c0d3c2
title: Estrutura D3DXPLANE (D3DX10Math. h)
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
- D3DX10Math.h
ms.openlocfilehash: 440246fb47a851f9f5339c72a484a2cb59e8f662
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103324"
---
# <a name="d3dxplane-structure-d3dx10mathh"></a><span data-ttu-id="fc500-103">Estrutura D3DXPLANE (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="fc500-103">D3DXPLANE structure (D3DX10Math.h)</span></span>

<span data-ttu-id="fc500-104">Descreve um plano.</span><span class="sxs-lookup"><span data-stu-id="fc500-104">Describes a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc500-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc500-105">Syntax</span></span>


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a><span data-ttu-id="fc500-106">Membros</span><span class="sxs-lookup"><span data-stu-id="fc500-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fc500-107">**um**</span><span class="sxs-lookup"><span data-stu-id="fc500-107">**a**</span></span>
</dt> <dd>

<span data-ttu-id="fc500-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc500-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fc500-109">O coeficiente de recorte na equação do plano geral.</span><span class="sxs-lookup"><span data-stu-id="fc500-109">The a coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="fc500-110">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="fc500-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fc500-111">**b**</span><span class="sxs-lookup"><span data-stu-id="fc500-111">**b**</span></span>
</dt> <dd>

<span data-ttu-id="fc500-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc500-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fc500-113">O coeficiente b do plano de recorte na equação do plano geral.</span><span class="sxs-lookup"><span data-stu-id="fc500-113">The b coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="fc500-114">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="fc500-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fc500-115">**c**</span><span class="sxs-lookup"><span data-stu-id="fc500-115">**c**</span></span>
</dt> <dd>

<span data-ttu-id="fc500-116">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc500-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fc500-117">O coeficiente de c do plano de recorte na equação do plano geral.</span><span class="sxs-lookup"><span data-stu-id="fc500-117">The c coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="fc500-118">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="fc500-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fc500-119">**d**</span><span class="sxs-lookup"><span data-stu-id="fc500-119">**d**</span></span>
</dt> <dd>

<span data-ttu-id="fc500-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc500-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fc500-121">O coeficiente d do plano de recorte na equação do plano geral.</span><span class="sxs-lookup"><span data-stu-id="fc500-121">The d coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="fc500-122">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="fc500-122">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc500-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc500-123">Remarks</span></span>

<span data-ttu-id="fc500-124">Os membros da estrutura **D3DXPLANE** assumem a forma da equação de plano geral.</span><span class="sxs-lookup"><span data-stu-id="fc500-124">The members of the **D3DXPLANE** structure take the form of the general plane equation.</span></span> <span data-ttu-id="fc500-125">Eles se encaixam na equação do plano geral para que o AX + por + cz + DW = 0.</span><span class="sxs-lookup"><span data-stu-id="fc500-125">They fit into the general plane equation so that ax + by + cz + dw = 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc500-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc500-126">Requirements</span></span>



| <span data-ttu-id="fc500-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc500-127">Requirement</span></span> | <span data-ttu-id="fc500-128">Valor</span><span class="sxs-lookup"><span data-stu-id="fc500-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc500-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fc500-129">Header</span></span><br/> | <dl> <span data-ttu-id="fc500-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc500-130"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc500-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fc500-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc500-132">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="fc500-132">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
