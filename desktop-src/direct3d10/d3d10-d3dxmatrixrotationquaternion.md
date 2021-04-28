---
description: Função D3DXMatrixRotationQuaternion (D3DX10Math. h) – compila uma matriz de rotação de um Quaternion.
ms.assetid: dcbf8696-b959-4475-a250-6094dd5fe358
title: Função D3DXMatrixRotationQuaternion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationQuaternion
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7d95d28b7f7106df9ddfb43a9175f5c19292d52c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103424"
---
# <a name="d3dxmatrixrotationquaternion-function-d3dx10mathh"></a><span data-ttu-id="4941a-103">Função D3DXMatrixRotationQuaternion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="4941a-103">D3DXMatrixRotationQuaternion function (D3DX10Math.h)</span></span>

<span data-ttu-id="4941a-104">Cria uma matriz de rotação de um Quaternion.</span><span class="sxs-lookup"><span data-stu-id="4941a-104">Builds a rotation matrix from a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="4941a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4941a-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationQuaternion(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="4941a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4941a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4941a-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="4941a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4941a-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4941a-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4941a-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="4941a-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4941a-110">*pQ* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4941a-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4941a-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="4941a-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4941a-112">Ponteiro para a estrutura de D3DXQUATERNION de origem.</span><span class="sxs-lookup"><span data-stu-id="4941a-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4941a-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4941a-113">Return value</span></span>

<span data-ttu-id="4941a-114">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4941a-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4941a-115">Ponteiro para uma estrutura D3DXMATRIX criada a partir do Quaternion de origem.</span><span class="sxs-lookup"><span data-stu-id="4941a-115">Pointer to a D3DXMATRIX structure built from the source quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="4941a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4941a-116">Remarks</span></span>

<span data-ttu-id="4941a-117">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="4941a-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="4941a-118">Dessa forma, a função D3DXMatrixRotationQuaternion pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="4941a-118">In this way, the D3DXMatrixRotationQuaternion function can be used as a parameter for another function.</span></span>

<span data-ttu-id="4941a-119">Para obter informações sobre como calcular valores de Quaternion de um vetor de direção (x, y, z) e um ângulo de rotação, consulte [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span><span class="sxs-lookup"><span data-stu-id="4941a-119">For information about how to calculate quaternion values from a direction vector ( x, y, z ) and an angle of rotation, see [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4941a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4941a-120">Requirements</span></span>



| <span data-ttu-id="4941a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4941a-121">Requirement</span></span> | <span data-ttu-id="4941a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4941a-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4941a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4941a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4941a-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4941a-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="4941a-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4941a-125">Library</span></span><br/> | <dl> <span data-ttu-id="4941a-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4941a-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4941a-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4941a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4941a-128">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="4941a-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
