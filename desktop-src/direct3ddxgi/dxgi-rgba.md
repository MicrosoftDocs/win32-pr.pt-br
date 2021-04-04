---
description: Representa um valor de cor com Alfa, que é usado para transparência.
ms.assetid: 5F9DDDC1-644E-4DA2-8E3D-F157789809E7
title: Estrutura de DXGI_RGBA (DXGItype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_RGBA
api_type:
- HeaderDef
api_location:
- DXGItype.h
ms.openlocfilehash: 77b526e916d43868304c6c01a7dbbe8ebbb5692b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645966"
---
# <a name="dxgi_rgba-structure"></a><span data-ttu-id="a5fc4-103">\_Estrutura RGBA dxgi</span><span class="sxs-lookup"><span data-stu-id="a5fc4-103">DXGI\_RGBA structure</span></span>

<span data-ttu-id="a5fc4-104">Representa um valor de cor com Alfa, que é usado para transparência.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-104">Represents a color value with alpha, which is used for transparency.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5fc4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5fc4-105">Syntax</span></span>


```C++
typedef struct _DXGI_RGBA {
  float r;
  float g;
  float b;
  float a;
} DXGI_RGBA;
```



## <a name="members"></a><span data-ttu-id="a5fc4-106">Membros</span><span class="sxs-lookup"><span data-stu-id="a5fc4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a5fc4-107">**r**</span><span class="sxs-lookup"><span data-stu-id="a5fc4-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="a5fc4-108">Valor de ponto flutuante que especifica o componente vermelho de uma cor.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-108">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="a5fc4-109">Esse valor geralmente está no intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-109">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="a5fc4-110">Um valor de 0,0 indica a ausência completa do componente vermelho, enquanto um valor de 1,0 indica que o vermelho está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-110">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="a5fc4-111">**m**</span><span class="sxs-lookup"><span data-stu-id="a5fc4-111">**g**</span></span>
</dt> <dd>

<span data-ttu-id="a5fc4-112">Valor de ponto flutuante que especifica o componente verde de uma cor.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-112">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="a5fc4-113">Esse valor geralmente está no intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-113">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="a5fc4-114">Um valor de 0,0 indica a ausência completa do componente verde, enquanto um valor de 1,0 indica que o verde está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-114">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="a5fc4-115">**b**</span><span class="sxs-lookup"><span data-stu-id="a5fc4-115">**b**</span></span>
</dt> <dd>

<span data-ttu-id="a5fc4-116">Valor de ponto flutuante que especifica o componente azul de uma cor.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-116">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="a5fc4-117">Esse valor geralmente está no intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-117">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="a5fc4-118">Um valor de 0,0 indica a ausência completa do componente azul, enquanto um valor de 1,0 indica que o azul está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-118">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="a5fc4-119">**um**</span><span class="sxs-lookup"><span data-stu-id="a5fc4-119">**a**</span></span>
</dt> <dd>

<span data-ttu-id="a5fc4-120">Valor de ponto flutuante que especifica o componente alfa de uma cor.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-120">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="a5fc4-121">Esse valor geralmente está no intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-121">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="a5fc4-122">Um valor de 0,0 indica totalmente transparente, enquanto um valor de 1,0 indica totalmente opaco.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-122">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5fc4-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5fc4-123">Remarks</span></span>

<span data-ttu-id="a5fc4-124">Você pode definir os membros dessa estrutura com valores fora do intervalo de 0 a 1 para implementar alguns efeitos incomuns.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-124">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="a5fc4-125">Valores maiores que 1 produzem luzes fortes que tendem a desbotar uma cena.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-125">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="a5fc4-126">Valores negativos produzem luzes escuras que realmente removem a luz de uma cena.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-126">Negative values produce dark lights that actually remove light from a scene.</span></span>

<span data-ttu-id="a5fc4-127">O tipo de cabeçalho DXGItype. h – define **dxgi \_ RGBA** como um alias de [**D3DCOLORVALUE**](d3dcolorvalue.md), da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a5fc4-127">The DXGItype.h header type-defines **DXGI\_RGBA** as an alias of [**D3DCOLORVALUE**](d3dcolorvalue.md), as follows:</span></span>


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



<span data-ttu-id="a5fc4-128">Você pode usar **dxgi \_ RGBA** com o [**\_ \_ modo alfa**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode) [**IDXGISwapChain1:: setBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1:: getBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)e dxgi.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-128">You can use **DXGI\_RGBA** with [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor), and [**DXGI\_ALPHA\_MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5fc4-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5fc4-129">Requirements</span></span>



| <span data-ttu-id="a5fc4-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5fc4-130">Requirement</span></span> | <span data-ttu-id="a5fc4-131">Valor</span><span class="sxs-lookup"><span data-stu-id="a5fc4-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5fc4-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5fc4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a5fc4-133">Windows 8 e atualização de plataforma para \[ aplicativos UWP de aplicativos de área de trabalho do Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="a5fc4-133">Windows 8 and Platform Update for Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a5fc4-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5fc4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a5fc4-135">Windows Server 2012 e atualização de plataforma para \[ aplicativos de aplicativos UWP do Windows server 2008 R2 desktop \|\]</span><span class="sxs-lookup"><span data-stu-id="a5fc4-135">Windows Server 2012 and Platform Update for Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="a5fc4-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a5fc4-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5fc4-137"><dt>DXGItype. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5fc4-137"><dt>DXGItype.h</dt></span></span> </dl>                      |



## <a name="see-also"></a><span data-ttu-id="a5fc4-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5fc4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5fc4-139">Estruturas DXGI</span><span class="sxs-lookup"><span data-stu-id="a5fc4-139">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[<span data-ttu-id="a5fc4-140">**D3DCOLORVALUE**</span><span class="sxs-lookup"><span data-stu-id="a5fc4-140">**D3DCOLORVALUE**</span></span>](d3dcolorvalue.md)
</dt> <dt>

[<span data-ttu-id="a5fc4-141">**D3DCOLORVALUE (no Direct3D 9)**</span><span class="sxs-lookup"><span data-stu-id="a5fc4-141">**D3DCOLORVALUE (in Direct3D 9)**</span></span>](../direct3d9/d3dcolorvalue.md)
</dt> </dl>

 

 
