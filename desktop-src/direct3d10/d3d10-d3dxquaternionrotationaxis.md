---
description: Função D3DXQuaternionRotationAxis (D3DX10Math. h) – gira um Quaternion sobre um eixo arbitrário.
ms.assetid: 9673ef89-458f-4a25-960e-8f03179e78ba
title: Função D3DXQuaternionRotationAxis (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationAxis
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 509df80023427a20125e1b5603e85424851a640e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108764"
---
# <a name="d3dxquaternionrotationaxis-function-d3dx10mathh"></a><span data-ttu-id="3976e-103">Função D3DXQuaternionRotationAxis (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="3976e-103">D3DXQuaternionRotationAxis function (D3DX10Math.h)</span></span>

<span data-ttu-id="3976e-104">Gira um Quaternion sobre um eixo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="3976e-104">Rotates a quaternion about an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="3976e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3976e-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationAxis(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_          FLOAT          Angle
);
```



## <a name="parameters"></a><span data-ttu-id="3976e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3976e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3976e-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="3976e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3976e-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="3976e-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="3976e-109">Ponteiro para o [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="3976e-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="3976e-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3976e-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3976e-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3976e-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="3976e-112">Ponteiro para o [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que identifica o eixo sobre o qual girar o Quaternion.</span><span class="sxs-lookup"><span data-stu-id="3976e-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that identifies the axis about which to rotate the quaternion.</span></span>

</dd> <dt>

<span data-ttu-id="3976e-113">*Ângulo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3976e-113">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3976e-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3976e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3976e-115">Ângulo de rotação, em radianos.</span><span class="sxs-lookup"><span data-stu-id="3976e-115">Angle of rotation, in radians.</span></span> <span data-ttu-id="3976e-116">Os ângulos são medidos no sentido horário olhando ao longo do eixo de rotação em direção à origem.</span><span class="sxs-lookup"><span data-stu-id="3976e-116">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3976e-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="3976e-117">Return value</span></span>

<span data-ttu-id="3976e-118">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="3976e-118">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="3976e-119">Ponteiro para uma estrutura D3DXQUATERNION girado em volta do eixo especificado.</span><span class="sxs-lookup"><span data-stu-id="3976e-119">Pointer to a D3DXQUATERNION structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="3976e-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="3976e-120">Remarks</span></span>

<span data-ttu-id="3976e-121">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="3976e-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="3976e-122">Dessa forma, a função D3DXQuaternionRotationAxis pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="3976e-122">In this way, the D3DXQuaternionRotationAxis function can be used as a parameter for another function.</span></span>

<span data-ttu-id="3976e-123">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="3976e-123">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="3976e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3976e-124">Requirements</span></span>



| <span data-ttu-id="3976e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3976e-125">Requirement</span></span> | <span data-ttu-id="3976e-126">Valor</span><span class="sxs-lookup"><span data-stu-id="3976e-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3976e-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3976e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="3976e-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3976e-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="3976e-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3976e-129">Library</span></span><br/> | <dl> <span data-ttu-id="3976e-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3976e-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3976e-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3976e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3976e-132">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="3976e-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
