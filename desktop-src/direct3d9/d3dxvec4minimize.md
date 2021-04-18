---
description: Retorna um vetor 4D que é composto pelos menores componentes de dois vetores de 4D.
ms.assetid: ae3819a3-a5b6-47c2-b789-3e3f07db9f03
title: Função D3DXVec4Minimize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Minimize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9ccd4806bfa368fafa481500d3bd28e0ff55b7d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105784600"
---
# <a name="d3dxvec4minimize-function"></a><span data-ttu-id="d6e50-103">Função D3DXVec4Minimize</span><span class="sxs-lookup"><span data-stu-id="d6e50-103">D3DXVec4Minimize function</span></span>

<span data-ttu-id="d6e50-104">Retorna um vetor 4D que é composto pelos menores componentes de dois vetores de 4D.</span><span class="sxs-lookup"><span data-stu-id="d6e50-104">Returns a 4D vector that is made up of the smallest components of two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6e50-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6e50-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Minimize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="d6e50-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6e50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6e50-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d6e50-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6e50-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="d6e50-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="d6e50-109">Ponteiro para a estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="d6e50-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d6e50-110">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d6e50-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6e50-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6e50-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="d6e50-112">Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="d6e50-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d6e50-113">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d6e50-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6e50-114">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6e50-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="d6e50-115">Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="d6e50-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6e50-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d6e50-116">Return value</span></span>

<span data-ttu-id="d6e50-117">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="d6e50-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="d6e50-118">Ponteiro para uma estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é composta pelos menores componentes dos dois vetores.</span><span class="sxs-lookup"><span data-stu-id="d6e50-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is made up of the smallest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6e50-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6e50-119">Remarks</span></span>

<span data-ttu-id="d6e50-120">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="d6e50-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d6e50-121">Dessa forma, a função **D3DXVec4Minimize** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="d6e50-121">In this way, the **D3DXVec4Minimize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6e50-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6e50-122">Requirements</span></span>



| <span data-ttu-id="d6e50-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6e50-123">Requirement</span></span> | <span data-ttu-id="d6e50-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d6e50-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6e50-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6e50-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d6e50-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6e50-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d6e50-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d6e50-127">Library</span></span><br/> | <dl> <span data-ttu-id="d6e50-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6e50-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d6e50-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6e50-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6e50-130">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="d6e50-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d6e50-131">**D3DXVec4Maximize**</span><span class="sxs-lookup"><span data-stu-id="d6e50-131">**D3DXVec4Maximize**</span></span>](d3dxvec4maximize.md)
</dt> </dl>

 

 




