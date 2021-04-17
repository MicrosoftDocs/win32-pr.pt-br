---
description: Retorna um ponto nas coordenadas de barycentric, usando os vetores de 4D especificados.
ms.assetid: 80d73232-76bf-4f40-add2-dd1bdcc5cd98
title: Função D3DXVec4BaryCentric (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4BaryCentric
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 75f0d068d1545f1b8b55dc3b976d3585e6f9bc88
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105752366"
---
# <a name="d3dxvec4barycentric-function-d3dx9mathh"></a><span data-ttu-id="a5f98-103">Função D3DXVec4BaryCentric (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a5f98-103">D3DXVec4BaryCentric function (D3dx9math.h)</span></span>

<span data-ttu-id="a5f98-104">Retorna um ponto nas coordenadas de barycentric, usando os vetores de 4D especificados.</span><span class="sxs-lookup"><span data-stu-id="a5f98-104">Returns a point in Barycentric coordinates, using the specified 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5f98-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5f98-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4BaryCentric(
  _Out_       D3DXVECTOR4 *pOut,
  _In_  const D3DXVECTOR4 *pV1,
  _In_  const D3DXVECTOR4 *pV2,
  _In_  const D3DXVECTOR4 *pV3,
  _In_        FLOAT       f,
  _In_        FLOAT       g
);
```



## <a name="parameters"></a><span data-ttu-id="a5f98-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5f98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5f98-107">*pout* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a5f98-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5f98-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="a5f98-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="a5f98-109">Ponteiro para a estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="a5f98-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a5f98-110">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a5f98-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5f98-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="a5f98-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="a5f98-112">Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="a5f98-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a5f98-113">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a5f98-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5f98-114">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="a5f98-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="a5f98-115">Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="a5f98-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a5f98-116">*pV3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a5f98-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5f98-117">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="a5f98-117">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="a5f98-118">Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="a5f98-118">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a5f98-119">*f* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="a5f98-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5f98-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5f98-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a5f98-121">Fator de ponderação.</span><span class="sxs-lookup"><span data-stu-id="a5f98-121">Weighting factor.</span></span> <span data-ttu-id="a5f98-122">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="a5f98-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a5f98-123">*g* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="a5f98-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5f98-124">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5f98-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a5f98-125">Fator de ponderação.</span><span class="sxs-lookup"><span data-stu-id="a5f98-125">Weighting factor.</span></span> <span data-ttu-id="a5f98-126">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="a5f98-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5f98-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a5f98-127">Return value</span></span>

<span data-ttu-id="a5f98-128">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="a5f98-128">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="a5f98-129">Ponteiro para uma estrutura [**D3DXVECTOR4**](d3dxvector4.md) em coordenadas barycentric.</span><span class="sxs-lookup"><span data-stu-id="a5f98-129">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5f98-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5f98-130">Remarks</span></span>

<span data-ttu-id="a5f98-131">A função **D3DXVec4BaryCentric** fornece uma maneira de entender os pontos em um triângulo, independentemente de onde o triângulo realmente está localizado.</span><span class="sxs-lookup"><span data-stu-id="a5f98-131">The **D3DXVec4BaryCentric** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="a5f98-132">Essa função retorna o ponto resultante usando a seguinte equação: v1 + f (v2-v1) + g (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="a5f98-132">This function returns the resulting point by using the following equation: V1 + f(V2-V1) + g(V3-V1).</span></span>

<span data-ttu-id="a5f98-133">Qualquer ponto no V1V2V3 do plano pode ser representado pela coordenada barycentric (f, g). O parâmetro *f* controla a quantidade de v2 que é ponderada no resultado e o parâmetro *g* controla a quantidade de v3 ponderada no resultado.</span><span class="sxs-lookup"><span data-stu-id="a5f98-133">Any point in the plane V1V2V3 can be represented by the Barycentric coordinate (f,g).The parameter *f* controls how much V2 gets weighted into the result and the parameter *g* controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="a5f98-134">Por fim, 1-f-g controla o quanto v1 é ponderado no resultado.</span><span class="sxs-lookup"><span data-stu-id="a5f98-134">Lastly, 1-f-g controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="a5f98-135">Observe as seguintes relações.</span><span class="sxs-lookup"><span data-stu-id="a5f98-135">Note the following relations.</span></span>

-   <span data-ttu-id="a5f98-136">Se (f>= 0 &, & g>= 0 &, & 1-f-g>= 0), o ponto estará dentro do triângulo V1V2V3.</span><span class="sxs-lookup"><span data-stu-id="a5f98-136">If (f>=0 &, & g>=0 &, & 1-f-g>=0), the point is inside the triangle V1V2V3.</span></span>
-   <span data-ttu-id="a5f98-137">Se (f = = 0 &, & g>= 0 &, & 1-f-g>= 0), o ponto estará na linha V1V3.</span><span class="sxs-lookup"><span data-stu-id="a5f98-137">If (f==0 &, & g>=0 &, & 1-f-g>=0), the point is on the line V1V3.</span></span>
-   <span data-ttu-id="a5f98-138">Se (f>= 0 &, & g = = 0 &, & 1-f-g>= 0), o ponto estará na linha V1V2.</span><span class="sxs-lookup"><span data-stu-id="a5f98-138">If (f>=0 &, & g==0 &, & 1-f-g>=0), the point is on the line V1V2.</span></span>
-   <span data-ttu-id="a5f98-139">Se (f>= 0 &, & g>= 0 &, & 1-f-g = = 0), o ponto estará na linha V2V3.</span><span class="sxs-lookup"><span data-stu-id="a5f98-139">If (f>=0 &, & g>=0 &, & 1-f-g==0), the point is on the line V2V3.</span></span>

<span data-ttu-id="a5f98-140">As coordenadas de barycentric são uma forma de coordenadas gerais.</span><span class="sxs-lookup"><span data-stu-id="a5f98-140">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="a5f98-141">Nesse contexto, o uso de coordenadas barycentric representa uma alteração nos sistemas de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="a5f98-141">In this context, using Barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="a5f98-142">O que se aplica a coordenadas cartesianas é verdadeiro para coordenadas Barycentrics.</span><span class="sxs-lookup"><span data-stu-id="a5f98-142">What holds true for Cartesian coordinates holds true for Barycentric coordinates.</span></span>

<span data-ttu-id="a5f98-143">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="a5f98-143">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a5f98-144">Dessa forma, a função **D3DXVec4BaryCentric** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="a5f98-144">In this way, the **D3DXVec4BaryCentric** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="a5f98-145">As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo.</span><span class="sxs-lookup"><span data-stu-id="a5f98-145">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="a5f98-146">Para obter uma descrição mais detalhada das coordenadas de barycentric, consulte [Descrição de coordenadas barycentric do MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="a5f98-146">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5f98-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5f98-147">Requirements</span></span>



| <span data-ttu-id="a5f98-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5f98-148">Requirement</span></span> | <span data-ttu-id="a5f98-149">Valor</span><span class="sxs-lookup"><span data-stu-id="a5f98-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5f98-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a5f98-150">Header</span></span><br/>  | <dl> <span data-ttu-id="a5f98-151"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5f98-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a5f98-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a5f98-152">Library</span></span><br/> | <dl> <span data-ttu-id="a5f98-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5f98-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a5f98-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5f98-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5f98-155">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="a5f98-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
