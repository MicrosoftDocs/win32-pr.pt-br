---
description: Executa uma interpolação de spline Hermite, usando os vetores de 4D especificados.
ms.assetid: 687d4dcf-ee75-4dda-b6d2-5ba0b5281a64
title: Função D3DXVec4Hermite (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Hermite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 85cf60150606a37c2e68ebf72bd4a3772d346660
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173039"
---
# <a name="d3dxvec4hermite-function-d3dx9mathh"></a><span data-ttu-id="f0674-103">Função D3DXVec4Hermite (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f0674-103">D3DXVec4Hermite function (D3dx9math.h)</span></span>

<span data-ttu-id="f0674-104">Executa uma interpolação de spline Hermite, usando os vetores de 4D especificados.</span><span class="sxs-lookup"><span data-stu-id="f0674-104">Performs a Hermite spline interpolation, using the specified 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0674-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0674-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Hermite(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pT1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="f0674-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0674-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0674-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f0674-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0674-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0674-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="f0674-109">Ponteiro para a estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="f0674-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f0674-110">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f0674-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0674-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="f0674-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="f0674-112">Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem, um vetor de posição.</span><span class="sxs-lookup"><span data-stu-id="f0674-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="f0674-113">*pT1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f0674-113">*pT1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0674-114">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="f0674-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="f0674-115">Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem, um vetor tangente.</span><span class="sxs-lookup"><span data-stu-id="f0674-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="f0674-116">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f0674-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0674-117">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="f0674-117">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="f0674-118">Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem, um vetor de posição.</span><span class="sxs-lookup"><span data-stu-id="f0674-118">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="f0674-119">*pT2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f0674-119">*pT2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0674-120">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="f0674-120">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="f0674-121">Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem, um vetor tangente.</span><span class="sxs-lookup"><span data-stu-id="f0674-121">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="f0674-122">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="f0674-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0674-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0674-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f0674-124">Fator de ponderação.</span><span class="sxs-lookup"><span data-stu-id="f0674-124">Weighting factor.</span></span> <span data-ttu-id="f0674-125">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="f0674-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0674-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f0674-126">Return value</span></span>

<span data-ttu-id="f0674-127">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0674-127">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="f0674-128">Ponteiro para uma estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o resultado da interpolação Hermite spline.</span><span class="sxs-lookup"><span data-stu-id="f0674-128">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the Hermite spline interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0674-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0674-129">Remarks</span></span>

<span data-ttu-id="f0674-130">A função **D3DXVec4Hermite** interpola de (positiona, tangentea) a (PositionB, tangentB) usando a interpolação Hermite spline.</span><span class="sxs-lookup"><span data-stu-id="f0674-130">The **D3DXVec4Hermite** function interpolates from (positionA, tangentA) to (positionB, tangentB) using Hermite spline interpolation.</span></span>

<span data-ttu-id="f0674-131">A interpolação de spline é uma generalização da spline de fácil entrada, de fácil saída.</span><span class="sxs-lookup"><span data-stu-id="f0674-131">The spline interpolation is a generalization of the ease-in, ease-out spline.</span></span> <span data-ttu-id="f0674-132">A rampa é uma função de Q (s) com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="f0674-132">The ramp is a function of Q(s) with the following properties.</span></span>

<span data-ttu-id="f0674-133">Q (s) = as ³ + BS ² + CS + D (e, portanto, Q ' s) = 3As ² + 2Bs + C)</span><span class="sxs-lookup"><span data-stu-id="f0674-133">Q(s) = As³ + Bs² + Cs + D (and therefore, Q'(s) = 3As² + 2Bs + C)</span></span>

<span data-ttu-id="f0674-134">a) Q (0) = v1, portanto, Q ' (0) = T1</span><span class="sxs-lookup"><span data-stu-id="f0674-134">a) Q(0) = v1, so Q'(0) = t1</span></span>

<span data-ttu-id="f0674-135">b) Q (1) = v2, portanto Q ' (1) = T2</span><span class="sxs-lookup"><span data-stu-id="f0674-135">b) Q(1) = v2, so Q'(1) = t2</span></span>

<span data-ttu-id="f0674-136">v1 é o conteúdo de pV1, V2 no conteúdo de pV2, T1 é o conteúdo de pT1 e T2 é o conteúdo de pT2.</span><span class="sxs-lookup"><span data-stu-id="f0674-136">v1 is the contents of pV1, v2 in the contents of pV2, t1 is the contents of pT1, and t2 is the contents of pT2.</span></span>

<span data-ttu-id="f0674-137">Essas propriedades são usadas para resolver para A, B, C, D.</span><span class="sxs-lookup"><span data-stu-id="f0674-137">These properties are used to solve for A, B, C, D.</span></span>

<span data-ttu-id="f0674-138">Conecte as soluções para a, B, C e D para gerar Q (s).</span><span class="sxs-lookup"><span data-stu-id="f0674-138">Plug in the solutions for A,B,C and D to generate Q(s).</span></span>

``` syntax
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```

<span data-ttu-id="f0674-139">Isso resulta em:</span><span class="sxs-lookup"><span data-stu-id="f0674-139">This yields:</span></span>

<span data-ttu-id="f0674-140">Q (s) = (2v1-2v2 + T2 + T1) s ³ + (3v2-3V1-2T1-T2) s ² + T1s + v1</span><span class="sxs-lookup"><span data-stu-id="f0674-140">Q(s) = (2v1 - 2v2 + t2 + t1)s³ + (3v2 - 3v1 - 2t1 - t2)s² + t1s + v1</span></span>

<span data-ttu-id="f0674-141">Que pode ser reorganizado como:</span><span class="sxs-lookup"><span data-stu-id="f0674-141">Which can be rearranged as:</span></span>

<span data-ttu-id="f0674-142">Q (s) = (2S ³-3S ² + 1) V1 + (-2S ³ + 3S ²) V2 + (s ³-2s ² + s) T1 + (s ³-s ²) T2</span><span class="sxs-lookup"><span data-stu-id="f0674-142">Q(s) = (2s³ - 3s² + 1)v1 + (-2s³ + 3s²)v2 + (s³ - 2s² + s)t1 + (s³ - s²)t2</span></span>

<span data-ttu-id="f0674-143">As Hermites são úteis para controlar a animação porque a curva é executada por todos os pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="f0674-143">Hermite splines are useful for controlling animation because the curve runs through all the control points.</span></span> <span data-ttu-id="f0674-144">Além disso, como a posição e a tangente são especificadas explicitamente nas extremidades de cada segmento, é fácil criar uma curva contínua C2, contanto que você verifique se a posição inicial e a tangente correspondem aos valores finais do último segmento.</span><span class="sxs-lookup"><span data-stu-id="f0674-144">Also, because the position and tangent are explicitly specified at the ends of each segment, it is easy to create a C2 continuous curve as long as you make sure that your starting position and tangent match the ending values of the last segment.</span></span>

<span data-ttu-id="f0674-145">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="f0674-145">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f0674-146">Dessa forma, a função **D3DXVec4Hermite** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="f0674-146">In this way, the **D3DXVec4Hermite** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0674-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0674-147">Requirements</span></span>



| <span data-ttu-id="f0674-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0674-148">Requirement</span></span> | <span data-ttu-id="f0674-149">Valor</span><span class="sxs-lookup"><span data-stu-id="f0674-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0674-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f0674-150">Header</span></span><br/>  | <dl> <span data-ttu-id="f0674-151"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0674-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f0674-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f0674-152">Library</span></span><br/> | <dl> <span data-ttu-id="f0674-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0674-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f0674-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0674-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0674-155">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="f0674-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
