---
description: Função D3DXVec2Hermite (D3DX10Math. h) – executa uma interpolação de spline Hermite, usando os vetores 2D especificados.
ms.assetid: 2d6ff836-a1a7-4cd0-aea3-4fe344f4e211
title: Função D3DXVec2Hermite (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Hermite
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e64350d4f54fef493ec7fe935474218a1b111503
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108374"
---
# <a name="d3dxvec2hermite-function-d3dx10mathh"></a><span data-ttu-id="74601-103">Função D3DXVec2Hermite (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="74601-103">D3DXVec2Hermite function (D3DX10Math.h)</span></span>

<span data-ttu-id="74601-104">Executa uma interpolação de spline Hermite, usando os vetores 2D especificados.</span><span class="sxs-lookup"><span data-stu-id="74601-104">Performs a Hermite spline interpolation, using the specified 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="74601-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74601-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Hermite(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pT1,
  _In_    const D3DXVECTOR2 *pV2,
  _In_    const D3DXVECTOR2 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="74601-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74601-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74601-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="74601-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="74601-108">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="74601-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="74601-109">Ponteiro para o [**D3DXVECTOR2**](d3d10-d3dxvector2.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="74601-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="74601-110">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="74601-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74601-111">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="74601-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="74601-112">Ponteiro para uma estrutura de D3DXVECTOR2 de origem, um vetor de posição.</span><span class="sxs-lookup"><span data-stu-id="74601-112">Pointer to a source D3DXVECTOR2 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="74601-113">*pT1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="74601-113">*pT1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74601-114">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="74601-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="74601-115">Ponteiro para uma estrutura de D3DXVECTOR2 de origem, um vetor tangente.</span><span class="sxs-lookup"><span data-stu-id="74601-115">Pointer to a source D3DXVECTOR2 structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="74601-116">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="74601-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74601-117">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="74601-117">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="74601-118">Ponteiro para uma estrutura de D3DXVECTOR2 de origem, um vetor de posição.</span><span class="sxs-lookup"><span data-stu-id="74601-118">Pointer to a source D3DXVECTOR2 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="74601-119">*pT2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="74601-119">*pT2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74601-120">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="74601-120">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="74601-121">Ponteiro para uma estrutura de D3DXVECTOR2 de origem, um vetor tangente.</span><span class="sxs-lookup"><span data-stu-id="74601-121">Pointer to a source D3DXVECTOR2 structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="74601-122">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="74601-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74601-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74601-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74601-124">Fator de ponderação.</span><span class="sxs-lookup"><span data-stu-id="74601-124">Weighting factor.</span></span> <span data-ttu-id="74601-125">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="74601-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74601-126">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="74601-126">Return value</span></span>

<span data-ttu-id="74601-127">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="74601-127">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="74601-128">Ponteiro para uma estrutura D3DXVECTOR2 que é o resultado da interpolação Hermite spline.</span><span class="sxs-lookup"><span data-stu-id="74601-128">Pointer to a D3DXVECTOR2 structure that is the result of the Hermite spline interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="74601-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="74601-129">Remarks</span></span>

<span data-ttu-id="74601-130">A função **D3DXVec2Hermite** interpola de (positiona, tangentea) a (PositionB, tangentB) usando a interpolação Hermite spline.</span><span class="sxs-lookup"><span data-stu-id="74601-130">The **D3DXVec2Hermite** function interpolates from (positionA, tangentA) to (positionB, tangentB) using Hermite spline interpolation.</span></span>

<span data-ttu-id="74601-131">A interpolação de spline é uma generalização da spline de fácil entrada, de fácil saída.</span><span class="sxs-lookup"><span data-stu-id="74601-131">The spline interpolation is a generalization of the ease-in, ease-out spline.</span></span> <span data-ttu-id="74601-132">A rampa é uma função de Q (s) com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="74601-132">The ramp is a function of Q(s) with the following properties.</span></span>

<span data-ttu-id="74601-133">Q (s) = as ³ + BS ² + CS + D (e, portanto, Q ' s) = 3As ² + 2Bs + C)</span><span class="sxs-lookup"><span data-stu-id="74601-133">Q(s) = As³ + Bs² + Cs + D (and therefore, Q'(s) = 3As² + 2Bs + C)</span></span>

<span data-ttu-id="74601-134">a) Q (0) = v1, portanto, Q ' (0) = T1</span><span class="sxs-lookup"><span data-stu-id="74601-134">a) Q(0) = v1, so Q'(0) = t1</span></span>

<span data-ttu-id="74601-135">b) Q (1) = v2, portanto Q ' (1) = T2</span><span class="sxs-lookup"><span data-stu-id="74601-135">b) Q(1) = v2, so Q'(1) = t2</span></span>

<span data-ttu-id="74601-136">v1 é o conteúdo de pV1, V2 no conteúdo de pV2, T1 é o conteúdo de pT1 e T2 é o conteúdo de pT2.</span><span class="sxs-lookup"><span data-stu-id="74601-136">v1 is the contents of pV1, v2 in the contents of pV2, t1 is the contents of pT1, and t2 is the contents of pT2.</span></span>

<span data-ttu-id="74601-137">Essas propriedades são usadas para resolver para A, B, C, D.</span><span class="sxs-lookup"><span data-stu-id="74601-137">These properties are used to solve for A, B, C, D.</span></span>


```
D = v1  (from a)
C = t1  (from a)
3A + 2B = t2 - t-1 (substituting for C)
A + B = v2 - v1 - t1 (substituting for C and D)
```



<span data-ttu-id="74601-138">Conecte as soluções para a, B, C e D para gerar Q (s).</span><span class="sxs-lookup"><span data-stu-id="74601-138">Plug in the solutions for A,B,C and D to generate Q(s).</span></span>


```
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```



<span data-ttu-id="74601-139">Isso resulta em:</span><span class="sxs-lookup"><span data-stu-id="74601-139">This yields:</span></span>

<span data-ttu-id="74601-140">Q (s) = (2v1-2v2 + T2 + T1) s ³ + (3v2-3V1-2T1-T2) s ² + T1s + v1</span><span class="sxs-lookup"><span data-stu-id="74601-140">Q(s) = (2v1 - 2v2 + t2 + t1)s³ + (3v2 - 3v1 - 2t1 - t2)s² + t1s + v1</span></span>

<span data-ttu-id="74601-141">Que pode ser reorganizado como:</span><span class="sxs-lookup"><span data-stu-id="74601-141">Which can be rearranged as:</span></span>

<span data-ttu-id="74601-142">Q (s) = (2S ³-3S ² + 1) V1 + (-2S ³ + 3S ²) V2 + (s ³-2s ² + s) T1 + (s ³-s ²) T2</span><span class="sxs-lookup"><span data-stu-id="74601-142">Q(s) = (2s³ - 3s² + 1)v1 + (-2s³ + 3s²)v2 + (s³ - 2s² + s)t1 + (s³ - s²)t2</span></span>

<span data-ttu-id="74601-143">As Hermites são úteis para controlar a animação porque a curva é executada por todos os pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="74601-143">Hermite splines are useful for controlling animation because the curve runs through all the control points.</span></span> <span data-ttu-id="74601-144">Além disso, como a posição e a tangente são especificadas explicitamente nas extremidades de cada segmento, é fácil criar uma curva contínua C2, contanto que você verifique se a posição inicial e a tangente correspondem aos valores finais do último segmento.</span><span class="sxs-lookup"><span data-stu-id="74601-144">Also, because the position and tangent are explicitly specified at the ends of each segment, it is easy to create a C2 continuous curve as long as you make sure that your starting position and tangent match the ending values of the last segment.</span></span>

<span data-ttu-id="74601-145">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="74601-145">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="74601-146">Dessa forma, a função **D3DXVec2Hermite** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="74601-146">In this way, the **D3DXVec2Hermite** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="74601-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74601-147">Requirements</span></span>



| <span data-ttu-id="74601-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="74601-148">Requirement</span></span> | <span data-ttu-id="74601-149">Valor</span><span class="sxs-lookup"><span data-stu-id="74601-149">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74601-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="74601-150">Header</span></span><br/>  | <dl> <span data-ttu-id="74601-151"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="74601-151"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="74601-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="74601-152">Library</span></span><br/> | <dl> <span data-ttu-id="74601-153"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74601-153"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="74601-154">Consulte também</span><span class="sxs-lookup"><span data-stu-id="74601-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74601-155">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="74601-155">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
