---
description: Cria uma matriz de projeção ortográfica de mão esquerda.
ms.assetid: 67bec4a3-2126-4f5a-9301-97faa6dc6e84
title: Função D3DXMatrixOrthoLH (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0b49e6008b52f7060075688730c72f5f5d3f725a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173151"
---
# <a name="d3dxmatrixortholh-function-d3dx10mathh"></a><span data-ttu-id="12b1a-103">Função D3DXMatrixOrthoLH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="12b1a-103">D3DXMatrixOrthoLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="12b1a-104">Cria uma matriz de projeção ortográfica de mão esquerda.</span><span class="sxs-lookup"><span data-stu-id="12b1a-104">Builds a left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="12b1a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12b1a-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="12b1a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12b1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12b1a-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="12b1a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="12b1a-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="12b1a-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="12b1a-109">Ponteiro para o [**D3DXMATRIX**](d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="12b1a-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="12b1a-110">*w* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="12b1a-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12b1a-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12b1a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12b1a-112">Largura do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="12b1a-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="12b1a-113">*h* \[\]</span><span class="sxs-lookup"><span data-stu-id="12b1a-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12b1a-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12b1a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12b1a-115">Altura do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="12b1a-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="12b1a-116">*Zn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12b1a-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12b1a-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12b1a-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12b1a-118">Valor z mínimo do volume de exibição que é referido como z-Near.</span><span class="sxs-lookup"><span data-stu-id="12b1a-118">Minimum z-value of the view volume which is referred to as z-near.</span></span>

</dd> <dt>

<span data-ttu-id="12b1a-119">*ZF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12b1a-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12b1a-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12b1a-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12b1a-121">Valor z máximo do volume de exibição que é referido como z-far.</span><span class="sxs-lookup"><span data-stu-id="12b1a-121">Maximum z-value of the view volume which is referred to as z-far.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12b1a-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12b1a-122">Return value</span></span>

<span data-ttu-id="12b1a-123">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="12b1a-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="12b1a-124">Ponteiro para o [**D3DXMATRIX**](d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="12b1a-124">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="12b1a-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="12b1a-125">Remarks</span></span>

<span data-ttu-id="12b1a-126">Todos os parâmetros da função D3DXMatrixOrthoLH são distâncias no espaço da câmera.</span><span class="sxs-lookup"><span data-stu-id="12b1a-126">All the parameters of the D3DXMatrixOrthoLH function are distances in camera space.</span></span> <span data-ttu-id="12b1a-127">Os parâmetros descrevem as dimensões do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="12b1a-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="12b1a-128">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="12b1a-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="12b1a-129">Dessa forma, a função D3DXMatrixOrthoLH pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="12b1a-129">In this way, the D3DXMatrixOrthoLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="12b1a-130">Essa função usa a fórmula a seguir para calcular a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="12b1a-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="12b1a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12b1a-131">Requirements</span></span>



| <span data-ttu-id="12b1a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="12b1a-132">Requirement</span></span> | <span data-ttu-id="12b1a-133">Valor</span><span class="sxs-lookup"><span data-stu-id="12b1a-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12b1a-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12b1a-134">Header</span></span><br/>  | <dl> <span data-ttu-id="12b1a-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="12b1a-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="12b1a-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="12b1a-136">Library</span></span><br/> | <dl> <span data-ttu-id="12b1a-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12b1a-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="12b1a-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="12b1a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12b1a-139">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="12b1a-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
