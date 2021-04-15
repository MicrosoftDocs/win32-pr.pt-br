---
description: Retorna um vetor 3D que é composto pelos maiores componentes de dois vetores 3D.
ms.assetid: 8d3a5310-bee9-4dbd-bef3-8a0e1586f365
title: Função D3DXVec3Maximize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Maximize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d86f3e54a6399693e37cc0c8970439558d82c9c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506467"
---
# <a name="d3dxvec3maximize-function"></a><span data-ttu-id="4f1a0-103">Função D3DXVec3Maximize</span><span class="sxs-lookup"><span data-stu-id="4f1a0-103">D3DXVec3Maximize function</span></span>

<span data-ttu-id="4f1a0-104">Retorna um vetor 3D que é composto pelos maiores componentes de dois vetores 3D.</span><span class="sxs-lookup"><span data-stu-id="4f1a0-104">Returns a 3D vector that is made up of the largest components of two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f1a0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f1a0-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Maximize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="4f1a0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f1a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f1a0-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="4f1a0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f1a0-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="4f1a0-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4f1a0-109">Ponteiro para a estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="4f1a0-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4f1a0-110">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4f1a0-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f1a0-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4f1a0-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4f1a0-112">Ponteiro para uma estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="4f1a0-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4f1a0-113">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4f1a0-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f1a0-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4f1a0-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4f1a0-115">Ponteiro para uma estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="4f1a0-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f1a0-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4f1a0-116">Return value</span></span>

<span data-ttu-id="4f1a0-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="4f1a0-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4f1a0-118">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é composta pelos maiores componentes dos dois vetores.</span><span class="sxs-lookup"><span data-stu-id="4f1a0-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is made up of the largest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f1a0-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f1a0-119">Remarks</span></span>

<span data-ttu-id="4f1a0-120">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="4f1a0-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="4f1a0-121">Dessa forma, a função **D3DXVec3Maximize** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="4f1a0-121">In this way, the **D3DXVec3Maximize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f1a0-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f1a0-122">Requirements</span></span>



| <span data-ttu-id="4f1a0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f1a0-123">Requirement</span></span> | <span data-ttu-id="4f1a0-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4f1a0-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f1a0-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4f1a0-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4f1a0-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f1a0-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4f1a0-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4f1a0-127">Library</span></span><br/> | <dl> <span data-ttu-id="4f1a0-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f1a0-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4f1a0-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f1a0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f1a0-130">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="4f1a0-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="4f1a0-131">**D3DXVec3Minimize**</span><span class="sxs-lookup"><span data-stu-id="4f1a0-131">**D3DXVec3Minimize**</span></span>](d3dxvec3minimize.md)
</dt> </dl>

 

 




