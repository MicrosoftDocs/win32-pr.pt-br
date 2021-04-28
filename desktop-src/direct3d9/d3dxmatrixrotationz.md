---
description: Função D3DXMatrixRotationZ (D3dx9math. h) – compila uma matriz que gira em volta do eixo z.
ms.assetid: 73db43e6-3831-4867-8eda-80127b61e169
title: Função D3DXMatrixRotationZ (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationZ
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0b109f71052657a5d9c32d9af5cb38b2cbcf1f0e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118104"
---
# <a name="d3dxmatrixrotationz-function-d3dx9mathh"></a><span data-ttu-id="e0379-103">Função D3DXMatrixRotationZ (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="e0379-103">D3DXMatrixRotationZ function (D3dx9math.h)</span></span>

<span data-ttu-id="e0379-104">Cria uma matriz que gira em volta do eixo z.</span><span class="sxs-lookup"><span data-stu-id="e0379-104">Builds a matrix that rotates around the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0379-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0379-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationZ(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="e0379-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0379-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0379-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e0379-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0379-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e0379-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e0379-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="e0379-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e0379-110">*Ângulo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e0379-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0379-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0379-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0379-112">Ângulo de rotação, em radianos.</span><span class="sxs-lookup"><span data-stu-id="e0379-112">Angle of rotation, in radians.</span></span> <span data-ttu-id="e0379-113">Os ângulos são medidos no sentido horário quando exibidos do eixo de rotação (lado positivo) em direção à origem.</span><span class="sxs-lookup"><span data-stu-id="e0379-113">Angles are measured clockwise when viewed from the rotation axis (positive side) toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0379-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e0379-114">Return value</span></span>

<span data-ttu-id="e0379-115">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e0379-115">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e0379-116">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) girado em volta do eixo z.</span><span class="sxs-lookup"><span data-stu-id="e0379-116">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the z-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0379-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0379-117">Remarks</span></span>

<span data-ttu-id="e0379-118">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="e0379-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e0379-119">Dessa forma, a função **D3DXMatrixRotationZ** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="e0379-119">In this way, the **D3DXMatrixRotationZ** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0379-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0379-120">Requirements</span></span>



| <span data-ttu-id="e0379-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0379-121">Requirement</span></span> | <span data-ttu-id="e0379-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e0379-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0379-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0379-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e0379-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0379-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e0379-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0379-125">Library</span></span><br/> | <dl> <span data-ttu-id="e0379-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0379-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e0379-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e0379-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0379-128">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="e0379-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e0379-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="e0379-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="e0379-130">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="e0379-130">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="e0379-131">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="e0379-131">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="e0379-132">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="e0379-132">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="e0379-133">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="e0379-133">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> </dl>

 

 
