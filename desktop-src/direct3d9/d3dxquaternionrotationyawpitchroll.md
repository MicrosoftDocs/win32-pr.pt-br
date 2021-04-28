---
description: Função D3DXQuaternionRotationYawPitchRoll (D3dx9math. h) – compila um Quaternion com a guinada, a densidade e o rolo fornecidos.
ms.assetid: be4a3bd5-114b-4652-8e0a-e51338317c16
title: Função D3DXQuaternionRotationYawPitchRoll (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 541e181425782662c6d40affc22c829b4ba343ab
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117994"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx9mathh"></a><span data-ttu-id="15cfe-103">Função D3DXQuaternionRotationYawPitchRoll (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="15cfe-103">D3DXQuaternionRotationYawPitchRoll function (D3dx9math.h)</span></span>

<span data-ttu-id="15cfe-104">Cria um Quaternion com uma determinada guinada, pitch e roll.</span><span class="sxs-lookup"><span data-stu-id="15cfe-104">Builds a quaternion with the given yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="15cfe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15cfe-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a><span data-ttu-id="15cfe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15cfe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15cfe-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="15cfe-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="15cfe-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="15cfe-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="15cfe-109">Ponteiro para a estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="15cfe-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="15cfe-110">*Guinada* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="15cfe-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15cfe-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15cfe-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="15cfe-112">Desvio em volta do eixo y, em radianos.</span><span class="sxs-lookup"><span data-stu-id="15cfe-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="15cfe-113">*Pitch* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="15cfe-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15cfe-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15cfe-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="15cfe-115">Inclinação em relação ao eixo x, em radianos.</span><span class="sxs-lookup"><span data-stu-id="15cfe-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="15cfe-116">*Rolar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="15cfe-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15cfe-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15cfe-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="15cfe-118">Sobreponha-se ao eixo z, em radianos.</span><span class="sxs-lookup"><span data-stu-id="15cfe-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15cfe-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="15cfe-119">Return value</span></span>

<span data-ttu-id="15cfe-120">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="15cfe-120">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="15cfe-121">Ponteiro para uma estrutura [**D3DXQUATERNION**](d3dxquaternion.md) com a guinada, a densidade e o rolo especificados.</span><span class="sxs-lookup"><span data-stu-id="15cfe-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="15cfe-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="15cfe-122">Remarks</span></span>

<span data-ttu-id="15cfe-123">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="15cfe-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="15cfe-124">Dessa forma, a função **D3DXQuaternionRotationYawPitchRoll** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="15cfe-124">In this way, the **D3DXQuaternionRotationYawPitchRoll** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="15cfe-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="15cfe-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="15cfe-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15cfe-126">Requirements</span></span>



| <span data-ttu-id="15cfe-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="15cfe-127">Requirement</span></span> | <span data-ttu-id="15cfe-128">Valor</span><span class="sxs-lookup"><span data-stu-id="15cfe-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="15cfe-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="15cfe-129">Header</span></span><br/>  | <dl> <span data-ttu-id="15cfe-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="15cfe-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="15cfe-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="15cfe-131">Library</span></span><br/> | <dl> <span data-ttu-id="15cfe-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15cfe-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="15cfe-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="15cfe-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15cfe-134">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="15cfe-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="15cfe-135">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="15cfe-135">**D3DXQuaternionRotationAxis**</span></span>](d3dxquaternionrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="15cfe-136">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="15cfe-136">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
</dt> </dl>

 

 
