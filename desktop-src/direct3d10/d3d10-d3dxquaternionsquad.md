---
description: Interpola entre quaternions, usando interpolação de Quadrangle esférica.
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
ms.openlocfilehash: af2bb582909cf09a4044b293f3f298a5da2335a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506509"
---
# <a name="d3dxquaternionsquad-function-d3dx10mathh"></a><span data-ttu-id="d6ed3-103">Função D3DXQuaternionSquad (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d6ed3-103">D3DXQuaternionSquad function (D3DX10Math.h)</span></span>

<span data-ttu-id="d6ed3-104">Interpola entre quaternions, usando interpolação de Quadrangle esférica.</span><span class="sxs-lookup"><span data-stu-id="d6ed3-104">Interpolates between quaternions, using spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6ed3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6ed3-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="d6ed3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6ed3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6ed3-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d6ed3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ed3-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="d6ed3-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d6ed3-109">Ponteiro para o [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="d6ed3-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d6ed3-110">*pQ1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d6ed3-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ed3-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6ed3-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d6ed3-112">Ponteiro para uma estrutura de D3DXQUATERNION de origem.</span><span class="sxs-lookup"><span data-stu-id="d6ed3-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="d6ed3-113">*PA* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d6ed3-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ed3-114">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6ed3-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d6ed3-115">Ponteiro para uma estrutura de D3DXQUATERNION de origem.</span><span class="sxs-lookup"><span data-stu-id="d6ed3-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="d6ed3-116">*PB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d6ed3-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ed3-117">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6ed3-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d6ed3-118">Ponteiro para uma estrutura de D3DXQUATERNION de origem.</span><span class="sxs-lookup"><span data-stu-id="d6ed3-118">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="d6ed3-119">*PC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d6ed3-119">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ed3-120">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6ed3-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d6ed3-121">Ponteiro para uma estrutura de D3DXQUATERNION de origem.</span><span class="sxs-lookup"><span data-stu-id="d6ed3-121">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="d6ed3-122">*t* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="d6ed3-122">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ed3-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6ed3-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6ed3-124">Parâmetro que indica a interpolarização entre os quaternions.</span><span class="sxs-lookup"><span data-stu-id="d6ed3-124">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6ed3-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d6ed3-125">Return value</span></span>

<span data-ttu-id="d6ed3-126">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="d6ed3-126">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d6ed3-127">Ponteiro para uma estrutura D3DXQUATERNION que é o resultado da interpolação quadrangle esférica.</span><span class="sxs-lookup"><span data-stu-id="d6ed3-127">Pointer to a D3DXQUATERNION structure that is the result of the spherical quadrangle interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6ed3-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6ed3-128">Remarks</span></span>

<span data-ttu-id="d6ed3-129">Essa função usa a seguinte sequência de operações de interpolação linear esférica:</span><span class="sxs-lookup"><span data-stu-id="d6ed3-129">This function uses the following sequence of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



<span data-ttu-id="d6ed3-130">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="d6ed3-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d6ed3-131">Dessa forma, a função D3DXQuaternionSquad pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="d6ed3-131">In this way, the D3DXQuaternionSquad function can be used as a parameter for another function.</span></span>

<span data-ttu-id="d6ed3-132">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="d6ed3-132">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6ed3-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6ed3-133">Requirements</span></span>



| <span data-ttu-id="d6ed3-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6ed3-134">Requirement</span></span> | <span data-ttu-id="d6ed3-135">Valor</span><span class="sxs-lookup"><span data-stu-id="d6ed3-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6ed3-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6ed3-136">Header</span></span><br/>  | <dl> <span data-ttu-id="d6ed3-137"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6ed3-137"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d6ed3-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d6ed3-138">Library</span></span><br/> | <dl> <span data-ttu-id="d6ed3-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6ed3-139"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d6ed3-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6ed3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6ed3-141">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="d6ed3-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
