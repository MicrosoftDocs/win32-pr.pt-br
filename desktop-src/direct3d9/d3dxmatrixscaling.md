---
description: Cria uma matriz que é dimensionada ao longo do eixo x, do eixo y e do eixo z.
ms.assetid: f51baa4e-0aec-4de8-b746-24cb52f318d6
title: Função D3DXMatrixScaling (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7cfc14fc1d514f68f2881d26c4729440d709af93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105788693"
---
# <a name="d3dxmatrixscaling-function-d3dx9mathh"></a><span data-ttu-id="0d32b-103">Função D3DXMatrixScaling (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0d32b-103">D3DXMatrixScaling function (D3dx9math.h)</span></span>

<span data-ttu-id="0d32b-104">Cria uma matriz que é dimensionada ao longo do eixo x, do eixo y e do eixo z.</span><span class="sxs-lookup"><span data-stu-id="0d32b-104">Builds a matrix that scales along the x-axis, the y-axis, and the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d32b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d32b-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixScaling(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      sx,
  _In_    FLOAT      sy,
  _In_    FLOAT      sz
);
```



## <a name="parameters"></a><span data-ttu-id="0d32b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d32b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d32b-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="0d32b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d32b-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0d32b-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0d32b-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="0d32b-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0d32b-110">*SX* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0d32b-110">*sx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d32b-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0d32b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0d32b-112">Fator de dimensionamento aplicado ao longo do eixo x.</span><span class="sxs-lookup"><span data-stu-id="0d32b-112">Scaling factor that is applied along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="0d32b-113">*Sy* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0d32b-113">*sy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d32b-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0d32b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0d32b-115">Fator de dimensionamento aplicado ao longo do eixo y.</span><span class="sxs-lookup"><span data-stu-id="0d32b-115">Scaling factor that is applied along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="0d32b-116">*sz* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0d32b-116">*sz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d32b-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0d32b-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0d32b-118">Fator de dimensionamento aplicado ao longo do eixo z.</span><span class="sxs-lookup"><span data-stu-id="0d32b-118">Scaling factor that is applied along the z-axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d32b-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0d32b-119">Return value</span></span>

<span data-ttu-id="0d32b-120">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0d32b-120">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0d32b-121">Ponteiro para o [**D3DXMATRIX**](d3dxmatrix.md)de transformação de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="0d32b-121">Pointer to the scaling transformation [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0d32b-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d32b-122">Remarks</span></span>

<span data-ttu-id="0d32b-123">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="0d32b-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="0d32b-124">Dessa forma, a função **D3DXMatrixScaling** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="0d32b-124">In this way, the **D3DXMatrixScaling** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d32b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d32b-125">Requirements</span></span>



| <span data-ttu-id="0d32b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d32b-126">Requirement</span></span> | <span data-ttu-id="0d32b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="0d32b-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d32b-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0d32b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="0d32b-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d32b-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0d32b-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0d32b-130">Library</span></span><br/> | <dl> <span data-ttu-id="0d32b-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d32b-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0d32b-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d32b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d32b-133">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="0d32b-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
