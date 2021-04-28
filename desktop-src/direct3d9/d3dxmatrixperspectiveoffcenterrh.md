---
description: Função D3DXMatrixPerspectiveOffCenterRH (D3dx9math. h) – compila uma matriz de projeção de perspectiva personalizada e com o lado direito.
ms.assetid: e6826e46-fc80-41fa-b0d8-45b6797df76f
title: Função D3DXMatrixPerspectiveOffCenterRH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3d051894a6706cf8d58b81a85003666513f2a956
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118274"
---
# <a name="d3dxmatrixperspectiveoffcenterrh-function-d3dx9mathh"></a><span data-ttu-id="e3db8-103">Função D3DXMatrixPerspectiveOffCenterRH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="e3db8-103">D3DXMatrixPerspectiveOffCenterRH function (D3dx9math.h)</span></span>

<span data-ttu-id="e3db8-104">Cria uma matriz de projeção de perspectiva personalizada para o lado direito.</span><span class="sxs-lookup"><span data-stu-id="e3db8-104">Builds a customized, right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3db8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3db8-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="e3db8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3db8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3db8-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e3db8-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3db8-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e3db8-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e3db8-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="e3db8-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e3db8-110">*l* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="e3db8-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3db8-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3db8-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3db8-112">Valor x mínimo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="e3db8-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="e3db8-113">*r* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="e3db8-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3db8-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3db8-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3db8-115">Valor x máximo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="e3db8-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="e3db8-116">*b* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="e3db8-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3db8-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3db8-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3db8-118">Valor y mínimo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="e3db8-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="e3db8-119">*t* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="e3db8-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3db8-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3db8-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3db8-121">Valor y máximo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="e3db8-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="e3db8-122">*Zn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e3db8-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3db8-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3db8-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3db8-124">Valor z mínimo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="e3db8-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="e3db8-125">*ZF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e3db8-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3db8-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3db8-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3db8-127">Valor z máximo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="e3db8-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3db8-128">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e3db8-128">Return value</span></span>

<span data-ttu-id="e3db8-129">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e3db8-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e3db8-130">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é uma matriz de projeção de perspectiva de mão com o lado direito personalizada.</span><span class="sxs-lookup"><span data-stu-id="e3db8-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a customized, right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3db8-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3db8-131">Remarks</span></span>

<span data-ttu-id="e3db8-132">Todos os parâmetros da função **D3DXMatrixPerspectiveOffCenterRH** são distâncias no espaço da câmera.</span><span class="sxs-lookup"><span data-stu-id="e3db8-132">All the parameters of the **D3DXMatrixPerspectiveOffCenterRH** function are distances in camera space.</span></span> <span data-ttu-id="e3db8-133">Os parâmetros descrevem as dimensões do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="e3db8-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="e3db8-134">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="e3db8-134">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e3db8-135">Dessa forma, a função **D3DXMatrixPerspectiveOffCenterRH** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="e3db8-135">In this way, the **D3DXMatrixPerspectiveOffCenterRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="e3db8-136">Essa função usa a fórmula a seguir para calcular a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="e3db8-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0                0
0            2*zn/(t-b)   0                0
(l+r)/(r-l)  (t+b)/(t-b)  zf/(zn-zf)      -1
0            0            zn*zf/(zn-zf)    0
```



## <a name="requirements"></a><span data-ttu-id="e3db8-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3db8-137">Requirements</span></span>



| <span data-ttu-id="e3db8-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3db8-138">Requirement</span></span> | <span data-ttu-id="e3db8-139">Valor</span><span class="sxs-lookup"><span data-stu-id="e3db8-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3db8-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3db8-140">Header</span></span><br/>  | <dl> <span data-ttu-id="e3db8-141"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3db8-141"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e3db8-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3db8-142">Library</span></span><br/> | <dl> <span data-ttu-id="e3db8-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3db8-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e3db8-144">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e3db8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3db8-145">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="e3db8-145">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e3db8-146">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="e3db8-146">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="e3db8-147">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="e3db8-147">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="e3db8-148">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="e3db8-148">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="e3db8-149">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="e3db8-149">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="e3db8-150">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="e3db8-150">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
