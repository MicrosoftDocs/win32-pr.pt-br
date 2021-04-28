---
description: Função D3DXQuaternionSlerp (D3dx9math. h) – interpola entre dois quaternions, usando interpolação linear esférica.
ms.assetid: 94a989c8-fa6b-4852-9aa3-e55ad814ffd7
title: Função D3DXQuaternionSlerp (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSlerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fb9110da7fae4ebbf4609d361124dbbcdedfe59b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093934"
---
# <a name="d3dxquaternionslerp-function-d3dx9mathh"></a><span data-ttu-id="3164d-103">Função D3DXQuaternionSlerp (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="3164d-103">D3DXQuaternionSlerp function (D3dx9math.h)</span></span>

<span data-ttu-id="3164d-104">Interpola entre dois quatérnios usando interpolação linear esférica.</span><span class="sxs-lookup"><span data-stu-id="3164d-104">Interpolates between two quaternions, using spherical linear interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3164d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3164d-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSlerp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="3164d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3164d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3164d-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="3164d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3164d-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="3164d-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="3164d-109">Ponteiro para a estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="3164d-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="3164d-110">*pQ1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3164d-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3164d-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="3164d-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="3164d-112">Ponteiro para uma estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="3164d-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3164d-113">*pQ2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3164d-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3164d-114">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="3164d-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="3164d-115">Ponteiro para uma estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="3164d-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3164d-116">*t* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="3164d-116">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3164d-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3164d-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3164d-118">Parâmetro que indica a interpolarização entre os quaternions.</span><span class="sxs-lookup"><span data-stu-id="3164d-118">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3164d-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="3164d-119">Return value</span></span>

<span data-ttu-id="3164d-120">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="3164d-120">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="3164d-121">Ponteiro para uma estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o resultado da interpolação.</span><span class="sxs-lookup"><span data-stu-id="3164d-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="3164d-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="3164d-122">Remarks</span></span>

<span data-ttu-id="3164d-123">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="3164d-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="3164d-124">Dessa forma, a função **D3DXQuaternionSlerp** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="3164d-124">In this way, the **D3DXQuaternionSlerp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="3164d-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="3164d-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="3164d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3164d-126">Requirements</span></span>



| <span data-ttu-id="3164d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3164d-127">Requirement</span></span> | <span data-ttu-id="3164d-128">Valor</span><span class="sxs-lookup"><span data-stu-id="3164d-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3164d-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3164d-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3164d-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3164d-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="3164d-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3164d-131">Library</span></span><br/> | <dl> <span data-ttu-id="3164d-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3164d-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3164d-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3164d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3164d-134">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="3164d-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
