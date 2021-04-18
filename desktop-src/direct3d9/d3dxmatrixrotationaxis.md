---
description: Cria uma matriz que gira em um eixo arbitrário.
ms.assetid: 368c8f64-7709-4200-94d3-3dbc92a960c1
title: Função D3DXMatrixRotationAxis (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationAxis
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fffc4a5bdd287c79352beb3ee0eeaf97b0573753
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105810790"
---
# <a name="d3dxmatrixrotationaxis-function-d3dx9mathh"></a><span data-ttu-id="06f0d-103">Função D3DXMatrixRotationAxis (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="06f0d-103">D3DXMatrixRotationAxis function (D3dx9math.h)</span></span>

<span data-ttu-id="06f0d-104">Cria uma matriz que gira em um eixo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="06f0d-104">Builds a matrix that rotates around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="06f0d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06f0d-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationAxis(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="06f0d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06f0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06f0d-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="06f0d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="06f0d-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="06f0d-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="06f0d-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="06f0d-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="06f0d-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="06f0d-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06f0d-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="06f0d-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="06f0d-112">Ponteiro para o eixo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="06f0d-112">Pointer to the arbitrary axis.</span></span> <span data-ttu-id="06f0d-113">Consulte [**D3DXVECTOR3**](d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="06f0d-113">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="06f0d-114">*Ângulo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="06f0d-114">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06f0d-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06f0d-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06f0d-116">Ângulo de rotação em radianos.</span><span class="sxs-lookup"><span data-stu-id="06f0d-116">Angle of rotation in radians.</span></span> <span data-ttu-id="06f0d-117">Os ângulos são medidos no sentido horário olhando ao longo do eixo de rotação em direção à origem.</span><span class="sxs-lookup"><span data-stu-id="06f0d-117">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06f0d-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="06f0d-118">Return value</span></span>

<span data-ttu-id="06f0d-119">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="06f0d-119">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="06f0d-120">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) girado em volta do eixo especificado.</span><span class="sxs-lookup"><span data-stu-id="06f0d-120">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="06f0d-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="06f0d-121">Remarks</span></span>

<span data-ttu-id="06f0d-122">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="06f0d-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="06f0d-123">Dessa forma, a função **D3DXMatrixRotationAxis** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="06f0d-123">In this way, the **D3DXMatrixRotationAxis** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="06f0d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06f0d-124">Requirements</span></span>



| <span data-ttu-id="06f0d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="06f0d-125">Requirement</span></span> | <span data-ttu-id="06f0d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="06f0d-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06f0d-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="06f0d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="06f0d-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="06f0d-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="06f0d-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="06f0d-129">Library</span></span><br/> | <dl> <span data-ttu-id="06f0d-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06f0d-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="06f0d-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="06f0d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06f0d-132">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="06f0d-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="06f0d-133">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="06f0d-133">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="06f0d-134">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="06f0d-134">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="06f0d-135">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="06f0d-135">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="06f0d-136">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="06f0d-136">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="06f0d-137">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="06f0d-137">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
