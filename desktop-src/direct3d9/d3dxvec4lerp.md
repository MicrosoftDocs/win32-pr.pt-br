---
description: Executa uma interpolação linear entre dois vetores de 4D.
ms.assetid: a068a626-17cd-4df9-8f41-9b417bfda1d1
title: Função D3DXVec4Lerp (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Lerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8df6f7b4be5a39335532dc86096f989727230942
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105786188"
---
# <a name="d3dxvec4lerp-function"></a><span data-ttu-id="ce326-103">Função D3DXVec4Lerp</span><span class="sxs-lookup"><span data-stu-id="ce326-103">D3DXVec4Lerp function</span></span>

<span data-ttu-id="ce326-104">Executa uma interpolação linear entre dois vetores de 4D.</span><span class="sxs-lookup"><span data-stu-id="ce326-104">Performs a linear interpolation between two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce326-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce326-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Lerp(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="ce326-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce326-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce326-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="ce326-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce326-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="ce326-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="ce326-109">Ponteiro para a estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="ce326-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ce326-110">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ce326-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce326-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="ce326-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="ce326-112">Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="ce326-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ce326-113">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ce326-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce326-114">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="ce326-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="ce326-115">Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="ce326-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ce326-116">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="ce326-116">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce326-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce326-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce326-118">Parâmetro que interpola linearmente entre os vetores.</span><span class="sxs-lookup"><span data-stu-id="ce326-118">Parameter that linearly interpolates between the vectors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce326-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ce326-119">Return value</span></span>

<span data-ttu-id="ce326-120">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="ce326-120">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="ce326-121">Ponteiro para uma estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o resultado da interpolação linear.</span><span class="sxs-lookup"><span data-stu-id="ce326-121">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the linear interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce326-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce326-122">Remarks</span></span>

<span data-ttu-id="ce326-123">Essa função executa a interpolação linear com base na seguinte fórmula: v1 + s (v2-v1).</span><span class="sxs-lookup"><span data-stu-id="ce326-123">This function performs the linear interpolation based on the following formula: V1 + s(V2-V1).</span></span>

<span data-ttu-id="ce326-124">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="ce326-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="ce326-125">Dessa forma, a função **D3DXVec4Lerp** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="ce326-125">In this way, the **D3DXVec4Lerp** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce326-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce326-126">Requirements</span></span>



| <span data-ttu-id="ce326-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce326-127">Requirement</span></span> | <span data-ttu-id="ce326-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ce326-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce326-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ce326-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ce326-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce326-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ce326-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ce326-131">Library</span></span><br/> | <dl> <span data-ttu-id="ce326-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce326-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ce326-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce326-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce326-134">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="ce326-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
