---
description: Função D3DXMatrixMultiply (D3dx9math. h) – determina o produto de duas matrizes.
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
ms.openlocfilehash: 3d183fc3c79797bab886d3a40211448ccf57d552
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107544"
---
# <a name="d3dxmatrixmultiply-function-d3dx9mathh"></a><span data-ttu-id="159bc-103">Função D3DXMatrixMultiply (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="159bc-103">D3DXMatrixMultiply function (D3dx9math.h)</span></span>

<span data-ttu-id="159bc-104">Determina o produto de duas matrizes.</span><span class="sxs-lookup"><span data-stu-id="159bc-104">Determines the product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="159bc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="159bc-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiply(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="159bc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="159bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="159bc-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="159bc-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="159bc-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="159bc-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="159bc-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="159bc-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="159bc-110">*pM1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="159bc-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="159bc-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="159bc-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="159bc-112">Ponteiro para uma estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="159bc-112">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="159bc-113">*pM2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="159bc-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="159bc-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="159bc-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="159bc-115">Ponteiro para uma estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="159bc-115">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="159bc-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="159bc-116">Return value</span></span>

<span data-ttu-id="159bc-117">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="159bc-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="159bc-118">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o produto de duas matrizes.</span><span class="sxs-lookup"><span data-stu-id="159bc-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="159bc-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="159bc-119">Remarks</span></span>

<span data-ttu-id="159bc-120">O resultado representa a transformação M1 seguida da transformação m2 (out = M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="159bc-120">The result represents the transformation M1 followed by the transformation M2 (Out = M1 \* M2).</span></span>

<span data-ttu-id="159bc-121">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="159bc-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="159bc-122">Dessa forma, a função **D3DXMatrixMultiply** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="159bc-122">In this way, the **D3DXMatrixMultiply** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="159bc-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="159bc-123">Requirements</span></span>



| <span data-ttu-id="159bc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="159bc-124">Requirement</span></span> | <span data-ttu-id="159bc-125">Valor</span><span class="sxs-lookup"><span data-stu-id="159bc-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="159bc-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="159bc-126">Header</span></span><br/>  | <dl> <span data-ttu-id="159bc-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="159bc-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="159bc-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="159bc-128">Library</span></span><br/> | <dl> <span data-ttu-id="159bc-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="159bc-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="159bc-130">Consulte também</span><span class="sxs-lookup"><span data-stu-id="159bc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="159bc-131">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="159bc-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="159bc-132">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="159bc-132">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




