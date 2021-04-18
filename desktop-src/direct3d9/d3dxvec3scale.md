---
description: Dimensiona um vetor 3D.
ms.assetid: b2483d6e-56e4-4557-a603-d59c0767774d
title: Função D3DXVec3Scale (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Scale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5357b862b9cf82e458429edea27001163eb9635
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793278"
---
# <a name="d3dxvec3scale-function"></a><span data-ttu-id="16a9b-103">Função D3DXVec3Scale</span><span class="sxs-lookup"><span data-stu-id="16a9b-103">D3DXVec3Scale function</span></span>

<span data-ttu-id="16a9b-104">Dimensiona um vetor 3D.</span><span class="sxs-lookup"><span data-stu-id="16a9b-104">Scales a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="16a9b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16a9b-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Scale(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="16a9b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16a9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16a9b-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="16a9b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="16a9b-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="16a9b-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="16a9b-109">Ponteiro para a estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="16a9b-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="16a9b-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16a9b-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16a9b-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="16a9b-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="16a9b-112">Ponteiro para a estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="16a9b-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="16a9b-113">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="16a9b-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16a9b-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16a9b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="16a9b-115">Valor de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="16a9b-115">Scaling value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16a9b-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="16a9b-116">Return value</span></span>

<span data-ttu-id="16a9b-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="16a9b-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="16a9b-118">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é o vetor dimensionado.</span><span class="sxs-lookup"><span data-stu-id="16a9b-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the scaled vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="16a9b-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="16a9b-119">Remarks</span></span>

<span data-ttu-id="16a9b-120">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="16a9b-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="16a9b-121">Dessa forma, a função **D3DXVec3Scale** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="16a9b-121">In this way, the **D3DXVec3Scale** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="16a9b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16a9b-122">Requirements</span></span>



| <span data-ttu-id="16a9b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="16a9b-123">Requirement</span></span> | <span data-ttu-id="16a9b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="16a9b-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16a9b-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16a9b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="16a9b-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="16a9b-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="16a9b-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="16a9b-127">Library</span></span><br/> | <dl> <span data-ttu-id="16a9b-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16a9b-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="16a9b-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="16a9b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16a9b-130">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="16a9b-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="16a9b-131">**D3DXVec3Add**</span><span class="sxs-lookup"><span data-stu-id="16a9b-131">**D3DXVec3Add**</span></span>](d3dxvec3add.md)
</dt> <dt>

[<span data-ttu-id="16a9b-132">**D3DXVec3Subtract**</span><span class="sxs-lookup"><span data-stu-id="16a9b-132">**D3DXVec3Subtract**</span></span>](d3dxvec3subtract.md)
</dt> </dl>

 

 
