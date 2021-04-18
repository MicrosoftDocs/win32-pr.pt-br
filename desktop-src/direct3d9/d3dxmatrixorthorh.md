---
description: Cria uma matriz de projeção ortográfica de mão direita.
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
ms.openlocfilehash: 00df0ee06768e4d57a68291dd1716e4a4574507e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771350"
---
# <a name="d3dxmatrixorthorh-function-d3dx9mathh"></a><span data-ttu-id="e7146-103">Função D3DXMatrixOrthoRH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="e7146-103">D3DXMatrixOrthoRH function (D3dx9math.h)</span></span>

<span data-ttu-id="e7146-104">Cria uma matriz de projeção ortográfica de mão direita.</span><span class="sxs-lookup"><span data-stu-id="e7146-104">Builds a right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7146-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7146-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="e7146-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7146-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7146-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e7146-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7146-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7146-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e7146-109">Ponteiro para o [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="e7146-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7146-110">*w* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="e7146-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7146-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7146-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7146-112">Largura do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="e7146-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="e7146-113">*h* \[\]</span><span class="sxs-lookup"><span data-stu-id="e7146-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7146-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7146-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7146-115">Altura do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="e7146-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="e7146-116">*Zn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7146-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7146-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7146-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7146-118">Valor z mínimo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="e7146-118">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="e7146-119">*ZF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7146-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7146-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7146-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7146-121">Valor z máximo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="e7146-121">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7146-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7146-122">Return value</span></span>

<span data-ttu-id="e7146-123">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7146-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e7146-124">Ponteiro para o [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="e7146-124">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e7146-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7146-125">Remarks</span></span>

<span data-ttu-id="e7146-126">Todos os parâmetros da função **D3DXMatrixOrthoRH** são distâncias no espaço da câmera.</span><span class="sxs-lookup"><span data-stu-id="e7146-126">All the parameters of the **D3DXMatrixOrthoRH** function are distances in camera space.</span></span> <span data-ttu-id="e7146-127">Os parâmetros descrevem as dimensões do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="e7146-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="e7146-128">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="e7146-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e7146-129">Dessa forma, a função **D3DXMatrixOrthoRH** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="e7146-129">In this way, the **D3DXMatrixOrthoRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="e7146-130">Essa função usa a fórmula a seguir para calcular a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="e7146-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zn-zf)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="e7146-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7146-131">Requirements</span></span>



| <span data-ttu-id="e7146-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7146-132">Requirement</span></span> | <span data-ttu-id="e7146-133">Valor</span><span class="sxs-lookup"><span data-stu-id="e7146-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7146-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7146-134">Header</span></span><br/>  | <dl> <span data-ttu-id="e7146-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7146-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e7146-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e7146-136">Library</span></span><br/> | <dl> <span data-ttu-id="e7146-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7146-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e7146-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7146-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7146-139">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="e7146-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e7146-140">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="e7146-140">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="e7146-141">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="e7146-141">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="e7146-142">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="e7146-142">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
