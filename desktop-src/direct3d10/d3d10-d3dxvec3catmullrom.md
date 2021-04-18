---
description: Executa uma interpolação de Catmull-Rom, usando os vetores 3D especificados.
ms.assetid: 324bd4b5-b0df-4dd3-b370-3c365c9f2db1
title: Função D3DXVec3CatmullRom (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3CatmullRom
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 70c6f605358bfc561e3e630fa4e4e1b87c455768
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105750088"
---
# <a name="d3dxvec3catmullrom-function-d3dx10mathh"></a><span data-ttu-id="f21a4-103">Função D3DXVec3CatmullRom (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="f21a4-103">D3DXVec3CatmullRom function (D3DX10Math.h)</span></span>

<span data-ttu-id="f21a4-104">Executa uma interpolação de Catmull-Rom, usando os vetores 3D especificados.</span><span class="sxs-lookup"><span data-stu-id="f21a4-104">Performs a Catmull-Rom interpolation, using the specified 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="f21a4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f21a4-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3CatmullRom(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV0,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="f21a4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f21a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f21a4-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f21a4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f21a4-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="f21a4-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="f21a4-109">Ponteiro para o [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="f21a4-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f21a4-110">*pV0* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f21a4-110">*pV0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f21a4-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f21a4-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="f21a4-112">Ponteiro para uma estrutura de D3DXVECTOR3 de origem, um vetor de posição.</span><span class="sxs-lookup"><span data-stu-id="f21a4-112">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="f21a4-113">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f21a4-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f21a4-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f21a4-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="f21a4-115">Ponteiro para uma estrutura de D3DXVECTOR3 de origem, um vetor de posição.</span><span class="sxs-lookup"><span data-stu-id="f21a4-115">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="f21a4-116">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f21a4-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f21a4-117">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f21a4-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="f21a4-118">Ponteiro para uma estrutura de D3DXVECTOR3 de origem, um vetor de posição.</span><span class="sxs-lookup"><span data-stu-id="f21a4-118">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="f21a4-119">*pV3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f21a4-119">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f21a4-120">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f21a4-120">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="f21a4-121">Ponteiro para uma estrutura de D3DXVECTOR3 de origem, um vetor de posição.</span><span class="sxs-lookup"><span data-stu-id="f21a4-121">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="f21a4-122">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="f21a4-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f21a4-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f21a4-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f21a4-124">Fator de ponderação.</span><span class="sxs-lookup"><span data-stu-id="f21a4-124">Weighting factor.</span></span> <span data-ttu-id="f21a4-125">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="f21a4-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f21a4-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f21a4-126">Return value</span></span>

<span data-ttu-id="f21a4-127">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="f21a4-127">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="f21a4-128">Ponteiro para uma estrutura D3DXVECTOR3 que é o resultado da interpolação de Catmull-Rom.</span><span class="sxs-lookup"><span data-stu-id="f21a4-128">Pointer to a D3DXVECTOR3 structure that is the result of the Catmull-Rom interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="f21a4-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="f21a4-129">Remarks</span></span>

<span data-ttu-id="f21a4-130">Considerando quatro pontos (P1, P2, P3, P4), encontre uma função Q (s) de modo que:</span><span class="sxs-lookup"><span data-stu-id="f21a4-130">Given four points (p1, p2, p3, p4), find a function Q(s) such that:</span></span>


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



<span data-ttu-id="f21a4-131">O Catmull-Rom spline pode ser derivado do spline Hermite por meio da configuração:</span><span class="sxs-lookup"><span data-stu-id="f21a4-131">The Catmull-Rom spline can be derived from the Hermite spline by setting:</span></span>


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



<span data-ttu-id="f21a4-132">onde:</span><span class="sxs-lookup"><span data-stu-id="f21a4-132">where:</span></span>

<span data-ttu-id="f21a4-133">v1 é o conteúdo de pV0.</span><span class="sxs-lookup"><span data-stu-id="f21a4-133">v1 is the contents of pV0.</span></span>

<span data-ttu-id="f21a4-134">V2 é o conteúdo de pV1.</span><span class="sxs-lookup"><span data-stu-id="f21a4-134">v2 is the contents of pV1.</span></span>

<span data-ttu-id="f21a4-135">P3 é o conteúdo de pV2.</span><span class="sxs-lookup"><span data-stu-id="f21a4-135">p3 is the contents of pV2.</span></span>

<span data-ttu-id="f21a4-136">P4 é o conteúdo de pV3.</span><span class="sxs-lookup"><span data-stu-id="f21a4-136">p4 is the contents of pV3.</span></span>

<span data-ttu-id="f21a4-137">Usando a equação de spline Hermite:</span><span class="sxs-lookup"><span data-stu-id="f21a4-137">Using the Hermite spline equation:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



<span data-ttu-id="f21a4-138">e a substituição para v1, v2, T1, T2 produz:</span><span class="sxs-lookup"><span data-stu-id="f21a4-138">and substituting for v1, v2, t1, t2 yields:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2) / 2
```



<span data-ttu-id="f21a4-139">Isso pode ser reorganizado como:</span><span class="sxs-lookup"><span data-stu-id="f21a4-139">This can be rearranged as:</span></span>


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a><span data-ttu-id="f21a4-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f21a4-140">Requirements</span></span>



| <span data-ttu-id="f21a4-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="f21a4-141">Requirement</span></span> | <span data-ttu-id="f21a4-142">Valor</span><span class="sxs-lookup"><span data-stu-id="f21a4-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f21a4-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f21a4-143">Header</span></span><br/> | <dl> <span data-ttu-id="f21a4-144"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f21a4-144"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f21a4-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="f21a4-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f21a4-146">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="f21a4-146">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
