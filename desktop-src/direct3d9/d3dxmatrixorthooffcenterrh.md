---
description: Função D3DXMatrixOrthoOffCenterRH (D3dx9math. h) – compila uma matriz de projeção ortográfica personalizada, de mão-de-lado.
ms.assetid: d6171e28-b138-4ccf-9f12-fb977a30aca1
title: Função D3DXMatrixOrthoOffCenterRH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8519dca07a4475ff043491802ae173ecc61c0bd3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107454"
---
# <a name="d3dxmatrixorthooffcenterrh-function-d3dx9mathh"></a><span data-ttu-id="def1a-103">Função D3DXMatrixOrthoOffCenterRH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="def1a-103">D3DXMatrixOrthoOffCenterRH function (D3dx9math.h)</span></span>

<span data-ttu-id="def1a-104">Cria uma matriz de projeção ortográfica personalizada de mão-de-lado.</span><span class="sxs-lookup"><span data-stu-id="def1a-104">Builds a customized, right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="def1a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="def1a-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="def1a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="def1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="def1a-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="def1a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="def1a-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="def1a-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="def1a-109">Ponteiro para o [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="def1a-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="def1a-110">*l* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="def1a-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def1a-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="def1a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="def1a-112">Valor x mínimo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="def1a-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="def1a-113">*r* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="def1a-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def1a-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="def1a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="def1a-115">Valor x máximo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="def1a-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="def1a-116">*b* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="def1a-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def1a-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="def1a-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="def1a-118">Valor y mínimo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="def1a-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="def1a-119">*t* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="def1a-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def1a-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="def1a-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="def1a-121">Valor y máximo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="def1a-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="def1a-122">*Zn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="def1a-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def1a-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="def1a-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="def1a-124">Valor z mínimo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="def1a-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="def1a-125">*ZF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="def1a-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def1a-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="def1a-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="def1a-127">Valor z máximo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="def1a-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="def1a-128">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="def1a-128">Return value</span></span>

<span data-ttu-id="def1a-129">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="def1a-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="def1a-130">Ponteiro para o [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="def1a-130">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="def1a-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="def1a-131">Remarks</span></span>

<span data-ttu-id="def1a-132">A função [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) é um caso especial da função **D3DXMatrixOrthoOffCenterRH** .</span><span class="sxs-lookup"><span data-stu-id="def1a-132">The [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) function is a special case of the **D3DXMatrixOrthoOffCenterRH** function.</span></span> <span data-ttu-id="def1a-133">Para criar a mesma projeção usando **D3DXMatrixOrthoOffCenterRH**, use os seguintes valores: l =-w/2, r = w/2, b =-h/2 e t = h/2.</span><span class="sxs-lookup"><span data-stu-id="def1a-133">To create the same projection using **D3DXMatrixOrthoOffCenterRH**, use the following values: l = -w/2, r = w/2, b = -h/2, and t = h/2.</span></span>

<span data-ttu-id="def1a-134">Todos os parâmetros da função **D3DXMatrixOrthoOffCenterRH** são distâncias no espaço da câmera.</span><span class="sxs-lookup"><span data-stu-id="def1a-134">All the parameters of the **D3DXMatrixOrthoOffCenterRH** function are distances in camera space.</span></span> <span data-ttu-id="def1a-135">Os parâmetros descrevem as dimensões do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="def1a-135">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="def1a-136">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="def1a-136">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="def1a-137">Dessa forma, a função **D3DXMatrixOrthoOffCenterRH** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="def1a-137">In this way, the **D3DXMatrixOrthoOffCenterRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="def1a-138">Essa função usa a fórmula a seguir para calcular a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="def1a-138">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zn-zf)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="def1a-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="def1a-139">Requirements</span></span>



| <span data-ttu-id="def1a-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="def1a-140">Requirement</span></span> | <span data-ttu-id="def1a-141">Valor</span><span class="sxs-lookup"><span data-stu-id="def1a-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="def1a-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="def1a-142">Header</span></span><br/>  | <dl> <span data-ttu-id="def1a-143"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="def1a-143"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="def1a-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="def1a-144">Library</span></span><br/> | <dl> <span data-ttu-id="def1a-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="def1a-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="def1a-146">Consulte também</span><span class="sxs-lookup"><span data-stu-id="def1a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="def1a-147">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="def1a-147">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="def1a-148">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="def1a-148">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="def1a-149">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="def1a-149">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="def1a-150">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="def1a-150">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
