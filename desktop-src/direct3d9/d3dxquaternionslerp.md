---
description: Interpola entre dois quatérnios usando interpolação linear esférica.
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
ms.openlocfilehash: f0f43e22ddc46007c6f589dfc5fd8b45aa885643
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764257"
---
# <a name="d3dxquaternionslerp-function-d3dx9mathh"></a><span data-ttu-id="b8e86-103">Função D3DXQuaternionSlerp (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="b8e86-103">D3DXQuaternionSlerp function (D3dx9math.h)</span></span>

<span data-ttu-id="b8e86-104">Interpola entre dois quatérnios usando interpolação linear esférica.</span><span class="sxs-lookup"><span data-stu-id="b8e86-104">Interpolates between two quaternions, using spherical linear interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8e86-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8e86-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSlerp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="b8e86-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8e86-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8e86-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="b8e86-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8e86-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="b8e86-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="b8e86-109">Ponteiro para a estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="b8e86-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b8e86-110">*pQ1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b8e86-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8e86-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="b8e86-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="b8e86-112">Ponteiro para uma estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="b8e86-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b8e86-113">*pQ2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b8e86-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8e86-114">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="b8e86-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="b8e86-115">Ponteiro para uma estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="b8e86-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b8e86-116">*t* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="b8e86-116">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8e86-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8e86-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8e86-118">Parâmetro que indica a interpolarização entre os quaternions.</span><span class="sxs-lookup"><span data-stu-id="b8e86-118">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8e86-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8e86-119">Return value</span></span>

<span data-ttu-id="b8e86-120">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="b8e86-120">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="b8e86-121">Ponteiro para uma estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o resultado da interpolação.</span><span class="sxs-lookup"><span data-stu-id="b8e86-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8e86-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8e86-122">Remarks</span></span>

<span data-ttu-id="b8e86-123">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="b8e86-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="b8e86-124">Dessa forma, a função **D3DXQuaternionSlerp** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="b8e86-124">In this way, the **D3DXQuaternionSlerp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b8e86-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="b8e86-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8e86-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8e86-126">Requirements</span></span>



| <span data-ttu-id="b8e86-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8e86-127">Requirement</span></span> | <span data-ttu-id="b8e86-128">Valor</span><span class="sxs-lookup"><span data-stu-id="b8e86-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e86-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b8e86-129">Header</span></span><br/>  | <dl> <span data-ttu-id="b8e86-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8e86-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b8e86-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b8e86-131">Library</span></span><br/> | <dl> <span data-ttu-id="b8e86-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8e86-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b8e86-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8e86-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8e86-134">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="b8e86-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
