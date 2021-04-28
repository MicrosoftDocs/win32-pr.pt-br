---
description: Função D3DXMatrixTranspose (D3dx9math. h) – retorna a transpoção de matriz de uma matriz.
ms.assetid: 0ba9682f-3dd6-48b2-82b1-6e34e8ce5452
title: Função D3DXMatrixTranspose (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9cb050061b10de963258bcd7527d3c86260d5abc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098104"
---
# <a name="d3dxmatrixtranspose-function-d3dx9mathh"></a><span data-ttu-id="c5d03-103">Função D3DXMatrixTranspose (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c5d03-103">D3DXMatrixTranspose function (D3dx9math.h)</span></span>

<span data-ttu-id="c5d03-104">Retorna a transpoção de matriz de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="c5d03-104">Returns the matrix transpose of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5d03-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5d03-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="c5d03-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5d03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5d03-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="c5d03-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5d03-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5d03-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c5d03-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="c5d03-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c5d03-110">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c5d03-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5d03-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c5d03-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c5d03-112">Ponteiro para a estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="c5d03-112">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5d03-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c5d03-113">Return value</span></span>

<span data-ttu-id="c5d03-114">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5d03-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c5d03-115">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é a transpoção de matriz da matriz.</span><span class="sxs-lookup"><span data-stu-id="c5d03-115">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the matrix transpose of the matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5d03-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5d03-116">Remarks</span></span>

<span data-ttu-id="c5d03-117">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="c5d03-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c5d03-118">Dessa forma, a função **D3DXMatrixTranspose** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="c5d03-118">In this way, the **D3DXMatrixTranspose** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5d03-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5d03-119">Requirements</span></span>



| <span data-ttu-id="c5d03-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5d03-120">Requirement</span></span> | <span data-ttu-id="c5d03-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c5d03-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5d03-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c5d03-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c5d03-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5d03-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c5d03-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c5d03-124">Library</span></span><br/> | <dl> <span data-ttu-id="c5d03-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5d03-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c5d03-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c5d03-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5d03-127">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="c5d03-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




