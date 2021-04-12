---
description: Cria uma matriz de projeção ortográfica de mão esquerda.
ms.assetid: e42151bd-2302-491b-a211-7d5a4b8e437f
title: Função D3DXMatrixOrthoLH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4aaf4a1a770ba0200a6afe389d37e248b9f4c7de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298734"
---
# <a name="d3dxmatrixortholh-function-d3dx9mathh"></a><span data-ttu-id="9c6b9-103">Função D3DXMatrixOrthoLH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="9c6b9-103">D3DXMatrixOrthoLH function (D3dx9math.h)</span></span>

<span data-ttu-id="9c6b9-104">Cria uma matriz de projeção ortográfica de mão esquerda.</span><span class="sxs-lookup"><span data-stu-id="9c6b9-104">Builds a left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c6b9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c6b9-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="9c6b9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c6b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c6b9-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="9c6b9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c6b9-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9c6b9-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9c6b9-109">Ponteiro para o [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="9c6b9-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c6b9-110">*w* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="9c6b9-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c6b9-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c6b9-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9c6b9-112">Largura do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="9c6b9-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="9c6b9-113">*h* \[\]</span><span class="sxs-lookup"><span data-stu-id="9c6b9-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c6b9-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c6b9-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9c6b9-115">Altura do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="9c6b9-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="9c6b9-116">*Zn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9c6b9-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c6b9-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c6b9-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9c6b9-118">Valor z mínimo do volume de exibição que é referido como z-Near.</span><span class="sxs-lookup"><span data-stu-id="9c6b9-118">Minimum z-value of the view volume which is referred to as z-near.</span></span>

</dd> <dt>

<span data-ttu-id="9c6b9-119">*ZF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9c6b9-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c6b9-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c6b9-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9c6b9-121">Valor z máximo do volume de exibição que é referido como z-far.</span><span class="sxs-lookup"><span data-stu-id="9c6b9-121">Maximum z-value of the view volume which is referred to as z-far.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c6b9-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9c6b9-122">Return value</span></span>

<span data-ttu-id="9c6b9-123">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9c6b9-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9c6b9-124">Ponteiro para o [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="9c6b9-124">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9c6b9-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c6b9-125">Remarks</span></span>

<span data-ttu-id="9c6b9-126">Todos os parâmetros da função **D3DXMatrixOrthoLH** são distâncias no espaço da câmera.</span><span class="sxs-lookup"><span data-stu-id="9c6b9-126">All the parameters of the **D3DXMatrixOrthoLH** function are distances in camera space.</span></span> <span data-ttu-id="9c6b9-127">Os parâmetros descrevem as dimensões do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="9c6b9-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="9c6b9-128">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="9c6b9-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="9c6b9-129">Dessa forma, a função **D3DXMatrixOrthoLH** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="9c6b9-129">In this way, the **D3DXMatrixOrthoLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="9c6b9-130">Essa função usa a fórmula a seguir para calcular a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="9c6b9-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
0    0   -zn/(zf-zn)  1
```



## <a name="requirements"></a><span data-ttu-id="9c6b9-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c6b9-131">Requirements</span></span>



| <span data-ttu-id="9c6b9-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c6b9-132">Requirement</span></span> | <span data-ttu-id="9c6b9-133">Valor</span><span class="sxs-lookup"><span data-stu-id="9c6b9-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c6b9-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9c6b9-134">Header</span></span><br/>  | <dl> <span data-ttu-id="9c6b9-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c6b9-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9c6b9-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9c6b9-136">Library</span></span><br/> | <dl> <span data-ttu-id="9c6b9-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c6b9-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9c6b9-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c6b9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c6b9-139">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="9c6b9-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="9c6b9-140">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="9c6b9-140">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="9c6b9-141">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="9c6b9-141">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="9c6b9-142">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="9c6b9-142">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
