---
description: Executa uma interpolação linear entre dois vetores 3D.
ms.assetid: f3f06f1b-8824-47f0-b2ed-c212fa4c3225
title: Função D3DXVec3Lerp (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Lerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed6905cc0b13908a4e60e221737e9b5dc5a627f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791305"
---
# <a name="d3dxvec3lerp-function"></a><span data-ttu-id="d4c1b-103">Função D3DXVec3Lerp</span><span class="sxs-lookup"><span data-stu-id="d4c1b-103">D3DXVec3Lerp function</span></span>

<span data-ttu-id="d4c1b-104">Executa uma interpolação linear entre dois vetores 3D.</span><span class="sxs-lookup"><span data-stu-id="d4c1b-104">Performs a linear interpolation between two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4c1b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d4c1b-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Lerp(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="d4c1b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4c1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4c1b-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d4c1b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4c1b-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="d4c1b-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d4c1b-109">Ponteiro para a estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="d4c1b-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d4c1b-110">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d4c1b-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4c1b-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d4c1b-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d4c1b-112">Ponteiro para uma estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="d4c1b-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d4c1b-113">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d4c1b-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4c1b-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d4c1b-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d4c1b-115">Ponteiro para uma estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="d4c1b-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d4c1b-116">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="d4c1b-116">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4c1b-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4c1b-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4c1b-118">Parâmetro que interpola linearmente entre os vetores.</span><span class="sxs-lookup"><span data-stu-id="d4c1b-118">Parameter that linearly interpolates between the vectors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4c1b-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d4c1b-119">Return value</span></span>

<span data-ttu-id="d4c1b-120">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="d4c1b-120">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d4c1b-121">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é o resultado da interpolação linear.</span><span class="sxs-lookup"><span data-stu-id="d4c1b-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the linear interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4c1b-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4c1b-122">Remarks</span></span>

<span data-ttu-id="d4c1b-123">Essa função executa a interpolação linear com base na seguinte fórmula: v1 + s (v2-v1).</span><span class="sxs-lookup"><span data-stu-id="d4c1b-123">This function performs the linear interpolation based on the following formula: V1 + s(V2-V1).</span></span>

<span data-ttu-id="d4c1b-124">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="d4c1b-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d4c1b-125">Dessa forma, a função **D3DXVec3Lerp** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="d4c1b-125">In this way, the **D3DXVec3Lerp** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4c1b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4c1b-126">Requirements</span></span>



| <span data-ttu-id="d4c1b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4c1b-127">Requirement</span></span> | <span data-ttu-id="d4c1b-128">Valor</span><span class="sxs-lookup"><span data-stu-id="d4c1b-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4c1b-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d4c1b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d4c1b-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4c1b-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d4c1b-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d4c1b-131">Library</span></span><br/> | <dl> <span data-ttu-id="d4c1b-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4c1b-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d4c1b-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4c1b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4c1b-134">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="d4c1b-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
