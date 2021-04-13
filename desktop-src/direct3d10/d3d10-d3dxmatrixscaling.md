---
description: Cria uma matriz que é dimensionada ao longo do eixo x, do eixo y e do eixo z.
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
ms.openlocfilehash: adb1becb67a561778b31c90ea3d6c96e776c9a67
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298769"
---
# <a name="d3dxmatrixscaling-function-d3dx10mathh"></a><span data-ttu-id="a4010-103">Função D3DXMatrixScaling (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="a4010-103">D3DXMatrixScaling function (D3DX10Math.h)</span></span>

<span data-ttu-id="a4010-104">Cria uma matriz que é dimensionada ao longo do eixo x, do eixo y e do eixo z.</span><span class="sxs-lookup"><span data-stu-id="a4010-104">Builds a matrix that scales along the x-axis, the y-axis, and the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4010-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4010-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixScaling(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      sx,
  _In_    FLOAT      sy,
  _In_    FLOAT      sz
);
```



## <a name="parameters"></a><span data-ttu-id="a4010-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4010-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4010-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="a4010-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4010-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a4010-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a4010-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="a4010-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a4010-110">*SX* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4010-110">*sx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4010-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4010-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a4010-112">Fator de dimensionamento aplicado ao longo do eixo x.</span><span class="sxs-lookup"><span data-stu-id="a4010-112">Scaling factor that is applied along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="a4010-113">*Sy* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4010-113">*sy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4010-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4010-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a4010-115">Fator de dimensionamento aplicado ao longo do eixo y.</span><span class="sxs-lookup"><span data-stu-id="a4010-115">Scaling factor that is applied along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="a4010-116">*sz* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4010-116">*sz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4010-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4010-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a4010-118">Fator de dimensionamento aplicado ao longo do eixo z.</span><span class="sxs-lookup"><span data-stu-id="a4010-118">Scaling factor that is applied along the z-axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4010-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a4010-119">Return value</span></span>

<span data-ttu-id="a4010-120">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a4010-120">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a4010-121">Ponteiro para o D3DXMATRIX de transformação de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="a4010-121">Pointer to the scaling transformation D3DXMATRIX.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4010-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4010-122">Remarks</span></span>

<span data-ttu-id="a4010-123">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="a4010-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a4010-124">Dessa forma, a função D3DXMatrixScaling pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="a4010-124">In this way, the D3DXMatrixScaling function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4010-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4010-125">Requirements</span></span>



| <span data-ttu-id="a4010-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4010-126">Requirement</span></span> | <span data-ttu-id="a4010-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a4010-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4010-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a4010-128">Header</span></span><br/>  | <dl> <span data-ttu-id="a4010-129"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4010-129"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="a4010-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a4010-130">Library</span></span><br/> | <dl> <span data-ttu-id="a4010-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4010-131"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a4010-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4010-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4010-133">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="a4010-133">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
