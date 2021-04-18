---
description: Computa o produto de ponto de um plano e um vetor 3D. O parâmetro w do vetor é considerado como 0.
ms.assetid: 7aba1e94-6531-4c07-83b0-6100805e8bbd
title: Função D3DXPlaneDotNormal (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 28903fc8ce0073e4014ae6ce75df636222ce32f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105785926"
---
# <a name="d3dxplanedotnormal-function"></a><span data-ttu-id="a0919-104">Função D3DXPlaneDotNormal</span><span class="sxs-lookup"><span data-stu-id="a0919-104">D3DXPlaneDotNormal function</span></span>

<span data-ttu-id="a0919-105">Computa o produto de ponto de um plano e um vetor 3D.</span><span class="sxs-lookup"><span data-stu-id="a0919-105">Computes the dot product of a plane and a 3D vector.</span></span> <span data-ttu-id="a0919-106">O parâmetro w do vetor é considerado como 0.</span><span class="sxs-lookup"><span data-stu-id="a0919-106">The w parameter of the vector is assumed to be 0.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0919-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0919-107">Syntax</span></span>


```C++
FLOAT D3DXPlaneDotNormal(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="a0919-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0919-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0919-109">*PP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a0919-109">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0919-110">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="a0919-110">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="a0919-111">Ponteiro para uma estrutura de [**D3DXPLANE**](d3dxplane.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="a0919-111">Pointer to a source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a0919-112">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a0919-112">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0919-113">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a0919-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a0919-114">Ponteiro para uma estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="a0919-114">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0919-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a0919-115">Return value</span></span>

<span data-ttu-id="a0919-116">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0919-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0919-117">O produto de ponto do plano e do vetor 3D.</span><span class="sxs-lookup"><span data-stu-id="a0919-117">The dot product of the plane and 3D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0919-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0919-118">Remarks</span></span>

<span data-ttu-id="a0919-119">Dado um plano (a, b, c, d) e um vetor 3D (x, y, z) o valor retornado dessa função é um \* x + b \* y + c \* z + d \* 0.</span><span class="sxs-lookup"><span data-stu-id="a0919-119">Given a plane (a, b, c, d) and a 3D vector (x, y, z) the return value of this function is a\*x + b\*y + c\*z + d\*0.</span></span> <span data-ttu-id="a0919-120">A função **D3DXPlaneDotNormal** é útil para calcular o ângulo entre o normal do plano e outro normal.</span><span class="sxs-lookup"><span data-stu-id="a0919-120">The **D3DXPlaneDotNormal** function is useful for calculating the angle between the normal of the plane, and another normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0919-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0919-121">Requirements</span></span>



| <span data-ttu-id="a0919-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0919-122">Requirement</span></span> | <span data-ttu-id="a0919-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a0919-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0919-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a0919-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a0919-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0919-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a0919-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a0919-126">Library</span></span><br/> | <dl> <span data-ttu-id="a0919-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0919-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a0919-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0919-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0919-129">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="a0919-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a0919-130">**D3DXPlaneDot**</span><span class="sxs-lookup"><span data-stu-id="a0919-130">**D3DXPlaneDot**</span></span>](d3dxplanedot.md)
</dt> <dt>

[<span data-ttu-id="a0919-131">**D3DXPlaneDotCoord**</span><span class="sxs-lookup"><span data-stu-id="a0919-131">**D3DXPlaneDotCoord**</span></span>](d3dxplanedotcoord.md)
</dt> </dl>

 

 
