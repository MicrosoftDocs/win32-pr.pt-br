---
description: Retorna a transpoção de matriz de uma matriz.
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
ms.openlocfilehash: 700fc023cd15227c2cf26cd5bdcab51dc0ae3297
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791324"
---
# <a name="d3dxmatrixtranspose-function-d3dx9mathh"></a><span data-ttu-id="b5785-103">Função D3DXMatrixTranspose (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="b5785-103">D3DXMatrixTranspose function (D3dx9math.h)</span></span>

<span data-ttu-id="b5785-104">Retorna a transpoção de matriz de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="b5785-104">Returns the matrix transpose of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5785-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5785-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="b5785-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5785-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5785-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="b5785-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5785-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5785-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b5785-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="b5785-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b5785-110">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b5785-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5785-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b5785-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b5785-112">Ponteiro para a estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="b5785-112">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5785-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b5785-113">Return value</span></span>

<span data-ttu-id="b5785-114">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5785-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b5785-115">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é a transpoção de matriz da matriz.</span><span class="sxs-lookup"><span data-stu-id="b5785-115">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the matrix transpose of the matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5785-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5785-116">Remarks</span></span>

<span data-ttu-id="b5785-117">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="b5785-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="b5785-118">Dessa forma, a função **D3DXMatrixTranspose** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="b5785-118">In this way, the **D3DXMatrixTranspose** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5785-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5785-119">Requirements</span></span>



| <span data-ttu-id="b5785-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5785-120">Requirement</span></span> | <span data-ttu-id="b5785-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b5785-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5785-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5785-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b5785-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5785-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b5785-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b5785-124">Library</span></span><br/> | <dl> <span data-ttu-id="b5785-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5785-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b5785-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5785-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5785-127">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="b5785-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




