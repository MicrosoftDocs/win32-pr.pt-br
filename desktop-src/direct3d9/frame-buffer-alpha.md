---
description: O buffer de quadro alpha-blending é um pouco diferente do vértice alfa, do material alfa e da textura alfa.
ms.assetid: 3664215d-ad03-400e-beab-b0421cf6b693
title: Buffer de quadro alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb310e2c66f43282e65425fd0d6c6a24961accaa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087385"
---
# <a name="frame-buffer-alpha-direct3d-9"></a><span data-ttu-id="6ee52-103">Buffer de quadro alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6ee52-103">Frame Buffer Alpha (Direct3D 9)</span></span>

<span data-ttu-id="6ee52-104">O buffer de quadro alpha-blending é um pouco diferente do vértice alfa, do material alfa e da textura alfa.</span><span class="sxs-lookup"><span data-stu-id="6ee52-104">Frame buffer alpha-blending is a bit different than vertex alpha, material alpha, and texture alpha.</span></span> <span data-ttu-id="6ee52-105">O vértice, o material e a textura Alpha definem valores de transparência que são usados apenas para o primitivo atual e, por si só, não têm nenhum efeito em outros primitivos.</span><span class="sxs-lookup"><span data-stu-id="6ee52-105">Vertex, material, and texture alpha set transparency values that are used only for the current primitive, and by themselves have no effect on other primitives.</span></span> <span data-ttu-id="6ee52-106">Mesclagem alfa do buffer de quadros controla como o primitivo atual é combinado com pixels existentes no buffer de quadro para gerar uma cor de pixel final.</span><span class="sxs-lookup"><span data-stu-id="6ee52-106">Frame buffer alpha-blending controls how the current primitive is combined with existing pixels in the frame buffer to yield a final pixel color.</span></span>

<span data-ttu-id="6ee52-107">Ao executar a mesclagem alfa, duas cores estão sendo combinadas: uma cor de origem e uma cor de destino.</span><span class="sxs-lookup"><span data-stu-id="6ee52-107">When performing alpha blending, two colors are being combined: a source color and a destination color.</span></span> <span data-ttu-id="6ee52-108">A cor de origem é do objeto transparente, a cor de destino é a cor que já está no local do pixel.</span><span class="sxs-lookup"><span data-stu-id="6ee52-108">The source color is from the transparent object, the destination color is the color already at the pixel location.</span></span> <span data-ttu-id="6ee52-109">A cor de destino é o resultado da renderização de algum outro objeto que está atrás do objeto transparente, ou seja, o objeto que ficará visível por meio do objeto transparente.</span><span class="sxs-lookup"><span data-stu-id="6ee52-109">The destination color is the result of rendering some other object that is behind the transparent object, that is, the object that will be visible through the transparent object.</span></span> <span data-ttu-id="6ee52-110">A mistura alfa usa uma fórmula para controlar a taxa entre os objetos de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="6ee52-110">Alpha blending uses a formula to control the ratio between the source and destination objects.</span></span>


```
Final Color = ObjectColor * SourceBlendFactor + PixelColor * DestinationBlendFactor 
```



<span data-ttu-id="6ee52-111">Objectcolor é a contribuição do primitivo que está sendo renderizado no local atual do pixel.</span><span class="sxs-lookup"><span data-stu-id="6ee52-111">ObjectColor is the contribution from the primitive being rendered at the current pixel location.</span></span> <span data-ttu-id="6ee52-112">PixelColor é a contribuição do buffer de quadro no local do pixel atual.</span><span class="sxs-lookup"><span data-stu-id="6ee52-112">PixelColor is the contribution from the frame buffer at the current pixel location.</span></span>

<span data-ttu-id="6ee52-113">O conjunto de fatores de mistura alfa que podem ser usados está listado abaixo.</span><span class="sxs-lookup"><span data-stu-id="6ee52-113">The set of alpha blend factors that can be used are listed below.</span></span>



| <span data-ttu-id="6ee52-114">Fator de modo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="6ee52-114">Blend mode factor</span></span>         | <span data-ttu-id="6ee52-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="6ee52-115">Description</span></span>                                                                                                                                                                              |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee52-116">D3DBLEND \_ zero</span><span class="sxs-lookup"><span data-stu-id="6ee52-116">D3DBLEND\_ZERO</span></span>            | <span data-ttu-id="6ee52-117">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="6ee52-117">(0, 0, 0, 0)</span></span>                                                                                                                                                                             |
| <span data-ttu-id="6ee52-118">D3DBLEND \_ um</span><span class="sxs-lookup"><span data-stu-id="6ee52-118">D3DBLEND\_ONE</span></span>             | <span data-ttu-id="6ee52-119">(1, 1, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="6ee52-119">(1, 1, 1, 1)</span></span>                                                                                                                                                                             |
| <span data-ttu-id="6ee52-120">D3DBLEND \_ SRCCOLOR</span><span class="sxs-lookup"><span data-stu-id="6ee52-120">D3DBLEND\_SRCCOLOR</span></span>        | <span data-ttu-id="6ee52-121">(RS, GS, BS, as)</span><span class="sxs-lookup"><span data-stu-id="6ee52-121">(Rs, Gs, Bs, As)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="6ee52-122">D3DBLEND \_ INVSRCCOLOR</span><span class="sxs-lookup"><span data-stu-id="6ee52-122">D3DBLEND\_INVSRCCOLOR</span></span>     | <span data-ttu-id="6ee52-123">(1-RS, 1-GS, 1-BS, 1-como)</span><span class="sxs-lookup"><span data-stu-id="6ee52-123">(1-Rs, 1-Gs, 1-Bs, 1-As)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="6ee52-124">D3DBLEND \_ SRCALPHA</span><span class="sxs-lookup"><span data-stu-id="6ee52-124">D3DBLEND\_SRCALPHA</span></span>        | <span data-ttu-id="6ee52-125">(As, as, as, as)</span><span class="sxs-lookup"><span data-stu-id="6ee52-125">(As, As, As, As)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="6ee52-126">D3DBLEND \_ INVSRCALPHA</span><span class="sxs-lookup"><span data-stu-id="6ee52-126">D3DBLEND\_INVSRCALPHA</span></span>     | <span data-ttu-id="6ee52-127">(1-como, 1-como, 1-como, 1-como)</span><span class="sxs-lookup"><span data-stu-id="6ee52-127">(1-As, 1-As, 1-As, 1-As)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="6ee52-128">D3DBLEND \_ DESTALPHA</span><span class="sxs-lookup"><span data-stu-id="6ee52-128">D3DBLEND\_DESTALPHA</span></span>       | <span data-ttu-id="6ee52-129">(AD, AD, AD, AD)</span><span class="sxs-lookup"><span data-stu-id="6ee52-129">(Ad, Ad, Ad, Ad)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="6ee52-130">D3DBLEND \_ INVDESTALPHA</span><span class="sxs-lookup"><span data-stu-id="6ee52-130">D3DBLEND\_INVDESTALPHA</span></span>    | <span data-ttu-id="6ee52-131">(1-AD, 1-AD, 1-AD, 1-AD)</span><span class="sxs-lookup"><span data-stu-id="6ee52-131">(1-Ad, 1-Ad, 1-Ad, 1-Ad)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="6ee52-132">D3DBLEND \_ DESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="6ee52-132">D3DBLEND\_DESTCOLOR</span></span>       | <span data-ttu-id="6ee52-133">(RD, GD, BD, AD)</span><span class="sxs-lookup"><span data-stu-id="6ee52-133">(Rd, Gd, Bd, Ad)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="6ee52-134">D3DBLEND \_ INVDESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="6ee52-134">D3DBLEND\_INVDESTCOLOR</span></span>    | <span data-ttu-id="6ee52-135">(1-Rd, 1-gd, 1-BD, 1-AD)</span><span class="sxs-lookup"><span data-stu-id="6ee52-135">(1-Rd, 1-Gd, 1-Bd, 1-Ad)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="6ee52-136">D3DBLEND \_ SRCALPHASAT</span><span class="sxs-lookup"><span data-stu-id="6ee52-136">D3DBLEND\_SRCALPHASAT</span></span>     | <span data-ttu-id="6ee52-137">(f, f, f, 1); f = min (as, 1-AD)</span><span class="sxs-lookup"><span data-stu-id="6ee52-137">(f, f, f, 1); f = min(As, 1-Ad)</span></span>                                                                                                                                                          |
| <span data-ttu-id="6ee52-138">D3DBLEND \_ BOTHSRCALPHA</span><span class="sxs-lookup"><span data-stu-id="6ee52-138">D3DBLEND\_BOTHSRCALPHA</span></span>    | <span data-ttu-id="6ee52-139">Obsoleto para DirectX 6 e posterior.</span><span class="sxs-lookup"><span data-stu-id="6ee52-139">Obsolete for DirectX 6 and later.</span></span> <span data-ttu-id="6ee52-140">Você pode obter o mesmo efeito definindo os fatores de mesclagem de origem e de destino como D3DBLEND \_ SRCALPHA e D3DBLEND \_ INVSRCALPHA em chamadas separadas.</span><span class="sxs-lookup"><span data-stu-id="6ee52-140">You can achieve the same effect by setting the source and destination blend factors to D3DBLEND\_SRCALPHA and D3DBLEND\_INVSRCALPHA in separate calls.</span></span> |
| <span data-ttu-id="6ee52-141">D3DBLEND \_ BOTHINVSRCALPHA</span><span class="sxs-lookup"><span data-stu-id="6ee52-141">D3DBLEND\_BOTHINVSRCALPHA</span></span> | <span data-ttu-id="6ee52-142">Obsoleto para DirectX 6.</span><span class="sxs-lookup"><span data-stu-id="6ee52-142">Obsolete for DirectX 6.</span></span> <span data-ttu-id="6ee52-143">Você pode obter o mesmo efeito definindo os fatores de mesclagem de origem e de destino como D3DBLEND \_ INVSRCALPHA e D3DBLEND \_ SRCALPHA em chamadas separadas.</span><span class="sxs-lookup"><span data-stu-id="6ee52-143">You can achieve the same effect by setting the source and destination blend factors to D3DBLEND\_INVSRCALPHA and D3DBLEND\_SRCALPHA in separate calls.</span></span>           |
| <span data-ttu-id="6ee52-144">D3DBLEND \_ BLENDFACTOR</span><span class="sxs-lookup"><span data-stu-id="6ee52-144">D3DBLEND\_BLENDFACTOR</span></span>     | <span data-ttu-id="6ee52-145">Use Color. r, Color. g, Color. b e Color. a obtida da \_ configuração D3DRS BLENDFACTOR.</span><span class="sxs-lookup"><span data-stu-id="6ee52-145">Use color.r, color.g, color.b, and color.a obtained from the D3DRS\_BLENDFACTOR setting.</span></span>                                                                                                 |
| <span data-ttu-id="6ee52-146">D3DBLEND \_ INVBLENDFACTOR</span><span class="sxs-lookup"><span data-stu-id="6ee52-146">D3DBLEND\_INVBLENDFACTOR</span></span>  | <span data-ttu-id="6ee52-147">Use 1-Color. r, 1-Color. g, 1-Color. b e 1-Color. a obtida na \_ configuração D3DRS BLENDFACTOR.</span><span class="sxs-lookup"><span data-stu-id="6ee52-147">Use 1-color.r, 1-color.g, 1-color.b, and 1-color.a obtained from the D3DRS\_BLENDFACTOR setting.</span></span>                                                                                         |



 

<span data-ttu-id="6ee52-148">O Direct3D usa o \_ estado de RENDERIZAÇÃO D3DRS ALPHABLENDENABLE para habilitar a mesclagem de transparência alfa.</span><span class="sxs-lookup"><span data-stu-id="6ee52-148">Direct3D uses the D3DRS\_ALPHABLENDENABLE render state to enable alpha transparency blending.</span></span> <span data-ttu-id="6ee52-149">O tipo de mistura alfa que é feito depende dos \_ Estados de RENDERIZAÇÃO D3DRS SRCBLEND e \_ D3DRS DESTBLEND.</span><span class="sxs-lookup"><span data-stu-id="6ee52-149">The type of alpha blending that is done depends on the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND render states.</span></span> <span data-ttu-id="6ee52-150">Os Estados de mesclagem de origem e destino são usados em pares.</span><span class="sxs-lookup"><span data-stu-id="6ee52-150">Source and destination blend states are used in pairs.</span></span> <span data-ttu-id="6ee52-151">O fragmento de código a seguir define o estado de mesclagem de origem como D3DBLEND \_ SRCCOLOR e o estado de mesclagem de destino como D3DBLEND \_ INVSRCCOLOR.</span><span class="sxs-lookup"><span data-stu-id="6ee52-151">The following code fragment sets the source blend state to D3DBLEND\_SRCCOLOR and the destination blend state to D3DBLEND\_INVSRCCOLOR.</span></span>


```
// This code fragment assumes that lpD3DDevice is a 
//   valid pointer to a device.

// Enable alpha blending.
lpD3DDevice->SetRenderState(D3DRS_ALPHABLENDENABLE, 
                            TRUE);

// Set the source blend state.
lpD3DDevice->SetRenderState(D3DRS_SRCBLEND, 
                            D3DBLEND_SRCCOLOR);

// Set the destination blend state.
lpD3DDevice->SetRenderState(D3DRS_DESTBLEND, 
                            D3DBLEND_INVSRCCOLOR);
```



<span data-ttu-id="6ee52-152">Esse código executa uma combinação linear entre a cor de origem (a cor da primitiva que está sendo renderizada no local atual) e a cor de destino (a cor no local atual no buffer de quadro).</span><span class="sxs-lookup"><span data-stu-id="6ee52-152">This code performs a linear blend between the source color (the color of the primitive being rendered at the current location) and the destination color (the color at the current location in the frame buffer).</span></span> <span data-ttu-id="6ee52-153">A aparência resultante é semelhante ao vidro colorido, pois parte da cor do objeto de destino parece ser transmitida por meio do objeto de origem; o restante dele parece ser absorvido.</span><span class="sxs-lookup"><span data-stu-id="6ee52-153">The resulting appearance is similar to tinted glass in that some of the color of the destination object seems to be transmitted through the source object; the rest of it appears to be absorbed.</span></span>

<span data-ttu-id="6ee52-154">Muitos desses fatores de mistura exigem valores Alfa na textura para operar corretamente.</span><span class="sxs-lookup"><span data-stu-id="6ee52-154">Many of these blend factors require alpha values in the texture to operate correctly.</span></span> <span data-ttu-id="6ee52-155">Portanto, ao usar o vértice ou o material alfa, o aplicativo é restrito ao que os modos produzirão resultados interessantes.</span><span class="sxs-lookup"><span data-stu-id="6ee52-155">Thus, when using vertex or material alpha, the application is restricted as to which modes will produce interesting results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ee52-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6ee52-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ee52-157">Mesclagem alfa</span><span class="sxs-lookup"><span data-stu-id="6ee52-157">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 



