---
description: Função D3DXVec3UnprojectArray (D3DX10Math. h)-projeta uma matriz (x, y, z, 0) do espaço da tela no espaço do objeto.
ms.assetid: 02db5b32-7fa3-4cde-bd63-0d8b3dfc31e7
title: Função D3DXVec3UnprojectArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3UnprojectArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 727744445e952fa0135feff944c768aaba1aba36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103004"
---
# <a name="d3dxvec3unprojectarray-function-d3dx10mathh"></a><span data-ttu-id="e5dce-103">Função D3DXVec3UnprojectArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="e5dce-103">D3DXVec3UnprojectArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="e5dce-104">Projeta uma matriz (x, y, z, 0) do espaço da tela no espaço do objeto.</span><span class="sxs-lookup"><span data-stu-id="e5dce-104">Projects an array (x, y, z, 0) from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5dce-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5dce-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3UnprojectArray(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_          UINT           OutStride,
  _In_    const D3DXVECTOR3    *pV,
  _In_          UINT           VStride,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld,
  _In_          UINT           n
);
```



## <a name="parameters"></a><span data-ttu-id="e5dce-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5dce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5dce-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e5dce-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5dce-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e5dce-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e5dce-109">Ponteiro para o [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="e5dce-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e5dce-110">*Didistância* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5dce-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5dce-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5dce-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5dce-112">Stride entre os vetores no fluxo de dados de saída.</span><span class="sxs-lookup"><span data-stu-id="e5dce-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="e5dce-113">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5dce-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5dce-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e5dce-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e5dce-115">Ponteiro para a estrutura de D3DXVECTOR3 de origem.</span><span class="sxs-lookup"><span data-stu-id="e5dce-115">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="e5dce-116">*VStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5dce-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5dce-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5dce-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5dce-118">Stride entre os vetores no fluxo de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="e5dce-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="e5dce-119">*pViewport* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5dce-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5dce-120">Tipo: **\* [**\_ visor d3d10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) const**</span><span class="sxs-lookup"><span data-stu-id="e5dce-120">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="e5dce-121">Ponteiro para um [**\_ visor d3d10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), que representa o visor.</span><span class="sxs-lookup"><span data-stu-id="e5dce-121">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="e5dce-122">*pProjection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5dce-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5dce-123">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e5dce-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e5dce-124">Ponteiro para uma estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , representando a matriz de projeção.</span><span class="sxs-lookup"><span data-stu-id="e5dce-124">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="e5dce-125">*pView* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5dce-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5dce-126">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e5dce-126">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e5dce-127">Ponteiro para uma estrutura D3DXMATRIX, representando a matriz de exibição.</span><span class="sxs-lookup"><span data-stu-id="e5dce-127">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="e5dce-128">*pWorld* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5dce-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5dce-129">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e5dce-129">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e5dce-130">Ponteiro para uma estrutura D3DXMATRIX, representando a matriz mundial.</span><span class="sxs-lookup"><span data-stu-id="e5dce-130">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="e5dce-131">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="e5dce-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5dce-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5dce-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5dce-133">Número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="e5dce-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5dce-134">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e5dce-134">Return value</span></span>

<span data-ttu-id="e5dce-135">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e5dce-135">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e5dce-136">Ponteiro para uma estrutura D3DXVECTOR3 que é a matriz projetada do espaço da tela para o espaço de objeto.</span><span class="sxs-lookup"><span data-stu-id="e5dce-136">Pointer to a D3DXVECTOR3 structure that is the array projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5dce-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5dce-137">Remarks</span></span>

<span data-ttu-id="e5dce-138">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="e5dce-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="e5dce-139">Dessa forma, a função [**D3DXVec3Unproject**](d3d10-d3dxvec3unproject.md) pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="e5dce-139">In this way, the [**D3DXVec3Unproject**](d3d10-d3dxvec3unproject.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5dce-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5dce-140">Requirements</span></span>



| <span data-ttu-id="e5dce-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5dce-141">Requirement</span></span> | <span data-ttu-id="e5dce-142">Valor</span><span class="sxs-lookup"><span data-stu-id="e5dce-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5dce-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e5dce-143">Header</span></span><br/> | <dl> <span data-ttu-id="e5dce-144"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5dce-144"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5dce-145">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e5dce-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5dce-146">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="e5dce-146">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
