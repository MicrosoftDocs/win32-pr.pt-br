---
description: Função D3DXMatrixPerspectiveRH (D3DX10Math. h) – compila uma matriz de projeção de perspectiva à direita.
ms.assetid: 324c8a21-24ef-4b3a-aac1-a753e26076d4
title: Função D3DXMatrixPerspectiveRH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 03ffd99d016023612daa3de96ae29275d71074a0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109004"
---
# <a name="d3dxmatrixperspectiverh-function-d3dx10mathh"></a><span data-ttu-id="1a8d0-103">Função D3DXMatrixPerspectiveRH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="1a8d0-103">D3DXMatrixPerspectiveRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="1a8d0-104">Cria uma matriz de projeção de perspectiva à direita.</span><span class="sxs-lookup"><span data-stu-id="1a8d0-104">Builds a right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a8d0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a8d0-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="1a8d0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a8d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a8d0-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="1a8d0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a8d0-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1a8d0-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1a8d0-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="1a8d0-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1a8d0-110">*w* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="1a8d0-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a8d0-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a8d0-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a8d0-112">Largura do volume de exibição no plano de exibição próximo.</span><span class="sxs-lookup"><span data-stu-id="1a8d0-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="1a8d0-113">*h* \[\]</span><span class="sxs-lookup"><span data-stu-id="1a8d0-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a8d0-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a8d0-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a8d0-115">Altura do volume de exibição no plano de exibição próximo.</span><span class="sxs-lookup"><span data-stu-id="1a8d0-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="1a8d0-116">*Zn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1a8d0-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a8d0-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a8d0-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a8d0-118">Valor Z do plano de exibição próximo.</span><span class="sxs-lookup"><span data-stu-id="1a8d0-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="1a8d0-119">*ZF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1a8d0-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a8d0-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a8d0-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a8d0-121">Z-valor do plano de exibição distante.</span><span class="sxs-lookup"><span data-stu-id="1a8d0-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a8d0-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1a8d0-122">Return value</span></span>

<span data-ttu-id="1a8d0-123">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1a8d0-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1a8d0-124">Ponteiro para uma estrutura D3DXMATRIX que é uma matriz de projeção de perspectiva à direita.</span><span class="sxs-lookup"><span data-stu-id="1a8d0-124">Pointer to a D3DXMATRIX structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a8d0-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a8d0-125">Remarks</span></span>

<span data-ttu-id="1a8d0-126">Todos os parâmetros da função D3DXMatrixPerspectiveRH são distâncias no espaço da câmera.</span><span class="sxs-lookup"><span data-stu-id="1a8d0-126">All the parameters of the D3DXMatrixPerspectiveRH function are distances in camera space.</span></span> <span data-ttu-id="1a8d0-127">Os parâmetros descrevem as dimensões do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="1a8d0-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="1a8d0-128">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="1a8d0-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1a8d0-129">Dessa forma, a função D3DXMatrixPerspectiveRH pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="1a8d0-129">In this way, the D3DXMatrixPerspectiveRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1a8d0-130">Essa função usa a fórmula a seguir para calcular a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="1a8d0-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zn-zf)    -1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="1a8d0-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a8d0-131">Requirements</span></span>



| <span data-ttu-id="1a8d0-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a8d0-132">Requirement</span></span> | <span data-ttu-id="1a8d0-133">Valor</span><span class="sxs-lookup"><span data-stu-id="1a8d0-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a8d0-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1a8d0-134">Header</span></span><br/>  | <dl> <span data-ttu-id="1a8d0-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a8d0-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1a8d0-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1a8d0-136">Library</span></span><br/> | <dl> <span data-ttu-id="1a8d0-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a8d0-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1a8d0-138">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1a8d0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a8d0-139">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="1a8d0-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
