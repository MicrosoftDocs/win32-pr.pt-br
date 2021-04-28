---
description: Função D3DXQuaternionBaryCentric (D3dx9math. h) – retorna um Quaternion em coordenadas barycentric.
ms.assetid: 8fcd2e16-1bf1-4e18-afc9-17c92f2bbac5
title: Função D3DXQuaternionBaryCentric (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionBaryCentric
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2ce0cfc7b3a59dc2a3cae6fa240015e70a035695
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094104"
---
# <a name="d3dxquaternionbarycentric-function-d3dx9mathh"></a><span data-ttu-id="50544-103">Função D3DXQuaternionBaryCentric (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="50544-103">D3DXQuaternionBaryCentric function (D3dx9math.h)</span></span>

<span data-ttu-id="50544-104">Retorna um Quaternion nas coordenadas de barycentric.</span><span class="sxs-lookup"><span data-stu-id="50544-104">Returns a quaternion in barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="50544-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50544-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionBaryCentric(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_    const D3DXQUATERNION *pQ3,
  _In_          FLOAT          f,
  _In_          FLOAT          g
);
```



## <a name="parameters"></a><span data-ttu-id="50544-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50544-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50544-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="50544-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="50544-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="50544-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="50544-109">Ponteiro para a estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="50544-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="50544-110">*pQ1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50544-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50544-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="50544-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="50544-112">Ponteiro para uma estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="50544-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="50544-113">*pQ2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50544-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50544-114">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="50544-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="50544-115">Ponteiro para uma estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="50544-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="50544-116">*pQ3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50544-116">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50544-117">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="50544-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="50544-118">Ponteiro para uma estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="50544-118">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="50544-119">*f* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="50544-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50544-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="50544-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="50544-121">Fator de ponderação.</span><span class="sxs-lookup"><span data-stu-id="50544-121">Weighting factor.</span></span> <span data-ttu-id="50544-122">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="50544-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="50544-123">*g* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="50544-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50544-124">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="50544-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="50544-125">Fator de ponderação.</span><span class="sxs-lookup"><span data-stu-id="50544-125">Weighting factor.</span></span> <span data-ttu-id="50544-126">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="50544-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50544-127">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="50544-127">Return value</span></span>

<span data-ttu-id="50544-128">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="50544-128">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="50544-129">Ponteiro para uma estrutura [**D3DXQUATERNION**](d3dxquaternion.md) em coordenadas barycentric.</span><span class="sxs-lookup"><span data-stu-id="50544-129">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="50544-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="50544-130">Remarks</span></span>

<span data-ttu-id="50544-131">Para computar as coordenadas barycentric, a função **D3DXQuaternionBaryCentric** implementa a seguinte série de operações de interpolação linear esférica:</span><span class="sxs-lookup"><span data-stu-id="50544-131">To compute the barycentric coordinates, the **D3DXQuaternionBaryCentric** function implements the following series of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(Q1, Q2, f+g), Slerp(Q1, Q3, f+g), g/(f+g))
```



<span data-ttu-id="50544-132">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="50544-132">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="50544-133">Dessa forma, a função **D3DXQuaternionBaryCentric** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="50544-133">In this way, the **D3DXQuaternionBaryCentric** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="50544-134">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="50544-134">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

<span data-ttu-id="50544-135">As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo.</span><span class="sxs-lookup"><span data-stu-id="50544-135">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="50544-136">Para obter uma descrição mais detalhada das coordenadas de barycentric, consulte [Descrição de coordenadas barycentric do MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="50544-136">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="50544-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50544-137">Requirements</span></span>



| <span data-ttu-id="50544-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="50544-138">Requirement</span></span> | <span data-ttu-id="50544-139">Valor</span><span class="sxs-lookup"><span data-stu-id="50544-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50544-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="50544-140">Header</span></span><br/>  | <dl> <span data-ttu-id="50544-141"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="50544-141"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="50544-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="50544-142">Library</span></span><br/> | <dl> <span data-ttu-id="50544-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50544-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="50544-144">Consulte também</span><span class="sxs-lookup"><span data-stu-id="50544-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50544-145">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="50544-145">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
