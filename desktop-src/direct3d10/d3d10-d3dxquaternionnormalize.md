---
description: Função D3DXQuaternionNormalize (D3DX10Math. h) – computa um Quaternion de comprimento de unidade.
ms.assetid: 6735a632-64d7-4bc1-b63e-d0cd27f5a29b
title: Função D3DXQuaternionNormalize (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionNormalize
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6d031dfc63cb92d43a9cca27813c9425e2ff1acb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103134"
---
# <a name="d3dxquaternionnormalize-function-d3dx10mathh"></a><span data-ttu-id="9aeee-103">Função D3DXQuaternionNormalize (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="9aeee-103">D3DXQuaternionNormalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="9aeee-104">Computa um Quaternion de comprimento de unidade.</span><span class="sxs-lookup"><span data-stu-id="9aeee-104">Computes a unit length quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aeee-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9aeee-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionNormalize(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="9aeee-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9aeee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aeee-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="9aeee-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9aeee-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="9aeee-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="9aeee-109">Ponteiro para o [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="9aeee-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9aeee-110">*pQ* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9aeee-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aeee-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="9aeee-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="9aeee-112">Ponteiro para a estrutura de D3DXQUATERNION de origem.</span><span class="sxs-lookup"><span data-stu-id="9aeee-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aeee-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9aeee-113">Return value</span></span>

<span data-ttu-id="9aeee-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="9aeee-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="9aeee-115">Ponteiro para uma estrutura D3DXQUATERNION que é o normal do Quaternion.</span><span class="sxs-lookup"><span data-stu-id="9aeee-115">Pointer to a D3DXQUATERNION structure that is the normal of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aeee-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9aeee-116">Remarks</span></span>

<span data-ttu-id="9aeee-117">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="9aeee-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="9aeee-118">Dessa forma, a função D3DXQuaternionNormalize pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="9aeee-118">In this way, the D3DXQuaternionNormalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aeee-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9aeee-119">Requirements</span></span>



| <span data-ttu-id="9aeee-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9aeee-120">Requirement</span></span> | <span data-ttu-id="9aeee-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9aeee-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9aeee-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9aeee-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9aeee-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9aeee-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="9aeee-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9aeee-124">Library</span></span><br/> | <dl> <span data-ttu-id="9aeee-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9aeee-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9aeee-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9aeee-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aeee-127">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="9aeee-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
