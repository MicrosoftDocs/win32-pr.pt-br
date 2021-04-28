---
description: Função D3DXMatrixOrthoRH (D3dx9math. h) – compila uma matriz de projeção ortográfica de mão direita.
ms.assetid: 6b9b50d5-0307-4fc7-a28d-8f42d2a21bf0
title: Função D3DXMatrixOrthoRH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d34a8379851d80ae8734c7f32cc0dc5977af2088
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107434"
---
# <a name="d3dxmatrixorthorh-function-d3dx9mathh"></a><span data-ttu-id="04549-103">Função D3DXMatrixOrthoRH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="04549-103">D3DXMatrixOrthoRH function (D3dx9math.h)</span></span>

<span data-ttu-id="04549-104">Cria uma matriz de projeção ortográfica de mão direita.</span><span class="sxs-lookup"><span data-stu-id="04549-104">Builds a right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="04549-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04549-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="04549-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04549-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04549-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="04549-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="04549-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="04549-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="04549-109">Ponteiro para o [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="04549-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="04549-110">*w* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="04549-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04549-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="04549-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="04549-112">Largura do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="04549-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="04549-113">*h* \[\]</span><span class="sxs-lookup"><span data-stu-id="04549-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04549-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="04549-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="04549-115">Altura do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="04549-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="04549-116">*Zn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="04549-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04549-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="04549-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="04549-118">Valor z mínimo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="04549-118">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="04549-119">*ZF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="04549-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04549-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="04549-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="04549-121">Valor z máximo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="04549-121">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04549-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="04549-122">Return value</span></span>

<span data-ttu-id="04549-123">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="04549-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="04549-124">Ponteiro para o [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="04549-124">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="04549-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="04549-125">Remarks</span></span>

<span data-ttu-id="04549-126">Todos os parâmetros da função **D3DXMatrixOrthoRH** são distâncias no espaço da câmera.</span><span class="sxs-lookup"><span data-stu-id="04549-126">All the parameters of the **D3DXMatrixOrthoRH** function are distances in camera space.</span></span> <span data-ttu-id="04549-127">Os parâmetros descrevem as dimensões do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="04549-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="04549-128">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="04549-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="04549-129">Dessa forma, a função **D3DXMatrixOrthoRH** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="04549-129">In this way, the **D3DXMatrixOrthoRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="04549-130">Essa função usa a fórmula a seguir para calcular a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="04549-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zn-zf)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="04549-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04549-131">Requirements</span></span>



| <span data-ttu-id="04549-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="04549-132">Requirement</span></span> | <span data-ttu-id="04549-133">Valor</span><span class="sxs-lookup"><span data-stu-id="04549-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04549-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="04549-134">Header</span></span><br/>  | <dl> <span data-ttu-id="04549-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="04549-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="04549-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="04549-136">Library</span></span><br/> | <dl> <span data-ttu-id="04549-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04549-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="04549-138">Consulte também</span><span class="sxs-lookup"><span data-stu-id="04549-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04549-139">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="04549-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="04549-140">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="04549-140">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="04549-141">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="04549-141">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="04549-142">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="04549-142">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
