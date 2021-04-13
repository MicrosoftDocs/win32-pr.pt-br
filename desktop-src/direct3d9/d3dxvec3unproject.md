---
description: Projeta um vetor do espaço da tela no espaço do objeto.
ms.assetid: 9fd69cae-1d9c-4fae-9e15-8eb9950b4850
title: Função D3DXVec3Unproject (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Unproject
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2bab9af4a2c88a3e3b3b7f342b6c7c9cc89ceb66
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298774"
---
# <a name="d3dxvec3unproject-function-d3dx9mathh"></a><span data-ttu-id="f0f5f-103">Função D3DXVec3Unproject (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f0f5f-103">D3DXVec3Unproject function (D3dx9math.h)</span></span>

<span data-ttu-id="f0f5f-104">Projeta um vetor do espaço da tela no espaço do objeto.</span><span class="sxs-lookup"><span data-stu-id="f0f5f-104">Projects a vector from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0f5f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0f5f-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Unproject(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_    const D3DXVECTOR3  *pV,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld
);
```



## <a name="parameters"></a><span data-ttu-id="f0f5f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0f5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0f5f-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f0f5f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0f5f-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0f5f-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f0f5f-109">Ponteiro para a estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="f0f5f-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f0f5f-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f0f5f-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0f5f-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f0f5f-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f0f5f-112">Ponteiro para a estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="f0f5f-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f0f5f-113">*pViewport* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f0f5f-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0f5f-114">Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="f0f5f-114">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="f0f5f-115">Ponteiro para uma estrutura [**D3DVIEWPORT9**](d3dviewport9.md) , representando o visor.</span><span class="sxs-lookup"><span data-stu-id="f0f5f-115">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="f0f5f-116">*pProjection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f0f5f-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0f5f-117">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f0f5f-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f0f5f-118">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) , representando a matriz de projeção.</span><span class="sxs-lookup"><span data-stu-id="f0f5f-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="f0f5f-119">*pView* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f0f5f-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0f5f-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f0f5f-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f0f5f-121">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) , representando a matriz de exibição.</span><span class="sxs-lookup"><span data-stu-id="f0f5f-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="f0f5f-122">*pWorld* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f0f5f-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0f5f-123">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f0f5f-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f0f5f-124">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) , representando a matriz mundial.</span><span class="sxs-lookup"><span data-stu-id="f0f5f-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0f5f-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f0f5f-125">Return value</span></span>

<span data-ttu-id="f0f5f-126">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0f5f-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f0f5f-127">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é o vetor projetado do espaço da tela para o espaço de objeto.</span><span class="sxs-lookup"><span data-stu-id="f0f5f-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the vector projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0f5f-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0f5f-128">Remarks</span></span>

<span data-ttu-id="f0f5f-129">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="f0f5f-129">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f0f5f-130">Dessa forma, a função **D3DXVec3Unproject** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="f0f5f-130">In this way, the **D3DXVec3Unproject** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0f5f-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0f5f-131">Requirements</span></span>



| <span data-ttu-id="f0f5f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0f5f-132">Requirement</span></span> | <span data-ttu-id="f0f5f-133">Valor</span><span class="sxs-lookup"><span data-stu-id="f0f5f-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0f5f-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f0f5f-134">Header</span></span><br/>  | <dl> <span data-ttu-id="f0f5f-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0f5f-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f0f5f-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f0f5f-136">Library</span></span><br/> | <dl> <span data-ttu-id="f0f5f-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0f5f-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f0f5f-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0f5f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0f5f-139">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="f0f5f-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f0f5f-140">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="f0f5f-140">**D3DXVec3Project**</span></span>](d3dxvec3project.md)
</dt> </dl>

 

 




