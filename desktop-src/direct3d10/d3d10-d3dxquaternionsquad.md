---
description: Função D3DXQuaternionSquad (D3DX10Math. h) – interpola entre quaternions, usando a interpolação de Quadrangle esférica.
ms.assetid: ba953731-4372-4b32-942b-23abfe479704
title: Função D3DXQuaternionSquad (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquad
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9671b2a161124228c264da7eac0a2aa3a915ff95
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108754"
---
# <a name="d3dxquaternionsquad-function-d3dx10mathh"></a><span data-ttu-id="7e09b-103">Função D3DXQuaternionSquad (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="7e09b-103">D3DXQuaternionSquad function (D3DX10Math.h)</span></span>

<span data-ttu-id="7e09b-104">Interpola entre quaternions, usando interpolação de Quadrangle esférica.</span><span class="sxs-lookup"><span data-stu-id="7e09b-104">Interpolates between quaternions, using spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e09b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e09b-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSquad(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pA,
  _In_    const D3DXQUATERNION *pB,
  _In_    const D3DXQUATERNION *pC,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="7e09b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e09b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e09b-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="7e09b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e09b-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="7e09b-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7e09b-109">Ponteiro para o [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="7e09b-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7e09b-110">*pQ1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e09b-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e09b-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="7e09b-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7e09b-112">Ponteiro para uma estrutura de D3DXQUATERNION de origem.</span><span class="sxs-lookup"><span data-stu-id="7e09b-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="7e09b-113">*PA* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e09b-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e09b-114">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="7e09b-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7e09b-115">Ponteiro para uma estrutura de D3DXQUATERNION de origem.</span><span class="sxs-lookup"><span data-stu-id="7e09b-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="7e09b-116">*PB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e09b-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e09b-117">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="7e09b-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7e09b-118">Ponteiro para uma estrutura de D3DXQUATERNION de origem.</span><span class="sxs-lookup"><span data-stu-id="7e09b-118">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="7e09b-119">*PC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e09b-119">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e09b-120">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="7e09b-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7e09b-121">Ponteiro para uma estrutura de D3DXQUATERNION de origem.</span><span class="sxs-lookup"><span data-stu-id="7e09b-121">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="7e09b-122">*t* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="7e09b-122">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e09b-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7e09b-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7e09b-124">Parâmetro que indica a interpolarização entre os quaternions.</span><span class="sxs-lookup"><span data-stu-id="7e09b-124">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e09b-125">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7e09b-125">Return value</span></span>

<span data-ttu-id="7e09b-126">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="7e09b-126">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7e09b-127">Ponteiro para uma estrutura D3DXQUATERNION que é o resultado da interpolação quadrangle esférica.</span><span class="sxs-lookup"><span data-stu-id="7e09b-127">Pointer to a D3DXQUATERNION structure that is the result of the spherical quadrangle interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e09b-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e09b-128">Remarks</span></span>

<span data-ttu-id="7e09b-129">Essa função usa a seguinte sequência de operações de interpolação linear esférica:</span><span class="sxs-lookup"><span data-stu-id="7e09b-129">This function uses the following sequence of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



<span data-ttu-id="7e09b-130">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="7e09b-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="7e09b-131">Dessa forma, a função D3DXQuaternionSquad pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="7e09b-131">In this way, the D3DXQuaternionSquad function can be used as a parameter for another function.</span></span>

<span data-ttu-id="7e09b-132">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="7e09b-132">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e09b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e09b-133">Requirements</span></span>



| <span data-ttu-id="7e09b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e09b-134">Requirement</span></span> | <span data-ttu-id="7e09b-135">Valor</span><span class="sxs-lookup"><span data-stu-id="7e09b-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e09b-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7e09b-136">Header</span></span><br/>  | <dl> <span data-ttu-id="7e09b-137"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e09b-137"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="7e09b-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7e09b-138">Library</span></span><br/> | <dl> <span data-ttu-id="7e09b-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e09b-139"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7e09b-140">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7e09b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e09b-141">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="7e09b-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
