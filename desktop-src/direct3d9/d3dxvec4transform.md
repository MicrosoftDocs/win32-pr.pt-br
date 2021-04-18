---
description: Transforma um vetor 4D por uma determinada matriz.
ms.assetid: de93f138-7cf8-43cc-8255-c053c799aea8
title: Função D3DXVec4Transform (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Transform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 20192cf51a6096bbbce1f009d91d96551aec12d8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105814063"
---
# <a name="d3dxvec4transform-function-d3dx9mathh"></a><span data-ttu-id="fa727-103">Função D3DXVec4Transform (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="fa727-103">D3DXVec4Transform function (D3dx9math.h)</span></span>

<span data-ttu-id="fa727-104">Transforma um vetor 4D por uma determinada matriz.</span><span class="sxs-lookup"><span data-stu-id="fa727-104">Transforms a 4D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa727-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa727-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="fa727-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa727-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa727-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="fa727-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa727-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="fa727-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="fa727-109">Ponteiro para a estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="fa727-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fa727-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fa727-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa727-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="fa727-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="fa727-112">Ponteiro para a estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="fa727-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fa727-113">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fa727-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa727-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fa727-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fa727-115">Ponteiro para a estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="fa727-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa727-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa727-116">Return value</span></span>

<span data-ttu-id="fa727-117">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="fa727-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="fa727-118">Ponteiro para uma estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o vetor 4D transformado.</span><span class="sxs-lookup"><span data-stu-id="fa727-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa727-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa727-119">Remarks</span></span>

<span data-ttu-id="fa727-120">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="fa727-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="fa727-121">Dessa forma, a função **D3DXVec4Transform** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="fa727-121">In this way, the **D3DXVec4Transform** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa727-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa727-122">Requirements</span></span>



| <span data-ttu-id="fa727-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa727-123">Requirement</span></span> | <span data-ttu-id="fa727-124">Valor</span><span class="sxs-lookup"><span data-stu-id="fa727-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa727-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa727-125">Header</span></span><br/>  | <dl> <span data-ttu-id="fa727-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa727-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fa727-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fa727-127">Library</span></span><br/> | <dl> <span data-ttu-id="fa727-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa727-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fa727-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa727-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa727-130">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="fa727-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




