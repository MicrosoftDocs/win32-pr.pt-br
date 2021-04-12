---
title: Efeito de gerenciamento de cores
description: Use o efeito de gerenciamento de cores para transformar uma imagem de um perfil de cor ICC (International Color Consortium) para outro. O efeito transforma a imagem de acordo com a especificação ICC.
ms.assetid: 7351C4B4-F289-4236-BB42-1B3BD8753248
keywords:
- efeito de gerenciamento de cores
ms.topic: article
ms.date: 02/05/2019
ms.openlocfilehash: 5f3783132e0e2af511a99fd8c44d5f899e577a3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369536"
---
# <a name="color-management-effect"></a><span data-ttu-id="8531c-105">Efeito de gerenciamento de cores</span><span class="sxs-lookup"><span data-stu-id="8531c-105">Color management effect</span></span>

<span data-ttu-id="8531c-106">Use o efeito de gerenciamento de cores para transformar uma imagem de um perfil de cor ICC (International Color Consortium) para outro.</span><span class="sxs-lookup"><span data-stu-id="8531c-106">Use the color management effect to transform an image from one ICC (International Color Consortium) color profile to another.</span></span> <span data-ttu-id="8531c-107">O efeito transforma a imagem de acordo com a [especificação ICC](https://www.color.org).</span><span class="sxs-lookup"><span data-stu-id="8531c-107">The effect transforms the image according to the [ICC specification](https://www.color.org).</span></span>

<span data-ttu-id="8531c-108">O CLSID para esse efeito é CLSID \_ D2D1ColorManagement.</span><span class="sxs-lookup"><span data-stu-id="8531c-108">The CLSID for this effect is CLSID\_D2D1ColorManagement.</span></span>

- [<span data-ttu-id="8531c-109">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="8531c-109">Effect properties</span></span>](#effect-properties)
- [<span data-ttu-id="8531c-110">Modos de intenção de renderização</span><span class="sxs-lookup"><span data-stu-id="8531c-110">Rendering intent modes</span></span>](#rendering-intent-modes)
- [<span data-ttu-id="8531c-111">Modos alfa da imagem de entrada</span><span class="sxs-lookup"><span data-stu-id="8531c-111">Input image alpha modes</span></span>](#input-image-alpha-modes)
- [<span data-ttu-id="8531c-112">Conformidade com a especificação ICC</span><span class="sxs-lookup"><span data-stu-id="8531c-112">Compliance with ICC specification</span></span>](#compliance-with-icc-specification)
- [<span data-ttu-id="8531c-113">Comportamento do canal alfa</span><span class="sxs-lookup"><span data-stu-id="8531c-113">Alpha channel behavior</span></span>](#alpha-channel-behavior)
- [<span data-ttu-id="8531c-114">Modos de qualidade</span><span class="sxs-lookup"><span data-stu-id="8531c-114">Quality modes</span></span>](#quality-modes)
- [<span data-ttu-id="8531c-115">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="8531c-115">Sample code</span></span>](#sample-code)
- [<span data-ttu-id="8531c-116">Requirements</span><span class="sxs-lookup"><span data-stu-id="8531c-116">Requirements</span></span>](#requirements)
- [<span data-ttu-id="8531c-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8531c-117">Related topics</span></span>](#related-topics)

## <a name="effect-properties"></a><span data-ttu-id="8531c-118">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="8531c-118">Effect properties</span></span>

| <span data-ttu-id="8531c-119">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="8531c-119">Display name and index enumeration</span></span> | <span data-ttu-id="8531c-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="8531c-120">Description</span></span> |
|-|-|
| <span data-ttu-id="8531c-121">SourceContext</span><span class="sxs-lookup"><span data-stu-id="8531c-121">SourceContext</span></span><br/> <span data-ttu-id="8531c-122">\_Contexto de \_ \_ cor de origem d2d1 COLORMANAGEMENT prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="8531c-122">D2D1\_COLORMANAGEMENT\_PROP\_SOURCE\_COLOR\_CONTEXT</span></span><br/> | <span data-ttu-id="8531c-123">As informações de espaço de cores de origem.</span><span class="sxs-lookup"><span data-stu-id="8531c-123">The source color space information.</span></span> <span data-ttu-id="8531c-124">O tipo é [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).</span><span class="sxs-lookup"><span data-stu-id="8531c-124">The type is [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).</span></span><br/> <span data-ttu-id="8531c-125">O valor padrão é NULL.</span><span class="sxs-lookup"><span data-stu-id="8531c-125">The default value is NULL.</span></span><br/> |
| <span data-ttu-id="8531c-126">SourceIntent</span><span class="sxs-lookup"><span data-stu-id="8531c-126">SourceIntent</span></span><br/> <span data-ttu-id="8531c-127">\_Tentativa de \_ \_ RENDERIZAÇÃO de origem d2d1 COLORMANAGEMENT prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="8531c-127">D2D1\_COLORMANAGEMENT\_PROP\_SOURCE\_RENDERING\_INTENT</span></span><br/> | <span data-ttu-id="8531c-128">Qual tentativa de renderização ICC usar.</span><span class="sxs-lookup"><span data-stu-id="8531c-128">Which ICC rendering intent to use.</span></span> <span data-ttu-id="8531c-129">O tipo é a \_ tentativa de RENDERIZAÇÃO d2d1 COLORMANAGEMENT \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8531c-129">The type is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT.</span></span><br/> <span data-ttu-id="8531c-130">O valor padrão é D2D1 \_ COLORMANAGEMENT de \_ tentativa de renderização \_ \_ perceptiva.</span><span class="sxs-lookup"><span data-stu-id="8531c-130">The default value is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_PERCEPTUAL.</span></span><br/> |
| <span data-ttu-id="8531c-131">DestinationContext</span><span class="sxs-lookup"><span data-stu-id="8531c-131">DestinationContext</span></span><br/> <span data-ttu-id="8531c-132">\_Contexto de \_ \_ cor de destino d2d1 COLORMANAGEMENT prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="8531c-132">D2D1\_COLORMANAGEMENT\_PROP\_DESTINATION\_COLOR\_CONTEXT</span></span><br/> | <span data-ttu-id="8531c-133">As informações de espaço de cores de destino.</span><span class="sxs-lookup"><span data-stu-id="8531c-133">The destination color space information.</span></span> <span data-ttu-id="8531c-134">O tipo é [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).</span><span class="sxs-lookup"><span data-stu-id="8531c-134">The type is [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).</span></span><br/> <span data-ttu-id="8531c-135">O valor padrão é NULL.</span><span class="sxs-lookup"><span data-stu-id="8531c-135">The default value is NULL.</span></span><br/> |
| <span data-ttu-id="8531c-136">DestinationIntent</span><span class="sxs-lookup"><span data-stu-id="8531c-136">DestinationIntent</span></span><br/> <span data-ttu-id="8531c-137">\_Tentativa de \_ \_ RENDERIZAÇÃO de destino d2d1 COLORMANAGEMENT prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="8531c-137">D2D1\_COLORMANAGEMENT\_PROP\_DESTINATION\_RENDERING\_INTENT</span></span><br/> | <span data-ttu-id="8531c-138">Qual tentativa de renderização ICC usar.</span><span class="sxs-lookup"><span data-stu-id="8531c-138">Which ICC rendering intent to use.</span></span> <span data-ttu-id="8531c-139">O tipo é a \_ tentativa de RENDERIZAÇÃO d2d1 COLORMANAGEMENT \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8531c-139">The type is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT.</span></span><br/> <span data-ttu-id="8531c-140">O valor padrão é D2D1 \_ COLORMANAGEMENT de \_ tentativa de renderização \_ \_ perceptiva.</span><span class="sxs-lookup"><span data-stu-id="8531c-140">The default value is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_PERCEPTUAL.</span></span><br/> |
| <span data-ttu-id="8531c-141">Alphamode</span><span class="sxs-lookup"><span data-stu-id="8531c-141">AlphaMode</span></span><br/> <span data-ttu-id="8531c-142">Modo alfa do D2D1 \_ COLORMANAGEMENT \_ prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="8531c-142">D2D1\_COLORMANAGEMENT\_PROP\_ALPHA\_MODE</span></span><br/> | <span data-ttu-id="8531c-143">Como interpretar dados alfa contidos na imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="8531c-143">How to interpret alpha data that is contained in the input image.</span></span> <span data-ttu-id="8531c-144">O tipo é D2D1 \_ COLORMANAGEMENT \_ Alpha \_ Mode.</span><span class="sxs-lookup"><span data-stu-id="8531c-144">The type is D2D1\_COLORMANAGEMENT\_ALPHA\_MODE.</span></span><br/> <span data-ttu-id="8531c-145">O valor padrão é D2D1 \_ COLORMANAGEMENT \_ Alpha \_ mode \_ premultiplicado.</span><span class="sxs-lookup"><span data-stu-id="8531c-145">The default value is D2D1\_COLORMANAGEMENT\_ALPHA\_MODE\_PREMULTIPLIED.</span></span><br/> |
| <span data-ttu-id="8531c-146">Qualidade</span><span class="sxs-lookup"><span data-stu-id="8531c-146">Quality</span></span><br/> <span data-ttu-id="8531c-147">\_Qualidade de \_ prop d2d1 COLORMANAGEMENT \_</span><span class="sxs-lookup"><span data-stu-id="8531c-147">D2D1\_COLORMANAGEMENT\_PROP\_QUALITY</span></span><br/> | <span data-ttu-id="8531c-148">O nível de qualidade da transformação.</span><span class="sxs-lookup"><span data-stu-id="8531c-148">The quality level of the transform.</span></span> <span data-ttu-id="8531c-149">O tipo é D2D1 \_ COLORMANAGEMENT \_ Quality.</span><span class="sxs-lookup"><span data-stu-id="8531c-149">The type is D2D1\_COLORMANAGEMENT\_QUALITY.</span></span><br/> <span data-ttu-id="8531c-150">O valor padrão é D2D1 \_ COLORMANAGEMENT \_ Quality \_ normal.</span><span class="sxs-lookup"><span data-stu-id="8531c-150">The default value is D2D1\_COLORMANAGEMENT\_QUALITY\_NORMAL.</span></span><br/> |

## <a name="rendering-intent-modes"></a><span data-ttu-id="8531c-151">Modos de intenção de renderização</span><span class="sxs-lookup"><span data-stu-id="8531c-151">Rendering intent modes</span></span>

| <span data-ttu-id="8531c-152">Enumeração</span><span class="sxs-lookup"><span data-stu-id="8531c-152">Enumeration</span></span> | <span data-ttu-id="8531c-153">Descrição</span><span class="sxs-lookup"><span data-stu-id="8531c-153">Description</span></span> |
|-|-|
| <span data-ttu-id="8531c-154">D2D1 \_ COLORMANAGEMENT \_ tentativa de renderização \_ \_ perceptiva</span><span class="sxs-lookup"><span data-stu-id="8531c-154">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_PERCEPTUAL</span></span> | <span data-ttu-id="8531c-155">O efeito compacta ou expande a gama de cores completa da imagem para preencher a gama de cores do dispositivo, para que o saldo cinza seja preservado, mas a precisão colorimétrico não possa ser preservada.</span><span class="sxs-lookup"><span data-stu-id="8531c-155">The effect compresses or expands the full color gamut of the image to fill the color gamut of the device, so that gray balance is preserved but colorimetric accuracy may not be preserved.</span></span> |
| <span data-ttu-id="8531c-156">Colorimétrico relativo da D2D1 COLORMANAGEMENT para a \_ \_ renderização \_ \_ relativa \_</span><span class="sxs-lookup"><span data-stu-id="8531c-156">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_RELATIVE\_COLORIMETRIC</span></span> | <span data-ttu-id="8531c-157">O efeito preserva o croma de cores na imagem, com a possível despesa de matiz e claridade.</span><span class="sxs-lookup"><span data-stu-id="8531c-157">The effect preserves the chroma of colors in the image at the possible expense of hue and lightness.</span></span> |
| <span data-ttu-id="8531c-158">\_Saturação da \_ tentativa de RENDERIZAÇÃO \_ \_ de d2d1 COLORMANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="8531c-158">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_SATURATION</span></span> | <span data-ttu-id="8531c-159">O efeito ajusta as cores que ficam fora do intervalo de cores que o dispositivo de saída renderiza para a cor mais próxima disponível.</span><span class="sxs-lookup"><span data-stu-id="8531c-159">The effect adjusts colors that fall outside the range of colors the output device renders to the closest color available.</span></span> <span data-ttu-id="8531c-160">Ele não preserva o ponto branco.</span><span class="sxs-lookup"><span data-stu-id="8531c-160">It does not preserve the white point.</span></span> |
| <span data-ttu-id="8531c-161">\_ \_ \_ Colorimétrico absoluto da tentativa de renderização \_ d2d1 COLORMANAGEMENT \_</span><span class="sxs-lookup"><span data-stu-id="8531c-161">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_ABSOLUTE\_COLORIMETRIC</span></span> | <span data-ttu-id="8531c-162">O efeito ajusta as cores que estão fora do intervalo que o dispositivo de saída pode processar para a cor mais próxima que pode ser renderizada.</span><span class="sxs-lookup"><span data-stu-id="8531c-162">The effect adjusts any colors that fall outside the range that the output device can render to the closest color that can be rendered.</span></span> <span data-ttu-id="8531c-163">O efeito não altera as outras cores e preserva o ponto branco.</span><span class="sxs-lookup"><span data-stu-id="8531c-163">The effect does not change the other colors and preserves the white point.</span></span> |

## <a name="input-image-alpha-modes"></a><span data-ttu-id="8531c-164">Modos alfa da imagem de entrada</span><span class="sxs-lookup"><span data-stu-id="8531c-164">Input image alpha modes</span></span>

| <span data-ttu-id="8531c-165">Enumeração</span><span class="sxs-lookup"><span data-stu-id="8531c-165">Enumeration</span></span> | <span data-ttu-id="8531c-166">Descrição</span><span class="sxs-lookup"><span data-stu-id="8531c-166">Description</span></span> |
|-|-|
| <span data-ttu-id="8531c-167">D2D1 \_ COLORMANAGEMENT \_ \_ modo alfa \_ premultiplicado</span><span class="sxs-lookup"><span data-stu-id="8531c-167">D2D1\_COLORMANAGEMENT\_ALPHA\_MODE\_PREMULTIPLIED</span></span> | <span data-ttu-id="8531c-168">O efeito pressupõe que o modo alfa é premultiplicado.</span><span class="sxs-lookup"><span data-stu-id="8531c-168">The effect assumes the alpha mode is premultiplied.</span></span> |
| <span data-ttu-id="8531c-169">\_ \_ Modo Alpha d2d1 \_ COLORMANAGEMENT \_ reto</span><span class="sxs-lookup"><span data-stu-id="8531c-169">D2D1\_COLORMANAGEMENT\_ALPHA\_MODE\_STRAIGHT</span></span> | <span data-ttu-id="8531c-170">O efeito pressupõe que o modo alfa é reto.</span><span class="sxs-lookup"><span data-stu-id="8531c-170">The effect assumes the alpha mode is straight.</span></span> |

## <a name="d2d1_gamma1_g2084-behavior-changes"></a><span data-ttu-id="8531c-171">D2D1_GAMMA1_G2084 alterações de comportamento</span><span class="sxs-lookup"><span data-stu-id="8531c-171">D2D1_GAMMA1_G2084 behavior changes</span></span>
    
<span data-ttu-id="8531c-172">Se seu aplicativo usa o espaço de [D2D1_GAMMA1_G2084](/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_gamma1) ou um dos valores de enumeração de [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) que usam o espaço de cores SMPTE St. 2084 (perceptiva quantizador), o aplicativo pretende trabalhar com dados HDR.</span><span class="sxs-lookup"><span data-stu-id="8531c-172">If your application uses the [D2D1_GAMMA1_G2084](/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_gamma1) space, or one of the [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) enumeration values that use the SMPTE ST.2084 (Perceptual Quantizer) color space, then the application intends to work with HDR data.</span></span>

<span data-ttu-id="8531c-173">As APIs [**ID2D1DeviceContext5:: CreateColorContextFromSimpleColorProfile**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile__id2d1colorcontext1)) e [**ID2D1DeviceContext5:: CreateColorContextFromDxgiColorSpace**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace) não são contadas para isso; em vez disso, o conteúdo HDR é dimensionado para caber no intervalo de 0-1 durante a operação de desdimensionamento de G2084.</span><span class="sxs-lookup"><span data-stu-id="8531c-173">The [**ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile__id2d1colorcontext1)) and [**ID2D1DeviceContext5::CreateColorContextFromDxgiColorSpace**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace) APIs don't account for that; rather, the HDR content is scaled to fit in the 0-1 range during the G2084 DeGamma operation.</span></span>

<span data-ttu-id="8531c-174">Na prática, o conteúdo codificado neste espaço de gama usa um WhiteLevel de referência de 10.000 nits, que normalmente seria representado em CCCS como 10.000/80 = 125,0.</span><span class="sxs-lookup"><span data-stu-id="8531c-174">In practice, content that is encoded in this gamma space uses a reference WhiteLevel of 10,000 Nits, which would normally be represented in CCCS as 10,000 / 80 = 125.0.</span></span> <span data-ttu-id="8531c-175">Portanto, para facilitar melhor seu aplicativo, é mais simples para essa conversão de gama também dimensionar a luminância por um fator de 125.</span><span class="sxs-lookup"><span data-stu-id="8531c-175">So, to better facilitate your app, it's simplest for this gamma conversion to also scale the luminance by a factor of 125.</span></span> <span data-ttu-id="8531c-176">A partir do Windows 10, versão 1809 (10,0; Build 17763), o comportamento do efeito de gerenciamento de cores é que ele aplica esse dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="8531c-176">As of Windows 10, version 1809 (10.0; Build 17763), the behavior of the color management effect is such that it applies this scaling.</span></span> <span data-ttu-id="8531c-177">Isso significa que você, como desenvolvedor, não precisa aplicar um segundo efeito de [ajuste de nível branco](white-level-adjustment-effect.md) no pipeline.</span><span class="sxs-lookup"><span data-stu-id="8531c-177">That means that you, as the developer, don't have to apply a second [White level adjustment effect](white-level-adjustment-effect.md) into the pipeline.</span></span>

## <a name="compliance-with-icc-specification"></a><span data-ttu-id="8531c-178">Conformidade com a especificação ICC</span><span class="sxs-lookup"><span data-stu-id="8531c-178">Compliance with ICC specification</span></span>

<span data-ttu-id="8531c-179">O efeito de gerenciamento de cores é compatível com a especificação ICC v 4.3, com estas limitações:</span><span class="sxs-lookup"><span data-stu-id="8531c-179">The color management effect is compliant with the ICC v4.3 specification, with these limitations:</span></span>

- <span data-ttu-id="8531c-180">O efeito dá suporte a espaços de cores de 1, 3 e 4 canais.</span><span class="sxs-lookup"><span data-stu-id="8531c-180">The effect supports 1, 3, and 4 channel color spaces.</span></span>
- <span data-ttu-id="8531c-181">O efeito não dá suporte a perfis de cor ColorSpace ou nomeados.</span><span class="sxs-lookup"><span data-stu-id="8531c-181">The effect doesn't support ColorSpace or Named Color profiles.</span></span>

## <a name="alpha-channel-behavior"></a><span data-ttu-id="8531c-182">Comportamento do canal alfa</span><span class="sxs-lookup"><span data-stu-id="8531c-182">Alpha channel behavior</span></span>

<span data-ttu-id="8531c-183">Em geral, o efeito define alfa como 1 (opaco) se não houver dados alfa na imagem de origem e os dados alfa serão descartados se não houver espaço na imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="8531c-183">In general, the effect sets alpha to 1 (opaque) if there is no alpha data in the source image and the alpha data is discarded if there is no room in the destination image.</span></span> <span data-ttu-id="8531c-184">A tabela aqui descreve o comportamento alfa.</span><span class="sxs-lookup"><span data-stu-id="8531c-184">The table here describes the alpha behavior.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8531c-185">Colorspace de origem, formato de pixel</span><span class="sxs-lookup"><span data-stu-id="8531c-185">Source colorspace, pixel format</span></span></th>
<th><span data-ttu-id="8531c-186">Colorspace de destino, formato de pixel</span><span class="sxs-lookup"><span data-stu-id="8531c-186">Destination colorspace, pixel format</span></span></th>
<th><span data-ttu-id="8531c-187">Comportamento alfa</span><span class="sxs-lookup"><span data-stu-id="8531c-187">Alpha behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="8531c-188">1 canal, formato R pixel $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="8531c-188">1 channel, R pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="8531c-189">formato de 1 canal, R pixel</span><span class="sxs-lookup"><span data-stu-id="8531c-189">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="8531c-190">(Não há dados alfa)</span><span class="sxs-lookup"><span data-stu-id="8531c-190">(No alpha data)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8531c-191">1 canal, formato de pixel RGBA</span><span class="sxs-lookup"><span data-stu-id="8531c-191">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="8531c-192">Os dados Alfa são definidos como 1 (opaco)</span><span class="sxs-lookup"><span data-stu-id="8531c-192">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8531c-193">3 canal, formato de pixel RGBA</span><span class="sxs-lookup"><span data-stu-id="8531c-193">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="8531c-194">Os dados Alfa são definidos como 1 (opaco)</span><span class="sxs-lookup"><span data-stu-id="8531c-194">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="8531c-195">4 canais, formato de pixel RGBA</span><span class="sxs-lookup"><span data-stu-id="8531c-195">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="8531c-196">(Não há dados alfa)</span><span class="sxs-lookup"><span data-stu-id="8531c-196">(No alpha data)</span></span></td>

</tr>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="8531c-197">1 canal, formato de pixel RGBA $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="8531c-197">1 channel, RGBA pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="8531c-198">formato de 1 canal, R pixel</span><span class="sxs-lookup"><span data-stu-id="8531c-198">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="8531c-199">Os dados Alfa são descartados</span><span class="sxs-lookup"><span data-stu-id="8531c-199">Alpha data is discarded</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8531c-200">1 canal, formato de pixel RGBA</span><span class="sxs-lookup"><span data-stu-id="8531c-200">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="8531c-201">Dados Alfa são passados por</span><span class="sxs-lookup"><span data-stu-id="8531c-201">Alpha data is passed through</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8531c-202">3 canal, formato de pixel RGBA</span><span class="sxs-lookup"><span data-stu-id="8531c-202">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="8531c-203">Dados Alfa são passados por</span><span class="sxs-lookup"><span data-stu-id="8531c-203">Alpha data is passed through</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="8531c-204">4 canais, formato de pixel RGBA</span><span class="sxs-lookup"><span data-stu-id="8531c-204">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="8531c-205">Os dados Alfa são descartados</span><span class="sxs-lookup"><span data-stu-id="8531c-205">Alpha data is discarded</span></span></td>

</tr>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="8531c-206">3 canal, formato de pixel RGBA $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="8531c-206">3 channel, RGBA pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="8531c-207">formato de 1 canal, R pixel</span><span class="sxs-lookup"><span data-stu-id="8531c-207">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="8531c-208">Os dados Alfa são descartados</span><span class="sxs-lookup"><span data-stu-id="8531c-208">Alpha data is discarded</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8531c-209">1 canal, formato de pixel RGBA</span><span class="sxs-lookup"><span data-stu-id="8531c-209">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="8531c-210">Dados Alfa são passados por</span><span class="sxs-lookup"><span data-stu-id="8531c-210">Alpha data is passed through</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8531c-211">3 canal, formato de pixel RGBA</span><span class="sxs-lookup"><span data-stu-id="8531c-211">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="8531c-212">Dados Alfa são passados por</span><span class="sxs-lookup"><span data-stu-id="8531c-212">Alpha data is passed through</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="8531c-213">4 canais, formato de pixel RGBA</span><span class="sxs-lookup"><span data-stu-id="8531c-213">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="8531c-214">Os dados Alfa são descartados</span><span class="sxs-lookup"><span data-stu-id="8531c-214">Alpha data is discarded</span></span></td>

</tr>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="8531c-215">4 Channel, formato de pixel RGBA $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="8531c-215">4 channel, RGBA pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="8531c-216">formato de 1 canal, R pixel</span><span class="sxs-lookup"><span data-stu-id="8531c-216">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="8531c-217">(Não há dados alfa)</span><span class="sxs-lookup"><span data-stu-id="8531c-217">(No alpha data)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8531c-218">1 canal, formato de pixel RGBA</span><span class="sxs-lookup"><span data-stu-id="8531c-218">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="8531c-219">Os dados Alfa são definidos como 1 (opaco)</span><span class="sxs-lookup"><span data-stu-id="8531c-219">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8531c-220">3 canal, formato de pixel RGBA</span><span class="sxs-lookup"><span data-stu-id="8531c-220">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="8531c-221">Os dados Alfa são definidos como 1 (opaco)</span><span class="sxs-lookup"><span data-stu-id="8531c-221">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="8531c-222">4 canais, formato de pixel RGBA</span><span class="sxs-lookup"><span data-stu-id="8531c-222">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="8531c-223">(Não há dados alfa)</span><span class="sxs-lookup"><span data-stu-id="8531c-223">(No alpha data)</span></span></td>

</tr>
</tbody>
</table>

## <a name="quality-modes"></a><span data-ttu-id="8531c-224">Modos de qualidade</span><span class="sxs-lookup"><span data-stu-id="8531c-224">Quality modes</span></span>

| <span data-ttu-id="8531c-225">Mode</span><span class="sxs-lookup"><span data-stu-id="8531c-225">Mode</span></span> | <span data-ttu-id="8531c-226">Descrição</span><span class="sxs-lookup"><span data-stu-id="8531c-226">Description</span></span> |
|-|-|
| <span data-ttu-id="8531c-227">Prova de qualidade de D2D1 \_ COLORMANAGEMENT \_ \_</span><span class="sxs-lookup"><span data-stu-id="8531c-227">D2D1\_COLORMANAGEMENT\_QUALITY\_PROOF</span></span> | <span data-ttu-id="8531c-228">O modo de qualidade mais baixo.</span><span class="sxs-lookup"><span data-stu-id="8531c-228">The lowest quality mode.</span></span> <span data-ttu-id="8531c-229">Esse modo requer o nível de recurso 9 \_ 1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="8531c-229">This mode requires feature level 9\_1 or above.</span></span> |
| <span data-ttu-id="8531c-230">D2D1 \_ COLORMANAGEMENT \_ Quality \_ normal</span><span class="sxs-lookup"><span data-stu-id="8531c-230">D2D1\_COLORMANAGEMENT\_QUALITY\_NORMAL</span></span> | <span data-ttu-id="8531c-231">Modo de qualidade normal.</span><span class="sxs-lookup"><span data-stu-id="8531c-231">Normal quality mode.</span></span> <span data-ttu-id="8531c-232">Esse modo requer o nível de recurso 9 \_ 1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="8531c-232">This mode requires feature level 9\_1 or above.</span></span> |
| <span data-ttu-id="8531c-233">D2D1 \_ COLORMANAGEMENT \_ qualidade \_ melhor</span><span class="sxs-lookup"><span data-stu-id="8531c-233">D2D1\_COLORMANAGEMENT\_QUALITY\_BEST</span></span> | <span data-ttu-id="8531c-234">O modo de melhor qualidade.</span><span class="sxs-lookup"><span data-stu-id="8531c-234">The best quality mode.</span></span> <span data-ttu-id="8531c-235">Esse modo requer o nível de recurso 10 \_ 0 ou superior, bem como buffers de precisão de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="8531c-235">This mode requires feature level 10\_0 or above, as well as floating point precision buffers.</span></span> <span data-ttu-id="8531c-236">Esse modo dá suporte à precisão de ponto flutuante, bem como ao intervalo estendido, conforme definido na especificação ICC v 4.3.</span><span class="sxs-lookup"><span data-stu-id="8531c-236">This mode supports floating point precision as well as extended range as defined in the ICC v4.3 specification.</span></span> |

<span data-ttu-id="8531c-237">O efeito de gerenciamento de cores falha ao desenhar se o aplicativo solicitar um modo de qualidade que não tenha suporte do hardware.</span><span class="sxs-lookup"><span data-stu-id="8531c-237">The color management effect fails when drawing if the application requests a quality mode that is not supported by the hardware.</span></span> <span data-ttu-id="8531c-238">Você pode determinar o nível do recurso ao chamar [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice).</span><span class="sxs-lookup"><span data-stu-id="8531c-238">You can determine the feature level when you call [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice).</span></span> <span data-ttu-id="8531c-239">Você pode verificar o suporte ao buffer de ponto flutuante chamando [**ID2D1EffectContext:: IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported) com o valor [**d2d1 \_ buffer \_ Precision \_ 32BPC \_ float**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_buffer_precision).</span><span class="sxs-lookup"><span data-stu-id="8531c-239">You can check for floating point buffer support by calling [**ID2D1EffectContext::IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported) with the value [**D2D1\_BUFFER\_PRECISION\_32BPC\_FLOAT**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_buffer_precision).</span></span>

## <a name="sample-code"></a><span data-ttu-id="8531c-240">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="8531c-240">Sample code</span></span>

<span data-ttu-id="8531c-241">Para obter um exemplo desse efeito, baixe o [exemplo de ajuste de foto de efeitos de Direct2D](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)e veja a lição 4 do exemplo.</span><span class="sxs-lookup"><span data-stu-id="8531c-241">For an example of this effect, download the [Direct2D effects photo adjustment sample](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment), and see Lesson 4 of the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="8531c-242">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8531c-242">Requirements</span></span>

| <span data-ttu-id="8531c-243">Requisito</span><span class="sxs-lookup"><span data-stu-id="8531c-243">Requirement</span></span> | <span data-ttu-id="8531c-244">Valor</span><span class="sxs-lookup"><span data-stu-id="8531c-244">Value</span></span> |
|-|-|
| <span data-ttu-id="8531c-245">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8531c-245">Minimum supported client</span></span> | <span data-ttu-id="8531c-246">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="8531c-246">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="8531c-247">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8531c-247">Minimum supported server</span></span> | <span data-ttu-id="8531c-248">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="8531c-248">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="8531c-249">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8531c-249">Header</span></span> | <span data-ttu-id="8531c-250">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="8531c-250">d2d1effects.h</span></span> |
| <span data-ttu-id="8531c-251">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8531c-251">Library</span></span> | <span data-ttu-id="8531c-252">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="8531c-252">d2d1.lib, dxguid.lib</span></span> |

## <a name="related-topics"></a><span data-ttu-id="8531c-253">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8531c-253">Related topics</span></span>

* [<span data-ttu-id="8531c-254">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="8531c-254">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
