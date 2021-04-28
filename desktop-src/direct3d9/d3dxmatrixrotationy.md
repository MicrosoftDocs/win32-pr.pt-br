---
description: Função D3DXMatrixRotationY (D3dx9math. h) – compila uma matriz que gira em volta do eixo y.
ms.assetid: 80449e5d-f9bb-48c0-a787-a5e5a9d1c9a3
title: Função D3DXMatrixRotationY (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationY
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 902325890b02416e796940388bca7a6548773be5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118124"
---
# <a name="d3dxmatrixrotationy-function-d3dx9mathh"></a><span data-ttu-id="177b9-103">Função D3DXMatrixRotationY (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="177b9-103">D3DXMatrixRotationY function (D3dx9math.h)</span></span>

<span data-ttu-id="177b9-104">Cria uma matriz que gira em volta do eixo y.</span><span class="sxs-lookup"><span data-stu-id="177b9-104">Builds a matrix that rotates around the y-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="177b9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="177b9-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationY(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="177b9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="177b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="177b9-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="177b9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="177b9-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="177b9-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="177b9-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="177b9-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="177b9-110">*Ângulo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="177b9-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="177b9-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="177b9-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="177b9-112">Ângulo de rotação em radianos.</span><span class="sxs-lookup"><span data-stu-id="177b9-112">Angle of rotation in radians.</span></span> <span data-ttu-id="177b9-113">Os ângulos são medidos no sentido horário olhando ao longo do eixo de rotação em direção à origem.</span><span class="sxs-lookup"><span data-stu-id="177b9-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="177b9-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="177b9-114">Return value</span></span>

<span data-ttu-id="177b9-115">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="177b9-115">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="177b9-116">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) girado em volta do eixo y.</span><span class="sxs-lookup"><span data-stu-id="177b9-116">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the y-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="177b9-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="177b9-117">Remarks</span></span>

<span data-ttu-id="177b9-118">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="177b9-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="177b9-119">Dessa forma, a função **D3DXMatrixRotationY** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="177b9-119">In this way, the **D3DXMatrixRotationY** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="177b9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="177b9-120">Requirements</span></span>



| <span data-ttu-id="177b9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="177b9-121">Requirement</span></span> | <span data-ttu-id="177b9-122">Valor</span><span class="sxs-lookup"><span data-stu-id="177b9-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="177b9-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="177b9-123">Header</span></span><br/>  | <dl> <span data-ttu-id="177b9-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="177b9-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="177b9-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="177b9-125">Library</span></span><br/> | <dl> <span data-ttu-id="177b9-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="177b9-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="177b9-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="177b9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="177b9-128">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="177b9-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="177b9-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="177b9-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="177b9-130">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="177b9-130">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="177b9-131">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="177b9-131">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="177b9-132">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="177b9-132">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="177b9-133">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="177b9-133">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
