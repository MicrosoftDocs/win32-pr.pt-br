---
description: Computa um Quaternion de comprimento de unidade.
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
ms.openlocfilehash: e121ef4892c65a0f04acaa89d44d4a5a9090740e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173112"
---
# <a name="d3dxquaternionnormalize-function-d3dx10mathh"></a><span data-ttu-id="bf93b-103">Função D3DXQuaternionNormalize (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="bf93b-103">D3DXQuaternionNormalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="bf93b-104">Computa um Quaternion de comprimento de unidade.</span><span class="sxs-lookup"><span data-stu-id="bf93b-104">Computes a unit length quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf93b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf93b-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionNormalize(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="bf93b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf93b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf93b-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="bf93b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf93b-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="bf93b-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="bf93b-109">Ponteiro para o [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="bf93b-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bf93b-110">*pQ* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bf93b-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf93b-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="bf93b-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="bf93b-112">Ponteiro para a estrutura de D3DXQUATERNION de origem.</span><span class="sxs-lookup"><span data-stu-id="bf93b-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf93b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bf93b-113">Return value</span></span>

<span data-ttu-id="bf93b-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="bf93b-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="bf93b-115">Ponteiro para uma estrutura D3DXQUATERNION que é o normal do Quaternion.</span><span class="sxs-lookup"><span data-stu-id="bf93b-115">Pointer to a D3DXQUATERNION structure that is the normal of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf93b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf93b-116">Remarks</span></span>

<span data-ttu-id="bf93b-117">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="bf93b-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="bf93b-118">Dessa forma, a função D3DXQuaternionNormalize pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="bf93b-118">In this way, the D3DXQuaternionNormalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf93b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf93b-119">Requirements</span></span>



| <span data-ttu-id="bf93b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf93b-120">Requirement</span></span> | <span data-ttu-id="bf93b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="bf93b-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf93b-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf93b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="bf93b-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf93b-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="bf93b-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf93b-124">Library</span></span><br/> | <dl> <span data-ttu-id="bf93b-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf93b-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bf93b-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf93b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf93b-127">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="bf93b-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
