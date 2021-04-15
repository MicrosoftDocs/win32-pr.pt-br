---
description: Conjuga e renormaliza um Quaternion.
ms.assetid: 25407a60-f7c0-4063-8d1d-2d6d03bdb217
title: Função D3DXQuaternionInverse (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b2f830b7f8f797e4ed94eb22b4c2a05c3bd3e4cd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370999"
---
# <a name="d3dxquaternioninverse-function-d3dx9mathh"></a><span data-ttu-id="118d5-103">Função D3DXQuaternionInverse (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="118d5-103">D3DXQuaternionInverse function (D3dx9math.h)</span></span>

<span data-ttu-id="118d5-104">Conjuga e renormaliza um Quaternion.</span><span class="sxs-lookup"><span data-stu-id="118d5-104">Conjugates and renormalizes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="118d5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="118d5-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionInverse(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="118d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="118d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="118d5-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="118d5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="118d5-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="118d5-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="118d5-109">Ponteiro para a estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="118d5-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="118d5-110">*pQ* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="118d5-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="118d5-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="118d5-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="118d5-112">Ponteiro para a estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="118d5-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="118d5-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="118d5-113">Return value</span></span>

<span data-ttu-id="118d5-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="118d5-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="118d5-115">Ponteiro para uma estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o quaternion inverso do Quaternion.</span><span class="sxs-lookup"><span data-stu-id="118d5-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the inverse quaternion of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="118d5-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="118d5-116">Remarks</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="118d5-117">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="118d5-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="118d5-118">Dessa forma, a função **D3DXQuaternionInverse** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="118d5-118">In this way, the **D3DXQuaternionInverse** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="118d5-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="118d5-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="118d5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="118d5-120">Requirements</span></span>



| <span data-ttu-id="118d5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="118d5-121">Requirement</span></span> | <span data-ttu-id="118d5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="118d5-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="118d5-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="118d5-123">Header</span></span><br/>  | <dl> <span data-ttu-id="118d5-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="118d5-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="118d5-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="118d5-125">Library</span></span><br/> | <dl> <span data-ttu-id="118d5-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="118d5-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="118d5-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="118d5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="118d5-128">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="118d5-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="118d5-129">**D3DXQuaternionConjugate**</span><span class="sxs-lookup"><span data-stu-id="118d5-129">**D3DXQuaternionConjugate**</span></span>](d3dxquaternionconjugate.md)
</dt> <dt>

[<span data-ttu-id="118d5-130">**D3DXQuaternionNormalize**</span><span class="sxs-lookup"><span data-stu-id="118d5-130">**D3DXQuaternionNormalize**</span></span>](d3dxquaternionnormalize.md)
</dt> </dl>

 

 




