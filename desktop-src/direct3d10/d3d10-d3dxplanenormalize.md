---
description: Normaliza os coeficientes de plano para que o plano normal tenha comprimento de unidade.
ms.assetid: 52ae36a7-e37b-457a-9832-e62900a85bde
title: Função D3DXPlaneNormalize (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 44d5e9d810653b2cdae233dec803383c74563d08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791068"
---
# <a name="d3dxplanenormalize-function-d3dx10mathh"></a><span data-ttu-id="fc3f0-103">Função D3DXPlaneNormalize (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="fc3f0-103">D3DXPlaneNormalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="fc3f0-104">Normaliza os coeficientes de plano para que o plano normal tenha comprimento de unidade.</span><span class="sxs-lookup"><span data-stu-id="fc3f0-104">Normalizes the plane coefficients so that the plane normal has unit length.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc3f0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc3f0-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a><span data-ttu-id="fc3f0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc3f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc3f0-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="fc3f0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc3f0-108">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="fc3f0-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="fc3f0-109">Ponteiro para o [**D3DXPLANE**](d3d10-d3dxplane.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="fc3f0-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fc3f0-110">*PP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fc3f0-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc3f0-111">Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="fc3f0-111">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="fc3f0-112">Ponteiro para a estrutura de D3DXPLANE de origem.</span><span class="sxs-lookup"><span data-stu-id="fc3f0-112">Pointer to the source D3DXPLANE structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc3f0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fc3f0-113">Return value</span></span>

<span data-ttu-id="fc3f0-114">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="fc3f0-114">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="fc3f0-115">Ponteiro para uma estrutura D3DXPLANE que representa o normal do plano.</span><span class="sxs-lookup"><span data-stu-id="fc3f0-115">Pointer to a D3DXPLANE structure that represents the normal of the plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc3f0-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc3f0-116">Remarks</span></span>

<span data-ttu-id="fc3f0-117">Essa função normaliza um plano de forma que \| a, b, c \| = = 1.</span><span class="sxs-lookup"><span data-stu-id="fc3f0-117">This function normalizes a plane so that \|a,b,c\| == 1.</span></span>

<span data-ttu-id="fc3f0-118">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="fc3f0-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="fc3f0-119">Dessa forma, essa função pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="fc3f0-119">In this way, this function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc3f0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc3f0-120">Requirements</span></span>



| <span data-ttu-id="fc3f0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc3f0-121">Requirement</span></span> | <span data-ttu-id="fc3f0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="fc3f0-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc3f0-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fc3f0-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fc3f0-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc3f0-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="fc3f0-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fc3f0-125">Library</span></span><br/> | <dl> <span data-ttu-id="fc3f0-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc3f0-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fc3f0-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc3f0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc3f0-128">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="fc3f0-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
