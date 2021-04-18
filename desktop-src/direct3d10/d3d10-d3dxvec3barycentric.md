---
description: Retorna um ponto em coordenadas barycentric, usando os vetores 3D especificados.
ms.assetid: 572e151d-8044-480e-92b2-3f973d92d03e
title: Função D3DXVec3BaryCentric (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3BaryCentric
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 3c14d01acc71a13cabb810d5b26d0afaf7f67f7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781098"
---
# <a name="d3dxvec3barycentric-function-d3dx10mathh"></a><span data-ttu-id="40106-103">Função D3DXVec3BaryCentric (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="40106-103">D3DXVec3BaryCentric function (D3DX10Math.h)</span></span>

<span data-ttu-id="40106-104">Retorna um ponto em coordenadas barycentric, usando os vetores 3D especificados.</span><span class="sxs-lookup"><span data-stu-id="40106-104">Returns a point in Barycentric coordinates, using the specified 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="40106-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40106-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3BaryCentric(
  _In_       D3DXVECTOR3 *pOut,
  _In_ const D3DXVECTOR3 *pV1,
  _In_ const D3DXVECTOR3 *pV2,
  _In_ const D3DXVECTOR3 *pV3,
  _In_       FLOAT       f,
  _In_       FLOAT       g
);
```



## <a name="parameters"></a><span data-ttu-id="40106-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40106-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40106-107">*pout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="40106-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40106-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="40106-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="40106-109">Ponteiro para o [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="40106-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="40106-110">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="40106-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40106-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="40106-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="40106-112">Ponteiro para uma estrutura de D3DXVECTOR3 de origem.</span><span class="sxs-lookup"><span data-stu-id="40106-112">Pointer to a source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="40106-113">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="40106-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40106-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="40106-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="40106-115">Ponteiro para uma estrutura de D3DXVECTOR3 de origem.</span><span class="sxs-lookup"><span data-stu-id="40106-115">Pointer to a source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="40106-116">*pV3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="40106-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40106-117">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="40106-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="40106-118">Ponteiro para uma estrutura de D3DXVECTOR3 de origem.</span><span class="sxs-lookup"><span data-stu-id="40106-118">Pointer to a source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="40106-119">*f* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="40106-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40106-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40106-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="40106-121">Fator de ponderação.</span><span class="sxs-lookup"><span data-stu-id="40106-121">Weighting factor.</span></span> <span data-ttu-id="40106-122">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="40106-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="40106-123">*g* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="40106-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40106-124">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40106-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="40106-125">Fator de ponderação.</span><span class="sxs-lookup"><span data-stu-id="40106-125">Weighting factor.</span></span> <span data-ttu-id="40106-126">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="40106-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40106-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="40106-127">Return value</span></span>

<span data-ttu-id="40106-128">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="40106-128">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="40106-129">Ponteiro para uma estrutura D3DXVECTOR3 em coordenadas barycentric.</span><span class="sxs-lookup"><span data-stu-id="40106-129">Pointer to a D3DXVECTOR3 structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="40106-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="40106-130">Remarks</span></span>

<span data-ttu-id="40106-131">A função D3DXVec3BaryCentric fornece uma maneira de entender os pontos em um triângulo, independentemente de onde o triângulo realmente está localizado.</span><span class="sxs-lookup"><span data-stu-id="40106-131">The D3DXVec3BaryCentric function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="40106-132">Essa função retorna o ponto resultante usando a seguinte equação: v1 + f (v2-v1) + g (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="40106-132">This function returns the resulting point by using the following equation: V1 + f(V2-V1) + g(V3-V1).</span></span>

<span data-ttu-id="40106-133">Qualquer ponto no V1V2V3 do plano pode ser representado pela coordenada barycentric (f, g). O parâmetro f controla a quantidade de v2 que é ponderada no resultado e o parâmetro g controla a quantidade de v3 ponderada no resultado.</span><span class="sxs-lookup"><span data-stu-id="40106-133">Any point in the plane V1V2V3 can be represented by the Barycentric coordinate (f,g).The parameter f controls how much V2 gets weighted into the result and the parameter g controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="40106-134">Por fim, 1-f-g controla o quanto v1 é ponderado no resultado.</span><span class="sxs-lookup"><span data-stu-id="40106-134">Lastly, 1-f-g controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="40106-135">Observe as seguintes relações.</span><span class="sxs-lookup"><span data-stu-id="40106-135">Note the following relations.</span></span>

-   <span data-ttu-id="40106-136">Se (f>= 0 &, & g>= 0 &, & 1-f-g>= 0), o ponto estará dentro do triângulo V1V2V3.</span><span class="sxs-lookup"><span data-stu-id="40106-136">If (f>=0 &, & g>=0 &, & 1-f-g>=0), the point is inside the triangle V1V2V3.</span></span>
-   <span data-ttu-id="40106-137">Se (f = = 0 &, & g>= 0 &, & 1-f-g>= 0), o ponto estará na linha V1V3.</span><span class="sxs-lookup"><span data-stu-id="40106-137">If (f==0 &, & g>=0 &, & 1-f-g>=0), the point is on the line V1V3.</span></span>
-   <span data-ttu-id="40106-138">Se (f>= 0 &, & g = = 0 &, & 1-f-g>= 0), o ponto estará na linha V1V2.</span><span class="sxs-lookup"><span data-stu-id="40106-138">If (f>=0 &, & g==0 &, & 1-f-g>=0), the point is on the line V1V2.</span></span>
-   <span data-ttu-id="40106-139">Se (f>= 0 &, & g>= 0 &, & 1-f-g = = 0), o ponto estará na linha V2V3.</span><span class="sxs-lookup"><span data-stu-id="40106-139">If (f>=0 &, & g>=0 &, & 1-f-g==0), the point is on the line V2V3.</span></span>

<span data-ttu-id="40106-140">As coordenadas de barycentric são uma forma de coordenadas gerais.</span><span class="sxs-lookup"><span data-stu-id="40106-140">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="40106-141">Nesse contexto, o uso de coordenadas barycentric representa uma alteração nos sistemas de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="40106-141">In this context, using Barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="40106-142">O que se aplica a coordenadas cartesianas é verdadeiro para coordenadas Barycentrics.</span><span class="sxs-lookup"><span data-stu-id="40106-142">What holds true for Cartesian coordinates holds true for Barycentric coordinates.</span></span>

<span data-ttu-id="40106-143">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="40106-143">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="40106-144">Dessa forma, a função D3DXVec3BaryCentric pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="40106-144">In this way, the D3DXVec3BaryCentric function can be used as a parameter for another function.</span></span>

<span data-ttu-id="40106-145">As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo.</span><span class="sxs-lookup"><span data-stu-id="40106-145">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="40106-146">Para obter uma descrição mais detalhada das coordenadas de barycentric, consulte [Descrição de coordenadas barycentric do MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="40106-146">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="40106-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40106-147">Requirements</span></span>



| <span data-ttu-id="40106-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="40106-148">Requirement</span></span> | <span data-ttu-id="40106-149">Valor</span><span class="sxs-lookup"><span data-stu-id="40106-149">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40106-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="40106-150">Header</span></span><br/> | <dl> <span data-ttu-id="40106-151"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="40106-151"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40106-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="40106-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40106-153">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="40106-153">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
