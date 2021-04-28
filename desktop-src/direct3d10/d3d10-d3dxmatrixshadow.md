---
description: Função D3DXMatrixShadow (D3DX10Math. h) – compila uma matriz que achata a geometria em um plano.
ms.assetid: 83c9e7d6-fc6c-48e7-bbf2-6aa10868351d
title: Função D3DXMatrixShadow (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixShadow
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d3a5bff99552a4c5d65267c390c25a2892d3d32f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103344"
---
# <a name="d3dxmatrixshadow-function-d3dx10mathh"></a><span data-ttu-id="98db1-103">Função D3DXMatrixShadow (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="98db1-103">D3DXMatrixShadow function (D3DX10Math.h)</span></span>

<span data-ttu-id="98db1-104">Cria uma matriz que achata a geometria em um plano.</span><span class="sxs-lookup"><span data-stu-id="98db1-104">Builds a matrix that flattens geometry into a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="98db1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98db1-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixShadow(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR4 *pLight,
  _In_    const D3DXPLANE   *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="98db1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98db1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98db1-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="98db1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="98db1-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="98db1-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="98db1-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="98db1-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="98db1-110">*plight* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="98db1-110">*pLight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98db1-111">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="98db1-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="98db1-112">Ponteiro para um [**D3DXVECTOR4**](d3d10-d3dxvector4.md) que descreve a posição da luz.</span><span class="sxs-lookup"><span data-stu-id="98db1-112">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) describing the light's position.</span></span>

</dd> <dt>

<span data-ttu-id="98db1-113">*pPlane* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="98db1-113">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98db1-114">Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="98db1-114">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="98db1-115">Ponteiro para o [**D3DXPLANE**](d3d10-d3dxplane.md)de origem.</span><span class="sxs-lookup"><span data-stu-id="98db1-115">Pointer to the source [**D3DXPLANE**](d3d10-d3dxplane.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98db1-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="98db1-116">Return value</span></span>

<span data-ttu-id="98db1-117">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="98db1-117">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="98db1-118">Ponteiro para uma estrutura D3DXMATRIX que achata a geometria em um plano.</span><span class="sxs-lookup"><span data-stu-id="98db1-118">Pointer to a D3DXMATRIX structure that flattens geometry into a plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="98db1-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="98db1-119">Remarks</span></span>

<span data-ttu-id="98db1-120">A função **D3DXMatrixShadow** nivela a geometria em um plano, como se estiver convertendo uma sombra de uma luz.</span><span class="sxs-lookup"><span data-stu-id="98db1-120">The **D3DXMatrixShadow** function flattens geometry into a plane, as if casting a shadow from a light.</span></span>

<span data-ttu-id="98db1-121">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="98db1-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="98db1-122">Dessa forma, a função **D3DXMatrixShadow** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="98db1-122">In this way, the **D3DXMatrixShadow** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="98db1-123">Essa função usa a fórmula a seguir para calcular a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="98db1-123">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
L = Light;
d = dot(P, L)
    
P.a * L.x + d  P.a * L.y      P.a * L.z      P.a * L.w  
P.b * L.x      P.b * L.y + d  P.b * L.z      P.b * L.w  
P.c * L.x      P.c * L.y      P.c * L.z + d  P.c * L.w  
P.d * L.x      P.d * L.y      P.d * L.z      P.d * L.w + d
```



<span data-ttu-id="98db1-124">Se o componente w da luz for 0, o raio da origem para a luz representará uma luz direcional.</span><span class="sxs-lookup"><span data-stu-id="98db1-124">If the light's w-component is 0, the ray from the origin to the light represents a directional light.</span></span> <span data-ttu-id="98db1-125">Se for 1, a luz será uma luz pontual.</span><span class="sxs-lookup"><span data-stu-id="98db1-125">If it is 1, the light is a point light.</span></span>

## <a name="requirements"></a><span data-ttu-id="98db1-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98db1-126">Requirements</span></span>



| <span data-ttu-id="98db1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="98db1-127">Requirement</span></span> | <span data-ttu-id="98db1-128">Valor</span><span class="sxs-lookup"><span data-stu-id="98db1-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98db1-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="98db1-129">Header</span></span><br/>  | <dl> <span data-ttu-id="98db1-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="98db1-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="98db1-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98db1-131">Library</span></span><br/> | <dl> <span data-ttu-id="98db1-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98db1-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="98db1-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="98db1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98db1-134">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="98db1-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
