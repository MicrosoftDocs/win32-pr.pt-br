---
description: Cria uma matriz que gira em um eixo arbitrário.
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
ms.openlocfilehash: bba74aa7258b39b8fdbbb8cab09684a14bfbda91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012156"
---
# <a name="d3dxmatrixrotationaxis-function-d3dx10mathh"></a><span data-ttu-id="70d88-103">Função D3DXMatrixRotationAxis (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="70d88-103">D3DXMatrixRotationAxis function (D3DX10Math.h)</span></span>

<span data-ttu-id="70d88-104">Cria uma matriz que gira em um eixo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="70d88-104">Builds a matrix that rotates around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="70d88-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70d88-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationAxis(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="70d88-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70d88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70d88-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="70d88-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="70d88-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="70d88-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="70d88-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="70d88-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="70d88-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="70d88-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70d88-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="70d88-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="70d88-112">Ponteiro para o eixo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="70d88-112">Pointer to the arbitrary axis.</span></span> <span data-ttu-id="70d88-113">Consulte [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="70d88-113">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="70d88-114">*Ângulo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="70d88-114">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70d88-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="70d88-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="70d88-116">Ângulo de rotação em radianos.</span><span class="sxs-lookup"><span data-stu-id="70d88-116">Angle of rotation in radians.</span></span> <span data-ttu-id="70d88-117">Os ângulos são medidos no sentido horário olhando ao longo do eixo de rotação em direção à origem.</span><span class="sxs-lookup"><span data-stu-id="70d88-117">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70d88-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="70d88-118">Return value</span></span>

<span data-ttu-id="70d88-119">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="70d88-119">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="70d88-120">Ponteiro para uma estrutura D3DXMATRIX girado em volta do eixo especificado.</span><span class="sxs-lookup"><span data-stu-id="70d88-120">Pointer to a D3DXMATRIX structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="70d88-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="70d88-121">Remarks</span></span>

<span data-ttu-id="70d88-122">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="70d88-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="70d88-123">Dessa forma, a função D3DXMatrixRotationAxis pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="70d88-123">In this way, the D3DXMatrixRotationAxis function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="70d88-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70d88-124">Requirements</span></span>



| <span data-ttu-id="70d88-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="70d88-125">Requirement</span></span> | <span data-ttu-id="70d88-126">Valor</span><span class="sxs-lookup"><span data-stu-id="70d88-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70d88-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="70d88-127">Header</span></span><br/>  | <dl> <span data-ttu-id="70d88-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="70d88-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="70d88-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="70d88-129">Library</span></span><br/> | <dl> <span data-ttu-id="70d88-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70d88-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="70d88-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="70d88-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70d88-132">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="70d88-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
