---
title: Codificação de taxa de bits variável (VBR)
description: Codificação de taxa de bits variável (VBR)
ms.assetid: d3fe0cc6-64d7-44ce-8bb4-dd2eed021345
keywords:
- SDK do Windows Media Format, codificação de VBR
- SDK do Windows Media Format, taxa de bits variável (VBR)
- SDK do Windows Media Format, codificação VBR com base na qualidade
- Windows Media Format SDK, codificação de VBR não restringida
- Windows Media Format SDK, codificação de taxa de bits restrita
- codecs, codificação de VBR
- codecs, taxa de bits variável (VBR)
- codecs, codificação de VBR com base na qualidade
- codecs, codificação de VBR não restringida
- codecs, codificação de taxa de bits restrita
- taxa de bits variável (VBR), sobre
- VBR (taxa de bits variável), sobre
- codificação de VBR com base na qualidade, sobre
- codificação de VBR não restringida, sobre
- codificação de taxa de bits restrita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b24a32b693cc4801f95695cc2d6e5f9ffa400c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105814452"
---
# <a name="variable-bit-rate-vbr-encoding"></a><span data-ttu-id="2d21d-118">Codificação de taxa de bits variável (VBR)</span><span class="sxs-lookup"><span data-stu-id="2d21d-118">Variable Bit Rate (VBR) Encoding</span></span>

<span data-ttu-id="2d21d-119">A codificação de taxa de bits variável (VBR) é uma alternativa para a taxa de bits constante (CBR) e é suportada por alguns codecs.</span><span class="sxs-lookup"><span data-stu-id="2d21d-119">Variable bit rate (VBR) encoding is an alternative to constant bit rate encoding (CBR) and is supported by some codecs.</span></span> <span data-ttu-id="2d21d-120">Onde a codificação CBR se esforça para manter a taxa de bits da mídia codificada, a VBR busca obter a melhor qualidade possível da mídia codificada.</span><span class="sxs-lookup"><span data-stu-id="2d21d-120">Where CBR encoding strives to maintain the bit rate of the encoded media, VBR strives to achieve the best possible quality of the encoded media.</span></span>

<span data-ttu-id="2d21d-121">A qualidade do conteúdo codificado é determinada pela quantidade de dados que é perdida quando o conteúdo é compactado e descompactado.</span><span class="sxs-lookup"><span data-stu-id="2d21d-121">The quality of encoded content is determined by the amount of data that is lost when the content is compressed and decompressed.</span></span> <span data-ttu-id="2d21d-122">Muitos fatores influenciam a perda de dados no processo de compressão, Porém, em geral, quanto mais complexos forem os dados originais e quanto maior for a taxa de compressão, mais detalhes são perdidos no processo de compactação.</span><span class="sxs-lookup"><span data-stu-id="2d21d-122">Many factors affect the loss of data in the compression process, but in general, the more complex the original data and the higher the compression ratio, the more detail is lost in the compression process.</span></span>

<span data-ttu-id="2d21d-123">Há três tipos de codificação de VBR: baseada em qualidade, irrestrito e restrito.</span><span class="sxs-lookup"><span data-stu-id="2d21d-123">There are three types of VBR encoding: quality-based, unconstrained, and constrained.</span></span>

## <a name="quality-based-vbr-encoding"></a><span data-ttu-id="2d21d-124">Codificação de VBR com base na qualidade</span><span class="sxs-lookup"><span data-stu-id="2d21d-124">Quality-based VBR Encoding</span></span>

<span data-ttu-id="2d21d-125">O primeiro tipo de codificação de VBR é baseado em qualidade, que usa uma passagem de codificação.</span><span class="sxs-lookup"><span data-stu-id="2d21d-125">The first type of VBR encoding is quality-based, which uses one encoding pass.</span></span> <span data-ttu-id="2d21d-126">A codificação VBR com base na qualidade permite que você especifique um nível de qualidade para um fluxo de mídia digital em vez de uma taxa de bits.</span><span class="sxs-lookup"><span data-stu-id="2d21d-126">Quality-based VBR encoding enables you to specify a level of quality for a digital media stream instead of a bit rate.</span></span> <span data-ttu-id="2d21d-127">O codec codificará o conteúdo para que todos os exemplos sejam de qualidade comparável.</span><span class="sxs-lookup"><span data-stu-id="2d21d-127">The codec will then encode the content so that all samples are of comparable quality.</span></span>

<span data-ttu-id="2d21d-128">A principal vantagem da codificação de VBR com base na qualidade é que a qualidade é consistente dentro de um arquivo e de um arquivo para o outro.</span><span class="sxs-lookup"><span data-stu-id="2d21d-128">The main advantage of quality-based VBR encoding is that quality is consistent within a file and from one file to the next.</span></span> <span data-ttu-id="2d21d-129">Por exemplo, você pode escrever um programa para copiar músicas de CD para arquivos ASF em um computador.</span><span class="sxs-lookup"><span data-stu-id="2d21d-129">For example, you can write a program to copy songs from CD to ASF files on a computer.</span></span> <span data-ttu-id="2d21d-130">Nesse caso, a qualidade consistente provavelmente é mais importante para a experiência do usuário final do que o tamanho de arquivo consistente.</span><span class="sxs-lookup"><span data-stu-id="2d21d-130">In this case, consistent quality is probably more important to the end-user experience than consistent file size.</span></span> <span data-ttu-id="2d21d-131">O uso da codificação VBR com base na qualidade garantiria que todas as músicas copiadas tenham a mesma qualidade.</span><span class="sxs-lookup"><span data-stu-id="2d21d-131">Using quality-based VBR encoding would ensure that all of the songs copied are of the same quality.</span></span>

<span data-ttu-id="2d21d-132">A desvantagem da codificação de VBR baseada em qualidade é que não há realmente nenhuma maneira de saber os requisitos de tamanho ou largura de banda da mídia codificada antes da codificação.</span><span class="sxs-lookup"><span data-stu-id="2d21d-132">The disadvantage of quality-based VBR encoding is that there is really no way to know the size or bandwidth requirements of the encoded media before encoding.</span></span> <span data-ttu-id="2d21d-133">Isso pode tornar arquivos codificados em taxa de bits com base em qualidade inadequados para circunstâncias em que a memória ou largura de banda são restritas, como players de mídia portáteis ou conexões de Internet de baixa largura de banda.</span><span class="sxs-lookup"><span data-stu-id="2d21d-133">This can make quality-based VBR-encoded files inappropriate for circumstances where memory or bandwidth are restricted, such as portable media players, or low-bandwidth Internet connections.</span></span>

<span data-ttu-id="2d21d-134">Em geral, a codificação VBR com base na qualidade é adequada para a reprodução local ou conexões de rede de largura de banda alta.</span><span class="sxs-lookup"><span data-stu-id="2d21d-134">In general, quality-based VBR encoding is well suited for local playback or high bandwidth network connections.</span></span> <span data-ttu-id="2d21d-135">Nesses casos, a qualidade consistente oferecerá uma melhor experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="2d21d-135">In those cases, the consistent quality will provide a better user experience.</span></span>

## <a name="unconstrained-vbr-encoding"></a><span data-ttu-id="2d21d-136">Codificação de VBR não restringida</span><span class="sxs-lookup"><span data-stu-id="2d21d-136">Unconstrained VBR Encoding</span></span>

<span data-ttu-id="2d21d-137">A codificação de VBR não restringida usa duas passagens de codificação.</span><span class="sxs-lookup"><span data-stu-id="2d21d-137">Unconstrained VBR encoding uses two encoding passes.</span></span> <span data-ttu-id="2d21d-138">Ao usar a codificação VBR não restringida, você especifica uma taxa de bits para o fluxo, como você faria com a codificação de CBR.</span><span class="sxs-lookup"><span data-stu-id="2d21d-138">When using unconstrained VBR encoding, you specify a bit rate for the stream, as you would with CBR encoding.</span></span> <span data-ttu-id="2d21d-139">No entanto, o codec usa esse valor somente como a taxa de bits média para o fluxo e codifica para que a qualidade seja a mais alta possível, mantendo a média.</span><span class="sxs-lookup"><span data-stu-id="2d21d-139">However, the codec uses this value only as the average bit rate for the stream and encodes so that the quality is as high as possible while maintaining the average.</span></span> <span data-ttu-id="2d21d-140">A taxa de bits real em qualquer ponto no fluxo codificado pode variar muito do valor médio.</span><span class="sxs-lookup"><span data-stu-id="2d21d-140">The actual bit rate at any point in the encoded stream can vary greatly from the average value.</span></span>

<span data-ttu-id="2d21d-141">Você não define uma janela de buffer para a codificação de taxa de bits não restringida como faria para um fluxo codificado em CBR.</span><span class="sxs-lookup"><span data-stu-id="2d21d-141">You do not set a buffer window for unconstrained VBR encoding as you would for a CBR-encoded stream.</span></span> <span data-ttu-id="2d21d-142">Em vez disso, o codec computa o tamanho da janela de buffer necessária com base nos requisitos dos exemplos codificados.</span><span class="sxs-lookup"><span data-stu-id="2d21d-142">Instead, the codec computes the size of the required buffer window based on the requirements of the encoded samples.</span></span>

<span data-ttu-id="2d21d-143">A vantagem da codificação de VBR não restringida é que o fluxo compactado tem a melhor qualidade possível enquanto permanece dentro de uma largura de banda média previsível.</span><span class="sxs-lookup"><span data-stu-id="2d21d-143">The advantage of unconstrained VBR encoding is that the compressed stream has the highest possible quality while staying within a predictable average bandwidth.</span></span>

## <a name="constrained-vbr-encoding"></a><span data-ttu-id="2d21d-144">Codificação de taxa de bits restrita</span><span class="sxs-lookup"><span data-stu-id="2d21d-144">Constrained VBR Encoding</span></span>

<span data-ttu-id="2d21d-145">A codificação de taxa de bits restrita é idêntica à codificação VBR não restrita, exceto pelo fato de que você especifica uma taxa de bit máxima e uma janela de buffer máximo no perfil.</span><span class="sxs-lookup"><span data-stu-id="2d21d-145">Constrained VBR encoding is identical to unconstrained VBR encoding, except that you specify a maximum bit rate and a maximum buffer window in the profile.</span></span> <span data-ttu-id="2d21d-146">Em seguida, o codec usa os valores máximos para determinar como compactar os dados.</span><span class="sxs-lookup"><span data-stu-id="2d21d-146">The codec then uses the maximum values to determine how to compress the data.</span></span> <span data-ttu-id="2d21d-147">Se você definir os valores máximos como alto o suficiente, a codificação de taxa de bits restrita produzirá o mesmo fluxo codificado como codificação de VBR não restrita.</span><span class="sxs-lookup"><span data-stu-id="2d21d-147">If you set the maximum values high enough, constrained VBR encoding will produce the same encoded stream as unconstrained VBR encoding.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d21d-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2d21d-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d21d-149">**Escolhendo um método de codificação**</span><span class="sxs-lookup"><span data-stu-id="2d21d-149">**Choosing an Encoding Method**</span></span>](choosing-an-encoding-method.md)
</dt> <dt>

[<span data-ttu-id="2d21d-150">**Recursos do codec**</span><span class="sxs-lookup"><span data-stu-id="2d21d-150">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="2d21d-151">**Configurando fluxos**</span><span class="sxs-lookup"><span data-stu-id="2d21d-151">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="2d21d-152">**Configurando fluxos de VBR**</span><span class="sxs-lookup"><span data-stu-id="2d21d-152">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> <dt>

[<span data-ttu-id="2d21d-153">**Codificação de taxa de bits constante (CBR)**</span><span class="sxs-lookup"><span data-stu-id="2d21d-153">**Constant Bit Rate (CBR) Encoding**</span></span>](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="2d21d-154">**Codificação de duas passagens**</span><span class="sxs-lookup"><span data-stu-id="2d21d-154">**Two-Pass Encoding**</span></span>](two-pass-encoding.md)
</dt> <dt>

[<span data-ttu-id="2d21d-155">**Usando a codificação Two-Pass**</span><span class="sxs-lookup"><span data-stu-id="2d21d-155">**Using Two-Pass Encoding**</span></span>](using-two-pass-encoding.md)
</dt> </dl>

 

 




