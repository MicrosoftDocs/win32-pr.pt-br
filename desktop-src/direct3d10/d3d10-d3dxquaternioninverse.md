---
description: Função D3DXQuaternionInverse (D3DX10Math. h)-conjugas e renormaliza um Quaternion.
ms.assetid: 8e1bba91-8895-43a2-805b-1368050f8e82
title: Função D3DXQuaternionInverse (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionInverse
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 84816ac72841dcda0aef726535b7f5219d5467e4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103194"
---
# <a name="d3dxquaternioninverse-function-d3dx10mathh"></a><span data-ttu-id="be47b-103">Função D3DXQuaternionInverse (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="be47b-103">D3DXQuaternionInverse function (D3DX10Math.h)</span></span>

<span data-ttu-id="be47b-104">Conjuga e renormaliza um Quaternion.</span><span class="sxs-lookup"><span data-stu-id="be47b-104">Conjugates and renormalizes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="be47b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be47b-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionInverse(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="be47b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be47b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be47b-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="be47b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="be47b-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="be47b-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="be47b-109">Ponteiro para o [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="be47b-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="be47b-110">*pQ* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="be47b-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be47b-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="be47b-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="be47b-112">Ponteiro para a estrutura de D3DXQUATERNION de origem.</span><span class="sxs-lookup"><span data-stu-id="be47b-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be47b-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="be47b-113">Return value</span></span>

<span data-ttu-id="be47b-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="be47b-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="be47b-115">Ponteiro para uma estrutura D3DXQUATERNION que é o quaternion inverso do Quaternion.</span><span class="sxs-lookup"><span data-stu-id="be47b-115">Pointer to a D3DXQUATERNION structure that is the inverse quaternion of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="be47b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="be47b-116">Remarks</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="be47b-117">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="be47b-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="be47b-118">Dessa forma, a função D3DXQuaternionInverse pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="be47b-118">In this way, the D3DXQuaternionInverse function can be used as a parameter for another function.</span></span>

<span data-ttu-id="be47b-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="be47b-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="be47b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be47b-120">Requirements</span></span>



| <span data-ttu-id="be47b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="be47b-121">Requirement</span></span> | <span data-ttu-id="be47b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="be47b-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be47b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be47b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="be47b-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="be47b-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="be47b-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="be47b-125">Library</span></span><br/> | <dl> <span data-ttu-id="be47b-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be47b-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="be47b-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="be47b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be47b-128">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="be47b-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
