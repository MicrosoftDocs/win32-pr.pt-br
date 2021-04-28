---
description: Função D3DXVec4Transform (D3dx9math. h) – transforma um vetor 4D por uma determinada matriz.
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
ms.openlocfilehash: 2e5a9fdd92a2d978c746543fbbbeec6503d07404
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115504"
---
# <a name="d3dxvec4transform-function-d3dx9mathh"></a><span data-ttu-id="dce4a-103">Função D3DXVec4Transform (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="dce4a-103">D3DXVec4Transform function (D3dx9math.h)</span></span>

<span data-ttu-id="dce4a-104">Transforma um vetor 4D por uma determinada matriz.</span><span class="sxs-lookup"><span data-stu-id="dce4a-104">Transforms a 4D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="dce4a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dce4a-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="dce4a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dce4a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dce4a-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="dce4a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dce4a-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="dce4a-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="dce4a-109">Ponteiro para a estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="dce4a-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="dce4a-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dce4a-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dce4a-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="dce4a-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="dce4a-112">Ponteiro para a estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="dce4a-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="dce4a-113">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dce4a-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dce4a-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="dce4a-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="dce4a-115">Ponteiro para a estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="dce4a-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dce4a-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="dce4a-116">Return value</span></span>

<span data-ttu-id="dce4a-117">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="dce4a-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="dce4a-118">Ponteiro para uma estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o vetor 4D transformado.</span><span class="sxs-lookup"><span data-stu-id="dce4a-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="dce4a-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="dce4a-119">Remarks</span></span>

<span data-ttu-id="dce4a-120">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="dce4a-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="dce4a-121">Dessa forma, a função **D3DXVec4Transform** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="dce4a-121">In this way, the **D3DXVec4Transform** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="dce4a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dce4a-122">Requirements</span></span>



| <span data-ttu-id="dce4a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="dce4a-123">Requirement</span></span> | <span data-ttu-id="dce4a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="dce4a-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dce4a-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dce4a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="dce4a-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="dce4a-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="dce4a-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dce4a-127">Library</span></span><br/> | <dl> <span data-ttu-id="dce4a-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dce4a-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dce4a-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="dce4a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dce4a-130">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="dce4a-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




