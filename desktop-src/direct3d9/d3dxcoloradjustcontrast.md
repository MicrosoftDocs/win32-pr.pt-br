---
description: Função D3DXColorAdjustContrast (D3dx9math. h) – ajusta o valor de contraste de uma cor.
ms.assetid: be49c9c7-b625-4cbc-bd63-1d5766ae2dbb
title: Função D3DXColorAdjustContrast (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9dc9bb79d1ebbe536661347d76d13846dead6aa8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115874"
---
# <a name="d3dxcoloradjustcontrast-function-d3dx9mathh"></a><span data-ttu-id="eafcd-103">Função D3DXColorAdjustContrast (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="eafcd-103">D3DXColorAdjustContrast function (D3dx9math.h)</span></span>

<span data-ttu-id="eafcd-104">Ajusta o valor de contraste de uma cor.</span><span class="sxs-lookup"><span data-stu-id="eafcd-104">Adjusts the contrast value of a color.</span></span>

## <a name="syntax"></a><span data-ttu-id="eafcd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eafcd-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdjustContrast(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     c
);
```



## <a name="parameters"></a><span data-ttu-id="eafcd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eafcd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eafcd-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="eafcd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eafcd-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="eafcd-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="eafcd-109">Ponteiro para uma estrutura [**D3DXCOLOR**](d3dxcolor.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="eafcd-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="eafcd-110">*PC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eafcd-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eafcd-111">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="eafcd-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="eafcd-112">Ponteiro para uma estrutura de [**D3DXCOLOR**](d3dxcolor.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="eafcd-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="eafcd-113">*c* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="eafcd-113">*c* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eafcd-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eafcd-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eafcd-115">Valor de contraste.</span><span class="sxs-lookup"><span data-stu-id="eafcd-115">Contrast value.</span></span> <span data-ttu-id="eafcd-116">Esse parâmetro interpola linearmente entre 50% de cinza e a cor, pC.</span><span class="sxs-lookup"><span data-stu-id="eafcd-116">This parameter linearly interpolates between fifty percent gray and the color, pC.</span></span> <span data-ttu-id="eafcd-117">Não há limites no valor de c.</span><span class="sxs-lookup"><span data-stu-id="eafcd-117">There are not limits on the value of c.</span></span> <span data-ttu-id="eafcd-118">Se esse parâmetro for zero, a cor retornada será de 50% de cinza.</span><span class="sxs-lookup"><span data-stu-id="eafcd-118">If this parameter is zero, then the returned color is fifty percent gray.</span></span> <span data-ttu-id="eafcd-119">Se esse parâmetro for 1, a cor retornada será a cor original.</span><span class="sxs-lookup"><span data-stu-id="eafcd-119">If this parameter is 1, then the returned color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eafcd-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="eafcd-120">Return value</span></span>

<span data-ttu-id="eafcd-121">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="eafcd-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="eafcd-122">Essa função retorna um ponteiro para uma estrutura [**D3DXCOLOR**](d3dxcolor.md) que é o resultado do ajuste de contraste.</span><span class="sxs-lookup"><span data-stu-id="eafcd-122">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the contrast adjustment.</span></span>

## <a name="remarks"></a><span data-ttu-id="eafcd-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="eafcd-123">Remarks</span></span>

<span data-ttu-id="eafcd-124">O canal alfa de entrada é copiado, não modificado, para o canal alfa de saída.</span><span class="sxs-lookup"><span data-stu-id="eafcd-124">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="eafcd-125">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="eafcd-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="eafcd-126">Dessa forma, essa função pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="eafcd-126">In this way, this function can be used as a parameter for another function.</span></span>

<span data-ttu-id="eafcd-127">Essa função interpola os componentes de cor vermelho, verde e azul de uma estrutura [**D3DXCOLOR**](d3dxcolor.md) entre 50% de cinza e um valor de contraste especificado, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="eafcd-127">This function interpolates the red, green, and blue color components of a [**D3DXCOLOR**](d3dxcolor.md) structure between fifty percent gray and a specified contrast value, as shown in the following example.</span></span>


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



<span data-ttu-id="eafcd-128">Se c for maior que 0 e menor que 1, o contraste será diminuído.</span><span class="sxs-lookup"><span data-stu-id="eafcd-128">If c is greater than 0 and less than 1, the contrast is decreased.</span></span> <span data-ttu-id="eafcd-129">Se c for maior que 1, o contraste será aumentado.</span><span class="sxs-lookup"><span data-stu-id="eafcd-129">If c is greater than 1, the contrast is increased.</span></span>

## <a name="requirements"></a><span data-ttu-id="eafcd-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eafcd-130">Requirements</span></span>



| <span data-ttu-id="eafcd-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="eafcd-131">Requirement</span></span> | <span data-ttu-id="eafcd-132">Valor</span><span class="sxs-lookup"><span data-stu-id="eafcd-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eafcd-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eafcd-133">Header</span></span><br/>  | <dl> <span data-ttu-id="eafcd-134"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="eafcd-134"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="eafcd-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eafcd-135">Library</span></span><br/> | <dl> <span data-ttu-id="eafcd-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eafcd-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eafcd-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="eafcd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eafcd-138">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="eafcd-138">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="eafcd-139">**D3DXColorAdjustSaturation**</span><span class="sxs-lookup"><span data-stu-id="eafcd-139">**D3DXColorAdjustSaturation**</span></span>](d3dxcoloradjustsaturation.md)
</dt> </dl>

 

 
