---
description: Computa o produto de ponto de um plano e um vetor 4D.
ms.assetid: e6232ca8-52cc-472d-8bdb-4f8dfc520d4f
title: Função D3DXPlaneDot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b6f33e591df364151a7090e5b4a9dd0773f5788a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793943"
---
# <a name="d3dxplanedot-function"></a><span data-ttu-id="88c92-103">Função D3DXPlaneDot</span><span class="sxs-lookup"><span data-stu-id="88c92-103">D3DXPlaneDot function</span></span>

<span data-ttu-id="88c92-104">Computa o produto de ponto de um plano e um vetor 4D.</span><span class="sxs-lookup"><span data-stu-id="88c92-104">Computes the dot product of a plane and a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="88c92-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88c92-105">Syntax</span></span>


```C++
FLOAT D3DXPlaneDot(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="88c92-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88c92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88c92-107">*PP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="88c92-107">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88c92-108">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="88c92-108">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="88c92-109">Ponteiro para uma estrutura de [**D3DXPLANE**](d3dxplane.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="88c92-109">Pointer to a source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="88c92-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="88c92-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88c92-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="88c92-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="88c92-112">Ponteiro para uma estrutura [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="88c92-112">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88c92-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="88c92-113">Return value</span></span>

<span data-ttu-id="88c92-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="88c92-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="88c92-115">O produto de ponto do plano e do vetor 4D.</span><span class="sxs-lookup"><span data-stu-id="88c92-115">The dot product of the plane and 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="88c92-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="88c92-116">Remarks</span></span>

<span data-ttu-id="88c92-117">Dado um plano (a, b, c, d) e um vetor de 4D (x, y, z, w) o valor de retorno dessa função é um \* x + b \* y + c \* z + d \* w.</span><span class="sxs-lookup"><span data-stu-id="88c92-117">Given a plane (a, b, c, d) and a 4D vector (x, y, z, w) the return value of this function is a\*x + b\*y + c\*z + d\*w.</span></span> <span data-ttu-id="88c92-118">A função **D3DXPlaneDot** é útil para determinar a relação do plano com uma coordenada homogênea.</span><span class="sxs-lookup"><span data-stu-id="88c92-118">The **D3DXPlaneDot** function is useful for determining the plane's relationship with a homogeneous coordinate.</span></span> <span data-ttu-id="88c92-119">Por exemplo, essa função pode ser usada para determinar se uma coordenada específica está em um plano específico, ou em qual lado de um plano específico está em uma coordenada específica.</span><span class="sxs-lookup"><span data-stu-id="88c92-119">For example, this function could be used to determine if a particular coordinate is on a particular plane, or on which side of a particular plane a particular coordinate lies.</span></span>

## <a name="requirements"></a><span data-ttu-id="88c92-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88c92-120">Requirements</span></span>



| <span data-ttu-id="88c92-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="88c92-121">Requirement</span></span> | <span data-ttu-id="88c92-122">Valor</span><span class="sxs-lookup"><span data-stu-id="88c92-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="88c92-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="88c92-123">Header</span></span><br/>  | <dl> <span data-ttu-id="88c92-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="88c92-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="88c92-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="88c92-125">Library</span></span><br/> | <dl> <span data-ttu-id="88c92-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88c92-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="88c92-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="88c92-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88c92-128">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="88c92-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="88c92-129">**D3DXPlaneDotCoord**</span><span class="sxs-lookup"><span data-stu-id="88c92-129">**D3DXPlaneDotCoord**</span></span>](d3dxplanedotcoord.md)
</dt> <dt>

[<span data-ttu-id="88c92-130">**D3DXPlaneDotNormal**</span><span class="sxs-lookup"><span data-stu-id="88c92-130">**D3DXPlaneDotNormal**</span></span>](d3dxplanedotnormal.md)
</dt> </dl>

 

 
