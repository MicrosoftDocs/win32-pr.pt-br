---
description: Função D3DXMatrixPerspectiveRH (D3dx9math. h) – compila uma matriz de projeção de perspectiva à direita.
ms.assetid: dd9b041b-922b-43df-a6e9-46c97204338a
title: Função D3DXMatrixPerspectiveRH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3c583b74366a0a00054bbeced1ece2bd3d1c1cd2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118234"
---
# <a name="d3dxmatrixperspectiverh-function-d3dx9mathh"></a><span data-ttu-id="1ffe8-103">Função D3DXMatrixPerspectiveRH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="1ffe8-103">D3DXMatrixPerspectiveRH function (D3dx9math.h)</span></span>

<span data-ttu-id="1ffe8-104">Cria uma matriz de projeção de perspectiva à direita.</span><span class="sxs-lookup"><span data-stu-id="1ffe8-104">Builds a right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ffe8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ffe8-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="1ffe8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ffe8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ffe8-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="1ffe8-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ffe8-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1ffe8-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1ffe8-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="1ffe8-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1ffe8-110">*w* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="1ffe8-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ffe8-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ffe8-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ffe8-112">Largura do volume de exibição no plano de exibição próximo.</span><span class="sxs-lookup"><span data-stu-id="1ffe8-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="1ffe8-113">*h* \[\]</span><span class="sxs-lookup"><span data-stu-id="1ffe8-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ffe8-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ffe8-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ffe8-115">Altura do volume de exibição no plano de exibição próximo.</span><span class="sxs-lookup"><span data-stu-id="1ffe8-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="1ffe8-116">*Zn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1ffe8-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ffe8-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ffe8-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ffe8-118">Valor Z do plano de exibição próximo.</span><span class="sxs-lookup"><span data-stu-id="1ffe8-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="1ffe8-119">*ZF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1ffe8-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ffe8-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ffe8-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ffe8-121">Z-valor do plano de exibição distante.</span><span class="sxs-lookup"><span data-stu-id="1ffe8-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ffe8-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1ffe8-122">Return value</span></span>

<span data-ttu-id="1ffe8-123">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1ffe8-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1ffe8-124">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é uma matriz de projeção de perspectiva à direita.</span><span class="sxs-lookup"><span data-stu-id="1ffe8-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ffe8-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ffe8-125">Remarks</span></span>

<span data-ttu-id="1ffe8-126">Todos os parâmetros da função **D3DXMatrixPerspectiveRH** são distâncias no espaço da câmera.</span><span class="sxs-lookup"><span data-stu-id="1ffe8-126">All the parameters of the **D3DXMatrixPerspectiveRH** function are distances in camera space.</span></span> <span data-ttu-id="1ffe8-127">Os parâmetros descrevem as dimensões do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="1ffe8-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="1ffe8-128">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="1ffe8-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="1ffe8-129">Dessa forma, a função **D3DXMatrixPerspectiveRH** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="1ffe8-129">In this way, the **D3DXMatrixPerspectiveRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1ffe8-130">Essa função usa a fórmula a seguir para calcular a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="1ffe8-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zn-zf)    -1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="1ffe8-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ffe8-131">Requirements</span></span>



| <span data-ttu-id="1ffe8-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ffe8-132">Requirement</span></span> | <span data-ttu-id="1ffe8-133">Valor</span><span class="sxs-lookup"><span data-stu-id="1ffe8-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ffe8-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ffe8-134">Header</span></span><br/>  | <dl> <span data-ttu-id="1ffe8-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ffe8-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1ffe8-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1ffe8-136">Library</span></span><br/> | <dl> <span data-ttu-id="1ffe8-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ffe8-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1ffe8-138">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1ffe8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ffe8-139">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="1ffe8-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="1ffe8-140">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="1ffe8-140">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="1ffe8-141">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="1ffe8-141">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="1ffe8-142">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="1ffe8-142">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="1ffe8-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="1ffe8-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="1ffe8-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="1ffe8-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
