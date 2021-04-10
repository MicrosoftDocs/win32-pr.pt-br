---
description: Interpola entre dois quatérnios usando interpolação linear esférica.
ms.assetid: 487e1df1-bf20-49cb-ad14-61fcf1300904
title: Função D3DXQuaternionSlerp (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 07f673d33b8f105e808fbae380a06942e2a69be4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012132"
---
# <a name="d3dxquaternionslerp-function-d3dx10mathh"></a><span data-ttu-id="eb9af-103">Função D3DXQuaternionSlerp (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="eb9af-103">D3DXQuaternionSlerp function (D3DX10Math.h)</span></span>

<span data-ttu-id="eb9af-104">Interpola entre dois quatérnios usando interpolação linear esférica.</span><span class="sxs-lookup"><span data-stu-id="eb9af-104">Interpolates between two quaternions, using spherical linear interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb9af-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb9af-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSlerp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="eb9af-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb9af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb9af-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="eb9af-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb9af-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="eb9af-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="eb9af-109">Ponteiro para o [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="eb9af-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="eb9af-110">*pQ1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eb9af-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb9af-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="eb9af-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="eb9af-112">Ponteiro para uma estrutura de D3DXQUATERNION de origem.</span><span class="sxs-lookup"><span data-stu-id="eb9af-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="eb9af-113">*pQ2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eb9af-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb9af-114">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="eb9af-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="eb9af-115">Ponteiro para uma estrutura de D3DXQUATERNION de origem.</span><span class="sxs-lookup"><span data-stu-id="eb9af-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="eb9af-116">*t* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="eb9af-116">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb9af-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb9af-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb9af-118">Parâmetro que indica a interpolarização entre os quaternions.</span><span class="sxs-lookup"><span data-stu-id="eb9af-118">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb9af-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eb9af-119">Return value</span></span>

<span data-ttu-id="eb9af-120">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="eb9af-120">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="eb9af-121">Ponteiro para uma estrutura D3DXQUATERNION que é o resultado da interpolação.</span><span class="sxs-lookup"><span data-stu-id="eb9af-121">Pointer to a D3DXQUATERNION structure that is the result of the interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb9af-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb9af-122">Remarks</span></span>

<span data-ttu-id="eb9af-123">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="eb9af-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="eb9af-124">Dessa forma, a função D3DXQuaternionSlerp pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="eb9af-124">In this way, the D3DXQuaternionSlerp function can be used as a parameter for another function.</span></span>

<span data-ttu-id="eb9af-125">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="eb9af-125">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb9af-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb9af-126">Requirements</span></span>



| <span data-ttu-id="eb9af-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb9af-127">Requirement</span></span> | <span data-ttu-id="eb9af-128">Valor</span><span class="sxs-lookup"><span data-stu-id="eb9af-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb9af-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eb9af-129">Header</span></span><br/>  | <dl> <span data-ttu-id="eb9af-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb9af-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="eb9af-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eb9af-131">Library</span></span><br/> | <dl> <span data-ttu-id="eb9af-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb9af-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eb9af-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb9af-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb9af-134">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="eb9af-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
