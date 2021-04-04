---
description: Retorna a versão normalizada de um vetor 2D.
ms.assetid: fac4f269-2778-4500-af9e-23a0112543b0
title: Função D3DXVec2Normalize (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Normalize
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e2894a86c0aa0c2ef6b45a41664b2d0cca1427c1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837963"
---
# <a name="d3dxvec2normalize-function-d3dx10mathh"></a><span data-ttu-id="bcd79-103">Função D3DXVec2Normalize (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="bcd79-103">D3DXVec2Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="bcd79-104">Retorna a versão normalizada de um vetor 2D.</span><span class="sxs-lookup"><span data-stu-id="bcd79-104">Returns the normalized version of a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcd79-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bcd79-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Normalize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="bcd79-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bcd79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcd79-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="bcd79-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bcd79-108">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="bcd79-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="bcd79-109">Ponteiro para o [**D3DXVECTOR2**](d3d10-d3dxvector2.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="bcd79-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bcd79-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bcd79-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcd79-111">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="bcd79-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="bcd79-112">Ponteiro para a estrutura de D3DXVECTOR2 de origem.</span><span class="sxs-lookup"><span data-stu-id="bcd79-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcd79-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bcd79-113">Return value</span></span>

<span data-ttu-id="bcd79-114">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="bcd79-114">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="bcd79-115">Ponteiro para uma estrutura D3DXVECTOR2 que é a versão normalizada do vetor.</span><span class="sxs-lookup"><span data-stu-id="bcd79-115">Pointer to a D3DXVECTOR2 structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcd79-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="bcd79-116">Remarks</span></span>

<span data-ttu-id="bcd79-117">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="bcd79-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="bcd79-118">Dessa forma, a função D3DXVec2Normalize pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="bcd79-118">In this way, the D3DXVec2Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcd79-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcd79-119">Requirements</span></span>



| <span data-ttu-id="bcd79-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcd79-120">Requirement</span></span> | <span data-ttu-id="bcd79-121">Valor</span><span class="sxs-lookup"><span data-stu-id="bcd79-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcd79-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bcd79-122">Header</span></span><br/>  | <dl> <span data-ttu-id="bcd79-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcd79-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="bcd79-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bcd79-124">Library</span></span><br/> | <dl> <span data-ttu-id="bcd79-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bcd79-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bcd79-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="bcd79-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcd79-127">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="bcd79-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
