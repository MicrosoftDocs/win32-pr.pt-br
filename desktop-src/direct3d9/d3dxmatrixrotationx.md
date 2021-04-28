---
description: Função D3DXMatrixRotationX (D3dx9math. h) – compila uma matriz que gira em volta do eixo x.
ms.assetid: 45a2668d-787f-4354-882a-94a72edaa543
title: Função D3DXMatrixRotationX (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a4f51f8acab7caddd4571d60f7deae795440f02a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118174"
---
# <a name="d3dxmatrixrotationx-function-d3dx9mathh"></a><span data-ttu-id="5ff86-103">Função D3DXMatrixRotationX (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="5ff86-103">D3DXMatrixRotationX function (D3dx9math.h)</span></span>

<span data-ttu-id="5ff86-104">Cria uma matriz que gira em volta do eixo x.</span><span class="sxs-lookup"><span data-stu-id="5ff86-104">Builds a matrix that rotates around the x-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ff86-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ff86-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationX(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="5ff86-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ff86-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ff86-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="5ff86-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ff86-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ff86-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5ff86-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="5ff86-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5ff86-110">*Ângulo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ff86-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ff86-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ff86-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ff86-112">Ângulo de rotação em radianos.</span><span class="sxs-lookup"><span data-stu-id="5ff86-112">Angle of rotation in radians.</span></span> <span data-ttu-id="5ff86-113">Os ângulos são medidos no sentido horário olhando ao longo do eixo de rotação em direção à origem.</span><span class="sxs-lookup"><span data-stu-id="5ff86-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ff86-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5ff86-114">Return value</span></span>

<span data-ttu-id="5ff86-115">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ff86-115">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5ff86-116">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) girado em volta do eixo x.</span><span class="sxs-lookup"><span data-stu-id="5ff86-116">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the x-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ff86-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ff86-117">Remarks</span></span>

<span data-ttu-id="5ff86-118">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="5ff86-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="5ff86-119">Dessa forma, a função **D3DXMatrixRotationX** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="5ff86-119">In this way, the **D3DXMatrixRotationX** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ff86-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ff86-120">Requirements</span></span>



| <span data-ttu-id="5ff86-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ff86-121">Requirement</span></span> | <span data-ttu-id="5ff86-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5ff86-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ff86-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ff86-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5ff86-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ff86-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5ff86-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5ff86-125">Library</span></span><br/> | <dl> <span data-ttu-id="5ff86-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ff86-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5ff86-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5ff86-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ff86-128">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="5ff86-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="5ff86-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="5ff86-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="5ff86-130">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="5ff86-130">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="5ff86-131">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="5ff86-131">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="5ff86-132">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="5ff86-132">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="5ff86-133">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="5ff86-133">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
