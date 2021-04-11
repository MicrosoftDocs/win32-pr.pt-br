---
description: Retorna o conjugado de um Quaternion.
ms.assetid: f690fdd8-7805-4fc1-9064-4f249d5f7c4f
title: Função D3DXQuaternionConjugate (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionConjugate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bbf288724dbdede9d98ec4ee21afd1bb57dd7a49
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173088"
---
# <a name="d3dxquaternionconjugate-function"></a><span data-ttu-id="804f1-103">Função D3DXQuaternionConjugate</span><span class="sxs-lookup"><span data-stu-id="804f1-103">D3DXQuaternionConjugate function</span></span>

<span data-ttu-id="804f1-104">Retorna o conjugado de um Quaternion.</span><span class="sxs-lookup"><span data-stu-id="804f1-104">Returns the conjugate of a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="804f1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="804f1-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionConjugate(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="804f1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="804f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="804f1-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="804f1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="804f1-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="804f1-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="804f1-109">Ponteiro para a estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="804f1-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="804f1-110">*pQ* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="804f1-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="804f1-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="804f1-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="804f1-112">Ponteiro para a estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="804f1-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="804f1-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="804f1-113">Return value</span></span>

<span data-ttu-id="804f1-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="804f1-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="804f1-115">Ponteiro para uma estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o conjugado do Quaternion.</span><span class="sxs-lookup"><span data-stu-id="804f1-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the conjugate of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="804f1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="804f1-116">Remarks</span></span>

<span data-ttu-id="804f1-117">Dado um Quaternion (x, y, z, w), a função **D3DXQuaternionConjugate** retornará o quaternion (-x,-y,-z, w).</span><span class="sxs-lookup"><span data-stu-id="804f1-117">Given a quaternion (x, y, z, w), the **D3DXQuaternionConjugate** function will return the quaternion (-x, -y, -z, w).</span></span>

<span data-ttu-id="804f1-118">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="804f1-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="804f1-119">Dessa forma, a função **D3DXQuaternionConjugate** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="804f1-119">In this way, the **D3DXQuaternionConjugate** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="804f1-120">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="804f1-120">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="804f1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="804f1-121">Requirements</span></span>



| <span data-ttu-id="804f1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="804f1-122">Requirement</span></span> | <span data-ttu-id="804f1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="804f1-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="804f1-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="804f1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="804f1-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="804f1-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="804f1-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="804f1-126">Library</span></span><br/> | <dl> <span data-ttu-id="804f1-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="804f1-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="804f1-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="804f1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="804f1-129">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="804f1-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="804f1-130">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="804f1-130">**D3DXQuaternionInverse**</span></span>](d3dxquaternioninverse.md)
</dt> </dl>

 

 




