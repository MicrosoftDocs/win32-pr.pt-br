---
description: Retorna a versão normalizada de um vetor 4D.
ms.assetid: ed3c48cf-4985-4ef3-b733-f8532e3ff6b5
title: Função D3DXVec4Normalize (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: ebedbdddbe558bfad71520b64aa0cf2ff4c2f451
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298708"
---
# <a name="d3dxvec4normalize-function-d3dx10mathh"></a><span data-ttu-id="f8757-103">Função D3DXVec4Normalize (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="f8757-103">D3DXVec4Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="f8757-104">Retorna a versão normalizada de um vetor 4D.</span><span class="sxs-lookup"><span data-stu-id="f8757-104">Returns the normalized version of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8757-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8757-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="f8757-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8757-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8757-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f8757-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8757-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8757-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="f8757-109">Ponteiro para o [**D3DXVECTOR4**](d3d10-d3dxvector4.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="f8757-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f8757-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f8757-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8757-111">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="f8757-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="f8757-112">Ponteiro para a estrutura de D3DXVECTOR4 de origem.</span><span class="sxs-lookup"><span data-stu-id="f8757-112">Pointer to the source D3DXVECTOR4 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8757-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f8757-113">Return value</span></span>

<span data-ttu-id="f8757-114">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8757-114">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="f8757-115">Ponteiro para uma estrutura D3DXVECTOR4 que é a versão normalizada do vetor.</span><span class="sxs-lookup"><span data-stu-id="f8757-115">Pointer to a D3DXVECTOR4 structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8757-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8757-116">Remarks</span></span>

<span data-ttu-id="f8757-117">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="f8757-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f8757-118">Dessa forma, a função D3DXVec4Normalize pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="f8757-118">In this way, the D3DXVec4Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8757-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8757-119">Requirements</span></span>



| <span data-ttu-id="f8757-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8757-120">Requirement</span></span> | <span data-ttu-id="f8757-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f8757-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8757-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f8757-122">Header</span></span><br/> | <dl> <span data-ttu-id="f8757-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8757-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8757-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8757-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8757-125">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="f8757-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
