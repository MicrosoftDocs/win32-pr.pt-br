---
description: Função D3DXMatrixShadow (D3dx9math. h) – compila uma matriz que achata a geometria em um plano.
ms.assetid: 8f283ff9-c879-476c-8057-f4fe77a7a9e7
title: Função D3DXMatrixShadow (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 111a1448f62cae3f782917de76d92e88aa5a3356
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118054"
---
# <a name="d3dxmatrixshadow-function-d3dx9mathh"></a><span data-ttu-id="bf456-103">Função D3DXMatrixShadow (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="bf456-103">D3DXMatrixShadow function (D3dx9math.h)</span></span>

<span data-ttu-id="bf456-104">Cria uma matriz que achata a geometria em um plano.</span><span class="sxs-lookup"><span data-stu-id="bf456-104">Builds a matrix that flattens geometry into a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf456-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf456-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixShadow(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR4 *pLight,
  _In_    const D3DXPLANE   *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="bf456-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf456-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf456-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="bf456-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf456-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="bf456-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bf456-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="bf456-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bf456-110">*plight* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bf456-110">*pLight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf456-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="bf456-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="bf456-112">Ponteiro para uma estrutura [**D3DXVECTOR4**](d3dxvector4.md) que descreve a posição da luz.</span><span class="sxs-lookup"><span data-stu-id="bf456-112">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure describing the light's position.</span></span>

</dd> <dt>

<span data-ttu-id="bf456-113">*pPlane* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bf456-113">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf456-114">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="bf456-114">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="bf456-115">Ponteiro para a estrutura de [**D3DXPLANE**](d3dxplane.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="bf456-115">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf456-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="bf456-116">Return value</span></span>

<span data-ttu-id="bf456-117">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="bf456-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bf456-118">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que achata a geometria em um plano.</span><span class="sxs-lookup"><span data-stu-id="bf456-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that flattens geometry into a plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf456-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf456-119">Remarks</span></span>

<span data-ttu-id="bf456-120">A função **D3DXMatrixShadow** nivela a geometria em um plano, como se estiver convertendo uma sombra de uma luz.</span><span class="sxs-lookup"><span data-stu-id="bf456-120">The **D3DXMatrixShadow** function flattens geometry into a plane, as if casting a shadow from a light.</span></span>

<span data-ttu-id="bf456-121">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="bf456-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="bf456-122">Dessa forma, a função **D3DXMatrixShadow** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="bf456-122">In this way, the **D3DXMatrixShadow** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="bf456-123">Essa função usa a fórmula a seguir para calcular a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="bf456-123">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
L = Light;
d = -dot(P, L)
    
P.a * L.x + d  P.a * L.y      P.a * L.z      P.a * L.w  
P.b * L.x      P.b * L.y + d  P.b * L.z      P.b * L.w  
P.c * L.x      P.c * L.y      P.c * L.z + d  P.c * L.w  
P.d * L.x      P.d * L.y      P.d * L.z      P.d * L.w + d
```



<span data-ttu-id="bf456-124">Se o componente w da luz for 0, o raio da origem para a luz representará uma luz direcional.</span><span class="sxs-lookup"><span data-stu-id="bf456-124">If the light's w-component is 0, the ray from the origin to the light represents a directional light.</span></span> <span data-ttu-id="bf456-125">Se for 1, a luz será uma luz pontual.</span><span class="sxs-lookup"><span data-stu-id="bf456-125">If it is 1, the light is a point light.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf456-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf456-126">Requirements</span></span>



| <span data-ttu-id="bf456-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf456-127">Requirement</span></span> | <span data-ttu-id="bf456-128">Valor</span><span class="sxs-lookup"><span data-stu-id="bf456-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf456-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf456-129">Header</span></span><br/>  | <dl> <span data-ttu-id="bf456-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf456-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="bf456-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf456-131">Library</span></span><br/> | <dl> <span data-ttu-id="bf456-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf456-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bf456-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="bf456-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf456-134">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="bf456-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




