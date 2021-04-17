---
description: Executa uma interpolação linear entre dois vetores 2D.
ms.assetid: f8e9e6be-9696-4a4a-a6c8-c021985decaa
title: Função D3DXVec2Lerp (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Lerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b08b767993143db3057985140b97854b9203d2b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798412"
---
# <a name="d3dxvec2lerp-function"></a><span data-ttu-id="637e3-103">Função D3DXVec2Lerp</span><span class="sxs-lookup"><span data-stu-id="637e3-103">D3DXVec2Lerp function</span></span>

<span data-ttu-id="637e3-104">Executa uma interpolação linear entre dois vetores 2D.</span><span class="sxs-lookup"><span data-stu-id="637e3-104">Performs a linear interpolation between two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="637e3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="637e3-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Lerp(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="637e3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="637e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="637e3-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="637e3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="637e3-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="637e3-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="637e3-109">Ponteiro para a estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="637e3-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="637e3-110">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="637e3-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="637e3-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="637e3-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="637e3-112">Ponteiro para uma estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="637e3-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="637e3-113">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="637e3-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="637e3-114">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="637e3-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="637e3-115">Ponteiro para uma estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="637e3-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="637e3-116">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="637e3-116">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="637e3-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="637e3-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="637e3-118">Parâmetro que interpola linearmente entre os vetores.</span><span class="sxs-lookup"><span data-stu-id="637e3-118">Parameter that linearly interpolates between the vectors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="637e3-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="637e3-119">Return value</span></span>

<span data-ttu-id="637e3-120">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="637e3-120">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="637e3-121">Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é o resultado da interpolação linear.</span><span class="sxs-lookup"><span data-stu-id="637e3-121">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the linear interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="637e3-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="637e3-122">Remarks</span></span>

<span data-ttu-id="637e3-123">Essa função executa a interpolação linear com base na seguinte fórmula: v1 + s (v2-v1).</span><span class="sxs-lookup"><span data-stu-id="637e3-123">This function performs the linear interpolation based on the following formula: V1 + s(V2-V1).</span></span>

<span data-ttu-id="637e3-124">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="637e3-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="637e3-125">Dessa forma, a função **D3DXVec2Lerp** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="637e3-125">In this way, the **D3DXVec2Lerp** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="637e3-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="637e3-126">Requirements</span></span>



| <span data-ttu-id="637e3-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="637e3-127">Requirement</span></span> | <span data-ttu-id="637e3-128">Valor</span><span class="sxs-lookup"><span data-stu-id="637e3-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="637e3-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="637e3-129">Header</span></span><br/>  | <dl> <span data-ttu-id="637e3-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="637e3-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="637e3-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="637e3-131">Library</span></span><br/> | <dl> <span data-ttu-id="637e3-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="637e3-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="637e3-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="637e3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="637e3-134">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="637e3-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
