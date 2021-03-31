---
description: Retorna a versão normalizada de um vetor 3D.
ms.assetid: 7bb8302e-8af2-4328-9b46-bc9f5a009f56
title: Função D3DXVec3Normalize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e563b17e53ead8199de582f6dcdeb9660fa622f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012088"
---
# <a name="d3dxvec3normalize-function-d3dx9mathh"></a><span data-ttu-id="d34a3-103">Função D3DXVec3Normalize (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="d34a3-103">D3DXVec3Normalize function (D3dx9math.h)</span></span>

<span data-ttu-id="d34a3-104">Retorna a versão normalizada de um vetor 3D.</span><span class="sxs-lookup"><span data-stu-id="d34a3-104">Returns the normalized version of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="d34a3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d34a3-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Normalize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="d34a3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d34a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d34a3-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d34a3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d34a3-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="d34a3-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d34a3-109">Ponteiro para a estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="d34a3-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d34a3-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d34a3-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d34a3-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d34a3-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d34a3-112">Ponteiro para a estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="d34a3-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d34a3-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d34a3-113">Return value</span></span>

<span data-ttu-id="d34a3-114">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="d34a3-114">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d34a3-115">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é a versão normalizada do vetor especificado.</span><span class="sxs-lookup"><span data-stu-id="d34a3-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the normalized version of the specified vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="d34a3-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d34a3-116">Remarks</span></span>

<span data-ttu-id="d34a3-117">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="d34a3-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d34a3-118">Dessa forma, a função **D3DXVec3Normalize** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="d34a3-118">In this way, the **D3DXVec3Normalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d34a3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d34a3-119">Requirements</span></span>



| <span data-ttu-id="d34a3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d34a3-120">Requirement</span></span> | <span data-ttu-id="d34a3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d34a3-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d34a3-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d34a3-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d34a3-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d34a3-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d34a3-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d34a3-124">Library</span></span><br/> | <dl> <span data-ttu-id="d34a3-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d34a3-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d34a3-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d34a3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d34a3-127">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="d34a3-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




