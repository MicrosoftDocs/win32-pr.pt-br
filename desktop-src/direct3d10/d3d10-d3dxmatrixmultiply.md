---
description: Função D3DXMatrixMultiply (D3DX10Math. h) – determina o produto de duas matrizes.
ms.assetid: d15cd680-0e19-4353-9eee-73933663960e
title: Função D3DXMatrixMultiply (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiply
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 89e103d441648643be0176ca34f72f6175c11213
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113124"
---
# <a name="d3dxmatrixmultiply-function-d3dx10mathh"></a><span data-ttu-id="6d71d-103">Função D3DXMatrixMultiply (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="6d71d-103">D3DXMatrixMultiply function (D3DX10Math.h)</span></span>

<span data-ttu-id="6d71d-104">Determina o produto de duas matrizes.</span><span class="sxs-lookup"><span data-stu-id="6d71d-104">Determines the product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d71d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d71d-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiply(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="6d71d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d71d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d71d-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="6d71d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d71d-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6d71d-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6d71d-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="6d71d-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6d71d-110">*pM1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d71d-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d71d-111">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6d71d-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6d71d-112">Ponteiro para uma estrutura de D3DXMATRIX de origem (lado esquerdo).</span><span class="sxs-lookup"><span data-stu-id="6d71d-112">Pointer to a source D3DXMATRIX structure (left hand side).</span></span>

</dd> <dt>

<span data-ttu-id="6d71d-113">*pM2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d71d-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d71d-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6d71d-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6d71d-115">Ponteiro para uma estrutura de D3DXMATRIX de origem (lado direito).</span><span class="sxs-lookup"><span data-stu-id="6d71d-115">Pointer to a source D3DXMATRIX structure (right hand side).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d71d-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6d71d-116">Return value</span></span>

<span data-ttu-id="6d71d-117">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6d71d-117">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6d71d-118">Ponteiro para uma estrutura D3DXMATRIX que é o produto de duas matrizes.</span><span class="sxs-lookup"><span data-stu-id="6d71d-118">Pointer to a D3DXMATRIX structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d71d-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d71d-119">Remarks</span></span>

<span data-ttu-id="6d71d-120">O resultado representa a transformação M1 seguida da transformação m2 (out = M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="6d71d-120">The result represents the transformation M1 followed by the transformation M2 (Out = M1 \* M2).</span></span>

<span data-ttu-id="6d71d-121">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="6d71d-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="6d71d-122">Dessa forma, a função D3DXMatrixMultiply pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="6d71d-122">In this way, the D3DXMatrixMultiply function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d71d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d71d-123">Requirements</span></span>



| <span data-ttu-id="6d71d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d71d-124">Requirement</span></span> | <span data-ttu-id="6d71d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="6d71d-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d71d-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6d71d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6d71d-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d71d-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="6d71d-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6d71d-128">Library</span></span><br/> | <dl> <span data-ttu-id="6d71d-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d71d-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6d71d-130">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6d71d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d71d-131">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="6d71d-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
