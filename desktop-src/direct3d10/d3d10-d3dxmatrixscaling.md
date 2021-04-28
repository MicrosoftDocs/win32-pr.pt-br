---
description: Função D3DXMatrixScaling (D3DX10Math. h) – compila uma matriz que é dimensionada ao longo do eixo x, do eixo y e do eixo z.
ms.assetid: 1804bf41-26de-4be1-ad62-7a871d7408e6
title: Função D3DXMatrixScaling (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixScaling
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: bf11b2196953775fb41412ad484a77ab00ae578e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108924"
---
# <a name="d3dxmatrixscaling-function-d3dx10mathh"></a><span data-ttu-id="6e18d-103">Função D3DXMatrixScaling (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="6e18d-103">D3DXMatrixScaling function (D3DX10Math.h)</span></span>

<span data-ttu-id="6e18d-104">Cria uma matriz que é dimensionada ao longo do eixo x, do eixo y e do eixo z.</span><span class="sxs-lookup"><span data-stu-id="6e18d-104">Builds a matrix that scales along the x-axis, the y-axis, and the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e18d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e18d-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixScaling(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      sx,
  _In_    FLOAT      sy,
  _In_    FLOAT      sz
);
```



## <a name="parameters"></a><span data-ttu-id="6e18d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e18d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e18d-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="6e18d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e18d-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6e18d-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6e18d-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="6e18d-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6e18d-110">*SX* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6e18d-110">*sx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e18d-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e18d-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6e18d-112">Fator de dimensionamento aplicado ao longo do eixo x.</span><span class="sxs-lookup"><span data-stu-id="6e18d-112">Scaling factor that is applied along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="6e18d-113">*Sy* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6e18d-113">*sy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e18d-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e18d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6e18d-115">Fator de dimensionamento aplicado ao longo do eixo y.</span><span class="sxs-lookup"><span data-stu-id="6e18d-115">Scaling factor that is applied along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="6e18d-116">*sz* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6e18d-116">*sz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e18d-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e18d-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6e18d-118">Fator de dimensionamento aplicado ao longo do eixo z.</span><span class="sxs-lookup"><span data-stu-id="6e18d-118">Scaling factor that is applied along the z-axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e18d-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6e18d-119">Return value</span></span>

<span data-ttu-id="6e18d-120">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6e18d-120">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6e18d-121">Ponteiro para o D3DXMATRIX de transformação de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="6e18d-121">Pointer to the scaling transformation D3DXMATRIX.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e18d-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e18d-122">Remarks</span></span>

<span data-ttu-id="6e18d-123">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="6e18d-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="6e18d-124">Dessa forma, a função D3DXMatrixScaling pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="6e18d-124">In this way, the D3DXMatrixScaling function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e18d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e18d-125">Requirements</span></span>



| <span data-ttu-id="6e18d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e18d-126">Requirement</span></span> | <span data-ttu-id="6e18d-127">Valor</span><span class="sxs-lookup"><span data-stu-id="6e18d-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e18d-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e18d-128">Header</span></span><br/>  | <dl> <span data-ttu-id="6e18d-129"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e18d-129"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="6e18d-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6e18d-130">Library</span></span><br/> | <dl> <span data-ttu-id="6e18d-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e18d-131"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6e18d-132">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6e18d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e18d-133">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="6e18d-133">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
