---
description: Função D3DXPlaneFromPointNormal (D3dx9math. h) – constrói um plano de um ponto e um normal.
ms.assetid: af396bbb-09b7-492f-a25f-9c950da7e605
title: Função D3DXPlaneFromPointNormal (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e34765d150932d6a7b3b0293e603237ffb2b45ad
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098084"
---
# <a name="d3dxplanefrompointnormal-function-d3dx9mathh"></a><span data-ttu-id="328bf-103">Função D3DXPlaneFromPointNormal (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="328bf-103">D3DXPlaneFromPointNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="328bf-104">Constrói um plano de um ponto e um normal.</span><span class="sxs-lookup"><span data-stu-id="328bf-104">Constructs a plane from a point and a normal.</span></span>

## <a name="syntax"></a><span data-ttu-id="328bf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="328bf-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a><span data-ttu-id="328bf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="328bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="328bf-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="328bf-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="328bf-108">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="328bf-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="328bf-109">Ponteiro para a estrutura [**D3DXPLANE**](d3dxplane.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="328bf-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="328bf-110">*pPoint* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="328bf-110">*pPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="328bf-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="328bf-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="328bf-112">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , definindo o ponto usado para construir o plano.</span><span class="sxs-lookup"><span data-stu-id="328bf-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining the point used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="328bf-113">*pNormal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="328bf-113">*pNormal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="328bf-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="328bf-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="328bf-115">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , definindo o normal usado para construir o plano.</span><span class="sxs-lookup"><span data-stu-id="328bf-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining the normal used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="328bf-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="328bf-116">Return value</span></span>

<span data-ttu-id="328bf-117">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="328bf-117">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="328bf-118">Ponteiro para a estrutura [**D3DXPLANE**](d3dxplane.md) construída a partir do ponto e do normal.</span><span class="sxs-lookup"><span data-stu-id="328bf-118">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure constructed from the point and the normal.</span></span>

## <a name="remarks"></a><span data-ttu-id="328bf-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="328bf-119">Remarks</span></span>

<span data-ttu-id="328bf-120">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="328bf-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="328bf-121">Dessa forma, a função **D3DXPlaneFromPointNormal** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="328bf-121">In this way, the **D3DXPlaneFromPointNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="328bf-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="328bf-122">Requirements</span></span>



| <span data-ttu-id="328bf-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="328bf-123">Requirement</span></span> | <span data-ttu-id="328bf-124">Valor</span><span class="sxs-lookup"><span data-stu-id="328bf-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="328bf-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="328bf-125">Header</span></span><br/>  | <dl> <span data-ttu-id="328bf-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="328bf-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="328bf-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="328bf-127">Library</span></span><br/> | <dl> <span data-ttu-id="328bf-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="328bf-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="328bf-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="328bf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="328bf-130">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="328bf-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="328bf-131">**D3DXPlaneFromPoints**</span><span class="sxs-lookup"><span data-stu-id="328bf-131">**D3DXPlaneFromPoints**</span></span>](d3dxplanefrompoints.md)
</dt> </dl>

 

 




