---
description: Determina o produto de duas matrizes.
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
ms.openlocfilehash: 5f07130c25ce9ef1c588309460e4e12e67bb2485
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930724"
---
# <a name="d3dxmatrixmultiply-function-d3dx10mathh"></a><span data-ttu-id="722a8-103">Função D3DXMatrixMultiply (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="722a8-103">D3DXMatrixMultiply function (D3DX10Math.h)</span></span>

<span data-ttu-id="722a8-104">Determina o produto de duas matrizes.</span><span class="sxs-lookup"><span data-stu-id="722a8-104">Determines the product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="722a8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="722a8-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiply(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="722a8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="722a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="722a8-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="722a8-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="722a8-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="722a8-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="722a8-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="722a8-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="722a8-110">*pM1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="722a8-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="722a8-111">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="722a8-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="722a8-112">Ponteiro para uma estrutura de D3DXMATRIX de origem (lado esquerdo).</span><span class="sxs-lookup"><span data-stu-id="722a8-112">Pointer to a source D3DXMATRIX structure (left hand side).</span></span>

</dd> <dt>

<span data-ttu-id="722a8-113">*pM2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="722a8-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="722a8-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="722a8-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="722a8-115">Ponteiro para uma estrutura de D3DXMATRIX de origem (lado direito).</span><span class="sxs-lookup"><span data-stu-id="722a8-115">Pointer to a source D3DXMATRIX structure (right hand side).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="722a8-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="722a8-116">Return value</span></span>

<span data-ttu-id="722a8-117">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="722a8-117">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="722a8-118">Ponteiro para uma estrutura D3DXMATRIX que é o produto de duas matrizes.</span><span class="sxs-lookup"><span data-stu-id="722a8-118">Pointer to a D3DXMATRIX structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="722a8-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="722a8-119">Remarks</span></span>

<span data-ttu-id="722a8-120">O resultado representa a transformação M1 seguida da transformação m2 (out = M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="722a8-120">The result represents the transformation M1 followed by the transformation M2 (Out = M1 \* M2).</span></span>

<span data-ttu-id="722a8-121">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="722a8-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="722a8-122">Dessa forma, a função D3DXMatrixMultiply pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="722a8-122">In this way, the D3DXMatrixMultiply function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="722a8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="722a8-123">Requirements</span></span>



| <span data-ttu-id="722a8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="722a8-124">Requirement</span></span> | <span data-ttu-id="722a8-125">Valor</span><span class="sxs-lookup"><span data-stu-id="722a8-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="722a8-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="722a8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="722a8-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="722a8-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="722a8-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="722a8-128">Library</span></span><br/> | <dl> <span data-ttu-id="722a8-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="722a8-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="722a8-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="722a8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="722a8-131">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="722a8-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
