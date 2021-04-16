---
description: Constrói um plano de um ponto e um normal.
ms.assetid: 93c644d2-ab8c-47a1-9a3b-8b9c6a13178b
title: Função D3DXPlaneFromPointNormal (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPointNormal
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9900a9f6838e253bd195374d00f90ee31fae07a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772719"
---
# <a name="d3dxplanefrompointnormal-function-d3dx10mathh"></a><span data-ttu-id="19abe-103">Função D3DXPlaneFromPointNormal (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="19abe-103">D3DXPlaneFromPointNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="19abe-104">Constrói um plano de um ponto e um normal.</span><span class="sxs-lookup"><span data-stu-id="19abe-104">Constructs a plane from a point and a normal.</span></span>

## <a name="syntax"></a><span data-ttu-id="19abe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19abe-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a><span data-ttu-id="19abe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19abe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19abe-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="19abe-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="19abe-108">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="19abe-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="19abe-109">Ponteiro para o [**D3DXPLANE**](d3d10-d3dxplane.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="19abe-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="19abe-110">*pPoint* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19abe-110">*pPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19abe-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="19abe-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="19abe-112">Ponteiro para um [**D3DXVECTOR3**](d3d10-d3dxvector3.md), definindo o ponto usado para construir o plano.</span><span class="sxs-lookup"><span data-stu-id="19abe-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), defining the point used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="19abe-113">*pNormal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19abe-113">*pNormal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19abe-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="19abe-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="19abe-115">Ponteiro para uma estrutura D3DXVECTOR3, definindo o normal usado para construir o plano.</span><span class="sxs-lookup"><span data-stu-id="19abe-115">Pointer to a D3DXVECTOR3 structure, defining the normal used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19abe-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="19abe-116">Return value</span></span>

<span data-ttu-id="19abe-117">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="19abe-117">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="19abe-118">Ponteiro para a estrutura D3DXPLANE construída a partir do ponto e do normal.</span><span class="sxs-lookup"><span data-stu-id="19abe-118">Pointer to the D3DXPLANE structure constructed from the point and the normal.</span></span>

## <a name="remarks"></a><span data-ttu-id="19abe-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="19abe-119">Remarks</span></span>

<span data-ttu-id="19abe-120">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="19abe-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="19abe-121">Dessa forma, a função D3DXPlaneFromPointNormal pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="19abe-121">In this way, the D3DXPlaneFromPointNormal function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="19abe-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19abe-122">Requirements</span></span>



| <span data-ttu-id="19abe-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="19abe-123">Requirement</span></span> | <span data-ttu-id="19abe-124">Valor</span><span class="sxs-lookup"><span data-stu-id="19abe-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19abe-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="19abe-125">Header</span></span><br/>  | <dl> <span data-ttu-id="19abe-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="19abe-126"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="19abe-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="19abe-127">Library</span></span><br/> | <dl> <span data-ttu-id="19abe-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19abe-128"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="19abe-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="19abe-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19abe-130">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="19abe-130">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
