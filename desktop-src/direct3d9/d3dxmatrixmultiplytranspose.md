---
description: Função D3DXMatrixMultiplyTranspose (D3dx9math. h) – calcula o produto transpodo de duas matrizes.
ms.assetid: 43927500-9413-41a4-a6ee-974d85dd1054
title: Função D3DXMatrixMultiplyTranspose (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87aaa45e7a7a16884d17ab340f0bf1efeccd93bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107534"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx9mathh"></a><span data-ttu-id="16458-103">Função D3DXMatrixMultiplyTranspose (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="16458-103">D3DXMatrixMultiplyTranspose function (D3dx9math.h)</span></span>

<span data-ttu-id="16458-104">Calcula o produto transpodo de duas matrizes.</span><span class="sxs-lookup"><span data-stu-id="16458-104">Calculates the transposed product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="16458-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16458-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="16458-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16458-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16458-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="16458-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="16458-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="16458-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="16458-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="16458-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="16458-110">*pM1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16458-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16458-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="16458-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="16458-112">Ponteiro para uma estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="16458-112">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="16458-113">*pM2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16458-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16458-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="16458-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="16458-115">Ponteiro para uma estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="16458-115">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16458-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="16458-116">Return value</span></span>

<span data-ttu-id="16458-117">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="16458-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="16458-118">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o produto de duas matrizes.</span><span class="sxs-lookup"><span data-stu-id="16458-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="16458-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="16458-119">Remarks</span></span>

<span data-ttu-id="16458-120">O resultado é o transpodo do produto de duas matrizes de transformação, out = T (M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="16458-120">The result is the transposed of the product of two transformation matrices, Out = T(M1\*M2).</span></span>

<span data-ttu-id="16458-121">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="16458-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="16458-122">Dessa forma, a função **D3DXMatrixMultiplyTranspose** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="16458-122">In this way, the **D3DXMatrixMultiplyTranspose** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="16458-123">Essa função é útil para definir matrizes como constantes para sombreadores de vértices e de pixel.</span><span class="sxs-lookup"><span data-stu-id="16458-123">This function is useful to set matrices as constants for vertex and pixel shaders.</span></span>

## <a name="requirements"></a><span data-ttu-id="16458-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16458-124">Requirements</span></span>



| <span data-ttu-id="16458-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="16458-125">Requirement</span></span> | <span data-ttu-id="16458-126">Valor</span><span class="sxs-lookup"><span data-stu-id="16458-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16458-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16458-127">Header</span></span><br/>  | <dl> <span data-ttu-id="16458-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="16458-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="16458-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="16458-129">Library</span></span><br/> | <dl> <span data-ttu-id="16458-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16458-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="16458-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="16458-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16458-132">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="16458-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="16458-133">**D3DXMatrixMultiply**</span><span class="sxs-lookup"><span data-stu-id="16458-133">**D3DXMatrixMultiply**</span></span>](d3dxmatrixmultiply.md)
</dt> <dt>

[<span data-ttu-id="16458-134">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="16458-134">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




