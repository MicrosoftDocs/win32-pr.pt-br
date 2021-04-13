---
description: Transforma o vetor (x, y, z, 1) por uma determinada matriz.
ms.assetid: 5b290c4c-22f1-4086-8e5e-f995757ef193
title: Função D3DXVec3Transform (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Transform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b653eeb7ea3797a3c385efda73ac974e2f4fbd97
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298843"
---
# <a name="d3dxvec3transform-function-d3dx9mathh"></a><span data-ttu-id="3461d-103">Função D3DXVec3Transform (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="3461d-103">D3DXVec3Transform function (D3dx9math.h)</span></span>

<span data-ttu-id="3461d-104">Transforma o vetor (x, y, z, 1) por uma determinada matriz.</span><span class="sxs-lookup"><span data-stu-id="3461d-104">Transforms vector (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="3461d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3461d-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec3Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="3461d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3461d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3461d-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="3461d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3461d-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="3461d-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="3461d-109">Ponteiro para a estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="3461d-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="3461d-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3461d-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3461d-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3461d-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3461d-112">Ponteiro para a estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="3461d-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3461d-113">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3461d-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3461d-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="3461d-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="3461d-115">Ponteiro para a estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="3461d-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3461d-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3461d-116">Return value</span></span>

<span data-ttu-id="3461d-117">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="3461d-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="3461d-118">Ponteiro para uma estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o vetor transformado.</span><span class="sxs-lookup"><span data-stu-id="3461d-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="3461d-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="3461d-119">Remarks</span></span>

<span data-ttu-id="3461d-120">Essa função transforma o vetor, *VP* (x, y, z, 1), pela matriz *PM*.</span><span class="sxs-lookup"><span data-stu-id="3461d-120">This function transforms the vector, *pV* (x, y, z, 1), by the matrix *pM*.</span></span>

<span data-ttu-id="3461d-121">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="3461d-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="3461d-122">Dessa forma, a função **D3DXVec3Transform** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="3461d-122">In this way, the **D3DXVec3Transform** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3461d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3461d-123">Requirements</span></span>



| <span data-ttu-id="3461d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3461d-124">Requirement</span></span> | <span data-ttu-id="3461d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="3461d-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3461d-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3461d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="3461d-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3461d-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="3461d-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3461d-128">Library</span></span><br/> | <dl> <span data-ttu-id="3461d-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3461d-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3461d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="3461d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3461d-131">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="3461d-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




