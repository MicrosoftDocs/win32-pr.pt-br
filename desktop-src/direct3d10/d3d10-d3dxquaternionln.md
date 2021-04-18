---
description: Calcula o logaritmo natural.
ms.assetid: 576cf676-bb42-45ec-8e45-4612a7cdb167
title: Função D3DXQuaternionLn (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 07b081e0e2063d18ab8f2bb010e2b436c38df097
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105758503"
---
# <a name="d3dxquaternionln-function-d3dx10mathh"></a><span data-ttu-id="19fc4-103">Função D3DXQuaternionLn (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="19fc4-103">D3DXQuaternionLn function (D3DX10Math.h)</span></span>

<span data-ttu-id="19fc4-104">Calcula o logaritmo natural.</span><span class="sxs-lookup"><span data-stu-id="19fc4-104">Calculates the natural logarithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="19fc4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19fc4-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionLn(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="19fc4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19fc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19fc4-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="19fc4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="19fc4-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="19fc4-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="19fc4-109">Ponteiro para o [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="19fc4-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="19fc4-110">*pQ* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19fc4-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19fc4-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="19fc4-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="19fc4-112">Ponteiro para a estrutura de D3DXQUATERNION de origem.</span><span class="sxs-lookup"><span data-stu-id="19fc4-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19fc4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="19fc4-113">Return value</span></span>

<span data-ttu-id="19fc4-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="19fc4-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="19fc4-115">Ponteiro para uma estrutura D3DXQUATERNION que é o logaritmo natural.</span><span class="sxs-lookup"><span data-stu-id="19fc4-115">Pointer to a D3DXQUATERNION structure that is the natural logarithm.</span></span>

## <a name="remarks"></a><span data-ttu-id="19fc4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="19fc4-116">Remarks</span></span>

<span data-ttu-id="19fc4-117">A função D3DXQuaternionLn funciona apenas para os quaternions da unidade.</span><span class="sxs-lookup"><span data-stu-id="19fc4-117">The D3DXQuaternionLn function works only for unit quaternions.</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="19fc4-118">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="19fc4-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="19fc4-119">Dessa forma, a função D3DXQuaternionLn pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="19fc4-119">In this way, the D3DXQuaternionLn function can be used as a parameter for another function.</span></span>

<span data-ttu-id="19fc4-120">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="19fc4-120">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="19fc4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19fc4-121">Requirements</span></span>



| <span data-ttu-id="19fc4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="19fc4-122">Requirement</span></span> | <span data-ttu-id="19fc4-123">Valor</span><span class="sxs-lookup"><span data-stu-id="19fc4-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19fc4-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="19fc4-124">Header</span></span><br/>  | <dl> <span data-ttu-id="19fc4-125"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="19fc4-125"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="19fc4-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="19fc4-126">Library</span></span><br/> | <dl> <span data-ttu-id="19fc4-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19fc4-127"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="19fc4-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="19fc4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19fc4-129">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="19fc4-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
