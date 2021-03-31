---
description: Define o estilo de transição entre os valores de uma animação de malha.
ms.assetid: 4416ef28-ba6b-47ca-be7d-831daad619e5
title: Enumeração de D3DXTRANSITION_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRANSITION_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0ca6ef7f9dcee8e865a1cd4089aecd1bc239d5d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930582"
---
# <a name="d3dxtransition_type-enumeration"></a><span data-ttu-id="611dd-103">\_Enumeração de tipo D3DXTRANSITION</span><span class="sxs-lookup"><span data-stu-id="611dd-103">D3DXTRANSITION\_TYPE enumeration</span></span>

<span data-ttu-id="611dd-104">Define o estilo de transição entre os valores de uma animação de malha.</span><span class="sxs-lookup"><span data-stu-id="611dd-104">Defines the transition style between values of a mesh animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="611dd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="611dd-105">Syntax</span></span>


```C++
typedef enum D3DXTRANSITION_TYPE { 
  D3DXTRANSITION_LINEAR         = 0x000,
  D3DXTRANSITION_EASEINEASEOUT  = 0x001,
  D3DXTRANSITION_FORCE_DWORD    = 0x7fffffff
} D3DXTRANSITION_TYPE, *LPD3DXTRANSITION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="611dd-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="611dd-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="611dd-107"><span id="D3DXTRANSITION_LINEAR"></span><span id="d3dxtransition_linear"></span>**D3DXTRANSITION \_ linear**</span><span class="sxs-lookup"><span data-stu-id="611dd-107"><span id="D3DXTRANSITION_LINEAR"></span><span id="d3dxtransition_linear"></span>**D3DXTRANSITION\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="611dd-108">Transição linear entre valores.</span><span class="sxs-lookup"><span data-stu-id="611dd-108">Linear transition between values.</span></span>

</dd> <dt>

<span data-ttu-id="611dd-109"><span id="D3DXTRANSITION_EASEINEASEOUT"></span><span id="d3dxtransition_easeineaseout"></span>**D3DXTRANSITION \_ EASEINEASEOUT**</span><span class="sxs-lookup"><span data-stu-id="611dd-109"><span id="D3DXTRANSITION_EASEINEASEOUT"></span><span id="d3dxtransition_easeineaseout"></span>**D3DXTRANSITION\_EASEINEASEOUT**</span></span>
</dt> <dd>

<span data-ttu-id="611dd-110">Uma transição de spline de fácil saída entre valores.</span><span class="sxs-lookup"><span data-stu-id="611dd-110">Ease-in, ease-out spline transition between values.</span></span>

</dd> <dt>

<span data-ttu-id="611dd-111"><span id="D3DXTRANSITION_FORCE_DWORD"></span><span id="d3dxtransition_force_dword"></span>**D3DXTRANSITION \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="611dd-111"><span id="D3DXTRANSITION_FORCE_DWORD"></span><span id="d3dxtransition_force_dword"></span>**D3DXTRANSITION\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="611dd-112">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="611dd-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="611dd-113">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="611dd-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="611dd-114">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="611dd-114">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="611dd-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="611dd-115">Remarks</span></span>

<span data-ttu-id="611dd-116">O cálculo para a rampa da atenuação para facilitar é calculado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="611dd-116">The calculation for the ramp from ease in to ease out is calculated as follows:</span></span>

<dl> <span data-ttu-id="611dd-117">Q (t) = 2 (x-y) t ³ + 3 (y-x) t ² + x</span><span class="sxs-lookup"><span data-stu-id="611dd-117">Q(t) = 2(x - y)t³ + 3(y - x)t² + x</span></span>  
</dl>

<span data-ttu-id="611dd-118">em que a rampa é uma função Q (t) com as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="611dd-118">where the ramp is a function Q(t) with the following properties:</span></span>

-   <span data-ttu-id="611dd-119">P (t) é uma spline cúbica.</span><span class="sxs-lookup"><span data-stu-id="611dd-119">Q(t) is a cubic spline.</span></span>
-   <span data-ttu-id="611dd-120">P (t) interpola entre x e y como t varia de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="611dd-120">Q(t) interpolates between x and y as t ranges from 0 to 1.</span></span>
-   <span data-ttu-id="611dd-121">Q (t) é horizontal quando t = 0 e t = 1.</span><span class="sxs-lookup"><span data-stu-id="611dd-121">Q(t) is horizontal when t = 0 and t = 1.</span></span>

<span data-ttu-id="611dd-122">Matematicamente, isso se traduz em:</span><span class="sxs-lookup"><span data-stu-id="611dd-122">Mathematically, this translates into:</span></span>

<dl> <span data-ttu-id="611dd-123">Q (t) = at ³ + BT ² + CT + D (e, portanto, Q ' (t) = 3At ² + 2Bt + C)</span><span class="sxs-lookup"><span data-stu-id="611dd-123">Q(t) = At³ + Bt² + Ct + D (and therefore, Q'(t) = 3At² + 2Bt + C)</span></span>  
<span data-ttu-id="611dd-124">2a) Q (0) = x</span><span class="sxs-lookup"><span data-stu-id="611dd-124">2a) Q(0) = x</span></span>  
<span data-ttu-id="611dd-125">2B) Q (1) = y</span><span class="sxs-lookup"><span data-stu-id="611dd-125">2b) Q(1) = y</span></span>  
<span data-ttu-id="611dd-126">3a) Q ' (0) = 0</span><span class="sxs-lookup"><span data-stu-id="611dd-126">3a) Q'(0) = 0</span></span>  
<span data-ttu-id="611dd-127">3B) Q ' (1) = 0</span><span class="sxs-lookup"><span data-stu-id="611dd-127">3b) Q'(1) = 0</span></span>  
</dl>

<span data-ttu-id="611dd-128">Resolvendo para A, B, C, D:</span><span class="sxs-lookup"><span data-stu-id="611dd-128">Solving for A, B, C, D:</span></span>

<dl> <span data-ttu-id="611dd-129">D = x (de 2a)</span><span class="sxs-lookup"><span data-stu-id="611dd-129">D = x (from 2a)</span></span>  
<span data-ttu-id="611dd-130">C = 0 (de 3a)</span><span class="sxs-lookup"><span data-stu-id="611dd-130">C = 0 (from 3a)</span></span>  
<span data-ttu-id="611dd-131">3A + 2B = 0 (de 3B)</span><span class="sxs-lookup"><span data-stu-id="611dd-131">3A + 2B = 0 (from 3b)</span></span>  
<span data-ttu-id="611dd-132">A + B = y-x (de 2B e D = x)</span><span class="sxs-lookup"><span data-stu-id="611dd-132">A + B = y - x (from 2b and D = x)</span></span>  
</dl>

<span data-ttu-id="611dd-133">Portanto:</span><span class="sxs-lookup"><span data-stu-id="611dd-133">Therefore:</span></span>

<dl> <span data-ttu-id="611dd-134">A = 2 (x-y), B = 3 (y-x), C = 0, D = x</span><span class="sxs-lookup"><span data-stu-id="611dd-134">A = 2(x - y), B = 3(y - x), C = 0, D = x</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="611dd-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="611dd-135">Requirements</span></span>



| <span data-ttu-id="611dd-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="611dd-136">Requirement</span></span> | <span data-ttu-id="611dd-137">Valor</span><span class="sxs-lookup"><span data-stu-id="611dd-137">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="611dd-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="611dd-138">Header</span></span><br/> | <dl> <span data-ttu-id="611dd-139"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="611dd-139"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="611dd-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="611dd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="611dd-141">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="611dd-141">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




