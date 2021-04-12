---
description: Transforma um vetor 3D por uma determinada matriz, projetando o resultado de volta em w = 1.
ms.assetid: 4075b067-1e64-46c9-be73-5fa765c9cb9d
title: Função D3DXVec3TransformCoord (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4bcf1a78f9da4cf5fb2a5f67360a1659182c7ffb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298841"
---
# <a name="d3dxvec3transformcoord-function-d3dx9mathh"></a><span data-ttu-id="96fef-103">Função D3DXVec3TransformCoord (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="96fef-103">D3DXVec3TransformCoord function (D3dx9math.h)</span></span>

<span data-ttu-id="96fef-104">Transforma um vetor 3D por uma determinada matriz, projetando o resultado de volta em w = 1.</span><span class="sxs-lookup"><span data-stu-id="96fef-104">Transforms a 3D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="96fef-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96fef-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformCoord(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="96fef-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96fef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96fef-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="96fef-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="96fef-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="96fef-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="96fef-109">Ponteiro para a estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="96fef-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="96fef-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="96fef-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96fef-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="96fef-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="96fef-112">Ponteiro para a estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="96fef-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="96fef-113">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="96fef-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96fef-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="96fef-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="96fef-115">Ponteiro para a estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="96fef-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96fef-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="96fef-116">Return value</span></span>

<span data-ttu-id="96fef-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="96fef-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="96fef-118">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é o vetor transformado.</span><span class="sxs-lookup"><span data-stu-id="96fef-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="96fef-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="96fef-119">Remarks</span></span>

<span data-ttu-id="96fef-120">Essa função transforma o vetor, *VP* (x, y, z, 1), pela matriz, *PM*, projetando o resultado de volta em w = 1.</span><span class="sxs-lookup"><span data-stu-id="96fef-120">This function transforms the vector, *pV* (x, y, z, 1), by the matrix, *pM*, projecting the result back into w=1.</span></span>

<span data-ttu-id="96fef-121">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="96fef-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="96fef-122">Dessa forma, a função **D3DXVec3TransformCoord** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="96fef-122">In this way, the **D3DXVec3TransformCoord** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="96fef-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96fef-123">Requirements</span></span>



| <span data-ttu-id="96fef-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="96fef-124">Requirement</span></span> | <span data-ttu-id="96fef-125">Valor</span><span class="sxs-lookup"><span data-stu-id="96fef-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96fef-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="96fef-126">Header</span></span><br/>  | <dl> <span data-ttu-id="96fef-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="96fef-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="96fef-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="96fef-128">Library</span></span><br/> | <dl> <span data-ttu-id="96fef-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96fef-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="96fef-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="96fef-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96fef-131">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="96fef-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="96fef-132">**D3DXVec3Transform**</span><span class="sxs-lookup"><span data-stu-id="96fef-132">**D3DXVec3Transform**</span></span>](d3dxvec3transform.md)
</dt> <dt>

[<span data-ttu-id="96fef-133">**D3DXVec3TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="96fef-133">**D3DXVec3TransformNormal**</span></span>](d3dxvec3transformnormal.md)
</dt> </dl>

 

 




