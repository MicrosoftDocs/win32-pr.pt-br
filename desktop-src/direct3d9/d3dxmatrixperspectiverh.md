---
description: Cria uma matriz de projeção de perspectiva à direita.
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
ms.openlocfilehash: 3bcec04202ecb2de15c479ac4ce84d4ee86c99a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172929"
---
# <a name="d3dxmatrixperspectiverh-function-d3dx9mathh"></a><span data-ttu-id="c78ab-103">Função D3DXMatrixPerspectiveRH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c78ab-103">D3DXMatrixPerspectiveRH function (D3dx9math.h)</span></span>

<span data-ttu-id="c78ab-104">Cria uma matriz de projeção de perspectiva à direita.</span><span class="sxs-lookup"><span data-stu-id="c78ab-104">Builds a right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c78ab-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c78ab-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="c78ab-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c78ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c78ab-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="c78ab-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c78ab-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c78ab-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c78ab-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="c78ab-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c78ab-110">*w* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="c78ab-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c78ab-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c78ab-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c78ab-112">Largura do volume de exibição no plano de exibição próximo.</span><span class="sxs-lookup"><span data-stu-id="c78ab-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="c78ab-113">*h* \[\]</span><span class="sxs-lookup"><span data-stu-id="c78ab-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c78ab-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c78ab-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c78ab-115">Altura do volume de exibição no plano de exibição próximo.</span><span class="sxs-lookup"><span data-stu-id="c78ab-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="c78ab-116">*Zn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c78ab-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c78ab-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c78ab-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c78ab-118">Valor Z do plano de exibição próximo.</span><span class="sxs-lookup"><span data-stu-id="c78ab-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="c78ab-119">*ZF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c78ab-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c78ab-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c78ab-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c78ab-121">Z-valor do plano de exibição distante.</span><span class="sxs-lookup"><span data-stu-id="c78ab-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c78ab-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c78ab-122">Return value</span></span>

<span data-ttu-id="c78ab-123">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c78ab-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c78ab-124">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é uma matriz de projeção de perspectiva à direita.</span><span class="sxs-lookup"><span data-stu-id="c78ab-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="c78ab-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="c78ab-125">Remarks</span></span>

<span data-ttu-id="c78ab-126">Todos os parâmetros da função **D3DXMatrixPerspectiveRH** são distâncias no espaço da câmera.</span><span class="sxs-lookup"><span data-stu-id="c78ab-126">All the parameters of the **D3DXMatrixPerspectiveRH** function are distances in camera space.</span></span> <span data-ttu-id="c78ab-127">Os parâmetros descrevem as dimensões do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="c78ab-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="c78ab-128">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="c78ab-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c78ab-129">Dessa forma, a função **D3DXMatrixPerspectiveRH** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="c78ab-129">In this way, the **D3DXMatrixPerspectiveRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="c78ab-130">Essa função usa a fórmula a seguir para calcular a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="c78ab-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zn-zf)    -1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="c78ab-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c78ab-131">Requirements</span></span>



| <span data-ttu-id="c78ab-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="c78ab-132">Requirement</span></span> | <span data-ttu-id="c78ab-133">Valor</span><span class="sxs-lookup"><span data-stu-id="c78ab-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c78ab-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c78ab-134">Header</span></span><br/>  | <dl> <span data-ttu-id="c78ab-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c78ab-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c78ab-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c78ab-136">Library</span></span><br/> | <dl> <span data-ttu-id="c78ab-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c78ab-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c78ab-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="c78ab-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c78ab-139">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="c78ab-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c78ab-140">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="c78ab-140">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="c78ab-141">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="c78ab-141">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="c78ab-142">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="c78ab-142">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="c78ab-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="c78ab-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="c78ab-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="c78ab-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
