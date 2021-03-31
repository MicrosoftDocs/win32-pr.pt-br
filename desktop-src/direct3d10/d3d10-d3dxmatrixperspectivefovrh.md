---
description: Cria uma matriz de projeção de perspectiva à direita com base em um campo de visão.
ms.assetid: a75e6666-e6c0-4a54-bc88-835fa012542f
title: Função D3DXMatrixPerspectiveFovRH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveFovRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: baad02b5840af8e244cd562def4aeb8f9ac2988a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930672"
---
# <a name="d3dxmatrixperspectivefovrh-function-d3dx10mathh"></a><span data-ttu-id="e5583-103">Função D3DXMatrixPerspectiveFovRH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="e5583-103">D3DXMatrixPerspectiveFovRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="e5583-104">Cria uma matriz de projeção de perspectiva à direita com base em um campo de visão.</span><span class="sxs-lookup"><span data-stu-id="e5583-104">Builds a right-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5583-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5583-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="e5583-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5583-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5583-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e5583-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5583-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e5583-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e5583-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="e5583-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e5583-110">*fovy* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5583-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5583-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5583-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5583-112">Campo de exibição na direção y, em radianos.</span><span class="sxs-lookup"><span data-stu-id="e5583-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="e5583-113">*Aspecto* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5583-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5583-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5583-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5583-115">Taxa de proporção, definida como exibir largura de espaço dividida por altura.</span><span class="sxs-lookup"><span data-stu-id="e5583-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="e5583-116">*Zn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5583-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5583-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5583-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5583-118">Valor Z do plano de exibição próximo.</span><span class="sxs-lookup"><span data-stu-id="e5583-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="e5583-119">*ZF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5583-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5583-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5583-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5583-121">Z-valor do plano de exibição distante.</span><span class="sxs-lookup"><span data-stu-id="e5583-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5583-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e5583-122">Return value</span></span>

<span data-ttu-id="e5583-123">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e5583-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e5583-124">Ponteiro para uma estrutura D3DXMATRIX que é uma matriz de projeção de perspectiva à direita.</span><span class="sxs-lookup"><span data-stu-id="e5583-124">Pointer to a D3DXMATRIX structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5583-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5583-125">Remarks</span></span>

<span data-ttu-id="e5583-126">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="e5583-126">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="e5583-127">Dessa forma, a função D3DXMatrixPerspectiveFovRH pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="e5583-127">In this way, the D3DXMatrixPerspectiveFovRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="e5583-128">Essa função computa a matriz retornada conforme mostrado.</span><span class="sxs-lookup"><span data-stu-id="e5583-128">This function computes the returned matrix as shown.</span></span>


```
xScale     0          0              0
0        yScale       0              0
0          0      zf/(zn-zf)        -1
0          0      zn*zf/(zn-zf)      0
where:
yScale = cot(fovY/2)
    
xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="e5583-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5583-129">Requirements</span></span>



| <span data-ttu-id="e5583-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5583-130">Requirement</span></span> | <span data-ttu-id="e5583-131">Valor</span><span class="sxs-lookup"><span data-stu-id="e5583-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5583-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e5583-132">Header</span></span><br/>  | <dl> <span data-ttu-id="e5583-133"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5583-133"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="e5583-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e5583-134">Library</span></span><br/> | <dl> <span data-ttu-id="e5583-135"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5583-135"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e5583-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5583-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5583-137">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="e5583-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
