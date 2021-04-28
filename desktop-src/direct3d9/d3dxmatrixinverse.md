---
description: Função D3DXMatrixInverse (D3dx9math. h) – calcula o inverso de uma matriz.
ms.assetid: b8cad5c5-caa5-4426-b045-1770f8806b6b
title: Função D3DXMatrixInverse (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixInverse
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0109481beaea282a785564c081e498fe4c7571b6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098144"
---
# <a name="d3dxmatrixinverse-function-d3dx9mathh"></a><span data-ttu-id="bbbf8-103">Função D3DXMatrixInverse (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="bbbf8-103">D3DXMatrixInverse function (D3dx9math.h)</span></span>

<span data-ttu-id="bbbf8-104">Calcula o inverso de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="bbbf8-104">Calculates the inverse of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbbf8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbbf8-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixInverse(
  _Inout_       D3DXMATRIX *pOut,
  _Inout_       FLOAT      *pDeterminant,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="bbbf8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbbf8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbbf8-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="bbbf8-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bbbf8-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="bbbf8-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bbbf8-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="bbbf8-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bbbf8-110">*pDeterminant* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="bbbf8-110">*pDeterminant* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bbbf8-111">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bbbf8-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bbbf8-112">Aponta para um valor FLOAT que contém o determinante da matriz.</span><span class="sxs-lookup"><span data-stu-id="bbbf8-112">Pointer to a FLOAT value containing the determinant of the matrix.</span></span> <span data-ttu-id="bbbf8-113">Se o determinante não for necessário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="bbbf8-113">If the determinant is not needed, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bbbf8-114">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bbbf8-114">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbbf8-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="bbbf8-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bbbf8-116">Ponteiro para a estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="bbbf8-116">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbbf8-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="bbbf8-117">Return value</span></span>

<span data-ttu-id="bbbf8-118">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="bbbf8-118">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bbbf8-119">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o inverso da matriz.</span><span class="sxs-lookup"><span data-stu-id="bbbf8-119">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the inverse of the matrix.</span></span> <span data-ttu-id="bbbf8-120">Se a inversão da matriz falhar, **NULL** será retornado.</span><span class="sxs-lookup"><span data-stu-id="bbbf8-120">If matrix inversion fails, **NULL** is returned.</span></span>

<span data-ttu-id="bbbf8-121">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="bbbf8-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="bbbf8-122">Dessa forma, a função **D3DXMatrixInverse** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="bbbf8-122">In this way, the **D3DXMatrixInverse** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbbf8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbbf8-123">Requirements</span></span>



| <span data-ttu-id="bbbf8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbbf8-124">Requirement</span></span> | <span data-ttu-id="bbbf8-125">Valor</span><span class="sxs-lookup"><span data-stu-id="bbbf8-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bbbf8-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bbbf8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="bbbf8-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbbf8-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="bbbf8-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bbbf8-128">Library</span></span><br/> | <dl> <span data-ttu-id="bbbf8-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bbbf8-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bbbf8-130">Consulte também</span><span class="sxs-lookup"><span data-stu-id="bbbf8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbbf8-131">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="bbbf8-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
