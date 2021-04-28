---
description: Função D3DXVec3Normalize (D3DX10Math. h) – retorna a versão normalizada de um vetor 3D.
ms.assetid: 420321a2-0c3b-419c-9620-acf184e7b4f0
title: Função D3DXVec3Normalize (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Normalize
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 3f1317b1b8887b9ff306fcaed2cb6da2d077010f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108174"
---
# <a name="d3dxvec3normalize-function-d3dx10mathh"></a><span data-ttu-id="6e935-103">Função D3DXVec3Normalize (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="6e935-103">D3DXVec3Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="6e935-104">Retorna a versão normalizada de um vetor 3D.</span><span class="sxs-lookup"><span data-stu-id="6e935-104">Returns the normalized version of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e935-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e935-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Normalize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="6e935-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e935-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e935-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="6e935-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e935-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6e935-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="6e935-109">Ponteiro para o [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="6e935-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6e935-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6e935-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e935-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6e935-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="6e935-112">Ponteiro para a estrutura de D3DXVECTOR3 de origem.</span><span class="sxs-lookup"><span data-stu-id="6e935-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e935-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6e935-113">Return value</span></span>

<span data-ttu-id="6e935-114">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6e935-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="6e935-115">Ponteiro para uma estrutura D3DXVECTOR3 que é a versão normalizada do vetor especificado.</span><span class="sxs-lookup"><span data-stu-id="6e935-115">Pointer to a D3DXVECTOR3 structure that is the normalized version of the specified vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e935-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e935-116">Remarks</span></span>

<span data-ttu-id="6e935-117">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="6e935-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="6e935-118">Dessa forma, a função D3DXVec3Normalize pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="6e935-118">In this way, the D3DXVec3Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e935-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e935-119">Requirements</span></span>



| <span data-ttu-id="6e935-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e935-120">Requirement</span></span> | <span data-ttu-id="6e935-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6e935-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e935-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e935-122">Header</span></span><br/> | <dl> <span data-ttu-id="6e935-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e935-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e935-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6e935-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e935-125">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="6e935-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
