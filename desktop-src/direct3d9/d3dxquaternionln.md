---
description: Função D3DXQuaternionLn (D3dx9math. h) – calcula o logaritmo natural.
ms.assetid: 73ca7d13-1e20-48fc-b0ed-0d3127d094a7
title: Função D3DXQuaternionLn (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLn
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1a529c1c6ca4d7f81bf4d41fcdb4a7c7179874b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094054"
---
# <a name="d3dxquaternionln-function-d3dx9mathh"></a><span data-ttu-id="0b7d5-103">Função D3DXQuaternionLn (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0b7d5-103">D3DXQuaternionLn function (D3dx9math.h)</span></span>

<span data-ttu-id="0b7d5-104">Calcula o logaritmo natural.</span><span class="sxs-lookup"><span data-stu-id="0b7d5-104">Calculates the natural logarithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b7d5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b7d5-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionLn(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="0b7d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b7d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b7d5-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="0b7d5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b7d5-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="0b7d5-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0b7d5-109">Ponteiro para a estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="0b7d5-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0b7d5-110">*pQ* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0b7d5-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b7d5-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="0b7d5-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0b7d5-112">Ponteiro para a estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="0b7d5-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b7d5-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0b7d5-113">Return value</span></span>

<span data-ttu-id="0b7d5-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="0b7d5-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0b7d5-115">Ponteiro para uma estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o logaritmo natural.</span><span class="sxs-lookup"><span data-stu-id="0b7d5-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the natural logarithm.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b7d5-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b7d5-116">Remarks</span></span>

<span data-ttu-id="0b7d5-117">A função **D3DXQuaternionLn** funciona apenas para os quaternions da unidade.</span><span class="sxs-lookup"><span data-stu-id="0b7d5-117">The **D3DXQuaternionLn** function works only for unit quaternions.</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="0b7d5-118">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="0b7d5-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="0b7d5-119">Dessa forma, a função **D3DXQuaternionLn** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="0b7d5-119">In this way, the **D3DXQuaternionLn** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="0b7d5-120">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="0b7d5-120">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b7d5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b7d5-121">Requirements</span></span>



| <span data-ttu-id="0b7d5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b7d5-122">Requirement</span></span> | <span data-ttu-id="0b7d5-123">Valor</span><span class="sxs-lookup"><span data-stu-id="0b7d5-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b7d5-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b7d5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0b7d5-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b7d5-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0b7d5-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0b7d5-126">Library</span></span><br/> | <dl> <span data-ttu-id="0b7d5-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b7d5-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0b7d5-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0b7d5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b7d5-129">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="0b7d5-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="0b7d5-130">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="0b7d5-130">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
</dt> <dt>

[<span data-ttu-id="0b7d5-131">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="0b7d5-131">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




