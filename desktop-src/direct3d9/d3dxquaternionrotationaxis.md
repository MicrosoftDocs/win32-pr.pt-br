---
description: Gira um Quaternion sobre um eixo arbitrário.
ms.assetid: 9ff0fe2c-54d6-482c-84e1-f38e3c57d8dd
title: Função D3DXQuaternionRotationAxis (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationAxis
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7974a1199c468ac762042ae41af59f5a3b66bafd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771476"
---
# <a name="d3dxquaternionrotationaxis-function-d3dx9mathh"></a><span data-ttu-id="fe44f-103">Função D3DXQuaternionRotationAxis (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="fe44f-103">D3DXQuaternionRotationAxis function (D3dx9math.h)</span></span>

<span data-ttu-id="fe44f-104">Gira um Quaternion sobre um eixo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="fe44f-104">Rotates a quaternion about an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe44f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe44f-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationAxis(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_          FLOAT          Angle
);
```



## <a name="parameters"></a><span data-ttu-id="fe44f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe44f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe44f-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="fe44f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe44f-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="fe44f-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fe44f-109">Ponteiro para a estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="fe44f-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fe44f-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fe44f-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe44f-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="fe44f-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fe44f-112">Ponteiro para a estrutura [**D3DXVECTOR3**](d3dxvector3.md) que identifica o eixo sobre o qual girar o Quaternion.</span><span class="sxs-lookup"><span data-stu-id="fe44f-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that identifies the axis about which to rotate the quaternion.</span></span>

</dd> <dt>

<span data-ttu-id="fe44f-113">*Ângulo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fe44f-113">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe44f-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe44f-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe44f-115">Ângulo de rotação, em radianos.</span><span class="sxs-lookup"><span data-stu-id="fe44f-115">Angle of rotation, in radians.</span></span> <span data-ttu-id="fe44f-116">Os ângulos são medidos no sentido horário olhando ao longo do eixo de rotação em direção à origem.</span><span class="sxs-lookup"><span data-stu-id="fe44f-116">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe44f-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fe44f-117">Return value</span></span>

<span data-ttu-id="fe44f-118">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="fe44f-118">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fe44f-119">Ponteiro para uma estrutura [**D3DXQUATERNION**](d3dxquaternion.md) girado em volta do eixo especificado.</span><span class="sxs-lookup"><span data-stu-id="fe44f-119">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe44f-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe44f-120">Remarks</span></span>

<span data-ttu-id="fe44f-121">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="fe44f-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="fe44f-122">Dessa forma, a função **D3DXQuaternionRotationAxis** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="fe44f-122">In this way, the **D3DXQuaternionRotationAxis** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="fe44f-123">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="fe44f-123">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe44f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe44f-124">Requirements</span></span>



| <span data-ttu-id="fe44f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe44f-125">Requirement</span></span> | <span data-ttu-id="fe44f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="fe44f-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe44f-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe44f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="fe44f-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe44f-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fe44f-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fe44f-129">Library</span></span><br/> | <dl> <span data-ttu-id="fe44f-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe44f-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fe44f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe44f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe44f-132">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="fe44f-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="fe44f-133">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="fe44f-133">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
</dt> <dt>

[<span data-ttu-id="fe44f-134">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="fe44f-134">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3dxquaternionrotationyawpitchroll.md)
</dt> </dl>

 

 
