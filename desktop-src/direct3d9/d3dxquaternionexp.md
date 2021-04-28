---
description: Função D3DXQuaternionExp (D3dx9math. h) – calcula o exponencial.
ms.assetid: 648aeaf1-ead3-4b21-819f-cd2a70881a13
title: Função D3DXQuaternionExp (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 30e48e21e2dc6af487f1fb076af3b3f2df57f9f3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094094"
---
# <a name="d3dxquaternionexp-function-d3dx9mathh"></a><span data-ttu-id="fdd91-103">Função D3DXQuaternionExp (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="fdd91-103">D3DXQuaternionExp function (D3dx9math.h)</span></span>

<span data-ttu-id="fdd91-104">Calcula o exponencial.</span><span class="sxs-lookup"><span data-stu-id="fdd91-104">Calculates the exponential.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdd91-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fdd91-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionExp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="fdd91-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fdd91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdd91-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="fdd91-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fdd91-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="fdd91-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fdd91-109">Ponteiro para a estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="fdd91-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fdd91-110">*pQ* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fdd91-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdd91-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="fdd91-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fdd91-112">Ponteiro para a estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="fdd91-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdd91-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fdd91-113">Return value</span></span>

<span data-ttu-id="fdd91-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="fdd91-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fdd91-115">Ponteiro para uma estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o exponencial.</span><span class="sxs-lookup"><span data-stu-id="fdd91-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the exponential.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdd91-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="fdd91-116">Remarks</span></span>

<span data-ttu-id="fdd91-117">Esse método converte um Quaternion puro em uma unidade Quaternion.</span><span class="sxs-lookup"><span data-stu-id="fdd91-117">This method converts a pure quaternion to a unit quaternion.</span></span> <span data-ttu-id="fdd91-118">**D3DXQuaternionExp** espera um Quaternion puro, em que w é ignorado no cálculo (w = = 0).</span><span class="sxs-lookup"><span data-stu-id="fdd91-118">**D3DXQuaternionExp** expects a pure quaternion, where w is ignored in the calculation (w == 0).</span></span>


```
Given a pure quaternion defined by:
q = (0, theta * v); 
    
This method calculates the exponential result.
exp(Q) = (cos(theta), sin(theta) * v)
```



<span data-ttu-id="fdd91-119">em que v é a parte de vetor de um Quaternion.</span><span class="sxs-lookup"><span data-stu-id="fdd91-119">where v is the vector portion of a quaternion.</span></span>

<span data-ttu-id="fdd91-120">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="fdd91-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="fdd91-121">Dessa forma, a função **D3DXQuaternionExp** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="fdd91-121">In this way, the **D3DXQuaternionExp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="fdd91-122">O método [**D3DXQuaternionSquadSetup**](d3dxquaternionsquadsetup.md) também pode ser usado para configurar os pontos de controle de um Quaternion.</span><span class="sxs-lookup"><span data-stu-id="fdd91-122">The [**D3DXQuaternionSquadSetup**](d3dxquaternionsquadsetup.md) method can also be used to set up the control points of a quaternion.</span></span>

<span data-ttu-id="fdd91-123">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="fdd91-123">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdd91-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdd91-124">Requirements</span></span>



| <span data-ttu-id="fdd91-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdd91-125">Requirement</span></span> | <span data-ttu-id="fdd91-126">Valor</span><span class="sxs-lookup"><span data-stu-id="fdd91-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdd91-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fdd91-127">Header</span></span><br/>  | <dl> <span data-ttu-id="fdd91-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdd91-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fdd91-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fdd91-129">Library</span></span><br/> | <dl> <span data-ttu-id="fdd91-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fdd91-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fdd91-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fdd91-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdd91-132">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="fdd91-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="fdd91-133">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="fdd91-133">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
</dt> <dt>

[<span data-ttu-id="fdd91-134">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="fdd91-134">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




