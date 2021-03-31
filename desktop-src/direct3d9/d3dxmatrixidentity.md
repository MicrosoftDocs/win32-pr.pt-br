---
description: Cria uma matriz de identidade.
ms.assetid: 0dd6d4fb-284c-4d01-9a85-63aa08e71723
title: Função D3DXMatrixIdentity (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 10dffa12a379754006ca65d1239be96632a68b93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930542"
---
# <a name="d3dxmatrixidentity-function"></a><span data-ttu-id="c5968-103">Função D3DXMatrixIdentity</span><span class="sxs-lookup"><span data-stu-id="c5968-103">D3DXMatrixIdentity function</span></span>

<span data-ttu-id="c5968-104">Cria uma matriz de identidade.</span><span class="sxs-lookup"><span data-stu-id="c5968-104">Creates an identity matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5968-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5968-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixIdentity(
  _Inout_ D3DXMATRIX *pOut
);
```



## <a name="parameters"></a><span data-ttu-id="c5968-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5968-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5968-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="c5968-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5968-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5968-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c5968-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="c5968-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5968-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c5968-110">Return value</span></span>

<span data-ttu-id="c5968-111">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5968-111">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c5968-112">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é a matriz de identidade.</span><span class="sxs-lookup"><span data-stu-id="c5968-112">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the identity matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5968-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5968-113">Remarks</span></span>

<span data-ttu-id="c5968-114">A matriz de identidade é uma matriz na qual todos os coeficientes são 0, exceto \[ 1, 1 \] \[ 2, 2 \] \[ 3, 3 \] \[ 4, 4 \] coeficientes, que são definidos como 1.</span><span class="sxs-lookup"><span data-stu-id="c5968-114">The identity matrix is a matrix in which all coefficients are 0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.</span></span> <span data-ttu-id="c5968-115">A matriz de identidade é especial quando ela é aplicada a vértices, elas não são alteradas.</span><span class="sxs-lookup"><span data-stu-id="c5968-115">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="c5968-116">A matriz de identidade é usada como ponto de partida para matrizes que modificarão valores de vértice para criar rotações, traduções e quaisquer outras transformações que possam ser representadas por uma matriz de 4 X4.</span><span class="sxs-lookup"><span data-stu-id="c5968-116">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4 x4 matrix.</span></span>

<span data-ttu-id="c5968-117">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="c5968-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c5968-118">Dessa forma, a função **D3DXMatrixIdentity** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="c5968-118">In this way, the **D3DXMatrixIdentity** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5968-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5968-119">Requirements</span></span>



| <span data-ttu-id="c5968-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5968-120">Requirement</span></span> | <span data-ttu-id="c5968-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c5968-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5968-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c5968-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c5968-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5968-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c5968-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c5968-124">Library</span></span><br/> | <dl> <span data-ttu-id="c5968-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5968-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c5968-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5968-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5968-127">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="c5968-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c5968-128">**D3DXMatrixIsIdentity**</span><span class="sxs-lookup"><span data-stu-id="c5968-128">**D3DXMatrixIsIdentity**</span></span>](d3dxmatrixisidentity.md)
</dt> </dl>

 

 




