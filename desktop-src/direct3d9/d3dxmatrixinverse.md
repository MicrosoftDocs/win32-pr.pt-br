---
description: Calcula o inverso de uma matriz.
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
ms.openlocfilehash: eac1072c0174a03482e60167180f900588a13a72
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105808286"
---
# <a name="d3dxmatrixinverse-function-d3dx9mathh"></a><span data-ttu-id="d519f-103">Função D3DXMatrixInverse (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="d519f-103">D3DXMatrixInverse function (D3dx9math.h)</span></span>

<span data-ttu-id="d519f-104">Calcula o inverso de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="d519f-104">Calculates the inverse of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d519f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d519f-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixInverse(
  _Inout_       D3DXMATRIX *pOut,
  _Inout_       FLOAT      *pDeterminant,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="d519f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d519f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d519f-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d519f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d519f-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d519f-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d519f-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="d519f-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d519f-110">*pDeterminant* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d519f-110">*pDeterminant* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d519f-111">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d519f-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d519f-112">Aponta para um valor FLOAT que contém o determinante da matriz.</span><span class="sxs-lookup"><span data-stu-id="d519f-112">Pointer to a FLOAT value containing the determinant of the matrix.</span></span> <span data-ttu-id="d519f-113">Se o determinante não for necessário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d519f-113">If the determinant is not needed, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d519f-114">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d519f-114">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d519f-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d519f-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d519f-116">Ponteiro para a estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="d519f-116">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d519f-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d519f-117">Return value</span></span>

<span data-ttu-id="d519f-118">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d519f-118">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d519f-119">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o inverso da matriz.</span><span class="sxs-lookup"><span data-stu-id="d519f-119">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the inverse of the matrix.</span></span> <span data-ttu-id="d519f-120">Se a inversão da matriz falhar, **NULL** será retornado.</span><span class="sxs-lookup"><span data-stu-id="d519f-120">If matrix inversion fails, **NULL** is returned.</span></span>

<span data-ttu-id="d519f-121">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="d519f-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d519f-122">Dessa forma, a função **D3DXMatrixInverse** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="d519f-122">In this way, the **D3DXMatrixInverse** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d519f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d519f-123">Requirements</span></span>



| <span data-ttu-id="d519f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d519f-124">Requirement</span></span> | <span data-ttu-id="d519f-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d519f-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d519f-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d519f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d519f-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d519f-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d519f-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d519f-128">Library</span></span><br/> | <dl> <span data-ttu-id="d519f-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d519f-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d519f-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="d519f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d519f-131">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="d519f-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
