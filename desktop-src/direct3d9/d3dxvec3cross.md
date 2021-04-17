---
description: Determina o produto cruzado de dois vetores 3D.
ms.assetid: c9623f35-c8fc-4fbe-87b6-0e5bb8ebd5e8
title: Função D3DXVec3Cross (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Cross
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ba0d8a80690f43d5f8e9f6df55aa3b2e0db23dc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105811560"
---
# <a name="d3dxvec3cross-function"></a><span data-ttu-id="2f6fc-103">Função D3DXVec3Cross</span><span class="sxs-lookup"><span data-stu-id="2f6fc-103">D3DXVec3Cross function</span></span>

<span data-ttu-id="2f6fc-104">Determina o produto cruzado de dois vetores 3D.</span><span class="sxs-lookup"><span data-stu-id="2f6fc-104">Determines the cross-product of two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f6fc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f6fc-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Cross(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="2f6fc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f6fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f6fc-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="2f6fc-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f6fc-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f6fc-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2f6fc-109">Ponteiro para a estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="2f6fc-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2f6fc-110">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2f6fc-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f6fc-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2f6fc-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2f6fc-112">Ponteiro para uma estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="2f6fc-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2f6fc-113">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2f6fc-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f6fc-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2f6fc-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2f6fc-115">Ponteiro para uma estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="2f6fc-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f6fc-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2f6fc-116">Return value</span></span>

<span data-ttu-id="2f6fc-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f6fc-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2f6fc-118">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é o produto cruzado de dois vetores 3D.</span><span class="sxs-lookup"><span data-stu-id="2f6fc-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the cross product of two 3D vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f6fc-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f6fc-119">Remarks</span></span>

<span data-ttu-id="2f6fc-120">Essa função determina o produto cruzado com o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="2f6fc-120">This function determines the cross-product with the following code.</span></span>


```
D3DXVECTOR3 v;
    
v.x = pV1->y * pV2->z - pV1->z * pV2->y;
v.y = pV1->z * pV2->x - pV1->x * pV2->z;
v.z = pV1->x * pV2->y - pV1->y * pV2->x;
    
*pOut = v;
```



<span data-ttu-id="2f6fc-121">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="2f6fc-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2f6fc-122">Dessa forma, a função **D3DXVec3Cross** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="2f6fc-122">In this way, the **D3DXVec3Cross** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f6fc-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f6fc-123">Requirements</span></span>



| <span data-ttu-id="2f6fc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f6fc-124">Requirement</span></span> | <span data-ttu-id="2f6fc-125">Valor</span><span class="sxs-lookup"><span data-stu-id="2f6fc-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f6fc-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2f6fc-126">Header</span></span><br/>  | <dl> <span data-ttu-id="2f6fc-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f6fc-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2f6fc-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f6fc-128">Library</span></span><br/> | <dl> <span data-ttu-id="2f6fc-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f6fc-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2f6fc-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f6fc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f6fc-131">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="2f6fc-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2f6fc-132">**D3DXVec3Dot**</span><span class="sxs-lookup"><span data-stu-id="2f6fc-132">**D3DXVec3Dot**</span></span>](d3dxvec3dot.md)
</dt> </dl>

 

 




