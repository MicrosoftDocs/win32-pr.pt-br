---
title: Efeito de mapa de deslocamento
description: Use o efeito de mapa de deslocamento para substituir os pixels da imagem de entrada pelos valores de intensidade de uma segunda imagem de entrada.
ms.assetid: 07AA64B1-B570-428E-924F-D7DF3E4DB3F8
keywords:
- efeito de mapa de deslocamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0ad2deb0c584ccc9c55faebd60f803d66efa42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085199"
---
# <a name="displacement-map-effect"></a><span data-ttu-id="af4c4-104">Efeito de mapa de deslocamento</span><span class="sxs-lookup"><span data-stu-id="af4c4-104">Displacement map effect</span></span>

<span data-ttu-id="af4c4-105">Use o efeito de mapa de deslocamento para substituir os pixels da imagem de entrada pelos valores de intensidade de uma segunda imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="af4c4-105">Use the displacement map effect to displace the pixels of the input image by the intensity values of a second input image.</span></span>

<span data-ttu-id="af4c4-106">O CLSID para esse efeito é CLSID \_ D2D1DisplacementMap.</span><span class="sxs-lookup"><span data-stu-id="af4c4-106">The CLSID for this effect is CLSID\_D2D1DisplacementMap.</span></span>

-   [<span data-ttu-id="af4c4-107">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="af4c4-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="af4c4-108">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="af4c4-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="af4c4-109">Canais de cores</span><span class="sxs-lookup"><span data-stu-id="af4c4-109">Color channels</span></span>](#color-channels)
-   [<span data-ttu-id="af4c4-110">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="af4c4-110">Output Bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="af4c4-111">Requirements</span><span class="sxs-lookup"><span data-stu-id="af4c4-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="af4c4-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="af4c4-112">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="af4c4-113">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="af4c4-113">Example image</span></span>



| <span data-ttu-id="af4c4-114">Antes</span><span class="sxs-lookup"><span data-stu-id="af4c4-114">Before</span></span>                                                           |
|------------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)       |
| <span data-ttu-id="af4c4-116">After (após)</span><span class="sxs-lookup"><span data-stu-id="af4c4-116">After</span></span>                                                            |
| ![a imagem após a transformação.](images/19-displacementmap.png) |



 


```C++
ComPtr<ID2D1Effect> displacementMapEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DisplacementMap, &displacementMapEffect);

displacementMapEffect->SetInput(0, bitmap);
displacementMapEffect->SetValue(D2D1_DISPLACEMENTMAP_PROP_SCALE, 100.0f);

// The second input of the displacement effect determines how the input image is transformed.
// For this example, we will use a turbulence effect as the second input to randomly distort the image.
ComPtr<ID2D1Effect> turbulenceEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Turbulence, &turbulenceEffect);
displacementMapEffect->SetInputEffect(1, turbulenceEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(displacementMapEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="af4c4-118">Os locais dos pixels na saída são determinados usando esta fórmula:</span><span class="sxs-lookup"><span data-stu-id="af4c4-118">The locations of the pixels in the output are determined using this formula:</span></span>

<span data-ttu-id="af4c4-119">C ' (x, y) = C (x + escala \* (XChannelSelector (bitmap de deslocamento (x, y))-0,5), y + escala \* (YChannelSelector (bitmap de deslocamento (x, y))-0,5))</span><span class="sxs-lookup"><span data-stu-id="af4c4-119">C' (x,y)=C(x+ scale\*(XChannelSelector(Displacement Bitmap (x,y))-0.5),y+ scale\*(YChannelSelector(Displacement Bitmap (x,y))-0.5))</span></span>

<span data-ttu-id="af4c4-120">Em que:</span><span class="sxs-lookup"><span data-stu-id="af4c4-120">Where:</span></span><dl> <span data-ttu-id="af4c4-121">*C (x, y)* é o pixel de saída em (x, y).</span><span class="sxs-lookup"><span data-stu-id="af4c4-121">*C  (x, y)* is the output pixel at (x, y).</span></span>  
<span data-ttu-id="af4c4-122">*C (x, y)* é o pixel de entrada em (x, y).</span><span class="sxs-lookup"><span data-stu-id="af4c4-122">*C (x, y)* is the input pixel at (x, y).</span></span>  
<span data-ttu-id="af4c4-123">*Bitmap de deslocamento (x, y)* é a intensidade de pixel de deslocamento nas coordenadas especificadas</span><span class="sxs-lookup"><span data-stu-id="af4c4-123">*Displacement Bitmap (x, y)* is the displacement pixel intensity at the specified coordinates</span></span>  
<span data-ttu-id="af4c4-124">*XChannelSelector* a intensidade do canal RGBA selecionado do bitmap de deslocamento que substitui a imagem de entrada na direção X.</span><span class="sxs-lookup"><span data-stu-id="af4c4-124">*XChannelSelector* the intensity of the selected RGBA channel from the displacement bitmap that displaces the input image in the X direction.</span></span>  
<span data-ttu-id="af4c4-125">*YChannelSelector* a intensidade do canal RGBA selecionado do bitmap de deslocamento que substitui a imagem de entrada na direção Y.</span><span class="sxs-lookup"><span data-stu-id="af4c4-125">*YChannelSelector* the intensity of the selected RGBA channel from the displacement bitmap that displaces the input image in the Y direction.</span></span>  
</dl>

<span data-ttu-id="af4c4-126">O efeito reamostra a imagem de entrada de acordo com a propriedade Scale e a intensidade da imagem de deslocamento.</span><span class="sxs-lookup"><span data-stu-id="af4c4-126">The effect resamples the input image according to the scale property and the intensity of the displacement image.</span></span> <span data-ttu-id="af4c4-127">Ele usa interpolação bilinear se a amostragem estiver entre pixels na imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="af4c4-127">It uses bilinear interpolation if sampling from between pixels in the input image.</span></span>

<span data-ttu-id="af4c4-128">Esse efeito funciona em imagens alfa retas e semimultiplicadas.</span><span class="sxs-lookup"><span data-stu-id="af4c4-128">This effect works on straight and premultiplied alpha images.</span></span> <span data-ttu-id="af4c4-129">O formato alfa de saída é o mesmo que o formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="af4c4-129">The output alpha format is the same as the input format.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="af4c4-130">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="af4c4-130">Effect properties</span></span>



| <span data-ttu-id="af4c4-131">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="af4c4-131">Display name and index enumeration</span></span>                                                   | <span data-ttu-id="af4c4-132">Tipo e valor padrão</span><span class="sxs-lookup"><span data-stu-id="af4c4-132">Type and default value</span></span>                                                   | <span data-ttu-id="af4c4-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="af4c4-133">Description</span></span>                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af4c4-134">Escala</span><span class="sxs-lookup"><span data-stu-id="af4c4-134">Scale</span></span><br/> <span data-ttu-id="af4c4-135">\_Escala de \_ prop d2d1 DISPLACEMENTMAP \_</span><span class="sxs-lookup"><span data-stu-id="af4c4-135">D2D1\_DISPLACEMENTMAP\_PROP\_SCALE</span></span><br/>                       | <span data-ttu-id="af4c4-136">FLOAT</span><span class="sxs-lookup"><span data-stu-id="af4c4-136">FLOAT</span></span><br/> <span data-ttu-id="af4c4-137">0,0 f</span><span class="sxs-lookup"><span data-stu-id="af4c4-137">0.0f</span></span><br/>                                         | <span data-ttu-id="af4c4-138">Multiplica a intensidade do canal selecionado da imagem de deslocamento.</span><span class="sxs-lookup"><span data-stu-id="af4c4-138">Multiplies the intensity of the selected channel from the displacement image.</span></span> <span data-ttu-id="af4c4-139">Quanto mais alto você definir essa propriedade, mais o efeito substituirá os pixels</span><span class="sxs-lookup"><span data-stu-id="af4c4-139">The higher you set this property, the more the effect displaces the pixels</span></span><br/>                       |
| <span data-ttu-id="af4c4-140">XChannelSelect</span><span class="sxs-lookup"><span data-stu-id="af4c4-140">XChannelSelect</span></span><br/> <span data-ttu-id="af4c4-141">Seleção de canal do D2D1 \_ DISPLACEMENTMAP \_ prop \_ X \_ \_</span><span class="sxs-lookup"><span data-stu-id="af4c4-141">D2D1\_DISPLACEMENTMAP\_PROP\_X\_CHANNEL\_SELECT</span></span><br/> | <span data-ttu-id="af4c4-142">\_Seletor de canal d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="af4c4-142">D2D1\_CHANNEL\_SELECTOR</span></span><br/> <span data-ttu-id="af4c4-143">\_ \_ Seletor de canal do d2d1 \_ A</span><span class="sxs-lookup"><span data-stu-id="af4c4-143">D2D1\_CHANNEL\_SELECTOR\_A</span></span><br/> | <span data-ttu-id="af4c4-144">O efeito extrai a intensidade desse canal de cor e a usa para inserir espacialmente a imagem na direção X.</span><span class="sxs-lookup"><span data-stu-id="af4c4-144">The effect extracts the intensity from this color channel and uses it to spatially displace the image in the X direction.</span></span> <span data-ttu-id="af4c4-145">Consulte [canais de cores](#color-channels) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="af4c4-145">See [Color channels](#color-channels) for more info.</span></span><br/> |
| <span data-ttu-id="af4c4-146">YChannelSelect</span><span class="sxs-lookup"><span data-stu-id="af4c4-146">YChannelSelect</span></span><br/> <span data-ttu-id="af4c4-147">\_Select do \_ \_ canal Y \_ \_ do d2d1 DISPLACEMENTMAP prop</span><span class="sxs-lookup"><span data-stu-id="af4c4-147">D2D1\_DISPLACEMENTMAP\_PROP\_Y\_CHANNEL\_SELECT</span></span><br/> | <span data-ttu-id="af4c4-148">\_Seletor de canal d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="af4c4-148">D2D1\_CHANNEL\_SELECTOR</span></span><br/> <span data-ttu-id="af4c4-149">\_ \_ Seletor de canal do d2d1 \_ A</span><span class="sxs-lookup"><span data-stu-id="af4c4-149">D2D1\_CHANNEL\_SELECTOR\_A</span></span><br/> | <span data-ttu-id="af4c4-150">O efeito extrai a intensidade desse canal de cor e a usa para inserir espacialmente a imagem na direção Y.</span><span class="sxs-lookup"><span data-stu-id="af4c4-150">The effect extracts the intensity from this color channel and uses it to spatially displace the image in the Y direction.</span></span> <span data-ttu-id="af4c4-151">Consulte [canais de cores](#color-channels) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="af4c4-151">See [Color channels](#color-channels) for more info.</span></span><br/> |



 

## <a name="color-channels"></a><span data-ttu-id="af4c4-152">Canais de cores</span><span class="sxs-lookup"><span data-stu-id="af4c4-152">Color channels</span></span>



| <span data-ttu-id="af4c4-153">Enumeração</span><span class="sxs-lookup"><span data-stu-id="af4c4-153">Enumeration</span></span>                | <span data-ttu-id="af4c4-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="af4c4-154">Description</span></span>                                                      |
|----------------------------|------------------------------------------------------------------|
| <span data-ttu-id="af4c4-155">\_Seletor de canal do d2d1 \_ \_ R</span><span class="sxs-lookup"><span data-stu-id="af4c4-155">D2D1\_CHANNEL\_SELECTOR\_R</span></span> | <span data-ttu-id="af4c4-156">O efeito extrai a saída de intensidade do canal vermelho.</span><span class="sxs-lookup"><span data-stu-id="af4c4-156">The effect extracts the intensity output from the red channel.</span></span>   |
| <span data-ttu-id="af4c4-157">\_Seletor de canal d2d1 \_ \_ G</span><span class="sxs-lookup"><span data-stu-id="af4c4-157">D2D1\_CHANNEL\_SELECTOR\_G</span></span> | <span data-ttu-id="af4c4-158">O efeito extrai a saída de intensidade do canal verde.</span><span class="sxs-lookup"><span data-stu-id="af4c4-158">The effect extracts the intensity output from the green channel.</span></span> |
| <span data-ttu-id="af4c4-159">\_Seletor de canal do d2d1 \_ \_ B</span><span class="sxs-lookup"><span data-stu-id="af4c4-159">D2D1\_CHANNEL\_SELECTOR\_B</span></span> | <span data-ttu-id="af4c4-160">O efeito extrai a saída de intensidade do canal azul.</span><span class="sxs-lookup"><span data-stu-id="af4c4-160">The effect extracts the intensity output from the blue channel.</span></span>  |
| <span data-ttu-id="af4c4-161">\_ \_ Seletor de canal do d2d1 \_ A</span><span class="sxs-lookup"><span data-stu-id="af4c4-161">D2D1\_CHANNEL\_SELECTOR\_A</span></span> | <span data-ttu-id="af4c4-162">O efeito extrai a saída de intensidade do canal alfa.</span><span class="sxs-lookup"><span data-stu-id="af4c4-162">The effect extracts the intensity output from the alpha channel.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="af4c4-163">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="af4c4-163">Output Bitmap</span></span>

<span data-ttu-id="af4c4-164">Você pode determinar o tamanho máximo do bitmap de saída com estas equações:</span><span class="sxs-lookup"><span data-stu-id="af4c4-164">You can determine the maximum size of the output bitmap with these equations:</span></span>

<span data-ttu-id="af4c4-165">Bitmap de saída?</span><span class="sxs-lookup"><span data-stu-id="af4c4-165">Output Bitmap?</span></span> <span data-ttu-id="af4c4-166">Pixels = (tamanho do bitmap de entrada? ( DIPs) + escala) \* (DPI do usuário/96)</span><span class="sxs-lookup"><span data-stu-id="af4c4-166">Pixels=(Input Bitmap Size?(DIPs)+Scale)\*(User DPI/96)</span></span>

<span data-ttu-id="af4c4-167">Bitmap de saída<sub>y</sub> pixels = (tamanho do bitmap de entrada<sub>y</sub>(DIPs) + escala) \* (DPI do usuário/96)</span><span class="sxs-lookup"><span data-stu-id="af4c4-167">Output Bitmap<sub>y</sub> Pixels=(Input Bitmap Size<sub>y</sub>(DIPs) + Scale)\*(User DPI/96)</span></span>

## <a name="requirements"></a><span data-ttu-id="af4c4-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af4c4-168">Requirements</span></span>



| <span data-ttu-id="af4c4-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="af4c4-169">Requirement</span></span> | <span data-ttu-id="af4c4-170">Valor</span><span class="sxs-lookup"><span data-stu-id="af4c4-170">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="af4c4-171">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af4c4-171">Minimum supported client</span></span> | <span data-ttu-id="af4c4-172">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="af4c4-172">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="af4c4-173">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af4c4-173">Minimum supported server</span></span> | <span data-ttu-id="af4c4-174">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="af4c4-174">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="af4c4-175">parâmetro</span><span class="sxs-lookup"><span data-stu-id="af4c4-175">Header</span></span>                   | <span data-ttu-id="af4c4-176">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="af4c4-176">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="af4c4-177">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="af4c4-177">Library</span></span>                  | <span data-ttu-id="af4c4-178">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="af4c4-178">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="af4c4-179">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="af4c4-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af4c4-180">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="af4c4-180">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

