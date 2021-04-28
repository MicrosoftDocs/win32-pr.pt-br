---
description: Função D3DXColorAdjustContrast (D3DX10Math. h) – ajusta o valor de contraste de uma cor.
ms.assetid: c111d3c7-19c6-4a6b-af0d-a9e1bc0bb7d9
title: Função D3DXColorAdjustContrast (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustContrast
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 09781c5c11560c3497a5af57528cf478f6259816
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113324"
---
# <a name="d3dxcoloradjustcontrast-function-d3dx10mathh"></a><span data-ttu-id="c52e9-103">Função D3DXColorAdjustContrast (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="c52e9-103">D3DXColorAdjustContrast function (D3DX10Math.h)</span></span>

<span data-ttu-id="c52e9-104">Ajusta o valor de contraste de uma cor.</span><span class="sxs-lookup"><span data-stu-id="c52e9-104">Adjusts the contrast value of a color.</span></span>

## <a name="syntax"></a><span data-ttu-id="c52e9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c52e9-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdjustContrast(
  _In_       D3DXCOLOR *pOut,
  _In_ const D3DXCOLOR *pC,
  _In_       FLOAT     c
);
```



## <a name="parameters"></a><span data-ttu-id="c52e9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c52e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c52e9-107">*pout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c52e9-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c52e9-108">Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="c52e9-108">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="c52e9-109">\[ponteiro de entrada \] para um [**D3DXCOLOR**](d3d10-d3dxcolor.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="c52e9-109">\[in, out\] Pointer to a [**D3DXCOLOR**](d3d10-d3dxcolor.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c52e9-110">*PC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c52e9-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c52e9-111">Tipo: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="c52e9-111">Type: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="c52e9-112">Ponteiro para uma estrutura de D3DXCOLOR de origem.</span><span class="sxs-lookup"><span data-stu-id="c52e9-112">Pointer to a source D3DXCOLOR structure.</span></span>

</dd> <dt>

<span data-ttu-id="c52e9-113">*c* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="c52e9-113">*c* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c52e9-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c52e9-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c52e9-115">Valor de contraste.</span><span class="sxs-lookup"><span data-stu-id="c52e9-115">Contrast value.</span></span> <span data-ttu-id="c52e9-116">Esse parâmetro interpola linearmente entre 50% de cinza e a cor, pC.</span><span class="sxs-lookup"><span data-stu-id="c52e9-116">This parameter linearly interpolates between fifty percent gray and the color, pC.</span></span> <span data-ttu-id="c52e9-117">Não há nenhum limite no valor de c.</span><span class="sxs-lookup"><span data-stu-id="c52e9-117">There are no limits on the value of c.</span></span> <span data-ttu-id="c52e9-118">Se esse parâmetro for zero, a cor retornada será de 50% de cinza.</span><span class="sxs-lookup"><span data-stu-id="c52e9-118">If this parameter is zero, then the returned color is fifty percent gray.</span></span> <span data-ttu-id="c52e9-119">Se esse parâmetro for 1, a cor retornada será a cor original.</span><span class="sxs-lookup"><span data-stu-id="c52e9-119">If this parameter is 1, then the returned color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c52e9-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c52e9-120">Return value</span></span>

<span data-ttu-id="c52e9-121">Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="c52e9-121">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="c52e9-122">Essa função retorna um ponteiro para uma estrutura D3DXCOLOR que é o resultado do ajuste de contraste.</span><span class="sxs-lookup"><span data-stu-id="c52e9-122">This function returns a pointer to a D3DXCOLOR structure that is the result of the contrast adjustment.</span></span>

## <a name="remarks"></a><span data-ttu-id="c52e9-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="c52e9-123">Remarks</span></span>

<span data-ttu-id="c52e9-124">O canal alfa de entrada é copiado, não modificado, para o canal alfa de saída.</span><span class="sxs-lookup"><span data-stu-id="c52e9-124">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="c52e9-125">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="c52e9-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="c52e9-126">Dessa forma, essa função pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="c52e9-126">In this way, this function can be used as a parameter for another function.</span></span>

<span data-ttu-id="c52e9-127">Essa função interpola os componentes de cor vermelho, verde e azul de uma estrutura D3DXCOLOR entre 50% de cinza e um valor de contraste especificado, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="c52e9-127">This function interpolates the red, green, and blue color components of a D3DXCOLOR structure between fifty percent gray and a specified contrast value, as shown in the following example.</span></span>


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



<span data-ttu-id="c52e9-128">Se c for maior que 0 e menor que 1, o contraste será diminuído.</span><span class="sxs-lookup"><span data-stu-id="c52e9-128">If c is greater than 0 and less than 1, the contrast is decreased.</span></span> <span data-ttu-id="c52e9-129">Se c for maior que 1, o contraste será aumentado.</span><span class="sxs-lookup"><span data-stu-id="c52e9-129">If c is greater than 1, the contrast is increased.</span></span>

## <a name="requirements"></a><span data-ttu-id="c52e9-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c52e9-130">Requirements</span></span>



| <span data-ttu-id="c52e9-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c52e9-131">Requirement</span></span> | <span data-ttu-id="c52e9-132">Valor</span><span class="sxs-lookup"><span data-stu-id="c52e9-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c52e9-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c52e9-133">Header</span></span><br/>  | <dl> <span data-ttu-id="c52e9-134"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c52e9-134"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="c52e9-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c52e9-135">Library</span></span><br/> | <dl> <span data-ttu-id="c52e9-136"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c52e9-136"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c52e9-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c52e9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c52e9-138">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="c52e9-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
