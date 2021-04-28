---
description: Função D3DXMatrixPerspectiveOffCenterLH (D3dx9math. h) – compila uma matriz de projeção de perspectiva de mão esquerda personalizada.
ms.assetid: de2732dd-a4f2-47bc-9509-de16f1ca85c2
title: Função D3DXMatrixPerspectiveOffCenterLH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 404147cfbab0b4fedb7c7356dc1c31d3e203eb5f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118284"
---
# <a name="d3dxmatrixperspectiveoffcenterlh-function-d3dx9mathh"></a><span data-ttu-id="00605-103">Função D3DXMatrixPerspectiveOffCenterLH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="00605-103">D3DXMatrixPerspectiveOffCenterLH function (D3dx9math.h)</span></span>

<span data-ttu-id="00605-104">Cria uma matriz de projeção de perspectiva personalizada para o lado esquerdo.</span><span class="sxs-lookup"><span data-stu-id="00605-104">Builds a customized, left-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="00605-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00605-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="00605-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00605-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00605-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="00605-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="00605-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="00605-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="00605-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="00605-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="00605-110">*l* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="00605-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00605-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00605-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00605-112">Valor x mínimo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="00605-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="00605-113">*r* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="00605-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00605-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00605-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00605-115">Valor x máximo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="00605-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="00605-116">*b* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="00605-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00605-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00605-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00605-118">Valor y mínimo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="00605-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="00605-119">*t* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="00605-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00605-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00605-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00605-121">Valor y máximo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="00605-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="00605-122">*Zn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="00605-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00605-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00605-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00605-124">Valor z mínimo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="00605-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="00605-125">*ZF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="00605-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00605-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00605-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00605-127">Valor z máximo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="00605-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00605-128">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="00605-128">Return value</span></span>

<span data-ttu-id="00605-129">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="00605-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="00605-130">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é uma matriz de projeção de perspectiva de mão da esquerda personalizada.</span><span class="sxs-lookup"><span data-stu-id="00605-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a customized, left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="00605-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="00605-131">Remarks</span></span>

<span data-ttu-id="00605-132">Todos os parâmetros da função **D3DXMatrixPerspectiveOffCenterLH** são distâncias no espaço da câmera.</span><span class="sxs-lookup"><span data-stu-id="00605-132">All the parameters of the **D3DXMatrixPerspectiveOffCenterLH** function are distances in camera space.</span></span> <span data-ttu-id="00605-133">Os parâmetros descrevem as dimensões do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="00605-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="00605-134">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="00605-134">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="00605-135">Dessa forma, a função **D3DXMatrixPerspectiveOffCenterLH** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="00605-135">In this way, the **D3DXMatrixPerspectiveOffCenterLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="00605-136">Essa função usa a fórmula a seguir para calcular a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="00605-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0              0
0            2*zn/(t-b)   0              0
(l+r)/(l-r)  (t+b)/(b-t)  zf/(zf-zn)     1
0            0            zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="00605-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00605-137">Requirements</span></span>



| <span data-ttu-id="00605-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="00605-138">Requirement</span></span> | <span data-ttu-id="00605-139">Valor</span><span class="sxs-lookup"><span data-stu-id="00605-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00605-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="00605-140">Header</span></span><br/>  | <dl> <span data-ttu-id="00605-141"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="00605-141"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="00605-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="00605-142">Library</span></span><br/> | <dl> <span data-ttu-id="00605-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00605-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="00605-144">Consulte também</span><span class="sxs-lookup"><span data-stu-id="00605-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00605-145">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="00605-145">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="00605-146">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="00605-146">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="00605-147">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="00605-147">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="00605-148">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="00605-148">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="00605-149">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="00605-149">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="00605-150">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="00605-150">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> </dl>

 

 
