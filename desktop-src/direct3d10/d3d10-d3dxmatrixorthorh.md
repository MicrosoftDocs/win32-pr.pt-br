---
description: Cria uma matriz de projeção ortográfica de mão direita.
ms.assetid: e6673ff4-06a2-4a16-b72e-5ca69ddf2438
title: Função D3DXMatrixOrthoRH (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2a8883f2690fa5a5f0bfa1bb1570163b714974b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765164"
---
# <a name="d3dxmatrixorthorh-function-d3dx10mathh"></a><span data-ttu-id="76111-103">Função D3DXMatrixOrthoRH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="76111-103">D3DXMatrixOrthoRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="76111-104">Cria uma matriz de projeção ortográfica de mão direita.</span><span class="sxs-lookup"><span data-stu-id="76111-104">Builds a right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="76111-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76111-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="76111-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76111-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76111-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="76111-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="76111-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="76111-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="76111-109">Ponteiro para o [**D3DXMATRIX**](d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="76111-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="76111-110">*w* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="76111-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76111-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76111-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76111-112">Largura do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="76111-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="76111-113">*h* \[\]</span><span class="sxs-lookup"><span data-stu-id="76111-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76111-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76111-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76111-115">Altura do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="76111-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="76111-116">*Zn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="76111-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76111-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76111-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76111-118">Valor z mínimo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="76111-118">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="76111-119">*ZF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="76111-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76111-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76111-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76111-121">Valor z máximo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="76111-121">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76111-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="76111-122">Return value</span></span>

<span data-ttu-id="76111-123">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="76111-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="76111-124">Ponteiro para o [**D3DXMATRIX**](d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="76111-124">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="76111-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="76111-125">Remarks</span></span>

<span data-ttu-id="76111-126">Todos os parâmetros da função D3DXMatrixOrthoRH são distâncias no espaço da câmera.</span><span class="sxs-lookup"><span data-stu-id="76111-126">All the parameters of the D3DXMatrixOrthoRH function are distances in camera space.</span></span> <span data-ttu-id="76111-127">Os parâmetros descrevem as dimensões do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="76111-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="76111-128">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="76111-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="76111-129">Dessa forma, a função D3DXMatrixOrthoRH pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="76111-129">In this way, the D3DXMatrixOrthoRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="76111-130">Essa função usa a fórmula a seguir para calcular a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="76111-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zn-zf)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="76111-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76111-131">Requirements</span></span>



| <span data-ttu-id="76111-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="76111-132">Requirement</span></span> | <span data-ttu-id="76111-133">Valor</span><span class="sxs-lookup"><span data-stu-id="76111-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76111-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="76111-134">Header</span></span><br/>  | <dl> <span data-ttu-id="76111-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="76111-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="76111-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="76111-136">Library</span></span><br/> | <dl> <span data-ttu-id="76111-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76111-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="76111-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="76111-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76111-139">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="76111-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
