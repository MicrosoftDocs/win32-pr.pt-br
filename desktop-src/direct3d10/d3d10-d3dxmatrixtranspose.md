---
description: Função D3DXMatrixTranspose (D3DX10Math. h) – retorna a transpoção de matriz de uma matriz.
ms.assetid: 934b17cc-39c4-425c-839b-69e080f0efd7
title: Função D3DXMatrixTranspose (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTranspose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e20fd8a29ba3f9adec7134a011f8f470c60f7011
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108854"
---
# <a name="d3dxmatrixtranspose-function-d3dx10mathh"></a><span data-ttu-id="1f687-103">Função D3DXMatrixTranspose (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="1f687-103">D3DXMatrixTranspose function (D3DX10Math.h)</span></span>

<span data-ttu-id="1f687-104">Retorna a transpoção de matriz de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="1f687-104">Returns the matrix transpose of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f687-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f687-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="1f687-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f687-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f687-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="1f687-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f687-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1f687-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1f687-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="1f687-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1f687-110">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f687-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f687-111">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1f687-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1f687-112">Ponteiro para a estrutura de D3DXMATRIX de origem.</span><span class="sxs-lookup"><span data-stu-id="1f687-112">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f687-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1f687-113">Return value</span></span>

<span data-ttu-id="1f687-114">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1f687-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1f687-115">Ponteiro para a estrutura D3DXMATRIX que é a transpoção de matriz da matriz.</span><span class="sxs-lookup"><span data-stu-id="1f687-115">Pointer to the D3DXMATRIX structure that is the matrix transpose of the matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f687-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f687-116">Remarks</span></span>

<span data-ttu-id="1f687-117">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="1f687-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1f687-118">Dessa forma, a função D3DXMatrixTranspose pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="1f687-118">In this way, the D3DXMatrixTranspose function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f687-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f687-119">Requirements</span></span>



| <span data-ttu-id="1f687-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f687-120">Requirement</span></span> | <span data-ttu-id="1f687-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1f687-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f687-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f687-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1f687-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f687-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1f687-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1f687-124">Library</span></span><br/> | <dl> <span data-ttu-id="1f687-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f687-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1f687-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1f687-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f687-127">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="1f687-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
