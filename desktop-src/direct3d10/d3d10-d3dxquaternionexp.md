---
description: Calcula o exponencial.
ms.assetid: bd70c432-ac61-4c38-b10b-3b103e49ead8
title: Função D3DXQuaternionExp (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionExp
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d00292cc073679e3e90c2470630ba1851d0d3cd8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664047"
---
# <a name="d3dxquaternionexp-function-d3dx10mathh"></a><span data-ttu-id="14803-103">Função D3DXQuaternionExp (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="14803-103">D3DXQuaternionExp function (D3DX10Math.h)</span></span>

<span data-ttu-id="14803-104">Calcula o exponencial.</span><span class="sxs-lookup"><span data-stu-id="14803-104">Calculates the exponential.</span></span>

## <a name="syntax"></a><span data-ttu-id="14803-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14803-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionExp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="14803-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14803-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14803-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="14803-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="14803-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="14803-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="14803-109">Ponteiro para o [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="14803-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="14803-110">*pQ* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14803-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14803-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="14803-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="14803-112">Ponteiro para a estrutura de D3DXQUATERNION de origem.</span><span class="sxs-lookup"><span data-stu-id="14803-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14803-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14803-113">Return value</span></span>

<span data-ttu-id="14803-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="14803-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="14803-115">Ponteiro para uma estrutura D3DXQUATERNION que é o exponencial.</span><span class="sxs-lookup"><span data-stu-id="14803-115">Pointer to a D3DXQUATERNION structure that is the exponential.</span></span>

## <a name="remarks"></a><span data-ttu-id="14803-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="14803-116">Remarks</span></span>

<span data-ttu-id="14803-117">Esse método converte um Quaternion puro em uma unidade Quaternion.</span><span class="sxs-lookup"><span data-stu-id="14803-117">This method converts a pure quaternion to a unit quaternion.</span></span> <span data-ttu-id="14803-118">D3DXQuaternionExp espera um Quaternion puro, em que w é ignorado no cálculo (w = = 0).</span><span class="sxs-lookup"><span data-stu-id="14803-118">D3DXQuaternionExp expects a pure quaternion, where w is ignored in the calculation (w == 0).</span></span>


```
Given a pure quaternion defined by:
q = (0, theta * v); 
    
This method calculates the exponential result.
exp(Q) = (cos(theta), sin(theta) * v)
```



<span data-ttu-id="14803-119">em que v é a parte de vetor de um Quaternion.</span><span class="sxs-lookup"><span data-stu-id="14803-119">where v is the vector portion of a quaternion.</span></span>

<span data-ttu-id="14803-120">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="14803-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="14803-121">Dessa forma, a função D3DXQuaternionExp pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="14803-121">In this way, the D3DXQuaternionExp function can be used as a parameter for another function.</span></span>

<span data-ttu-id="14803-122">O método [**D3DXQuaternionSquadSetup**](d3d10-d3dxquaternionsquadsetup.md) também pode ser usado para configurar os pontos de controle de um Quaternion.</span><span class="sxs-lookup"><span data-stu-id="14803-122">The [**D3DXQuaternionSquadSetup**](d3d10-d3dxquaternionsquadsetup.md) method can also be used to set up the control points of a quaternion.</span></span>

<span data-ttu-id="14803-123">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="14803-123">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="14803-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14803-124">Requirements</span></span>



| <span data-ttu-id="14803-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="14803-125">Requirement</span></span> | <span data-ttu-id="14803-126">Valor</span><span class="sxs-lookup"><span data-stu-id="14803-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14803-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="14803-127">Header</span></span><br/>  | <dl> <span data-ttu-id="14803-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="14803-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="14803-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="14803-129">Library</span></span><br/> | <dl> <span data-ttu-id="14803-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14803-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="14803-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="14803-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14803-132">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="14803-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
