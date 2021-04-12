---
description: Computa o produto de ponto de um plano e um vetor 3D. Presume-se que o parâmetro w do vetor seja 1.
ms.assetid: 634de6bc-b631-493d-a7a6-292a3c3253d6
title: Função D3DXPlaneDotCoord (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 99ee9db7df541dcf74867b828a73ede80f11e22b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172922"
---
# <a name="d3dxplanedotcoord-function"></a><span data-ttu-id="605d3-104">Função D3DXPlaneDotCoord</span><span class="sxs-lookup"><span data-stu-id="605d3-104">D3DXPlaneDotCoord function</span></span>

<span data-ttu-id="605d3-105">Computa o produto de ponto de um plano e um vetor 3D.</span><span class="sxs-lookup"><span data-stu-id="605d3-105">Computes the dot product of a plane and a 3D vector.</span></span> <span data-ttu-id="605d3-106">Presume-se que o parâmetro w do vetor seja 1.</span><span class="sxs-lookup"><span data-stu-id="605d3-106">The w parameter of the vector is assumed to be 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="605d3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="605d3-107">Syntax</span></span>


```C++
FLOAT D3DXPlaneDotCoord(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="605d3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="605d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="605d3-109">*PP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="605d3-109">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="605d3-110">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="605d3-110">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="605d3-111">Ponteiro para uma estrutura de [**D3DXPLANE**](d3dxplane.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="605d3-111">Pointer to a source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="605d3-112">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="605d3-112">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="605d3-113">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="605d3-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="605d3-114">Ponteiro para uma estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="605d3-114">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="605d3-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="605d3-115">Return value</span></span>

<span data-ttu-id="605d3-116">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="605d3-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="605d3-117">O produto de ponto do plano e do vetor 3D.</span><span class="sxs-lookup"><span data-stu-id="605d3-117">The dot product of the plane and 3D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="605d3-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="605d3-118">Remarks</span></span>

<span data-ttu-id="605d3-119">Dado um plano (a, b, c, d) e um vetor 3D (x, y, z) o valor de retorno dessa função é um \* x + b \* y + c \* z + d \* 1.</span><span class="sxs-lookup"><span data-stu-id="605d3-119">Given a plane (a, b, c, d) and a 3D vector (x, y, z) the return value of this function is a\*x + b\*y + c\*z + d\*1.</span></span> <span data-ttu-id="605d3-120">A função **D3DXPlaneDotCoord** é útil para determinar a relação do plano com uma coordenada no espaço 3D.</span><span class="sxs-lookup"><span data-stu-id="605d3-120">The **D3DXPlaneDotCoord** function is useful for determining the plane's relationship with a coordinate in 3D space.</span></span>

## <a name="requirements"></a><span data-ttu-id="605d3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="605d3-121">Requirements</span></span>



| <span data-ttu-id="605d3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="605d3-122">Requirement</span></span> | <span data-ttu-id="605d3-123">Valor</span><span class="sxs-lookup"><span data-stu-id="605d3-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="605d3-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="605d3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="605d3-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="605d3-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="605d3-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="605d3-126">Library</span></span><br/> | <dl> <span data-ttu-id="605d3-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="605d3-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="605d3-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="605d3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="605d3-129">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="605d3-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="605d3-130">**D3DXPlaneDot**</span><span class="sxs-lookup"><span data-stu-id="605d3-130">**D3DXPlaneDot**</span></span>](d3dxplanedot.md)
</dt> <dt>

[<span data-ttu-id="605d3-131">**D3DXPlaneDotNormal**</span><span class="sxs-lookup"><span data-stu-id="605d3-131">**D3DXPlaneDotNormal**</span></span>](d3dxplanedotnormal.md)
</dt> </dl>

 

 
