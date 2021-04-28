---
description: Função D3DXMatrixMultiplyTranspose (D3DX10Math. h) – calcula o produto transpodo de duas matrizes.
ms.assetid: 3db4138c-407c-47b5-b8b9-04af8771e98e
title: Função D3DXMatrixMultiplyTranspose (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiplyTranspose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fcf3d5578aa6e2ad13bd3f91dfd2206d6eaf0b13
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103413"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx10mathh"></a><span data-ttu-id="2d84b-103">Função D3DXMatrixMultiplyTranspose (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="2d84b-103">D3DXMatrixMultiplyTranspose function (D3DX10Math.h)</span></span>

<span data-ttu-id="2d84b-104">Calcula o produto transpodo de duas matrizes.</span><span class="sxs-lookup"><span data-stu-id="2d84b-104">Calculates the transposed product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d84b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d84b-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="2d84b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d84b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d84b-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="2d84b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d84b-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2d84b-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2d84b-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="2d84b-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2d84b-110">*pM1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2d84b-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d84b-111">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2d84b-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2d84b-112">Ponteiro para uma estrutura de D3DXMATRIX de origem (lado esquerdo).</span><span class="sxs-lookup"><span data-stu-id="2d84b-112">Pointer to a source D3DXMATRIX structure (left hand side).</span></span>

</dd> <dt>

<span data-ttu-id="2d84b-113">*pM2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2d84b-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d84b-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2d84b-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2d84b-115">Ponteiro para uma estrutura de D3DXMATRIX de origem (lado direito).</span><span class="sxs-lookup"><span data-stu-id="2d84b-115">Pointer to a source D3DXMATRIX structure (right hand side).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d84b-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2d84b-116">Return value</span></span>

<span data-ttu-id="2d84b-117">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2d84b-117">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2d84b-118">Ponteiro para uma estrutura D3DXMATRIX que é o produto de duas matrizes.</span><span class="sxs-lookup"><span data-stu-id="2d84b-118">Pointer to a D3DXMATRIX structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d84b-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d84b-119">Remarks</span></span>

<span data-ttu-id="2d84b-120">O resultado é o transpodo do produto de duas matrizes de transformação, out = T (M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="2d84b-120">The result is the transposed of the product of two transformation matrices, Out = T(M1\*M2).</span></span>

<span data-ttu-id="2d84b-121">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="2d84b-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="2d84b-122">Dessa forma, a função D3DXMatrixMultiplyTranspose pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="2d84b-122">In this way, the D3DXMatrixMultiplyTranspose function can be used as a parameter for another function.</span></span>

<span data-ttu-id="2d84b-123">Essa função é útil para definir matrizes como constantes para sombreadores de vértices e de pixel.</span><span class="sxs-lookup"><span data-stu-id="2d84b-123">This function is useful to set matrices as constants for vertex and pixel shaders.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d84b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d84b-124">Requirements</span></span>



| <span data-ttu-id="2d84b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d84b-125">Requirement</span></span> | <span data-ttu-id="2d84b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="2d84b-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d84b-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d84b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="2d84b-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d84b-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="2d84b-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d84b-129">Library</span></span><br/> | <dl> <span data-ttu-id="2d84b-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d84b-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2d84b-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2d84b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d84b-132">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="2d84b-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
