---
description: Função D3DXQuaternionSquadSetup (D3dx9math. h) – configura pontos de controle para a interpolação de Quadrangle esférica.
ms.assetid: f800d457-8546-49a1-800e-e5c27af96710
title: Função D3DXQuaternionSquadSetup (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1dcaa90380ec703b4b56458906ab8bd965d7568c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093944"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx9mathh"></a><span data-ttu-id="85905-103">Função D3DXQuaternionSquadSetup (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="85905-103">D3DXQuaternionSquadSetup function (D3dx9math.h)</span></span>

<span data-ttu-id="85905-104">Configura pontos de controle para a interpolação de Quadrangle esférica.</span><span class="sxs-lookup"><span data-stu-id="85905-104">Sets up control points for spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="85905-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="85905-105">Syntax</span></span>


```C++
void D3DXQuaternionSquadSetup(
  _Out_       D3DXQUATERNION *pAOut,
  _Out_       D3DXQUATERNION *pBOut,
  _Out_       D3DXQUATERNION *pCOut,
  _In_  const D3DXQUATERNION *pQ0,
  _In_  const D3DXQUATERNION *pQ1,
  _In_  const D3DXQUATERNION *pQ2,
  _In_  const D3DXQUATERNION *pQ3
);
```



## <a name="parameters"></a><span data-ttu-id="85905-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85905-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85905-107">*pAOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="85905-107">*pAOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85905-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="85905-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="85905-109">Ponteiro para AOut.</span><span class="sxs-lookup"><span data-stu-id="85905-109">Pointer to AOut.</span></span>

</dd> <dt>

<span data-ttu-id="85905-110">*pBOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="85905-110">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85905-111">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="85905-111">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="85905-112">Ponteiro para obre.</span><span class="sxs-lookup"><span data-stu-id="85905-112">Pointer to BOut.</span></span>

</dd> <dt>

<span data-ttu-id="85905-113">*pCOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="85905-113">*pCOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85905-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="85905-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="85905-115">Ponteiro para COut.</span><span class="sxs-lookup"><span data-stu-id="85905-115">Pointer to COut.</span></span>

</dd> <dt>

<span data-ttu-id="85905-116">*pQ0* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="85905-116">*pQ0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85905-117">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="85905-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="85905-118">Ponteiro para o ponto de controle de entrada, Q0.</span><span class="sxs-lookup"><span data-stu-id="85905-118">Pointer to the input control point, Q0.</span></span>

</dd> <dt>

<span data-ttu-id="85905-119">*pQ1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="85905-119">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85905-120">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="85905-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="85905-121">Ponteiro para o ponto de controle de entrada, Q1.</span><span class="sxs-lookup"><span data-stu-id="85905-121">Pointer to the input control point, Q1.</span></span>

</dd> <dt>

<span data-ttu-id="85905-122">*pQ2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="85905-122">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85905-123">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="85905-123">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="85905-124">Ponteiro para o ponto de controle de entrada, Q2.</span><span class="sxs-lookup"><span data-stu-id="85905-124">Pointer to the input control point, Q2.</span></span>

</dd> <dt>

<span data-ttu-id="85905-125">*pQ3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="85905-125">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85905-126">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="85905-126">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="85905-127">Ponteiro para o ponto de controle de entrada, Q3.</span><span class="sxs-lookup"><span data-stu-id="85905-127">Pointer to the input control point, Q3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85905-128">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="85905-128">Return value</span></span>

<span data-ttu-id="85905-129">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="85905-129">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="85905-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="85905-130">Remarks</span></span>

<span data-ttu-id="85905-131">Essa função usa quatro pontos de controle, que são fornecidos para as entradas pQ0, pQ1, pQ2 e pQ3.</span><span class="sxs-lookup"><span data-stu-id="85905-131">This function takes four control points, which are supplied to the inputs pQ0, pQ1, pQ2, and pQ3.</span></span> <span data-ttu-id="85905-132">Em seguida, a função altera esses valores para encontrar uma curva que flui ao longo do caminho mais curto.</span><span class="sxs-lookup"><span data-stu-id="85905-132">The function then alters these values to find a curve that flows along the shortest path.</span></span> <span data-ttu-id="85905-133">Os valores de q0, Q2 e Q3 são calculados conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="85905-133">The values of q0, q2, and q3 are calculated as shown below.</span></span>


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



<span data-ttu-id="85905-134">Depois de calcular os novos valores de Q, os valores para AOut, obre e COut são calculados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="85905-134">Having calculated the new Q values, the values for AOut, BOut, and COut are calculated as follows:</span></span>

<span data-ttu-id="85905-135">AOut = T1 \* e<sup> \[ -0,25 \ \* (\ ln \[ exp (Q1) \* T2 \] \ + \ ln \[ exp (Q1) \* q0 \] \) \ \] </sup></span><span class="sxs-lookup"><span data-stu-id="85905-135">AOut = q1 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q1)\*q2\]\ +\ Ln\[Exp(q1)\*q0\]\ )\ \]</sup></span></span>

<span data-ttu-id="85905-136">Obre = T2 \* e<sup> \[ -0,25 \ \* (\ ln \[ exp (Q2) \* Q3 \] \ + \ f ln \[ exp (T2) \* Q1 \] \) \] \</sup></span><span class="sxs-lookup"><span data-stu-id="85905-136">BOut = q2 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q2)\*q3\]\ +\ Ln\[Exp(q2)\*q1\]\ )\ \]</sup></span></span>

<span data-ttu-id="85905-137">COut = Q2</span><span class="sxs-lookup"><span data-stu-id="85905-137">COut = q2</span></span>

> [!Note]  
> <span data-ttu-id="85905-138">Ln é o método de API [**D3DXQuaternionLn**](d3dxquaternionln.md) e exp é o método de API [**D3DXQuaternionExp**](d3dxquaternionexp.md).</span><span class="sxs-lookup"><span data-stu-id="85905-138">Ln is the API method [**D3DXQuaternionLn**](d3dxquaternionln.md) and Exp is the API method [**D3DXQuaternionExp**](d3dxquaternionexp.md).</span></span>

 

<span data-ttu-id="85905-139">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="85905-139">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

### <a name="examples"></a><span data-ttu-id="85905-140">Exemplos</span><span class="sxs-lookup"><span data-stu-id="85905-140">Examples</span></span>

<span data-ttu-id="85905-141">O exemplo a seguir mostra como usar um conjunto de chaves quaternions (q0, Q1, T2, Q3) para computar os pontos Quadrangle internos (A, B, C).</span><span class="sxs-lookup"><span data-stu-id="85905-141">The following example shows how to use a set of quaternion keys (Q0, Q1, Q2, Q3) to compute the inner quadrangle points (A, B, C).</span></span> <span data-ttu-id="85905-142">Isso garante que as tangentes sejam contínuas em segmentos adjacentes.</span><span class="sxs-lookup"><span data-stu-id="85905-142">This ensures that the tangents are continuous across adjacent segments.</span></span>


```
      A     B
Q0    Q1    Q2    Q3
```



<span data-ttu-id="85905-143">O exemplo de código a seguir demonstra como você pode interpolar entre Q1 e Q2.</span><span class="sxs-lookup"><span data-stu-id="85905-143">The following code example demonstrates how you can interpolate between Q1 and Q2.</span></span>


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
> -   <span data-ttu-id="85905-144">C é +/-Q2, dependendo do resultado da função.</span><span class="sxs-lookup"><span data-stu-id="85905-144">C is +/- Q2 depending on the result of the function.</span></span>
> -   <span data-ttu-id="85905-145">Qt é o resultado da função.</span><span class="sxs-lookup"><span data-stu-id="85905-145">Qt is the result of the function.</span></span>
>
> <span data-ttu-id="85905-146">O resultado é uma rotação de 45 graus em volta do eixo z para time = 0,5.</span><span class="sxs-lookup"><span data-stu-id="85905-146">The result is a rotation of 45 degrees around the z-axis for time = 0.5.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="85905-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85905-147">Requirements</span></span>



| <span data-ttu-id="85905-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="85905-148">Requirement</span></span> | <span data-ttu-id="85905-149">Valor</span><span class="sxs-lookup"><span data-stu-id="85905-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85905-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="85905-150">Header</span></span><br/>  | <dl> <span data-ttu-id="85905-151"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="85905-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="85905-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="85905-152">Library</span></span><br/> | <dl> <span data-ttu-id="85905-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85905-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="85905-154">Consulte também</span><span class="sxs-lookup"><span data-stu-id="85905-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85905-155">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="85905-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="85905-156">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="85905-156">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




