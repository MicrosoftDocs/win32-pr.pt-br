---
description: Projeta um vetor do espaço da tela no espaço do objeto.
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
ms.openlocfilehash: 21916392c689bcac794d44ec2c42c3e0b39abb0c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105778798"
---
# <a name="d3dxvec3unproject-function-d3dx10mathh"></a><span data-ttu-id="cd613-103">Função D3DXVec3Unproject (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="cd613-103">D3DXVec3Unproject function (D3DX10Math.h)</span></span>

<span data-ttu-id="cd613-104">Projeta um vetor do espaço da tela no espaço do objeto.</span><span class="sxs-lookup"><span data-stu-id="cd613-104">Projects a vector from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd613-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd613-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="cd613-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd613-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd613-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="cd613-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd613-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd613-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="cd613-109">Ponteiro para o [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="cd613-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="cd613-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cd613-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd613-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="cd613-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="cd613-112">Ponteiro para a estrutura de D3DXVECTOR3 de origem.</span><span class="sxs-lookup"><span data-stu-id="cd613-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="cd613-113">*pViewport* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cd613-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd613-114">Tipo: **\* [**\_ visor d3d10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) const**</span><span class="sxs-lookup"><span data-stu-id="cd613-114">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="cd613-115">Ponteiro para um [**\_ visor d3d10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), que representa o visor.</span><span class="sxs-lookup"><span data-stu-id="cd613-115">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="cd613-116">*pProjection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cd613-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd613-117">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="cd613-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cd613-118">Ponteiro para uma estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , representando a matriz de projeção.</span><span class="sxs-lookup"><span data-stu-id="cd613-118">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="cd613-119">*pView* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cd613-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd613-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="cd613-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cd613-121">Ponteiro para uma estrutura D3DXMATRIX, representando a matriz de exibição.</span><span class="sxs-lookup"><span data-stu-id="cd613-121">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="cd613-122">*pWorld* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cd613-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd613-123">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="cd613-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cd613-124">Ponteiro para uma estrutura D3DXMATRIX, representando a matriz mundial.</span><span class="sxs-lookup"><span data-stu-id="cd613-124">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd613-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cd613-125">Return value</span></span>

<span data-ttu-id="cd613-126">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd613-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="cd613-127">Ponteiro para uma estrutura D3DXVECTOR3 que é o vetor projetado do espaço da tela para o espaço de objeto.</span><span class="sxs-lookup"><span data-stu-id="cd613-127">Pointer to a D3DXVECTOR3 structure that is the vector projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd613-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd613-128">Remarks</span></span>

<span data-ttu-id="cd613-129">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="cd613-129">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="cd613-130">Dessa forma, a função D3DXVec3Unproject pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="cd613-130">In this way, the D3DXVec3Unproject function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd613-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd613-131">Requirements</span></span>



| <span data-ttu-id="cd613-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd613-132">Requirement</span></span> | <span data-ttu-id="cd613-133">Valor</span><span class="sxs-lookup"><span data-stu-id="cd613-133">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd613-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cd613-134">Header</span></span><br/> | <dl> <span data-ttu-id="cd613-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd613-135"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd613-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd613-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd613-137">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="cd613-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
