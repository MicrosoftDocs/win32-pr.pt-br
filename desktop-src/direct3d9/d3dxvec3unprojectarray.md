---
description: Projeta uma matriz (x, y, z, 0) do espaço da tela no espaço do objeto.
ms.assetid: fef2a76c-c2fe-48c5-a1bb-6669bcc76b9b
title: Função D3DXVec3UnprojectArray (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3UnprojectArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3af4cc05b5f8ee30c624f904df7e2ae5cd4b844a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930714"
---
# <a name="d3dxvec3unprojectarray-function-d3dx9mathh"></a><span data-ttu-id="0107a-103">Função D3DXVec3UnprojectArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0107a-103">D3DXVec3UnprojectArray function (D3dx9math.h)</span></span>

<span data-ttu-id="0107a-104">Projeta uma matriz (x, y, z, 0) do espaço da tela no espaço do objeto.</span><span class="sxs-lookup"><span data-stu-id="0107a-104">Projects an array (x, y, z, 0) from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="0107a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0107a-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3UnprojectArray(
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



## <a name="parameters"></a><span data-ttu-id="0107a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0107a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0107a-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="0107a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0107a-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="0107a-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0107a-109">Ponteiro para a estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="0107a-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0107a-110">*Didistância* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0107a-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0107a-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0107a-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0107a-112">Stride entre os vetores no fluxo de dados de saída.</span><span class="sxs-lookup"><span data-stu-id="0107a-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="0107a-113">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0107a-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0107a-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0107a-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0107a-115">Ponteiro para a estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="0107a-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0107a-116">*VStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0107a-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0107a-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0107a-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0107a-118">Stride entre os vetores no fluxo de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="0107a-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="0107a-119">*pViewport* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0107a-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0107a-120">Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="0107a-120">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="0107a-121">Ponteiro para uma estrutura [**D3DVIEWPORT9**](d3dviewport9.md) , representando o visor.</span><span class="sxs-lookup"><span data-stu-id="0107a-121">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="0107a-122">*pProjection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0107a-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0107a-123">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0107a-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0107a-124">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) , representando a matriz de projeção.</span><span class="sxs-lookup"><span data-stu-id="0107a-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="0107a-125">*pView* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0107a-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0107a-126">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0107a-126">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0107a-127">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) , representando a matriz de exibição.</span><span class="sxs-lookup"><span data-stu-id="0107a-127">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="0107a-128">*pWorld* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0107a-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0107a-129">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0107a-129">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0107a-130">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) , representando a matriz mundial.</span><span class="sxs-lookup"><span data-stu-id="0107a-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="0107a-131">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="0107a-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0107a-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0107a-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0107a-133">Número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="0107a-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0107a-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0107a-134">Return value</span></span>

<span data-ttu-id="0107a-135">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="0107a-135">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0107a-136">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é a matriz projetada do espaço da tela para o espaço de objeto.</span><span class="sxs-lookup"><span data-stu-id="0107a-136">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the array projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="0107a-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="0107a-137">Remarks</span></span>

<span data-ttu-id="0107a-138">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="0107a-138">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="0107a-139">Dessa forma, a função [**D3DXVec3Unproject**](d3dxvec3unproject.md) pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="0107a-139">In this way, the [**D3DXVec3Unproject**](d3dxvec3unproject.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0107a-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0107a-140">Requirements</span></span>



| <span data-ttu-id="0107a-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="0107a-141">Requirement</span></span> | <span data-ttu-id="0107a-142">Valor</span><span class="sxs-lookup"><span data-stu-id="0107a-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0107a-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0107a-143">Header</span></span><br/>  | <dl> <span data-ttu-id="0107a-144"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0107a-144"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0107a-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0107a-145">Library</span></span><br/> | <dl> <span data-ttu-id="0107a-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0107a-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0107a-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="0107a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0107a-148">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="0107a-148">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="0107a-149">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="0107a-149">**D3DXVec3Project**</span></span>](d3dxvec3project.md)
</dt> </dl>

 

 
