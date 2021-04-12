---
description: Representa um valor de cor com Alfa, que é usado para transparência.
ms.assetid: 27A86A10-FC0E-421E-BEA7-2DEB539849BB
title: Estrutura D3DCOLORVALUE (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLORVALUE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 2b7d768af9e471f3183c6a400622c2b0e0719a2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298601"
---
# <a name="d3dcolorvalue-structure-dxgitypeh"></a><span data-ttu-id="65b11-103">Estrutura D3DCOLORVALUE (Dxgitype. h)</span><span class="sxs-lookup"><span data-stu-id="65b11-103">D3DCOLORVALUE structure (Dxgitype.h)</span></span>

<span data-ttu-id="65b11-104">Representa um valor de cor com Alfa, que é usado para transparência.</span><span class="sxs-lookup"><span data-stu-id="65b11-104">Represents a color value with alpha, which is used for transparency.</span></span>

## <a name="syntax"></a><span data-ttu-id="65b11-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65b11-105">Syntax</span></span>


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a><span data-ttu-id="65b11-106">Membros</span><span class="sxs-lookup"><span data-stu-id="65b11-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="65b11-107">**r**</span><span class="sxs-lookup"><span data-stu-id="65b11-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="65b11-108">Valor de ponto flutuante que especifica o componente vermelho de uma cor.</span><span class="sxs-lookup"><span data-stu-id="65b11-108">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="65b11-109">Esse valor geralmente está no intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="65b11-109">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="65b11-110">Um valor de 0,0 indica a ausência completa do componente vermelho, enquanto um valor de 1,0 indica que o vermelho está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="65b11-110">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="65b11-111">**m**</span><span class="sxs-lookup"><span data-stu-id="65b11-111">**g**</span></span>
</dt> <dd>

<span data-ttu-id="65b11-112">Valor de ponto flutuante que especifica o componente verde de uma cor.</span><span class="sxs-lookup"><span data-stu-id="65b11-112">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="65b11-113">Esse valor geralmente está no intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="65b11-113">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="65b11-114">Um valor de 0,0 indica a ausência completa do componente verde, enquanto um valor de 1,0 indica que o verde está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="65b11-114">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="65b11-115">**b**</span><span class="sxs-lookup"><span data-stu-id="65b11-115">**b**</span></span>
</dt> <dd>

<span data-ttu-id="65b11-116">Valor de ponto flutuante que especifica o componente azul de uma cor.</span><span class="sxs-lookup"><span data-stu-id="65b11-116">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="65b11-117">Esse valor geralmente está no intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="65b11-117">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="65b11-118">Um valor de 0,0 indica a ausência completa do componente azul, enquanto um valor de 1,0 indica que o azul está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="65b11-118">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="65b11-119">**um**</span><span class="sxs-lookup"><span data-stu-id="65b11-119">**a**</span></span>
</dt> <dd>

<span data-ttu-id="65b11-120">Valor de ponto flutuante que especifica o componente alfa de uma cor.</span><span class="sxs-lookup"><span data-stu-id="65b11-120">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="65b11-121">Esse valor geralmente está no intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="65b11-121">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="65b11-122">Um valor de 0,0 indica totalmente transparente, enquanto um valor de 1,0 indica totalmente opaco.</span><span class="sxs-lookup"><span data-stu-id="65b11-122">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65b11-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="65b11-123">Remarks</span></span>

<span data-ttu-id="65b11-124">Você pode definir os membros dessa estrutura com valores fora do intervalo de 0 a 1 para implementar alguns efeitos incomuns.</span><span class="sxs-lookup"><span data-stu-id="65b11-124">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="65b11-125">Valores maiores que 1 produzem luzes fortes que tendem a desbotar uma cena.</span><span class="sxs-lookup"><span data-stu-id="65b11-125">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="65b11-126">Valores negativos produzem luzes escuras que realmente removem a luz de uma cena.</span><span class="sxs-lookup"><span data-stu-id="65b11-126">Negative values produce dark lights that actually remove light from a scene.</span></span>

<span data-ttu-id="65b11-127">O tipo de cabeçalho DXGItype. h – define [**dxgi \_ RGBA**](dxgi-rgba.md) como um alias de **D3DCOLORVALUE**, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="65b11-127">The DXGItype.h header type-defines [**DXGI\_RGBA**](dxgi-rgba.md) as an alias of **D3DCOLORVALUE**, as follows:</span></span>


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



<span data-ttu-id="65b11-128">Você pode usar D3DCOLORVALUE ou [**dxgi \_ RGBA**](dxgi-rgba.md) com o [**\_ \_ modo alfa**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode) [**IDXGISwapChain1:: setBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1:: getBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)e dxgi.</span><span class="sxs-lookup"><span data-stu-id="65b11-128">You can use D3DCOLORVALUE or [**DXGI\_RGBA**](dxgi-rgba.md) with [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor), and [**DXGI\_ALPHA\_MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span></span>

## <a name="requirements"></a><span data-ttu-id="65b11-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65b11-129">Requirements</span></span>



| <span data-ttu-id="65b11-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="65b11-130">Requirement</span></span> | <span data-ttu-id="65b11-131">Valor</span><span class="sxs-lookup"><span data-stu-id="65b11-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65b11-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="65b11-132">Header</span></span><br/> | <dl> <span data-ttu-id="65b11-133"><dt>Dxgitype. h</dt></span><span class="sxs-lookup"><span data-stu-id="65b11-133"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65b11-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="65b11-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b11-135">Estruturas DXGI</span><span class="sxs-lookup"><span data-stu-id="65b11-135">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[<span data-ttu-id="65b11-136">**\_RGBA dxgi**</span><span class="sxs-lookup"><span data-stu-id="65b11-136">**DXGI\_RGBA**</span></span>](dxgi-rgba.md)
</dt> </dl>

 

 




