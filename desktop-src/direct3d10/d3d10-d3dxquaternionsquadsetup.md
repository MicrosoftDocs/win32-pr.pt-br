---
description: Configura pontos de controle para a interpolação de Quadrangle esférica.
ms.assetid: c66227bd-8cc1-4173-9dc2-5aab9d57301e
title: Função D3DXQuaternionSquadSetup (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquadSetup
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4a0683bce3642b0300e68be348d8aed39b3c333d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764453"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx10mathh"></a><span data-ttu-id="872fe-103">Função D3DXQuaternionSquadSetup (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="872fe-103">D3DXQuaternionSquadSetup function (D3DX10Math.h)</span></span>

<span data-ttu-id="872fe-104">Configura pontos de controle para a interpolação de Quadrangle esférica.</span><span class="sxs-lookup"><span data-stu-id="872fe-104">Sets up control points for spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="872fe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="872fe-105">Syntax</span></span>


```C++
void D3DXQuaternionSquadSetup(
  _In_       D3DXQUATERNION *pAOut,
  _In_       D3DXQUATERNION *pBOut,
  _In_       D3DXQUATERNION *pCOut,
  _In_ const D3DXQUATERNION *pQ0,
  _In_ const D3DXQUATERNION *pQ1,
  _In_ const D3DXQUATERNION *pQ2,
  _In_ const D3DXQUATERNION *pQ3
);
```



## <a name="parameters"></a><span data-ttu-id="872fe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="872fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="872fe-107">*pAOut* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="872fe-107">*pAOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="872fe-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="872fe-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="872fe-109">Ponteiro para AOut.</span><span class="sxs-lookup"><span data-stu-id="872fe-109">Pointer to AOut.</span></span>

</dd> <dt>

<span data-ttu-id="872fe-110">*pBOut* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="872fe-110">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="872fe-111">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="872fe-111">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="872fe-112">Ponteiro para obre.</span><span class="sxs-lookup"><span data-stu-id="872fe-112">Pointer to BOut.</span></span>

</dd> <dt>

<span data-ttu-id="872fe-113">*pCOut* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="872fe-113">*pCOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="872fe-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="872fe-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="872fe-115">Ponteiro para COut.</span><span class="sxs-lookup"><span data-stu-id="872fe-115">Pointer to COut.</span></span>

</dd> <dt>

<span data-ttu-id="872fe-116">*pQ0* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="872fe-116">*pQ0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="872fe-117">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="872fe-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="872fe-118">Ponteiro para o ponto de controle de entrada, Q0.</span><span class="sxs-lookup"><span data-stu-id="872fe-118">Pointer to the input control point, Q0.</span></span>

</dd> <dt>

<span data-ttu-id="872fe-119">*pQ1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="872fe-119">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="872fe-120">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="872fe-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="872fe-121">Ponteiro para o ponto de controle de entrada, Q1.</span><span class="sxs-lookup"><span data-stu-id="872fe-121">Pointer to the input control point, Q1.</span></span>

</dd> <dt>

<span data-ttu-id="872fe-122">*pQ2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="872fe-122">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="872fe-123">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="872fe-123">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="872fe-124">Ponteiro para o ponto de controle de entrada, Q2.</span><span class="sxs-lookup"><span data-stu-id="872fe-124">Pointer to the input control point, Q2.</span></span>

</dd> <dt>

<span data-ttu-id="872fe-125">*pQ3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="872fe-125">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="872fe-126">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="872fe-126">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="872fe-127">Ponteiro para o ponto de controle de entrada, Q3.</span><span class="sxs-lookup"><span data-stu-id="872fe-127">Pointer to the input control point, Q3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="872fe-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="872fe-128">Return value</span></span>

<span data-ttu-id="872fe-129">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="872fe-129">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="872fe-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="872fe-130">Remarks</span></span>

<span data-ttu-id="872fe-131">Essa função usa quatro pontos de controle, que são fornecidos para as entradas pQ0, pQ1, pQ2 e pQ3.</span><span class="sxs-lookup"><span data-stu-id="872fe-131">This function takes four control points, which are supplied to the inputs pQ0, pQ1, pQ2, and pQ3.</span></span> <span data-ttu-id="872fe-132">Em seguida, a função altera esses valores para encontrar uma curva que flui ao longo do caminho mais curto.</span><span class="sxs-lookup"><span data-stu-id="872fe-132">The function then alters these values to find a curve that flows along the shortest path.</span></span> <span data-ttu-id="872fe-133">Os valores de q0, Q2 e Q3 são calculados conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="872fe-133">The values of q0, q2, and q3 are calculated as shown below.</span></span>


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



<span data-ttu-id="872fe-134">Depois de calcular os novos valores de Q, os valores para AOut, obre e COut são calculados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="872fe-134">Having calculated the new Q values, the values for AOut, BOut, and COut are calculated as follows:</span></span>

<span data-ttu-id="872fe-135">AOut = T1 \* e<sup> \[ -0,25 \ \* (\ ln \[ exp (Q1) \* T2 \] \ + \ ln \[ exp (Q1) \* q0 \] \) \ \] </sup></span><span class="sxs-lookup"><span data-stu-id="872fe-135">AOut = q1 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q1)\*q2\]\ +\ Ln\[Exp(q1)\*q0\]\ )\ \]</sup></span></span>

<span data-ttu-id="872fe-136">Obre = T2 \* e<sup> \[ -0,25 \ \* (\ ln \[ exp (Q2) \* Q3 \] \ + \ f ln \[ exp (T2) \* Q1 \] \) \] \</sup></span><span class="sxs-lookup"><span data-stu-id="872fe-136">BOut = q2 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q2)\*q3\]\ +\ Ln\[Exp(q2)\*q1\]\ )\ \]</sup></span></span>

<span data-ttu-id="872fe-137">COut = Q2</span><span class="sxs-lookup"><span data-stu-id="872fe-137">COut = q2</span></span>

> [!Note]  
> <span data-ttu-id="872fe-138">Ln é o método de API [**D3DXQuaternionLn**](d3d10-d3dxquaternionln.md) e exp é o método de API [**D3DXQuaternionExp**](d3d10-d3dxquaternionexp.md).</span><span class="sxs-lookup"><span data-stu-id="872fe-138">Ln is the API method [**D3DXQuaternionLn**](d3d10-d3dxquaternionln.md) and Exp is the API method [**D3DXQuaternionExp**](d3d10-d3dxquaternionexp.md).</span></span>

 

<span data-ttu-id="872fe-139">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="872fe-139">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

### <a name="examples"></a><span data-ttu-id="872fe-140">Exemplos</span><span class="sxs-lookup"><span data-stu-id="872fe-140">Examples</span></span>

<span data-ttu-id="872fe-141">O exemplo a seguir mostra como usar um conjunto de chaves quaternions (q0, Q1, T2, Q3) para computar os pontos Quadrangle internos (A, B, C).</span><span class="sxs-lookup"><span data-stu-id="872fe-141">The following example shows how to use a set of quaternion keys (Q0, Q1, Q2, Q3) to compute the inner quadrangle points (A, B, C).</span></span> <span data-ttu-id="872fe-142">Isso garante que as tangentes sejam contínuas em segmentos adjacentes.</span><span class="sxs-lookup"><span data-stu-id="872fe-142">This ensures that the tangents are continuous across adjacent segments.</span></span>


```
      A     B
Q0    Q1    Q2    Q3
```



<span data-ttu-id="872fe-143">O exemplo de código a seguir demonstra como você pode interpolar entre Q1 e Q2.</span><span class="sxs-lookup"><span data-stu-id="872fe-143">The following code example demonstrates how you can interpolate between Q1 and Q2.</span></span>


```
// Rotation about the z-axis
D3DXQUATERNION Q0 = D3DXQUATERNION(0,  0, 0.707f, -.707f);
D3DXQUATERNION Q1 = D3DXQUATERNION(0,  0, 0.000f, 1.000f);
D3DXQUATERNION Q2 = D3DXQUATERNION(0,  0, 0.707f, 0.707f);
D3DXQUATERNION Q3 = D3DXQUATERNION(0,  0, 1.000f, 0.000f);
D3DXQUATERNION A, B, C, Qt;
FLOAT time = 0.5f;

D3DXQuaternionSquadSetup(&A, &B, &C, &Q0, &Q1, &Q2, &Q3);
D3DXQuaternionSquad(&Qt, &Q1, &A, &B, &C, time);
```



> [!Note]
>
> -   <span data-ttu-id="872fe-144">C é +/-Q2, dependendo do resultado da função.</span><span class="sxs-lookup"><span data-stu-id="872fe-144">C is +/- Q2 depending on the result of the function.</span></span>
> -   <span data-ttu-id="872fe-145">Qt é o resultado da função.</span><span class="sxs-lookup"><span data-stu-id="872fe-145">Qt is the result of the function.</span></span>
>
> <span data-ttu-id="872fe-146">O resultado é uma rotação de 45 graus em volta do eixo z para time = 0,5.</span><span class="sxs-lookup"><span data-stu-id="872fe-146">The result is a rotation of 45 degrees around the z-axis for time = 0.5.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="872fe-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="872fe-147">Requirements</span></span>



| <span data-ttu-id="872fe-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="872fe-148">Requirement</span></span> | <span data-ttu-id="872fe-149">Valor</span><span class="sxs-lookup"><span data-stu-id="872fe-149">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="872fe-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="872fe-150">Header</span></span><br/>  | <dl> <span data-ttu-id="872fe-151"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="872fe-151"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="872fe-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="872fe-152">Library</span></span><br/> | <dl> <span data-ttu-id="872fe-153"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="872fe-153"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="872fe-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="872fe-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="872fe-155">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="872fe-155">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
