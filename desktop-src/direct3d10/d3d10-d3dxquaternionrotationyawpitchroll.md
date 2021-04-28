---
description: Função D3DXQuaternionRotationYawPitchRoll (D3DX10Math. h) – compila um Quaternion com a guinada, a densidade e o rolo fornecidos.
ms.assetid: c929d9d4-b9cb-4de6-86c1-26fec3617846
title: Função D3DXQuaternionRotationYawPitchRoll (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationYawPitchRoll
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cefcf9a927cee0d8f7c83ff42ae6ca4fc699bb09
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108744"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx10mathh"></a><span data-ttu-id="4aa72-103">Função D3DXQuaternionRotationYawPitchRoll (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="4aa72-103">D3DXQuaternionRotationYawPitchRoll function (D3DX10Math.h)</span></span>

<span data-ttu-id="4aa72-104">Cria um Quaternion com uma determinada guinada, pitch e roll.</span><span class="sxs-lookup"><span data-stu-id="4aa72-104">Builds a quaternion with the given yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aa72-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4aa72-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a><span data-ttu-id="4aa72-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4aa72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4aa72-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="4aa72-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4aa72-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="4aa72-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4aa72-109">Ponteiro para o [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="4aa72-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4aa72-110">*Guinada* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4aa72-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4aa72-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4aa72-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4aa72-112">Desvio em volta do eixo y, em radianos.</span><span class="sxs-lookup"><span data-stu-id="4aa72-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="4aa72-113">*Pitch* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4aa72-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4aa72-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4aa72-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4aa72-115">Inclinação em relação ao eixo x, em radianos.</span><span class="sxs-lookup"><span data-stu-id="4aa72-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="4aa72-116">*Rolar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4aa72-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4aa72-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4aa72-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4aa72-118">Sobreponha-se ao eixo z, em radianos.</span><span class="sxs-lookup"><span data-stu-id="4aa72-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4aa72-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4aa72-119">Return value</span></span>

<span data-ttu-id="4aa72-120">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="4aa72-120">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4aa72-121">Ponteiro para uma estrutura D3DXQUATERNION com a guinada, a densidade e o rolo especificados.</span><span class="sxs-lookup"><span data-stu-id="4aa72-121">Pointer to a D3DXQUATERNION structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="4aa72-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="4aa72-122">Remarks</span></span>

<span data-ttu-id="4aa72-123">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="4aa72-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="4aa72-124">Dessa forma, a função D3DXQuaternionRotationYawPitchRoll pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="4aa72-124">In this way, the D3DXQuaternionRotationYawPitchRoll function can be used as a parameter for another function.</span></span>

<span data-ttu-id="4aa72-125">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="4aa72-125">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="4aa72-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4aa72-126">Requirements</span></span>



| <span data-ttu-id="4aa72-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4aa72-127">Requirement</span></span> | <span data-ttu-id="4aa72-128">Valor</span><span class="sxs-lookup"><span data-stu-id="4aa72-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4aa72-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4aa72-129">Header</span></span><br/>  | <dl> <span data-ttu-id="4aa72-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4aa72-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="4aa72-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4aa72-131">Library</span></span><br/> | <dl> <span data-ttu-id="4aa72-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4aa72-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4aa72-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4aa72-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aa72-134">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="4aa72-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
