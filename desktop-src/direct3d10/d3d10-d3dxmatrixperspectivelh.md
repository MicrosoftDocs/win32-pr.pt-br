---
description: Função D3DXMatrixPerspectiveLH (D3DX10Math. h) – compila uma matriz de projeção de perspectiva do lado esquerdo
ms.assetid: 5fd8da67-ff12-42fa-b915-b50fa2680b32
title: Função D3DXMatrixPerspectiveLH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a0f6c976f64fe64d3ca583351ae5c7c32aa958fd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109094"
---
# <a name="d3dxmatrixperspectivelh-function-d3dx10mathh"></a><span data-ttu-id="2f971-103">Função D3DXMatrixPerspectiveLH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="2f971-103">D3DXMatrixPerspectiveLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="2f971-104">Cria uma matriz de projeção de perspectiva do lado esquerdo</span><span class="sxs-lookup"><span data-stu-id="2f971-104">Builds a left-handed perspective projection matrix</span></span>

## <a name="syntax"></a><span data-ttu-id="2f971-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f971-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="2f971-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f971-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f971-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="2f971-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f971-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f971-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2f971-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="2f971-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2f971-110">*w* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="2f971-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f971-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f971-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f971-112">Largura do volume de exibição no plano de exibição próximo.</span><span class="sxs-lookup"><span data-stu-id="2f971-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="2f971-113">*h* \[\]</span><span class="sxs-lookup"><span data-stu-id="2f971-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f971-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f971-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f971-115">Altura do volume de exibição no plano de exibição próximo.</span><span class="sxs-lookup"><span data-stu-id="2f971-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="2f971-116">*Zn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2f971-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f971-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f971-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f971-118">Valor Z do plano de exibição próximo.</span><span class="sxs-lookup"><span data-stu-id="2f971-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="2f971-119">*ZF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2f971-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f971-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f971-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f971-121">Z-valor do plano de exibição distante.</span><span class="sxs-lookup"><span data-stu-id="2f971-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f971-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2f971-122">Return value</span></span>

<span data-ttu-id="2f971-123">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f971-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2f971-124">Ponteiro para uma estrutura D3DXMATRIX que é uma matriz de projeção de perspectiva do lado esquerdo.</span><span class="sxs-lookup"><span data-stu-id="2f971-124">Pointer to a D3DXMATRIX structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f971-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f971-125">Remarks</span></span>

<span data-ttu-id="2f971-126">Todos os parâmetros da função D3DXMatrixPerspectiveLH são distâncias no espaço da câmera.</span><span class="sxs-lookup"><span data-stu-id="2f971-126">All the parameters of the D3DXMatrixPerspectiveLH function are distances in camera space.</span></span> <span data-ttu-id="2f971-127">Os parâmetros descrevem as dimensões do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="2f971-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="2f971-128">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="2f971-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="2f971-129">Dessa forma, a função D3DXMatrixPerspectiveLH pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="2f971-129">In this way, the D3DXMatrixPerspectiveLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="2f971-130">Essa função usa a fórmula a seguir para calcular a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="2f971-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zf-zn)     1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="2f971-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f971-131">Requirements</span></span>



| <span data-ttu-id="2f971-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f971-132">Requirement</span></span> | <span data-ttu-id="2f971-133">Valor</span><span class="sxs-lookup"><span data-stu-id="2f971-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f971-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2f971-134">Header</span></span><br/>  | <dl> <span data-ttu-id="2f971-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f971-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="2f971-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f971-136">Library</span></span><br/> | <dl> <span data-ttu-id="2f971-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f971-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2f971-138">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2f971-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f971-139">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="2f971-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
