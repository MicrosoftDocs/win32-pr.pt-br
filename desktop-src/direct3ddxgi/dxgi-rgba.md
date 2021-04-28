---
description: Estrutura de DXGI_RGBA – representa um valor de cor com Alfa, que é usado para transparência.
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
ms.openlocfilehash: b0447d6470401d4136fbfd36f6d9c089e331b14b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114264"
---
# <a name="dxgi_rgba-structure"></a><span data-ttu-id="90d22-103">\_Estrutura RGBA dxgi</span><span class="sxs-lookup"><span data-stu-id="90d22-103">DXGI\_RGBA structure</span></span>

<span data-ttu-id="90d22-104">Representa um valor de cor com Alfa, que é usado para transparência.</span><span class="sxs-lookup"><span data-stu-id="90d22-104">Represents a color value with alpha, which is used for transparency.</span></span>

## <a name="syntax"></a><span data-ttu-id="90d22-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90d22-105">Syntax</span></span>


```C++
typedef struct _DXGI_RGBA {
  float r;
  float g;
  float b;
  float a;
} DXGI_RGBA;
```



## <a name="members"></a><span data-ttu-id="90d22-106">Membros</span><span class="sxs-lookup"><span data-stu-id="90d22-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="90d22-107">**r**</span><span class="sxs-lookup"><span data-stu-id="90d22-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="90d22-108">Valor de ponto flutuante que especifica o componente vermelho de uma cor.</span><span class="sxs-lookup"><span data-stu-id="90d22-108">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="90d22-109">Esse valor geralmente está no intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="90d22-109">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="90d22-110">Um valor de 0,0 indica a ausência completa do componente vermelho, enquanto um valor de 1,0 indica que o vermelho está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="90d22-110">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="90d22-111">**m**</span><span class="sxs-lookup"><span data-stu-id="90d22-111">**g**</span></span>
</dt> <dd>

<span data-ttu-id="90d22-112">Valor de ponto flutuante que especifica o componente verde de uma cor.</span><span class="sxs-lookup"><span data-stu-id="90d22-112">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="90d22-113">Esse valor geralmente está no intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="90d22-113">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="90d22-114">Um valor de 0,0 indica a ausência completa do componente verde, enquanto um valor de 1,0 indica que o verde está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="90d22-114">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="90d22-115">**b**</span><span class="sxs-lookup"><span data-stu-id="90d22-115">**b**</span></span>
</dt> <dd>

<span data-ttu-id="90d22-116">Valor de ponto flutuante que especifica o componente azul de uma cor.</span><span class="sxs-lookup"><span data-stu-id="90d22-116">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="90d22-117">Esse valor geralmente está no intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="90d22-117">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="90d22-118">Um valor de 0,0 indica a ausência completa do componente azul, enquanto um valor de 1,0 indica que o azul está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="90d22-118">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="90d22-119">**um**</span><span class="sxs-lookup"><span data-stu-id="90d22-119">**a**</span></span>
</dt> <dd>

<span data-ttu-id="90d22-120">Valor de ponto flutuante que especifica o componente alfa de uma cor.</span><span class="sxs-lookup"><span data-stu-id="90d22-120">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="90d22-121">Esse valor geralmente está no intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="90d22-121">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="90d22-122">Um valor de 0,0 indica totalmente transparente, enquanto um valor de 1,0 indica totalmente opaco.</span><span class="sxs-lookup"><span data-stu-id="90d22-122">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90d22-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="90d22-123">Remarks</span></span>

<span data-ttu-id="90d22-124">Você pode definir os membros dessa estrutura com valores fora do intervalo de 0 a 1 para implementar alguns efeitos incomuns.</span><span class="sxs-lookup"><span data-stu-id="90d22-124">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="90d22-125">Valores maiores que 1 produzem luzes fortes que tendem a desbotar uma cena.</span><span class="sxs-lookup"><span data-stu-id="90d22-125">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="90d22-126">Valores negativos produzem luzes escuras que realmente removem a luz de uma cena.</span><span class="sxs-lookup"><span data-stu-id="90d22-126">Negative values produce dark lights that actually remove light from a scene.</span></span>

<span data-ttu-id="90d22-127">O tipo de cabeçalho DXGItype. h – define **dxgi \_ RGBA** como um alias de [**D3DCOLORVALUE**](d3dcolorvalue.md), da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="90d22-127">The DXGItype.h header type-defines **DXGI\_RGBA** as an alias of [**D3DCOLORVALUE**](d3dcolorvalue.md), as follows:</span></span>


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



<span data-ttu-id="90d22-128">Você pode usar **dxgi \_ RGBA** com o [**\_ \_ modo alfa**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode) [**IDXGISwapChain1:: setBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1:: getBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)e dxgi.</span><span class="sxs-lookup"><span data-stu-id="90d22-128">You can use **DXGI\_RGBA** with [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor), and [**DXGI\_ALPHA\_MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span></span>

## <a name="requirements"></a><span data-ttu-id="90d22-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90d22-129">Requirements</span></span>



| <span data-ttu-id="90d22-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="90d22-130">Requirement</span></span> | <span data-ttu-id="90d22-131">Valor</span><span class="sxs-lookup"><span data-stu-id="90d22-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90d22-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90d22-132">Minimum supported client</span></span><br/> | <span data-ttu-id="90d22-133">Windows 8 e atualização de plataforma para \[ aplicativos UWP de aplicativos de área de trabalho do Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="90d22-133">Windows 8 and Platform Update for Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="90d22-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90d22-134">Minimum supported server</span></span><br/> | <span data-ttu-id="90d22-135">Windows Server 2012 e atualização de plataforma para \[ aplicativos de aplicativos UWP do Windows server 2008 R2 desktop \|\]</span><span class="sxs-lookup"><span data-stu-id="90d22-135">Windows Server 2012 and Platform Update for Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="90d22-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="90d22-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="90d22-137"><dt>DXGItype. h</dt></span><span class="sxs-lookup"><span data-stu-id="90d22-137"><dt>DXGItype.h</dt></span></span> </dl>                      |



## <a name="see-also"></a><span data-ttu-id="90d22-138">Consulte também</span><span class="sxs-lookup"><span data-stu-id="90d22-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90d22-139">Estruturas DXGI</span><span class="sxs-lookup"><span data-stu-id="90d22-139">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[<span data-ttu-id="90d22-140">**D3DCOLORVALUE**</span><span class="sxs-lookup"><span data-stu-id="90d22-140">**D3DCOLORVALUE**</span></span>](d3dcolorvalue.md)
</dt> <dt>

[<span data-ttu-id="90d22-141">**D3DCOLORVALUE (no Direct3D 9)**</span><span class="sxs-lookup"><span data-stu-id="90d22-141">**D3DCOLORVALUE (in Direct3D 9)**</span></span>](../direct3d9/d3dcolorvalue.md)
</dt> </dl>

 

 
