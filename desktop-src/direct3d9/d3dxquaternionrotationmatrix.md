---
description: Cria um Quaternion a partir de uma matriz de rotação.
ms.assetid: 4fafb1aa-5d6f-46e6-84b1-e0bac22952d2
title: Função D3DXQuaternionRotationMatrix (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationMatrix
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0a9513c9aededdd06080db97aac78278986244b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298577"
---
# <a name="d3dxquaternionrotationmatrix-function-d3dx9mathh"></a><span data-ttu-id="e843d-103">Função D3DXQuaternionRotationMatrix (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="e843d-103">D3DXQuaternionRotationMatrix function (D3dx9math.h)</span></span>

<span data-ttu-id="e843d-104">Cria um Quaternion a partir de uma matriz de rotação.</span><span class="sxs-lookup"><span data-stu-id="e843d-104">Builds a quaternion from a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e843d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e843d-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationMatrix(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="e843d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e843d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e843d-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e843d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e843d-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e843d-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e843d-109">Ponteiro para a estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="e843d-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e843d-110">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e843d-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e843d-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e843d-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e843d-112">Ponteiro para a estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="e843d-112">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e843d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e843d-113">Return value</span></span>

<span data-ttu-id="e843d-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e843d-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e843d-115">Ponteiro para a estrutura [**D3DXQUATERNION**](d3dxquaternion.md) criada a partir de uma matriz de rotação.</span><span class="sxs-lookup"><span data-stu-id="e843d-115">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure built from a rotation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="e843d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e843d-116">Remarks</span></span>

<span data-ttu-id="e843d-117">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="e843d-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e843d-118">Dessa forma, a função **D3DXQuaternionRotationMatrix** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="e843d-118">In this way, the **D3DXQuaternionRotationMatrix** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="e843d-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="e843d-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="e843d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e843d-120">Requirements</span></span>



| <span data-ttu-id="e843d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e843d-121">Requirement</span></span> | <span data-ttu-id="e843d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e843d-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e843d-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e843d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e843d-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e843d-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e843d-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e843d-125">Library</span></span><br/> | <dl> <span data-ttu-id="e843d-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e843d-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e843d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="e843d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e843d-128">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="e843d-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e843d-129">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="e843d-129">**D3DXQuaternionRotationAxis**</span></span>](d3dxquaternionrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="e843d-130">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="e843d-130">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3dxquaternionrotationyawpitchroll.md)
</dt> </dl>

 

 




