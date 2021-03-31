---
description: Cria uma matriz que reflete o sistema de coordenadas sobre um plano.
ms.assetid: f6dc3834-42f2-4ad0-8098-8c5e25e10d58
title: Função D3DXMatrixReflect (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixReflect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2e54c5f93164e5fccee0d74199a1843a1476e69a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930540"
---
# <a name="d3dxmatrixreflect-function-d3dx9mathh"></a><span data-ttu-id="815b4-103">Função D3DXMatrixReflect (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="815b4-103">D3DXMatrixReflect function (D3dx9math.h)</span></span>

<span data-ttu-id="815b4-104">Cria uma matriz que reflete o sistema de coordenadas sobre um plano.</span><span class="sxs-lookup"><span data-stu-id="815b4-104">Builds a matrix that reflects the coordinate system about a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="815b4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="815b4-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixReflect(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXPLANE  *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="815b4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="815b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="815b4-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="815b4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="815b4-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="815b4-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="815b4-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="815b4-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="815b4-110">*pPlane* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="815b4-110">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="815b4-111">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="815b4-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="815b4-112">Ponteiro para a estrutura de [**D3DXPLANE**](d3dxplane.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="815b4-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="815b4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="815b4-113">Return value</span></span>

<span data-ttu-id="815b4-114">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="815b4-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="815b4-115">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que reflete o sistema de coordenadas sobre o plano de origem.</span><span class="sxs-lookup"><span data-stu-id="815b4-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that reflects the coordinate system about the source plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="815b4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="815b4-116">Remarks</span></span>

<span data-ttu-id="815b4-117">Essa função normaliza a equação do plano antes de criar a matriz refletida.</span><span class="sxs-lookup"><span data-stu-id="815b4-117">This function normalizes the plane equation before it creates the reflected matrix.</span></span>

<span data-ttu-id="815b4-118">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="815b4-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="815b4-119">Dessa forma, a função **D3DXMatrixReflect** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="815b4-119">In this way, the **D3DXMatrixReflect** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="815b4-120">Essa função usa a fórmula a seguir para calcular a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="815b4-120">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
    
-2 * P.a * P.a + 1  -2 * P.b * P.a      -2 * P.c * P.a        0
-2 * P.a * P.b      -2 * P.b * P.b + 1  -2 * P.c * P.b        0
-2 * P.a * P.c      -2 * P.b * P.c      -2 * P.c * P.c + 1    0
-2 * P.a * P.d      -2 * P.b * P.d      -2 * P.c * P.d        1
```



## <a name="requirements"></a><span data-ttu-id="815b4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="815b4-121">Requirements</span></span>



| <span data-ttu-id="815b4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="815b4-122">Requirement</span></span> | <span data-ttu-id="815b4-123">Valor</span><span class="sxs-lookup"><span data-stu-id="815b4-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="815b4-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="815b4-124">Header</span></span><br/>  | <dl> <span data-ttu-id="815b4-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="815b4-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="815b4-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="815b4-126">Library</span></span><br/> | <dl> <span data-ttu-id="815b4-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="815b4-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="815b4-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="815b4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="815b4-129">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="815b4-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




