---
description: Cria uma matriz de projeção de perspectiva do lado esquerdo
ms.assetid: 07bbbca8-ad1e-4177-97d4-601b33179b47
title: Função D3DXMatrixPerspectiveLH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf7e6a446202a86e126b2cea0c4a09f19bf6ffa0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798511"
---
# <a name="d3dxmatrixperspectivelh-function-d3dx9mathh"></a><span data-ttu-id="8c301-103">Função D3DXMatrixPerspectiveLH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="8c301-103">D3DXMatrixPerspectiveLH function (D3dx9math.h)</span></span>

<span data-ttu-id="8c301-104">Cria uma matriz de projeção de perspectiva do lado esquerdo</span><span class="sxs-lookup"><span data-stu-id="8c301-104">Builds a left-handed perspective projection matrix</span></span>

## <a name="syntax"></a><span data-ttu-id="8c301-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c301-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="8c301-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c301-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c301-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="8c301-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c301-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8c301-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8c301-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="8c301-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8c301-110">*w* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="8c301-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c301-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c301-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c301-112">Largura do volume de exibição no plano de exibição próximo.</span><span class="sxs-lookup"><span data-stu-id="8c301-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="8c301-113">*h* \[\]</span><span class="sxs-lookup"><span data-stu-id="8c301-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c301-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c301-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c301-115">Altura do volume de exibição no plano de exibição próximo.</span><span class="sxs-lookup"><span data-stu-id="8c301-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="8c301-116">*Zn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8c301-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c301-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c301-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c301-118">Valor Z do plano de exibição próximo.</span><span class="sxs-lookup"><span data-stu-id="8c301-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="8c301-119">*ZF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8c301-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c301-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c301-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c301-121">Z-valor do plano de exibição distante.</span><span class="sxs-lookup"><span data-stu-id="8c301-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c301-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8c301-122">Return value</span></span>

<span data-ttu-id="8c301-123">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8c301-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8c301-124">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é uma matriz de projeção de perspectiva do lado esquerdo.</span><span class="sxs-lookup"><span data-stu-id="8c301-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c301-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c301-125">Remarks</span></span>

<span data-ttu-id="8c301-126">Todos os parâmetros da função **D3DXMatrixPerspectiveLH** são distâncias no espaço da câmera.</span><span class="sxs-lookup"><span data-stu-id="8c301-126">All the parameters of the **D3DXMatrixPerspectiveLH** function are distances in camera space.</span></span> <span data-ttu-id="8c301-127">Os parâmetros descrevem as dimensões do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="8c301-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="8c301-128">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="8c301-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="8c301-129">Dessa forma, a função **D3DXMatrixPerspectiveLH** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="8c301-129">In this way, the **D3DXMatrixPerspectiveLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="8c301-130">Essa função usa a fórmula a seguir para calcular a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="8c301-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zf-zn)     1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="8c301-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c301-131">Requirements</span></span>



| <span data-ttu-id="8c301-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c301-132">Requirement</span></span> | <span data-ttu-id="8c301-133">Valor</span><span class="sxs-lookup"><span data-stu-id="8c301-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c301-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8c301-134">Header</span></span><br/>  | <dl> <span data-ttu-id="8c301-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c301-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8c301-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8c301-136">Library</span></span><br/> | <dl> <span data-ttu-id="8c301-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c301-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8c301-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c301-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c301-139">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="8c301-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="8c301-140">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="8c301-140">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="8c301-141">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="8c301-141">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="8c301-142">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="8c301-142">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="8c301-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="8c301-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="8c301-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="8c301-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
