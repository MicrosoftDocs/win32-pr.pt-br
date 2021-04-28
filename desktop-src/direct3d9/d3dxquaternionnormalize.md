---
description: Função D3DXQuaternionNormalize (D3dx9math. h) – computa um Quaternion de comprimento de unidade.
ms.assetid: 31f56c2b-96b0-4110-a5b9-ce09983779b6
title: Função D3DXQuaternionNormalize (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a5d4a7938b96d3d8693fd2091fcbd4f664f465c5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094034"
---
# <a name="d3dxquaternionnormalize-function-d3dx9mathh"></a><span data-ttu-id="9ab28-103">Função D3DXQuaternionNormalize (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="9ab28-103">D3DXQuaternionNormalize function (D3dx9math.h)</span></span>

<span data-ttu-id="9ab28-104">Computa um Quaternion de comprimento de unidade.</span><span class="sxs-lookup"><span data-stu-id="9ab28-104">Computes a unit length quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ab28-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ab28-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionNormalize(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="9ab28-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ab28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ab28-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="9ab28-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ab28-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="9ab28-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="9ab28-109">Ponteiro para a estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="9ab28-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9ab28-110">*pQ* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9ab28-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ab28-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="9ab28-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="9ab28-112">Ponteiro para a estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="9ab28-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ab28-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9ab28-113">Return value</span></span>

<span data-ttu-id="9ab28-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="9ab28-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="9ab28-115">Ponteiro para uma estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o normal do Quaternion.</span><span class="sxs-lookup"><span data-stu-id="9ab28-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the normal of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ab28-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ab28-116">Remarks</span></span>

<span data-ttu-id="9ab28-117">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="9ab28-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="9ab28-118">Dessa forma, a função **D3DXQuaternionNormalize** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="9ab28-118">In this way, the **D3DXQuaternionNormalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ab28-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ab28-119">Requirements</span></span>



| <span data-ttu-id="9ab28-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ab28-120">Requirement</span></span> | <span data-ttu-id="9ab28-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9ab28-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ab28-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9ab28-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9ab28-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ab28-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9ab28-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9ab28-124">Library</span></span><br/> | <dl> <span data-ttu-id="9ab28-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ab28-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9ab28-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9ab28-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ab28-127">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="9ab28-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="9ab28-128">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="9ab28-128">**D3DXQuaternionInverse**</span></span>](d3dxquaternioninverse.md)
</dt> </dl>

 

 




