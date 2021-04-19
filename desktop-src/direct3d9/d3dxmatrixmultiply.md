---
description: Determina o produto de duas matrizes.
ms.assetid: 160c801a-6589-4a0d-8e90-7e7a99fbd5f7
title: Função D3DXMatrixMultiply (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ea578f54d3f690f01d9280e840cb9ee039d0cdf0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771608"
---
# <a name="d3dxmatrixmultiply-function-d3dx9mathh"></a><span data-ttu-id="bfba3-103">Função D3DXMatrixMultiply (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="bfba3-103">D3DXMatrixMultiply function (D3dx9math.h)</span></span>

<span data-ttu-id="bfba3-104">Determina o produto de duas matrizes.</span><span class="sxs-lookup"><span data-stu-id="bfba3-104">Determines the product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfba3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bfba3-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiply(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="bfba3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bfba3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfba3-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="bfba3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bfba3-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="bfba3-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bfba3-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="bfba3-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bfba3-110">*pM1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bfba3-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfba3-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="bfba3-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bfba3-112">Ponteiro para uma estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="bfba3-112">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="bfba3-113">*pM2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bfba3-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfba3-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="bfba3-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bfba3-115">Ponteiro para uma estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="bfba3-115">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfba3-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bfba3-116">Return value</span></span>

<span data-ttu-id="bfba3-117">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="bfba3-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bfba3-118">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o produto de duas matrizes.</span><span class="sxs-lookup"><span data-stu-id="bfba3-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfba3-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="bfba3-119">Remarks</span></span>

<span data-ttu-id="bfba3-120">O resultado representa a transformação M1 seguida da transformação m2 (out = M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="bfba3-120">The result represents the transformation M1 followed by the transformation M2 (Out = M1 \* M2).</span></span>

<span data-ttu-id="bfba3-121">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="bfba3-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="bfba3-122">Dessa forma, a função **D3DXMatrixMultiply** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="bfba3-122">In this way, the **D3DXMatrixMultiply** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfba3-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfba3-123">Requirements</span></span>



| <span data-ttu-id="bfba3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfba3-124">Requirement</span></span> | <span data-ttu-id="bfba3-125">Valor</span><span class="sxs-lookup"><span data-stu-id="bfba3-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfba3-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bfba3-126">Header</span></span><br/>  | <dl> <span data-ttu-id="bfba3-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfba3-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="bfba3-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bfba3-128">Library</span></span><br/> | <dl> <span data-ttu-id="bfba3-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bfba3-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bfba3-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="bfba3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfba3-131">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="bfba3-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="bfba3-132">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="bfba3-132">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




