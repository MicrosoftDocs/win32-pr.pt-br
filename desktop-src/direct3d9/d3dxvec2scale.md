---
description: Dimensiona um vetor 2D.
ms.assetid: 1887bc48-3766-42d7-840b-1e29d78db4ce
title: Função D3DXVec2Scale (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Scale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 941e85763b15724e3c810c0416b5b142c9d95913
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298569"
---
# <a name="d3dxvec2scale-function"></a><span data-ttu-id="7e1e6-103">Função D3DXVec2Scale</span><span class="sxs-lookup"><span data-stu-id="7e1e6-103">D3DXVec2Scale function</span></span>

<span data-ttu-id="7e1e6-104">Dimensiona um vetor 2D.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-104">Scales a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e1e6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e1e6-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Scale(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="7e1e6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e1e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e1e6-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="7e1e6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e1e6-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="7e1e6-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7e1e6-109">Ponteiro para a estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7e1e6-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e1e6-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e1e6-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="7e1e6-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7e1e6-112">Ponteiro para a estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7e1e6-113">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="7e1e6-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e1e6-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7e1e6-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7e1e6-115">Valor de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-115">Scaling value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e1e6-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7e1e6-116">Return value</span></span>

<span data-ttu-id="7e1e6-117">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="7e1e6-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7e1e6-118">Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é o vetor dimensionado.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the scaled vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e1e6-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e1e6-119">Remarks</span></span>

<span data-ttu-id="7e1e6-120">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="7e1e6-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="7e1e6-121">Dessa forma, a função **D3DXVec2Scale** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-121">In this way, the **D3DXVec2Scale** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e1e6-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e1e6-122">Requirements</span></span>



| <span data-ttu-id="7e1e6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e1e6-123">Requirement</span></span> | <span data-ttu-id="7e1e6-124">Valor</span><span class="sxs-lookup"><span data-stu-id="7e1e6-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e1e6-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7e1e6-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7e1e6-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e1e6-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7e1e6-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7e1e6-127">Library</span></span><br/> | <dl> <span data-ttu-id="7e1e6-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e1e6-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7e1e6-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e1e6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e1e6-130">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="7e1e6-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7e1e6-131">**D3DXVec2Add**</span><span class="sxs-lookup"><span data-stu-id="7e1e6-131">**D3DXVec2Add**</span></span>](d3dxvec2add.md)
</dt> <dt>

[<span data-ttu-id="7e1e6-132">**D3DXVec2Subtract**</span><span class="sxs-lookup"><span data-stu-id="7e1e6-132">**D3DXVec2Subtract**</span></span>](d3dxvec2subtract.md)
</dt> </dl>

 

 
