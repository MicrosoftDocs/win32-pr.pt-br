---
description: Cria uma matriz de rotação de um Quaternion.
ms.assetid: e590058c-772b-4eef-aab0-a12bb04c299a
title: Função D3DXMatrixRotationQuaternion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 275a369da106e9f114ce47286f0f6ea9ce381ecb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105752147"
---
# <a name="d3dxmatrixrotationquaternion-function-d3dx9mathh"></a><span data-ttu-id="a421e-103">Função D3DXMatrixRotationQuaternion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a421e-103">D3DXMatrixRotationQuaternion function (D3dx9math.h)</span></span>

<span data-ttu-id="a421e-104">Cria uma matriz de rotação de um Quaternion.</span><span class="sxs-lookup"><span data-stu-id="a421e-104">Builds a rotation matrix from a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="a421e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a421e-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationQuaternion(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="a421e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a421e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a421e-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="a421e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a421e-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a421e-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a421e-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="a421e-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a421e-110">*pQ* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a421e-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a421e-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="a421e-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a421e-112">Ponteiro para a estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="a421e-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a421e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a421e-113">Return value</span></span>

<span data-ttu-id="a421e-114">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a421e-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a421e-115">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) criada a partir do Quaternion de origem.</span><span class="sxs-lookup"><span data-stu-id="a421e-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure built from the source quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="a421e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a421e-116">Remarks</span></span>

<span data-ttu-id="a421e-117">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="a421e-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a421e-118">Dessa forma, a função **D3DXMatrixRotationQuaternion** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="a421e-118">In this way, the **D3DXMatrixRotationQuaternion** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="a421e-119">Para obter informações sobre como calcular valores de Quaternion de um vetor de direção (x, y, z) e um ângulo de rotação, consulte [**D3DXQUATERNION**](d3dxquaternion.md).</span><span class="sxs-lookup"><span data-stu-id="a421e-119">For information about how to calculate quaternion values from a direction vector ( x, y, z ) and an angle of rotation, see [**D3DXQUATERNION**](d3dxquaternion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a421e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a421e-120">Requirements</span></span>



| <span data-ttu-id="a421e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a421e-121">Requirement</span></span> | <span data-ttu-id="a421e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a421e-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a421e-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a421e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a421e-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a421e-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a421e-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a421e-125">Library</span></span><br/> | <dl> <span data-ttu-id="a421e-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a421e-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a421e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="a421e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a421e-128">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="a421e-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a421e-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="a421e-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="a421e-130">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="a421e-130">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="a421e-131">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="a421e-131">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="a421e-132">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="a421e-132">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="a421e-133">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="a421e-133">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 




