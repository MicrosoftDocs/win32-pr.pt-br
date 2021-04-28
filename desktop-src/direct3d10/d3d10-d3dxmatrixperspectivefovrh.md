---
description: Função D3DXMatrixPerspectiveFovRH (D3DX10Math. h) – cria uma matriz de projeção de perspectiva à direita com base em um campo de exibição.
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
ms.openlocfilehash: 38d48789bab9b968b6bcf657459c408abdba774b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109104"
---
# <a name="d3dxmatrixperspectivefovrh-function-d3dx10mathh"></a><span data-ttu-id="d7c59-103">Função D3DXMatrixPerspectiveFovRH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d7c59-103">D3DXMatrixPerspectiveFovRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="d7c59-104">Cria uma matriz de projeção de perspectiva à direita com base em um campo de visão.</span><span class="sxs-lookup"><span data-stu-id="d7c59-104">Builds a right-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7c59-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7c59-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="d7c59-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7c59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7c59-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d7c59-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7c59-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d7c59-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d7c59-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="d7c59-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d7c59-110">*fovy* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d7c59-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7c59-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7c59-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d7c59-112">Campo de exibição na direção y, em radianos.</span><span class="sxs-lookup"><span data-stu-id="d7c59-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="d7c59-113">*Aspecto* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d7c59-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7c59-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7c59-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d7c59-115">Taxa de proporção, definida como exibir largura de espaço dividida por altura.</span><span class="sxs-lookup"><span data-stu-id="d7c59-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="d7c59-116">*Zn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d7c59-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7c59-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7c59-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d7c59-118">Valor Z do plano de exibição próximo.</span><span class="sxs-lookup"><span data-stu-id="d7c59-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="d7c59-119">*ZF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d7c59-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7c59-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7c59-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d7c59-121">Z-valor do plano de exibição distante.</span><span class="sxs-lookup"><span data-stu-id="d7c59-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7c59-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d7c59-122">Return value</span></span>

<span data-ttu-id="d7c59-123">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d7c59-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d7c59-124">Ponteiro para uma estrutura D3DXMATRIX que é uma matriz de projeção de perspectiva à direita.</span><span class="sxs-lookup"><span data-stu-id="d7c59-124">Pointer to a D3DXMATRIX structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7c59-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7c59-125">Remarks</span></span>

<span data-ttu-id="d7c59-126">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="d7c59-126">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d7c59-127">Dessa forma, a função D3DXMatrixPerspectiveFovRH pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="d7c59-127">In this way, the D3DXMatrixPerspectiveFovRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="d7c59-128">Essa função computa a matriz retornada conforme mostrado.</span><span class="sxs-lookup"><span data-stu-id="d7c59-128">This function computes the returned matrix as shown.</span></span>


```
xScale     0          0              0
0        yScale       0              0
0          0      zf/(zn-zf)        -1
0          0      zn*zf/(zn-zf)      0
where:
yScale = cot(fovY/2)
    
xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="d7c59-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7c59-129">Requirements</span></span>



| <span data-ttu-id="d7c59-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7c59-130">Requirement</span></span> | <span data-ttu-id="d7c59-131">Valor</span><span class="sxs-lookup"><span data-stu-id="d7c59-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7c59-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7c59-132">Header</span></span><br/>  | <dl> <span data-ttu-id="d7c59-133"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7c59-133"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d7c59-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d7c59-134">Library</span></span><br/> | <dl> <span data-ttu-id="d7c59-135"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7c59-135"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d7c59-136">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d7c59-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7c59-137">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="d7c59-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
