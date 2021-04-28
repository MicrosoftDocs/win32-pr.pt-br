---
description: Função D3DXMatrixOrthoOffCenterLH (D3DX10Math. h) – compila uma matriz de projeção ortográfica personalizada, da mão esquerda.
ms.assetid: 84175c08-5a0b-4183-afe2-8aecafd73897
title: Função D3DXMatrixOrthoOffCenterLH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2eb10963372519827eb544371ebb0df04df2e178
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109134"
---
# <a name="d3dxmatrixorthooffcenterlh-function-d3dx10mathh"></a><span data-ttu-id="f1666-103">Função D3DXMatrixOrthoOffCenterLH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="f1666-103">D3DXMatrixOrthoOffCenterLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="f1666-104">Cria uma matriz de projeção ortográfica personalizada de mão esquerda.</span><span class="sxs-lookup"><span data-stu-id="f1666-104">Builds a customized, left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1666-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1666-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="f1666-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1666-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1666-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f1666-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1666-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f1666-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f1666-109">Ponteiro para o [**D3DXMATRIX**](d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="f1666-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1666-110">*l* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="f1666-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1666-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f1666-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f1666-112">Valor x mínimo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="f1666-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="f1666-113">*r* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="f1666-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1666-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f1666-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f1666-115">Valor x máximo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="f1666-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="f1666-116">*b* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="f1666-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1666-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f1666-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f1666-118">Valor y mínimo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="f1666-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="f1666-119">*t* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="f1666-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1666-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f1666-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f1666-121">Valor y máximo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="f1666-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="f1666-122">*Zn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f1666-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1666-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f1666-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f1666-124">Valor z mínimo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="f1666-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="f1666-125">*ZF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f1666-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1666-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f1666-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f1666-127">Valor z máximo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="f1666-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1666-128">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f1666-128">Return value</span></span>

<span data-ttu-id="f1666-129">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f1666-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f1666-130">Ponteiro para o [**D3DXMATRIX**](d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="f1666-130">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f1666-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1666-131">Remarks</span></span>

<span data-ttu-id="f1666-132">O [**D3DXMatrixOrthoLH**](d3d10-d3dxmatrixortholh.md) é um caso especial da função D3DXMatrixOrthoOffCenterLH.</span><span class="sxs-lookup"><span data-stu-id="f1666-132">The [**D3DXMatrixOrthoLH**](d3d10-d3dxmatrixortholh.md) is a special case of the D3DXMatrixOrthoOffCenterLH function.</span></span> <span data-ttu-id="f1666-133">Para criar a mesma projeção usando D3DXMatrixOrthoOffCenterLH, use os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="f1666-133">To create the same projection using D3DXMatrixOrthoOffCenterLH, use the following values:</span></span>

<span data-ttu-id="f1666-134">l =-w/2,</span><span class="sxs-lookup"><span data-stu-id="f1666-134">l = -w/2,</span></span>

<span data-ttu-id="f1666-135">r = w/2,</span><span class="sxs-lookup"><span data-stu-id="f1666-135">r = w/2,</span></span>

<span data-ttu-id="f1666-136">b =-h/2 e</span><span class="sxs-lookup"><span data-stu-id="f1666-136">b = -h/2, and</span></span>

<span data-ttu-id="f1666-137">t = h/2.</span><span class="sxs-lookup"><span data-stu-id="f1666-137">t = h/2.</span></span>

<span data-ttu-id="f1666-138">Todos os parâmetros da função D3DXMatrixOrthoOffCenterLH são distâncias no espaço da câmera.</span><span class="sxs-lookup"><span data-stu-id="f1666-138">All the parameters of the D3DXMatrixOrthoOffCenterLH function are distances in camera space.</span></span> <span data-ttu-id="f1666-139">Os parâmetros descrevem as dimensões do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="f1666-139">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="f1666-140">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="f1666-140">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f1666-141">Dessa forma, a função D3DXMatrixOrthoOffCenterLH pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="f1666-141">In this way, the D3DXMatrixOrthoOffCenterLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f1666-142">Essa função usa a fórmula a seguir para calcular a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="f1666-142">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zf-zn)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="f1666-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1666-143">Requirements</span></span>



| <span data-ttu-id="f1666-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1666-144">Requirement</span></span> | <span data-ttu-id="f1666-145">Valor</span><span class="sxs-lookup"><span data-stu-id="f1666-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1666-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1666-146">Header</span></span><br/>  | <dl> <span data-ttu-id="f1666-147"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1666-147"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="f1666-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f1666-148">Library</span></span><br/> | <dl> <span data-ttu-id="f1666-149"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1666-149"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f1666-150">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f1666-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1666-151">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="f1666-151">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
