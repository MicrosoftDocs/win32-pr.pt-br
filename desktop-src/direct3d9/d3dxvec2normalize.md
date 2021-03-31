---
description: Retorna a versão normalizada de um vetor 2D.
ms.assetid: 2796a5d1-cb1c-4093-87f2-a2ad43279d91
title: Função D3DXVec2Normalize (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce3152c622c9083438d35c73b20e05ca2523efc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012089"
---
# <a name="d3dxvec2normalize-function-d3dx9mathh"></a><span data-ttu-id="817f0-103">Função D3DXVec2Normalize (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="817f0-103">D3DXVec2Normalize function (D3dx9math.h)</span></span>

<span data-ttu-id="817f0-104">Retorna a versão normalizada de um vetor 2D.</span><span class="sxs-lookup"><span data-stu-id="817f0-104">Returns the normalized version of a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="817f0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="817f0-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Normalize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="817f0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="817f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="817f0-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="817f0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="817f0-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="817f0-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="817f0-109">Ponteiro para a estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="817f0-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="817f0-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="817f0-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="817f0-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="817f0-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="817f0-112">Ponteiro para a estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="817f0-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="817f0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="817f0-113">Return value</span></span>

<span data-ttu-id="817f0-114">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="817f0-114">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="817f0-115">Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é a versão normalizada do vetor.</span><span class="sxs-lookup"><span data-stu-id="817f0-115">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="817f0-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="817f0-116">Remarks</span></span>

<span data-ttu-id="817f0-117">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="817f0-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="817f0-118">Dessa forma, a função **D3DXVec2Normalize** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="817f0-118">In this way, the **D3DXVec2Normalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="817f0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="817f0-119">Requirements</span></span>



| <span data-ttu-id="817f0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="817f0-120">Requirement</span></span> | <span data-ttu-id="817f0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="817f0-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="817f0-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="817f0-122">Header</span></span><br/>  | <dl> <span data-ttu-id="817f0-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="817f0-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="817f0-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="817f0-124">Library</span></span><br/> | <dl> <span data-ttu-id="817f0-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="817f0-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="817f0-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="817f0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="817f0-127">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="817f0-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




