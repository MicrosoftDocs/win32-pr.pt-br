---
description: Gira o vetor harmônica (SH) esférico pela matriz especificada.
ms.assetid: 9e319725-6cbb-441e-b996-ec2c6f66e5df
title: Função D3DXSHRotate (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 606ef1909237fd9c0277c5d7112284f6b7018e0e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105747864"
---
# <a name="d3dxshrotate-function-d3dx9mathh"></a><span data-ttu-id="88092-103">Função D3DXSHRotate (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="88092-103">D3DXSHRotate function (D3dx9math.h)</span></span>

<span data-ttu-id="88092-104">Gira o vetor harmônica (SH) esférico pela matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="88092-104">Rotates the spherical harmonic (SH) vector by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="88092-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88092-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotate(
  _Out_       FLOAT      *pOut,
  _In_        UINT       Order,
  _In_  const D3DXMATRIX *pMatrix,
  _In_  const FLOAT      *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="88092-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88092-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88092-107">*pout* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="88092-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88092-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="88092-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="88092-109">Ponteiro para os coeficientes de saída harmônicas (SH).</span><span class="sxs-lookup"><span data-stu-id="88092-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="88092-110">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="88092-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="88092-111">Esse ponteiro não deve ser alias com *pIn*.</span><span class="sxs-lookup"><span data-stu-id="88092-111">This pointer should not alias with *pIn*.</span></span> <span data-ttu-id="88092-112">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="88092-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="88092-113">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="88092-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88092-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="88092-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="88092-115">Ordem da avaliação SH.</span><span class="sxs-lookup"><span data-stu-id="88092-115">Order of the SH evaluation.</span></span> <span data-ttu-id="88092-116">Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="88092-116">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="88092-117">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="88092-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="88092-118">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="88092-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="88092-119">*pMatrix* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="88092-119">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88092-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="88092-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="88092-121">Ponteiro para a matriz de rotação.</span><span class="sxs-lookup"><span data-stu-id="88092-121">Pointer to the rotation matrix.</span></span> <span data-ttu-id="88092-122">A submatriz de rotação deve ser ortogonal, com um determinante de unidade.</span><span class="sxs-lookup"><span data-stu-id="88092-122">The rotation sub-matrix must be orthogonal, with a unit determinant.</span></span>

</dd> <dt>

<span data-ttu-id="88092-123">*fixar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="88092-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88092-124">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="88092-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="88092-125">Ponteiro para de doeficientes de forma girada.</span><span class="sxs-lookup"><span data-stu-id="88092-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88092-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="88092-126">Return value</span></span>

<span data-ttu-id="88092-127">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="88092-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="88092-128">Ponteiro para SH coeficientes de saída.</span><span class="sxs-lookup"><span data-stu-id="88092-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="88092-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="88092-129">Remarks</span></span>

<span data-ttu-id="88092-130">Cada coeficiente da função base Ylm é armazenado no local da memória l ² + m + l, em que:</span><span class="sxs-lookup"><span data-stu-id="88092-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="88092-131">l é o grau da função base.</span><span class="sxs-lookup"><span data-stu-id="88092-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="88092-132">m é o índice de função base para o valor l fornecido e varia de-l a l, inclusive.</span><span class="sxs-lookup"><span data-stu-id="88092-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="88092-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88092-133">Requirements</span></span>



| <span data-ttu-id="88092-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="88092-134">Requirement</span></span> | <span data-ttu-id="88092-135">Valor</span><span class="sxs-lookup"><span data-stu-id="88092-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="88092-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="88092-136">Header</span></span><br/>  | <dl> <span data-ttu-id="88092-137"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="88092-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="88092-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="88092-138">Library</span></span><br/> | <dl> <span data-ttu-id="88092-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88092-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="88092-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="88092-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88092-141">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="88092-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="88092-142">Transferência radiante de computação (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="88092-142">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
