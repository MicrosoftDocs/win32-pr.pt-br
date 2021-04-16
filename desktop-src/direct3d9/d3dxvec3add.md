---
description: Adiciona dois vetores 3D.
ms.assetid: 2979e291-786b-4bc9-b584-421f08db949a
title: Função D3DXVec3Add (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Add
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 16fb06c5e7b32506a94a5828fe7f5e1305afff7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772907"
---
# <a name="d3dxvec3add-function"></a><span data-ttu-id="82010-103">Função D3DXVec3Add</span><span class="sxs-lookup"><span data-stu-id="82010-103">D3DXVec3Add function</span></span>

<span data-ttu-id="82010-104">Adiciona dois vetores 3D.</span><span class="sxs-lookup"><span data-stu-id="82010-104">Adds two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="82010-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82010-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Add(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="82010-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82010-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82010-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="82010-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="82010-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="82010-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="82010-109">Ponteiro para a estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="82010-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="82010-110">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="82010-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82010-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="82010-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="82010-112">Ponteiro para uma estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="82010-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="82010-113">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="82010-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82010-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="82010-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="82010-115">Ponteiro para uma estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="82010-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82010-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="82010-116">Return value</span></span>

<span data-ttu-id="82010-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="82010-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="82010-118">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é a soma dos dois vetores 3D.</span><span class="sxs-lookup"><span data-stu-id="82010-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the sum of the two 3D vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="82010-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="82010-119">Remarks</span></span>

<span data-ttu-id="82010-120">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="82010-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="82010-121">Dessa forma, a função **D3DXVec3Add** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="82010-121">In this way, the **D3DXVec3Add** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="82010-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82010-122">Requirements</span></span>



| <span data-ttu-id="82010-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="82010-123">Requirement</span></span> | <span data-ttu-id="82010-124">Valor</span><span class="sxs-lookup"><span data-stu-id="82010-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="82010-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="82010-125">Header</span></span><br/>  | <dl> <span data-ttu-id="82010-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="82010-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="82010-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="82010-127">Library</span></span><br/> | <dl> <span data-ttu-id="82010-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82010-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="82010-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="82010-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82010-130">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="82010-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="82010-131">**D3DXVec3Subtract**</span><span class="sxs-lookup"><span data-stu-id="82010-131">**D3DXVec3Subtract**</span></span>](d3dxvec3subtract.md)
</dt> <dt>

[<span data-ttu-id="82010-132">**D3DXVec3Scale**</span><span class="sxs-lookup"><span data-stu-id="82010-132">**D3DXVec3Scale**</span></span>](d3dxvec3scale.md)
</dt> </dl>

 

 




