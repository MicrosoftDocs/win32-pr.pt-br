---
description: Função D3DXMatrixRotationAxis (D3DX10Math. h) – compila uma matriz que gira em um eixo arbitrário.
ms.assetid: dc4b8b3f-e1d2-475f-9dcb-622ada9fae6b
title: Função D3DXMatrixRotationAxis (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8ea5b8b0a40e876af454daa8915c0e455d691d08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108994"
---
# <a name="d3dxmatrixrotationaxis-function-d3dx10mathh"></a><span data-ttu-id="238e4-103">Função D3DXMatrixRotationAxis (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="238e4-103">D3DXMatrixRotationAxis function (D3DX10Math.h)</span></span>

<span data-ttu-id="238e4-104">Cria uma matriz que gira em um eixo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="238e4-104">Builds a matrix that rotates around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="238e4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="238e4-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationAxis(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="238e4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="238e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="238e4-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="238e4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="238e4-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="238e4-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="238e4-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="238e4-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="238e4-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="238e4-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="238e4-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="238e4-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="238e4-112">Ponteiro para o eixo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="238e4-112">Pointer to the arbitrary axis.</span></span> <span data-ttu-id="238e4-113">Consulte [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="238e4-113">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="238e4-114">*Ângulo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="238e4-114">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="238e4-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="238e4-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="238e4-116">Ângulo de rotação em radianos.</span><span class="sxs-lookup"><span data-stu-id="238e4-116">Angle of rotation in radians.</span></span> <span data-ttu-id="238e4-117">Os ângulos são medidos no sentido horário olhando ao longo do eixo de rotação em direção à origem.</span><span class="sxs-lookup"><span data-stu-id="238e4-117">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="238e4-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="238e4-118">Return value</span></span>

<span data-ttu-id="238e4-119">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="238e4-119">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="238e4-120">Ponteiro para uma estrutura D3DXMATRIX girado em volta do eixo especificado.</span><span class="sxs-lookup"><span data-stu-id="238e4-120">Pointer to a D3DXMATRIX structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="238e4-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="238e4-121">Remarks</span></span>

<span data-ttu-id="238e4-122">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="238e4-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="238e4-123">Dessa forma, a função D3DXMatrixRotationAxis pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="238e4-123">In this way, the D3DXMatrixRotationAxis function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="238e4-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="238e4-124">Requirements</span></span>



| <span data-ttu-id="238e4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="238e4-125">Requirement</span></span> | <span data-ttu-id="238e4-126">Valor</span><span class="sxs-lookup"><span data-stu-id="238e4-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="238e4-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="238e4-127">Header</span></span><br/>  | <dl> <span data-ttu-id="238e4-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="238e4-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="238e4-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="238e4-129">Library</span></span><br/> | <dl> <span data-ttu-id="238e4-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="238e4-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="238e4-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="238e4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="238e4-132">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="238e4-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
