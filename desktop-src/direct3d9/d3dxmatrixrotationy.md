---
description: Cria uma matriz que gira em volta do eixo y.
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
ms.openlocfilehash: 81e233f3d643e99c829c7d567721e52b9b5d3e82
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298731"
---
# <a name="d3dxmatrixrotationy-function-d3dx9mathh"></a><span data-ttu-id="3b1f2-103">Função D3DXMatrixRotationY (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="3b1f2-103">D3DXMatrixRotationY function (D3dx9math.h)</span></span>

<span data-ttu-id="3b1f2-104">Cria uma matriz que gira em volta do eixo y.</span><span class="sxs-lookup"><span data-stu-id="3b1f2-104">Builds a matrix that rotates around the y-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b1f2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b1f2-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationY(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="3b1f2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b1f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b1f2-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="3b1f2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b1f2-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="3b1f2-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="3b1f2-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="3b1f2-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="3b1f2-110">*Ângulo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b1f2-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b1f2-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3b1f2-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3b1f2-112">Ângulo de rotação em radianos.</span><span class="sxs-lookup"><span data-stu-id="3b1f2-112">Angle of rotation in radians.</span></span> <span data-ttu-id="3b1f2-113">Os ângulos são medidos no sentido horário olhando ao longo do eixo de rotação em direção à origem.</span><span class="sxs-lookup"><span data-stu-id="3b1f2-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b1f2-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b1f2-114">Return value</span></span>

<span data-ttu-id="3b1f2-115">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="3b1f2-115">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="3b1f2-116">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) girado em volta do eixo y.</span><span class="sxs-lookup"><span data-stu-id="3b1f2-116">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the y-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b1f2-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b1f2-117">Remarks</span></span>

<span data-ttu-id="3b1f2-118">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="3b1f2-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="3b1f2-119">Dessa forma, a função **D3DXMatrixRotationY** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="3b1f2-119">In this way, the **D3DXMatrixRotationY** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b1f2-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b1f2-120">Requirements</span></span>



| <span data-ttu-id="3b1f2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b1f2-121">Requirement</span></span> | <span data-ttu-id="3b1f2-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3b1f2-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b1f2-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b1f2-123">Header</span></span><br/>  | <dl> <span data-ttu-id="3b1f2-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b1f2-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="3b1f2-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b1f2-125">Library</span></span><br/> | <dl> <span data-ttu-id="3b1f2-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b1f2-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3b1f2-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b1f2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b1f2-128">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="3b1f2-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="3b1f2-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="3b1f2-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="3b1f2-130">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="3b1f2-130">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="3b1f2-131">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="3b1f2-131">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="3b1f2-132">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="3b1f2-132">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="3b1f2-133">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="3b1f2-133">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
