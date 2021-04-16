---
description: Normaliza os coeficientes de plano para que o plano normal tenha comprimento de unidade.
ms.assetid: 9c595986-e1f8-4153-ba23-1fa6e583a050
title: Função D3DXPlaneNormalize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneNormalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0f0c87028d3b37f785005725e7510f689cf56d61
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761505"
---
# <a name="d3dxplanenormalize-function-d3dx9mathh"></a><span data-ttu-id="f6939-103">Função D3DXPlaneNormalize (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f6939-103">D3DXPlaneNormalize function (D3dx9math.h)</span></span>

<span data-ttu-id="f6939-104">Normaliza os coeficientes de plano para que o plano normal tenha comprimento de unidade.</span><span class="sxs-lookup"><span data-stu-id="f6939-104">Normalizes the plane coefficients so that the plane normal has unit length.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6939-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6939-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a><span data-ttu-id="f6939-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6939-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6939-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f6939-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6939-108">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="f6939-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="f6939-109">Ponteiro para a estrutura [**D3DXPLANE**](d3dxplane.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="f6939-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f6939-110">*PP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f6939-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6939-111">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="f6939-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="f6939-112">Ponteiro para a estrutura de [**D3DXPLANE**](d3dxplane.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="f6939-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6939-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f6939-113">Return value</span></span>

<span data-ttu-id="f6939-114">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="f6939-114">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="f6939-115">Ponteiro para uma estrutura [**D3DXPLANE**](d3dxplane.md) que representa o normal do plano.</span><span class="sxs-lookup"><span data-stu-id="f6939-115">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure that represents the normal of the plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6939-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6939-116">Remarks</span></span>

<span data-ttu-id="f6939-117">Essa função normaliza um plano de forma que \| a, b, c \| = = 1.</span><span class="sxs-lookup"><span data-stu-id="f6939-117">This function normalizes a plane so that \|a,b,c\| == 1.</span></span>

<span data-ttu-id="f6939-118">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="f6939-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f6939-119">Dessa forma, essa função pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="f6939-119">In this way, this function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6939-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6939-120">Requirements</span></span>



| <span data-ttu-id="f6939-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6939-121">Requirement</span></span> | <span data-ttu-id="f6939-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f6939-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6939-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f6939-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f6939-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6939-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f6939-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f6939-125">Library</span></span><br/> | <dl> <span data-ttu-id="f6939-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6939-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f6939-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6939-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6939-128">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="f6939-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




