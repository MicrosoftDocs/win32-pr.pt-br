---
description: Projeta uma matriz (x, y, z, 0) do espaço do objeto no espaço da tela.
ms.assetid: cf022741-0bae-4c22-872f-bd94c3721aff
title: Função D3DXVec3ProjectArray (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3ProjectArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f802d8ab564f2cbfe1cc60ad6aed13959bef9383
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105788622"
---
# <a name="d3dxvec3projectarray-function-d3dx9mathh"></a><span data-ttu-id="a125f-103">Função D3DXVec3ProjectArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a125f-103">D3DXVec3ProjectArray function (D3dx9math.h)</span></span>

<span data-ttu-id="a125f-104">Projeta uma matriz (x, y, z, 0) do espaço do objeto no espaço da tela.</span><span class="sxs-lookup"><span data-stu-id="a125f-104">Projects an array (x, y, z, 0) from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="a125f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a125f-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3ProjectArray(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_          UINT         OutStride,
  _In_    const D3DXVECTOR3  *pV,
  _In_          UINT         VStride,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld,
  _In_          UINT         n
);
```



## <a name="parameters"></a><span data-ttu-id="a125f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a125f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a125f-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="a125f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a125f-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a125f-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a125f-109">Ponteiro para a estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="a125f-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a125f-110">*Didistância* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a125f-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a125f-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a125f-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a125f-112">Stride entre os vetores no fluxo de dados de saída.</span><span class="sxs-lookup"><span data-stu-id="a125f-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="a125f-113">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a125f-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a125f-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a125f-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a125f-115">Ponteiro para a estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="a125f-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a125f-116">*VStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a125f-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a125f-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a125f-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a125f-118">Stride entre os vetores no fluxo de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="a125f-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="a125f-119">*pViewport* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a125f-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a125f-120">Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="a125f-120">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="a125f-121">Ponteiro para uma estrutura [**D3DVIEWPORT9**](d3dviewport9.md) , representando o visor.</span><span class="sxs-lookup"><span data-stu-id="a125f-121">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="a125f-122">*pProjection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a125f-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a125f-123">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a125f-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a125f-124">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) , representando a matriz de projeção.</span><span class="sxs-lookup"><span data-stu-id="a125f-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="a125f-125">*pView* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a125f-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a125f-126">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a125f-126">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a125f-127">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) , representando a matriz de exibição.</span><span class="sxs-lookup"><span data-stu-id="a125f-127">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="a125f-128">*pWorld* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a125f-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a125f-129">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a125f-129">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a125f-130">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) , representando a matriz mundial.</span><span class="sxs-lookup"><span data-stu-id="a125f-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="a125f-131">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="a125f-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a125f-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a125f-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a125f-133">Número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="a125f-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a125f-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a125f-134">Return value</span></span>

<span data-ttu-id="a125f-135">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a125f-135">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a125f-136">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é a matriz projetada do espaço de objeto para o espaço da tela.</span><span class="sxs-lookup"><span data-stu-id="a125f-136">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the array projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="a125f-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="a125f-137">Remarks</span></span>

<span data-ttu-id="a125f-138">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="a125f-138">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a125f-139">Dessa forma, a função **D3DXVec3ProjectArray** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="a125f-139">In this way, the **D3DXVec3ProjectArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a125f-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a125f-140">Requirements</span></span>



| <span data-ttu-id="a125f-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="a125f-141">Requirement</span></span> | <span data-ttu-id="a125f-142">Valor</span><span class="sxs-lookup"><span data-stu-id="a125f-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a125f-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a125f-143">Header</span></span><br/>  | <dl> <span data-ttu-id="a125f-144"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a125f-144"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a125f-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a125f-145">Library</span></span><br/> | <dl> <span data-ttu-id="a125f-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a125f-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a125f-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="a125f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a125f-148">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="a125f-148">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a125f-149">**D3DXVec3Unproject**</span><span class="sxs-lookup"><span data-stu-id="a125f-149">**D3DXVec3Unproject**</span></span>](d3dxvec3unproject.md)
</dt> </dl>

 

 
