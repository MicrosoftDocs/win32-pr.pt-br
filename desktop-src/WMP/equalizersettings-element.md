---
title: Elemento EQUALIZERSETTINGS
description: Elemento EQUALIZERSETTINGS
ms.assetid: 521f1c95-7904-4085-a8bc-5399d667dfb1
keywords:
- Capas do Windows Media Player, elemento EQUALIZERSETTINGS
- Skins, elemento EQUALIZERSETTINGS
- Elemento EQUALIZERSETTINGS
- referência para capas, elemento EQUALIZERSETTINGS
- elementos, EQUALIZERSETTINGS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae20500dfba656450c3102ee80b4a06e089fe8ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498708"
---
# <a name="equalizersettings-element"></a><span data-ttu-id="eb8bd-108">Elemento EQUALIZERSETTINGS</span><span class="sxs-lookup"><span data-stu-id="eb8bd-108">EQUALIZERSETTINGS Element</span></span>

<span data-ttu-id="eb8bd-109">O elemento **EQUALIZERSETTINGS** fornece uma maneira de manipular o equalizador gráfico e outras configurações de áudio do Windows Media Player usando os atributos e o método listados aqui.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-109">The **EQUALIZERSETTINGS** element provides a way to manipulate the graphic equalizer and other audio settings of Windows Media Player using the attributes and method listed here.</span></span>

<span data-ttu-id="eb8bd-110">O elemento **EQUALIZERSETTINGS** dá suporte aos seguintes atributos.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-110">The **EQUALIZERSETTINGS** element supports the following attributes.</span></span>



| <span data-ttu-id="eb8bd-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="eb8bd-111">Attribute</span></span>                                                          | <span data-ttu-id="eb8bd-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="eb8bd-112">Description</span></span>                                                                                             |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb8bd-113">bandas</span><span class="sxs-lookup"><span data-stu-id="eb8bd-113">bands</span></span>](equalizersettings-bands.md)                               | <span data-ttu-id="eb8bd-114">Recupera o número de faixas de frequência com suporte.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-114">Retrieves the number of frequency bands supported.</span></span>                                                      |
| [<span data-ttu-id="eb8bd-115">pular</span><span class="sxs-lookup"><span data-stu-id="eb8bd-115">bypass</span></span>](equalizersettings-bypass.md)                             | <span data-ttu-id="eb8bd-116">Especifica ou recupera um valor que indica se o filtro de equalizador é ignorado no gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-116">Specifies or retrieves a value indicating whether the equalizer filter is bypassed in the filter graph.</span></span> |
| [<span data-ttu-id="eb8bd-117">Fading cruzado</span><span class="sxs-lookup"><span data-stu-id="eb8bd-117">crossFade</span></span>](equalizersettings-crossfade.md)                       | <span data-ttu-id="eb8bd-118">Especifica ou recupera um valor que indica se o esmaecimento cruzado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-118">Specifies or retrieves a value indicating whether cross-fade is enabled.</span></span>                                |
| [<span data-ttu-id="eb8bd-119">crossFadeWindow</span><span class="sxs-lookup"><span data-stu-id="eb8bd-119">crossFadeWindow</span></span>](equalizersettings-crossfadewindow.md)           | <span data-ttu-id="eb8bd-120">Especifica ou recupera a quantidade de sobreposição de esmaecimento cruzado em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-120">Specifies or retrieves the amount of cross-fade overlap in milliseconds.</span></span>                                |
| [<span data-ttu-id="eb8bd-121">currentPreset</span><span class="sxs-lookup"><span data-stu-id="eb8bd-121">currentPreset</span></span>](equalizersettings-currentpreset.md)               | <span data-ttu-id="eb8bd-122">Especifica ou recupera o índice da predefinição atual.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-122">Specifies or retrieves the index of the current preset.</span></span>                                                 |
| [<span data-ttu-id="eb8bd-123">currentPresetTitle</span><span class="sxs-lookup"><span data-stu-id="eb8bd-123">currentPresetTitle</span></span>](equalizersettings-currentpresettitle.md)     | <span data-ttu-id="eb8bd-124">Recupera o título da predefinição atual.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-124">Retrieves the title of the current preset.</span></span>                                                              |
| [<span data-ttu-id="eb8bd-125">currentSpeakerName</span><span class="sxs-lookup"><span data-stu-id="eb8bd-125">currentSpeakerName</span></span>](equalizersettings-currentspeakername.md)     | <span data-ttu-id="eb8bd-126">Recupera o nome da configuração do alto-falante atual.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-126">Retrieves the name of the current speaker setting.</span></span>                                                      |
| [<span data-ttu-id="eb8bd-127">enableSplineTension</span><span class="sxs-lookup"><span data-stu-id="eb8bd-127">enableSplineTension</span></span>](equalizersettings-enablesplinetension.md)   | <span data-ttu-id="eb8bd-128">Especifica ou recupera um valor que indica se a tensão de spline está habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-128">Specifies or retrieves a value indicating whether spline tension is enabled or disabled.</span></span>                |
| [<span data-ttu-id="eb8bd-129">enhancedAudio</span><span class="sxs-lookup"><span data-stu-id="eb8bd-129">enhancedAudio</span></span>](equalizersettings-enhancedaudio.md)               | <span data-ttu-id="eb8bd-130">Especifica ou recupera um valor que indica se o áudio avançado está ativado.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-130">Specifies or retrieves a value indicating whether enhanced audio is turned on.</span></span>                          |
| [<span data-ttu-id="eb8bd-131">gainLevels</span><span class="sxs-lookup"><span data-stu-id="eb8bd-131">gainLevels</span></span>](equalizersettings-gainlevels.md)                     | <span data-ttu-id="eb8bd-132">Especifica ou recupera o nível de lucro da faixa correspondente ao índice fornecido.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-132">Specifies or retrieves the gain level of the band corresponding to the index provided.</span></span>                  |
| [<span data-ttu-id="eb8bd-133">gainLevel1</span><span class="sxs-lookup"><span data-stu-id="eb8bd-133">gainLevel1</span></span>](equalizersettings-gainlevel1.md)                     | <span data-ttu-id="eb8bd-134">Especifica ou recupera o nível de lucro da faixa 1.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-134">Specifies or retrieves the gain level of band 1.</span></span>                                                        |
| [<span data-ttu-id="eb8bd-135">gainLevel2</span><span class="sxs-lookup"><span data-stu-id="eb8bd-135">gainLevel2</span></span>](equalizersettings-gainlevel2.md)                     | <span data-ttu-id="eb8bd-136">Especifica ou recupera o nível de lucro da faixa 2.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-136">Specifies or retrieves the gain level of band 2.</span></span>                                                        |
| [<span data-ttu-id="eb8bd-137">gainLevel3</span><span class="sxs-lookup"><span data-stu-id="eb8bd-137">gainLevel3</span></span>](equalizersettings-gainlevel3.md)                     | <span data-ttu-id="eb8bd-138">Especifica ou recupera o nível de lucro da faixa 3.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-138">Specifies or retrieves the gain level of band 3.</span></span>                                                        |
| [<span data-ttu-id="eb8bd-139">gainLevel4</span><span class="sxs-lookup"><span data-stu-id="eb8bd-139">gainLevel4</span></span>](equalizersettings-gainlevel4.md)                     | <span data-ttu-id="eb8bd-140">Especifica ou recupera o nível de lucro da faixa 4.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-140">Specifies or retrieves the gain level of band 4.</span></span>                                                        |
| [<span data-ttu-id="eb8bd-141">gainLevel5</span><span class="sxs-lookup"><span data-stu-id="eb8bd-141">gainLevel5</span></span>](equalizersettings-gainlevel5.md)                     | <span data-ttu-id="eb8bd-142">Especifica ou recupera o nível de lucro da banda 5.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-142">Specifies or retrieves the gain level of band 5.</span></span>                                                        |
| [<span data-ttu-id="eb8bd-143">gainLevel6</span><span class="sxs-lookup"><span data-stu-id="eb8bd-143">gainLevel6</span></span>](equalizersettings-gainlevel6.md)                     | <span data-ttu-id="eb8bd-144">Especifica ou recupera o nível de lucro da faixa 6.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-144">Specifies or retrieves the gain level of band 6.</span></span>                                                        |
| [<span data-ttu-id="eb8bd-145">gainLevel7</span><span class="sxs-lookup"><span data-stu-id="eb8bd-145">gainLevel7</span></span>](equalizersettings-gainlevel7.md)                     | <span data-ttu-id="eb8bd-146">Especifica ou recupera o nível de lucro da banda 7.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-146">Specifies or retrieves the gain level of band 7.</span></span>                                                        |
| [<span data-ttu-id="eb8bd-147">gainLevel8</span><span class="sxs-lookup"><span data-stu-id="eb8bd-147">gainLevel8</span></span>](equalizersettings-gainlevel8.md)                     | <span data-ttu-id="eb8bd-148">Especifica ou recupera o nível de lucro da banda 8.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-148">Specifies or retrieves the gain level of band 8.</span></span>                                                        |
| [<span data-ttu-id="eb8bd-149">gainLevel9</span><span class="sxs-lookup"><span data-stu-id="eb8bd-149">gainLevel9</span></span>](equalizersettings-gainlevel9.md)                     | <span data-ttu-id="eb8bd-150">Especifica ou recupera o nível de lucro da banda 9.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-150">Specifies or retrieves the gain level of band 9.</span></span>                                                        |
| [<span data-ttu-id="eb8bd-151">gainLevel10</span><span class="sxs-lookup"><span data-stu-id="eb8bd-151">gainLevel10</span></span>](equalizersettings-gainlevel10.md)                   | <span data-ttu-id="eb8bd-152">Especifica ou recupera o nível de lucro da faixa 10.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-152">Specifies or retrieves the gain level of band 10.</span></span>                                                       |
| [<span data-ttu-id="eb8bd-153">normalização</span><span class="sxs-lookup"><span data-stu-id="eb8bd-153">normalization</span></span>](equalizersettings-normalization.md)               | <span data-ttu-id="eb8bd-154">Especifica ou recupera um valor que indica se a normalização está habilitada.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-154">Specifies or retrieves a value indicating whether normalization is enabled.</span></span>                             |
| [<span data-ttu-id="eb8bd-155">normalizationAverage</span><span class="sxs-lookup"><span data-stu-id="eb8bd-155">normalizationAverage</span></span>](equalizersettings-normalizationaverage.md) | <span data-ttu-id="eb8bd-156">Recupera o valor de normalização média.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-156">Retrieves the average normalization value.</span></span>                                                              |
| [<span data-ttu-id="eb8bd-157">normalizationPeak</span><span class="sxs-lookup"><span data-stu-id="eb8bd-157">normalizationPeak</span></span>](equalizersettings-normalizationpeak.md)       | <span data-ttu-id="eb8bd-158">Recupera o valor de normalização de pico.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-158">Retrieves the peak normalization value.</span></span>                                                                 |
| [<span data-ttu-id="eb8bd-159">presetCount</span><span class="sxs-lookup"><span data-stu-id="eb8bd-159">presetCount</span></span>](equalizersettings-presetcount.md)                   | <span data-ttu-id="eb8bd-160">Recupera o número de predefinições disponíveis.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-160">Retrieves the number of presets available.</span></span>                                                              |
| [<span data-ttu-id="eb8bd-161">Alto-falante</span><span class="sxs-lookup"><span data-stu-id="eb8bd-161">speakerSize</span></span>](equalizersettings-speakersize.md)                   | <span data-ttu-id="eb8bd-162">Especifica ou recupera o índice do tamanho atual do alto-falante.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-162">Specifies or retrieves the index of the current speaker size.</span></span>                                           |
| [<span data-ttu-id="eb8bd-163">splineTension</span><span class="sxs-lookup"><span data-stu-id="eb8bd-163">splineTension</span></span>](equalizersettings-splinetension.md)               | <span data-ttu-id="eb8bd-164">Especifica ou recupera a tensão de spline para o controle equalizador.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-164">Specifies or retrieves the spline tension for the equalizer control.</span></span>                                    |
| [<span data-ttu-id="eb8bd-165">truBassLevel</span><span class="sxs-lookup"><span data-stu-id="eb8bd-165">truBassLevel</span></span>](equalizersettings-trubasslevel.md)                 | <span data-ttu-id="eb8bd-166">Especifica ou recupera o nível de TruBass do SRS.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-166">Specifies or retrieves the SRS TruBass level.</span></span>                                                           |
| [<span data-ttu-id="eb8bd-167">wowLevel</span><span class="sxs-lookup"><span data-stu-id="eb8bd-167">wowLevel</span></span>](equalizersettings-wowlevel.md)                         | <span data-ttu-id="eb8bd-168">Especifica ou recupera o nível de efeito de WOW do SRS.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-168">Specifies or retrieves the SRS WOW Effect level.</span></span>                                                        |



 

<span data-ttu-id="eb8bd-169">O elemento **EQUALIZERSETTINGS** dá suporte aos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-169">The **EQUALIZERSETTINGS** element supports the following methods.</span></span>



| <span data-ttu-id="eb8bd-170">Método</span><span class="sxs-lookup"><span data-stu-id="eb8bd-170">Method</span></span>                                                 | <span data-ttu-id="eb8bd-171">Descrição</span><span class="sxs-lookup"><span data-stu-id="eb8bd-171">Description</span></span>                                                          |
|--------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="eb8bd-172">nextPreset</span><span class="sxs-lookup"><span data-stu-id="eb8bd-172">nextPreset</span></span>](equalizersettings-nextpreset.md)         | <span data-ttu-id="eb8bd-173">Aplica a próxima predefinição de equalizador.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-173">Applies the next equalizer preset.</span></span>                                   |
| [<span data-ttu-id="eb8bd-174">presetTitle</span><span class="sxs-lookup"><span data-stu-id="eb8bd-174">presetTitle</span></span>](equalizersettings-presettitle.md)       | <span data-ttu-id="eb8bd-175">Recupera o nome da predefinição do equalizador com o índice especificado.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-175">Retrieves the name of the equalizer preset with the specified index.</span></span> |
| [<span data-ttu-id="eb8bd-176">previousPreset</span><span class="sxs-lookup"><span data-stu-id="eb8bd-176">previousPreset</span></span>](equalizersettings-previouspreset.md) | <span data-ttu-id="eb8bd-177">Aplica a predefinição anterior do equalizador.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-177">Applies the previous equalizer preset.</span></span>                               |
| [<span data-ttu-id="eb8bd-178">reset</span><span class="sxs-lookup"><span data-stu-id="eb8bd-178">reset</span></span>](equalizersettings-reset.md)                   | <span data-ttu-id="eb8bd-179">Redefine os níveis de lucro de todas as faixas para zero decibéis.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-179">Resets the gain levels of all bands to zero decibels.</span></span>                |



 

<span data-ttu-id="eb8bd-180">O elemento **EQUALIZERSETTINGS** pode implementar o [atributo \_ onChange](attribute-onchange.md) manipuladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="eb8bd-180">The **EQUALIZERSETTINGS** element can implement the [attribute\_onchange](attribute-onchange.md) event handlers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb8bd-181">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eb8bd-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb8bd-182">**Referência de programação de capa**</span><span class="sxs-lookup"><span data-stu-id="eb8bd-182">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




