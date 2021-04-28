---
description: Função D3DXMatrixReflect (D3DX10Math. h) – compila uma matriz que reflete o sistema de coordenadas sobre um plano.
ms.assetid: bd2c5905-780e-4fac-a848-d7dbcfc390c6
title: Função D3DXMatrixReflect (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f96224c881dcd5db2cc1c356003ab96e8a626900
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103404"
---
# <a name="d3dxmatrixreflect-function-d3dx10mathh"></a><span data-ttu-id="8ab17-103">Função D3DXMatrixReflect (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="8ab17-103">D3DXMatrixReflect function (D3DX10Math.h)</span></span>

<span data-ttu-id="8ab17-104">Cria uma matriz que reflete o sistema de coordenadas sobre um plano.</span><span class="sxs-lookup"><span data-stu-id="8ab17-104">Builds a matrix that reflects the coordinate system about a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ab17-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ab17-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixReflect(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXPLANE  *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="8ab17-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ab17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ab17-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="8ab17-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ab17-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ab17-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8ab17-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="8ab17-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8ab17-110">*pPlane* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8ab17-110">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ab17-111">Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="8ab17-111">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="8ab17-112">Ponteiro para o [**D3DXPLANE**](d3d10-d3dxplane.md)de origem.</span><span class="sxs-lookup"><span data-stu-id="8ab17-112">Pointer to the source [**D3DXPLANE**](d3d10-d3dxplane.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ab17-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8ab17-113">Return value</span></span>

<span data-ttu-id="8ab17-114">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ab17-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8ab17-115">Ponteiro para uma estrutura D3DXMATRIX que reflete o sistema de coordenadas sobre o plano de origem.</span><span class="sxs-lookup"><span data-stu-id="8ab17-115">Pointer to a D3DXMATRIX structure that reflects the coordinate system about the source plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ab17-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ab17-116">Remarks</span></span>

<span data-ttu-id="8ab17-117">Essa função normaliza a equação do plano antes de criar a matriz refletida.</span><span class="sxs-lookup"><span data-stu-id="8ab17-117">This function normalizes the plane equation before it creates the reflected matrix.</span></span>

<span data-ttu-id="8ab17-118">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="8ab17-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="8ab17-119">Dessa forma, a função D3DXMatrixReflect pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="8ab17-119">In this way, the D3DXMatrixReflect function can be used as a parameter for another function.</span></span>

<span data-ttu-id="8ab17-120">Essa função usa a fórmula a seguir para calcular a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="8ab17-120">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
    
-2 * P.a * P.a + 1  -2 * P.b * P.a      -2 * P.c * P.a        0
-2 * P.a * P.b      -2 * P.b * P.b + 1  -2 * P.c * P.b        0
-2 * P.a * P.c      -2 * P.b * P.c      -2 * P.c * P.c + 1    0
-2 * P.a * P.d      -2 * P.b * P.d      -2 * P.c * P.d        1
```



## <a name="requirements"></a><span data-ttu-id="8ab17-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ab17-121">Requirements</span></span>



| <span data-ttu-id="8ab17-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ab17-122">Requirement</span></span> | <span data-ttu-id="8ab17-123">Valor</span><span class="sxs-lookup"><span data-stu-id="8ab17-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ab17-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8ab17-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8ab17-125"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ab17-125"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="8ab17-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8ab17-126">Library</span></span><br/> | <dl> <span data-ttu-id="8ab17-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ab17-127"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8ab17-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8ab17-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ab17-129">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="8ab17-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
