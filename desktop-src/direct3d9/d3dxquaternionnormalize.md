---
description: Computa um Quaternion de comprimento de unidade.
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
ms.openlocfilehash: d052d4dfc88feb2a00237392071f63d724070b3d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506473"
---
# <a name="d3dxquaternionnormalize-function-d3dx9mathh"></a><span data-ttu-id="45242-103">Função D3DXQuaternionNormalize (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="45242-103">D3DXQuaternionNormalize function (D3dx9math.h)</span></span>

<span data-ttu-id="45242-104">Computa um Quaternion de comprimento de unidade.</span><span class="sxs-lookup"><span data-stu-id="45242-104">Computes a unit length quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="45242-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45242-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionNormalize(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="45242-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45242-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45242-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="45242-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="45242-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="45242-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="45242-109">Ponteiro para a estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="45242-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="45242-110">*pQ* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45242-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45242-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="45242-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="45242-112">Ponteiro para a estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="45242-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45242-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="45242-113">Return value</span></span>

<span data-ttu-id="45242-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="45242-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="45242-115">Ponteiro para uma estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o normal do Quaternion.</span><span class="sxs-lookup"><span data-stu-id="45242-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the normal of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="45242-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="45242-116">Remarks</span></span>

<span data-ttu-id="45242-117">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="45242-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="45242-118">Dessa forma, a função **D3DXQuaternionNormalize** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="45242-118">In this way, the **D3DXQuaternionNormalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="45242-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45242-119">Requirements</span></span>



| <span data-ttu-id="45242-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="45242-120">Requirement</span></span> | <span data-ttu-id="45242-121">Valor</span><span class="sxs-lookup"><span data-stu-id="45242-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45242-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45242-122">Header</span></span><br/>  | <dl> <span data-ttu-id="45242-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="45242-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="45242-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="45242-124">Library</span></span><br/> | <dl> <span data-ttu-id="45242-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45242-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="45242-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="45242-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45242-127">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="45242-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="45242-128">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="45242-128">**D3DXQuaternionInverse**</span></span>](d3dxquaternioninverse.md)
</dt> </dl>

 

 




