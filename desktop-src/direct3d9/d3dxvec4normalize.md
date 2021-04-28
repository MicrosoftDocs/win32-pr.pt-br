---
description: Função D3DXVec4Normalize (D3dx9math. h) – retorna a versão normalizada de um vetor 4D.
ms.assetid: e12d5dc7-b26f-41dd-b89d-1df9ba23077a
title: Função D3DXVec4Normalize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 78984c393d7caf259b4c310a31e01ed8fcbd4d47
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097654"
---
# <a name="d3dxvec4normalize-function-d3dx9mathh"></a><span data-ttu-id="6541e-103">Função D3DXVec4Normalize (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="6541e-103">D3DXVec4Normalize function (D3dx9math.h)</span></span>

<span data-ttu-id="6541e-104">Retorna a versão normalizada de um vetor 4D.</span><span class="sxs-lookup"><span data-stu-id="6541e-104">Returns the normalized version of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="6541e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6541e-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="6541e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6541e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6541e-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="6541e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6541e-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="6541e-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="6541e-109">Ponteiro para a estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="6541e-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6541e-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6541e-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6541e-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="6541e-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="6541e-112">Ponteiro para a estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="6541e-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6541e-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6541e-113">Return value</span></span>

<span data-ttu-id="6541e-114">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="6541e-114">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="6541e-115">Ponteiro para uma estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é a versão normalizada do vetor.</span><span class="sxs-lookup"><span data-stu-id="6541e-115">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="6541e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="6541e-116">Remarks</span></span>

<span data-ttu-id="6541e-117">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="6541e-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="6541e-118">Dessa forma, a função **D3DXVec4Normalize** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="6541e-118">In this way, the **D3DXVec4Normalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6541e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6541e-119">Requirements</span></span>



| <span data-ttu-id="6541e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6541e-120">Requirement</span></span> | <span data-ttu-id="6541e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6541e-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6541e-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6541e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6541e-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6541e-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6541e-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6541e-124">Library</span></span><br/> | <dl> <span data-ttu-id="6541e-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6541e-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6541e-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6541e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6541e-127">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="6541e-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




