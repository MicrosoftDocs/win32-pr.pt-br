---
description: Cria uma matriz de projeção de perspectiva à esquerda com base em um campo de visão.
ms.assetid: 35ee12d6-0a58-4b00-ac8f-82f82215f02e
title: Função D3DXMatrixPerspectiveFovLH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveFovLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 141c0a1468b2e073881976738cbd2a10b6108edc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793994"
---
# <a name="d3dxmatrixperspectivefovlh-function-d3dx10mathh"></a><span data-ttu-id="e5f54-103">Função D3DXMatrixPerspectiveFovLH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="e5f54-103">D3DXMatrixPerspectiveFovLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="e5f54-104">Cria uma matriz de projeção de perspectiva à esquerda com base em um campo de visão.</span><span class="sxs-lookup"><span data-stu-id="e5f54-104">Builds a left-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5f54-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5f54-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="e5f54-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5f54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5f54-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e5f54-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5f54-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e5f54-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e5f54-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="e5f54-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e5f54-110">*fovy* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5f54-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5f54-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5f54-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5f54-112">Campo de exibição na direção y, em radianos.</span><span class="sxs-lookup"><span data-stu-id="e5f54-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="e5f54-113">*Aspecto* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5f54-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5f54-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5f54-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5f54-115">Taxa de proporção, definida como exibir largura de espaço dividida por altura.</span><span class="sxs-lookup"><span data-stu-id="e5f54-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="e5f54-116">*Zn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5f54-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5f54-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5f54-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5f54-118">Valor Z do plano de exibição próximo.</span><span class="sxs-lookup"><span data-stu-id="e5f54-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="e5f54-119">*ZF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5f54-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5f54-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5f54-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5f54-121">Z-valor do plano de exibição distante.</span><span class="sxs-lookup"><span data-stu-id="e5f54-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5f54-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e5f54-122">Return value</span></span>

<span data-ttu-id="e5f54-123">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e5f54-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e5f54-124">Ponteiro para uma estrutura D3DXMATRIX que é uma matriz de projeção de perspectiva do lado esquerdo.</span><span class="sxs-lookup"><span data-stu-id="e5f54-124">Pointer to a D3DXMATRIX structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5f54-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5f54-125">Remarks</span></span>

<span data-ttu-id="e5f54-126">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="e5f54-126">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="e5f54-127">Dessa forma, a função D3DXMatrixPerspectiveFovLH pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="e5f54-127">In this way, the D3DXMatrixPerspectiveFovLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="e5f54-128">Essa função computa a matriz retornada, conforme mostrado:</span><span class="sxs-lookup"><span data-stu-id="e5f54-128">This function computes the returned matrix as shown:</span></span>


```
xScale     0          0               0
0        yScale       0               0
0          0       zf/(zf-zn)         1
0          0       -zn*zf/(zf-zn)     0
where:
yScale = cot(fovY/2)

xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="e5f54-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5f54-129">Requirements</span></span>



| <span data-ttu-id="e5f54-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5f54-130">Requirement</span></span> | <span data-ttu-id="e5f54-131">Valor</span><span class="sxs-lookup"><span data-stu-id="e5f54-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5f54-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e5f54-132">Header</span></span><br/>  | <dl> <span data-ttu-id="e5f54-133"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5f54-133"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="e5f54-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e5f54-134">Library</span></span><br/> | <dl> <span data-ttu-id="e5f54-135"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5f54-135"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e5f54-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5f54-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5f54-137">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="e5f54-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
