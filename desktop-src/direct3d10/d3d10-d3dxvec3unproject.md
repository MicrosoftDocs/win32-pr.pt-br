---
description: Função D3DXVec3Unproject (D3DX10Math. h)-projeta um vetor do espaço da tela no espaço do objeto.
ms.assetid: c96d732d-0594-42b4-bc54-458a313f153e
title: Função D3DXVec3Unproject (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Unproject
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 08d38691d0e780e49293149bdb7a08b1ea0ef1fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103024"
---
# <a name="d3dxvec3unproject-function-d3dx10mathh"></a><span data-ttu-id="07512-103">Função D3DXVec3Unproject (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="07512-103">D3DXVec3Unproject function (D3DX10Math.h)</span></span>

<span data-ttu-id="07512-104">Projeta um vetor do espaço da tela no espaço do objeto.</span><span class="sxs-lookup"><span data-stu-id="07512-104">Projects a vector from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="07512-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07512-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Unproject(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld
);
```



## <a name="parameters"></a><span data-ttu-id="07512-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07512-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07512-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="07512-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="07512-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="07512-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="07512-109">Ponteiro para o [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="07512-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="07512-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="07512-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07512-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="07512-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="07512-112">Ponteiro para a estrutura de D3DXVECTOR3 de origem.</span><span class="sxs-lookup"><span data-stu-id="07512-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="07512-113">*pViewport* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="07512-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07512-114">Tipo: **\* [**\_ visor d3d10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) const**</span><span class="sxs-lookup"><span data-stu-id="07512-114">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="07512-115">Ponteiro para um [**\_ visor d3d10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), que representa o visor.</span><span class="sxs-lookup"><span data-stu-id="07512-115">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="07512-116">*pProjection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="07512-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07512-117">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="07512-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="07512-118">Ponteiro para uma estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , representando a matriz de projeção.</span><span class="sxs-lookup"><span data-stu-id="07512-118">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="07512-119">*pView* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="07512-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07512-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="07512-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="07512-121">Ponteiro para uma estrutura D3DXMATRIX, representando a matriz de exibição.</span><span class="sxs-lookup"><span data-stu-id="07512-121">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="07512-122">*pWorld* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="07512-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07512-123">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="07512-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="07512-124">Ponteiro para uma estrutura D3DXMATRIX, representando a matriz mundial.</span><span class="sxs-lookup"><span data-stu-id="07512-124">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07512-125">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="07512-125">Return value</span></span>

<span data-ttu-id="07512-126">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="07512-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="07512-127">Ponteiro para uma estrutura D3DXVECTOR3 que é o vetor projetado do espaço da tela para o espaço de objeto.</span><span class="sxs-lookup"><span data-stu-id="07512-127">Pointer to a D3DXVECTOR3 structure that is the vector projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="07512-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="07512-128">Remarks</span></span>

<span data-ttu-id="07512-129">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="07512-129">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="07512-130">Dessa forma, a função D3DXVec3Unproject pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="07512-130">In this way, the D3DXVec3Unproject function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="07512-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07512-131">Requirements</span></span>



| <span data-ttu-id="07512-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="07512-132">Requirement</span></span> | <span data-ttu-id="07512-133">Valor</span><span class="sxs-lookup"><span data-stu-id="07512-133">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07512-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="07512-134">Header</span></span><br/> | <dl> <span data-ttu-id="07512-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="07512-135"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07512-136">Consulte também</span><span class="sxs-lookup"><span data-stu-id="07512-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07512-137">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="07512-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
