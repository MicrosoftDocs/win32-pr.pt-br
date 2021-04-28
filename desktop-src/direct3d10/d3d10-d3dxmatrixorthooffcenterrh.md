---
description: Função D3DXMatrixOrthoOffCenterRH (D3DX10Math. h) – compila uma matriz de projeção ortográfica personalizada, de mão-de-lado.
ms.assetid: 01d4d61e-de7b-4431-a168-68a50b1d6021
title: Função D3DXMatrixOrthoOffCenterRH (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0b41038021cc34cb02961cb9894415995955404c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113074"
---
# <a name="d3dxmatrixorthooffcenterrh-function-d3dx10mathh"></a><span data-ttu-id="b6794-103">Função D3DXMatrixOrthoOffCenterRH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="b6794-103">D3DXMatrixOrthoOffCenterRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="b6794-104">Cria uma matriz de projeção ortográfica personalizada de mão-de-lado.</span><span class="sxs-lookup"><span data-stu-id="b6794-104">Builds a customized, right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6794-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6794-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="b6794-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6794-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6794-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="b6794-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6794-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b6794-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b6794-109">Ponteiro para o [**D3DXMATRIX**](d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="b6794-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6794-110">*l* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="b6794-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6794-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b6794-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b6794-112">Valor x mínimo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="b6794-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="b6794-113">*r* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="b6794-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6794-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b6794-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b6794-115">Valor x máximo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="b6794-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="b6794-116">*b* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="b6794-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6794-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b6794-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b6794-118">Valor y mínimo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="b6794-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="b6794-119">*t* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="b6794-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6794-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b6794-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b6794-121">Valor y máximo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="b6794-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="b6794-122">*Zn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b6794-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6794-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b6794-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b6794-124">Valor z mínimo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="b6794-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="b6794-125">*ZF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b6794-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6794-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b6794-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b6794-127">Valor z máximo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="b6794-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6794-128">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b6794-128">Return value</span></span>

<span data-ttu-id="b6794-129">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b6794-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b6794-130">Ponteiro para o [**D3DXMATRIX**](d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="b6794-130">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b6794-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6794-131">Remarks</span></span>

<span data-ttu-id="b6794-132">A função [**D3DXMatrixOrthoRH**](d3d10-d3dxmatrixorthorh.md) é um caso especial da função D3DXMatrixOrthoOffCenterRH.</span><span class="sxs-lookup"><span data-stu-id="b6794-132">The [**D3DXMatrixOrthoRH**](d3d10-d3dxmatrixorthorh.md) function is a special case of the D3DXMatrixOrthoOffCenterRH function.</span></span> <span data-ttu-id="b6794-133">Para criar a mesma projeção usando D3DXMatrixOrthoOffCenterRH, use os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="b6794-133">To create the same projection using D3DXMatrixOrthoOffCenterRH, use the following values:</span></span>

<span data-ttu-id="b6794-134">l =-w/2,</span><span class="sxs-lookup"><span data-stu-id="b6794-134">l = -w/2,</span></span>

<span data-ttu-id="b6794-135">r = w/2,</span><span class="sxs-lookup"><span data-stu-id="b6794-135">r = w/2,</span></span>

<span data-ttu-id="b6794-136">b =-h/2 e</span><span class="sxs-lookup"><span data-stu-id="b6794-136">b = -h/2, and</span></span>

<span data-ttu-id="b6794-137">t = h/2.</span><span class="sxs-lookup"><span data-stu-id="b6794-137">t = h/2.</span></span>

<span data-ttu-id="b6794-138">Todos os parâmetros da função D3DXMatrixOrthoOffCenterRH são distâncias no espaço da câmera.</span><span class="sxs-lookup"><span data-stu-id="b6794-138">All the parameters of the D3DXMatrixOrthoOffCenterRH function are distances in camera space.</span></span> <span data-ttu-id="b6794-139">Os parâmetros descrevem as dimensões do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="b6794-139">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="b6794-140">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="b6794-140">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b6794-141">Dessa forma, a função D3DXMatrixOrthoOffCenterRH pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="b6794-141">In this way, the D3DXMatrixOrthoOffCenterRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b6794-142">Essa função usa a fórmula a seguir para calcular a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="b6794-142">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zn-zf)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="b6794-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6794-143">Requirements</span></span>



| <span data-ttu-id="b6794-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6794-144">Requirement</span></span> | <span data-ttu-id="b6794-145">Valor</span><span class="sxs-lookup"><span data-stu-id="b6794-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6794-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6794-146">Header</span></span><br/>  | <dl> <span data-ttu-id="b6794-147"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6794-147"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b6794-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b6794-148">Library</span></span><br/> | <dl> <span data-ttu-id="b6794-149"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6794-149"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b6794-150">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b6794-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6794-151">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="b6794-151">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
