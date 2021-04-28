---
description: Função D3DXMatrixRotationX (D3DX10Math. h) – compila uma matriz que gira em volta do eixo x.
ms.assetid: 895079bf-b807-4bfd-9222-a7c1251d7d1e
title: Função D3DXMatrixRotationX (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 53c4bf27a359bd6d131f8d6d9c685e929d1a9ec1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108984"
---
# <a name="d3dxmatrixrotationx-function-d3dx10mathh"></a><span data-ttu-id="05459-103">Função D3DXMatrixRotationX (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="05459-103">D3DXMatrixRotationX function (D3DX10Math.h)</span></span>

<span data-ttu-id="05459-104">Cria uma matriz que gira em volta do eixo x.</span><span class="sxs-lookup"><span data-stu-id="05459-104">Builds a matrix that rotates around the x-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="05459-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05459-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationX(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="05459-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05459-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05459-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="05459-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="05459-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="05459-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="05459-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="05459-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="05459-110">*Ângulo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="05459-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05459-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="05459-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="05459-112">Ângulo de rotação em radianos.</span><span class="sxs-lookup"><span data-stu-id="05459-112">Angle of rotation in radians.</span></span> <span data-ttu-id="05459-113">Os ângulos são medidos no sentido horário olhando ao longo do eixo de rotação em direção à origem.</span><span class="sxs-lookup"><span data-stu-id="05459-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05459-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="05459-114">Return value</span></span>

<span data-ttu-id="05459-115">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="05459-115">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="05459-116">Ponteiro para uma estrutura D3DXMATRIX girado em volta do eixo x.</span><span class="sxs-lookup"><span data-stu-id="05459-116">Pointer to a D3DXMATRIX structure rotated around the x-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="05459-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="05459-117">Remarks</span></span>

<span data-ttu-id="05459-118">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="05459-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="05459-119">Dessa forma, a função D3DXMatrixRotationX pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="05459-119">In this way, the D3DXMatrixRotationX function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="05459-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05459-120">Requirements</span></span>



| <span data-ttu-id="05459-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="05459-121">Requirement</span></span> | <span data-ttu-id="05459-122">Valor</span><span class="sxs-lookup"><span data-stu-id="05459-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05459-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="05459-123">Header</span></span><br/>  | <dl> <span data-ttu-id="05459-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="05459-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="05459-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="05459-125">Library</span></span><br/> | <dl> <span data-ttu-id="05459-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05459-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="05459-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="05459-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05459-128">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="05459-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
