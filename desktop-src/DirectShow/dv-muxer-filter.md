---
description: Filtro DV Muxer
ms.assetid: 4dd57202-f4de-40d9-b720-efaba8a60a7c
title: Filtro DV Muxer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2154dd1fc1617ff3f717b1ace6e52c9c507a38e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646124"
---
# <a name="dv-muxer-filter"></a><span data-ttu-id="43215-103">Filtro DV Muxer</span><span class="sxs-lookup"><span data-stu-id="43215-103">DV Muxer Filter</span></span>

<span data-ttu-id="43215-104">Esse filtro combina um vídeo digital (DV) – fluxo de vídeo codificado com um ou dois fluxos de áudio para produzir um fluxo de DV intercalado.</span><span class="sxs-lookup"><span data-stu-id="43215-104">This filter combines a digital video (DV)—encoded video stream with one or two audio streams to produce an interleaved DV stream.</span></span> <span data-ttu-id="43215-105">Para gravar o fluxo em um arquivo AVI, conecte esse filtro ao filtro [AVI Mux](avi-mux-filter.md) e conecte o *multiplexador AVI* ao filtro do [gravador de arquivo](file-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="43215-105">To write the stream to an AVI file, connect this filter to the [AVI Mux](avi-mux-filter.md) filter and connect the *AVI Mux* to the [File Writer](file-writer-filter.md) filter.</span></span> <span data-ttu-id="43215-106">Para obter mais informações, consulte [vídeo digital no DirectShow](digital-video-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="43215-106">For more information, see [Digital Video in DirectShow](digital-video-in-directshow.md).</span></span>



|                                          |                                                                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43215-107">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="43215-107">Filter Interfaces</span></span>                        | <span data-ttu-id="43215-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="43215-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span>                                                             |
| <span data-ttu-id="43215-109">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="43215-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="43215-110">**Vídeo**: \_ vídeo de MediaType, MEDIASUBTYPE \_ Dvsd, Format \_ VIDEOINFO **Audio**: MediaType \_ áudio, MEDIASUBTYPE \_ PCM, Format \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="43215-110">**Video**: MEDIATYPE\_Video, MEDIASUBTYPE\_dvsd, FORMAT\_VideoInfo **Audio**: MEDIATYPE\_Audio, MEDIASUBTYPE\_PCM, FORMAT\_WaveFormatEx</span></span> |
| <span data-ttu-id="43215-111">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="43215-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="43215-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="43215-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                 |
| <span data-ttu-id="43215-113">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="43215-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="43215-114">MEDIATYPE \_ intercalado, MEDIASUBTYPE \_ DVSD, formato \_ DvInfo</span><span class="sxs-lookup"><span data-stu-id="43215-114">MEDIATYPE\_Interleaved, MEDIASUBTYPE\_dvsd, FORMAT\_DvInfo</span></span>                                                                             |
| <span data-ttu-id="43215-115">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="43215-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="43215-116">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="43215-116">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                       |
| <span data-ttu-id="43215-117">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="43215-117">Filter CLSID</span></span>                             | <span data-ttu-id="43215-118">\_DVMUX CLSID</span><span class="sxs-lookup"><span data-stu-id="43215-118">CLSID\_DVMux</span></span>                                                                                                                           |
| <span data-ttu-id="43215-119">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="43215-119">Property Page CLSID</span></span>                      | <span data-ttu-id="43215-120">Nenhuma página de propriedades</span><span class="sxs-lookup"><span data-stu-id="43215-120">No property page</span></span>                                                                                                                       |
| <span data-ttu-id="43215-121">Executável</span><span class="sxs-lookup"><span data-stu-id="43215-121">Executable</span></span>                               | <span data-ttu-id="43215-122">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="43215-122">qdv.dll</span></span>                                                                                                                                |
| [<span data-ttu-id="43215-123">Núcleo</span><span class="sxs-lookup"><span data-stu-id="43215-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="43215-124">MÉRITO \_ improvável</span><span class="sxs-lookup"><span data-stu-id="43215-124">MERIT\_UNLIKELY</span></span>                                                                                                                        |
| [<span data-ttu-id="43215-125">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="43215-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="43215-126">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="43215-126">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="43215-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="43215-127">Remarks</span></span>

<span data-ttu-id="43215-128">O DV Muxer pode criar dois pinos de entrada de áudio.</span><span class="sxs-lookup"><span data-stu-id="43215-128">The DV Muxer can create two audio input pins.</span></span> <span data-ttu-id="43215-129">Ele dá suporte aos formatos de áudio mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="43215-129">It supports the audio formats shown in the following table.</span></span>



<span data-ttu-id="43215-130">PIN de áudio 1</span><span class="sxs-lookup"><span data-stu-id="43215-130">Audio Pin 1</span></span>

<span data-ttu-id="43215-131">PIN de áudio 2</span><span class="sxs-lookup"><span data-stu-id="43215-131">Audio Pin 2</span></span>

<span data-ttu-id="43215-132">Formato de Saída</span><span class="sxs-lookup"><span data-stu-id="43215-132">Output Format</span></span>

<span data-ttu-id="43215-133">Taxa de amostra (kHz)</span><span class="sxs-lookup"><span data-stu-id="43215-133">Sample Rate (kHz)</span></span>

<span data-ttu-id="43215-134">Bits/exemplo</span><span class="sxs-lookup"><span data-stu-id="43215-134">Bits/Sample</span></span>

<span data-ttu-id="43215-135">Canais</span><span class="sxs-lookup"><span data-stu-id="43215-135">Channels</span></span>

<span data-ttu-id="43215-136">Taxa de amostragem</span><span class="sxs-lookup"><span data-stu-id="43215-136">Sample Rate</span></span>

<span data-ttu-id="43215-137">Bits/exemplo</span><span class="sxs-lookup"><span data-stu-id="43215-137">Bits/Sample</span></span>

<span data-ttu-id="43215-138">Canais</span><span class="sxs-lookup"><span data-stu-id="43215-138">Channels</span></span>

<span data-ttu-id="43215-139">32</span><span class="sxs-lookup"><span data-stu-id="43215-139">32</span></span>

<span data-ttu-id="43215-140">16</span><span class="sxs-lookup"><span data-stu-id="43215-140">16</span></span>

<span data-ttu-id="43215-141">Mono</span><span class="sxs-lookup"><span data-stu-id="43215-141">Mono</span></span>

<span data-ttu-id="43215-142">Desconectado</span><span class="sxs-lookup"><span data-stu-id="43215-142">Unconnected</span></span>

<span data-ttu-id="43215-143">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="43215-143">SD 2 Channel</span></span>

<span data-ttu-id="43215-144">32</span><span class="sxs-lookup"><span data-stu-id="43215-144">32</span></span>

<span data-ttu-id="43215-145">16</span><span class="sxs-lookup"><span data-stu-id="43215-145">16</span></span>

<span data-ttu-id="43215-146">Estéreo</span><span class="sxs-lookup"><span data-stu-id="43215-146">Stereo</span></span>

<span data-ttu-id="43215-147">Desconectado</span><span class="sxs-lookup"><span data-stu-id="43215-147">Unconnected</span></span>

<span data-ttu-id="43215-148">Canal SD 4</span><span class="sxs-lookup"><span data-stu-id="43215-148">SD 4 Channel</span></span>

<span data-ttu-id="43215-149">44,1 ou 48</span><span class="sxs-lookup"><span data-stu-id="43215-149">44.1 or 48</span></span>

<span data-ttu-id="43215-150">16</span><span class="sxs-lookup"><span data-stu-id="43215-150">16</span></span>

<span data-ttu-id="43215-151">Estéreo ou mono</span><span class="sxs-lookup"><span data-stu-id="43215-151">Stereo or Mono</span></span>

<span data-ttu-id="43215-152">Desconectado</span><span class="sxs-lookup"><span data-stu-id="43215-152">Unconnected</span></span>

<span data-ttu-id="43215-153">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="43215-153">SD 2 Channel</span></span>

<span data-ttu-id="43215-154">Desconectado</span><span class="sxs-lookup"><span data-stu-id="43215-154">Unconnected</span></span>

<span data-ttu-id="43215-155">32</span><span class="sxs-lookup"><span data-stu-id="43215-155">32</span></span>

<span data-ttu-id="43215-156">16</span><span class="sxs-lookup"><span data-stu-id="43215-156">16</span></span>

<span data-ttu-id="43215-157">Estéreo ou mono</span><span class="sxs-lookup"><span data-stu-id="43215-157">Stereo or Mono</span></span>

<span data-ttu-id="43215-158">Não permitido</span><span class="sxs-lookup"><span data-stu-id="43215-158">Disallowed</span></span>

<span data-ttu-id="43215-159">Desconectado</span><span class="sxs-lookup"><span data-stu-id="43215-159">Unconnected</span></span>

<span data-ttu-id="43215-160">44,1 ou 48</span><span class="sxs-lookup"><span data-stu-id="43215-160">44.1 or 48</span></span>

<span data-ttu-id="43215-161">16</span><span class="sxs-lookup"><span data-stu-id="43215-161">16</span></span>

<span data-ttu-id="43215-162">Mono</span><span class="sxs-lookup"><span data-stu-id="43215-162">Mono</span></span>

<span data-ttu-id="43215-163">Não permitido</span><span class="sxs-lookup"><span data-stu-id="43215-163">Disallowed</span></span>

<span data-ttu-id="43215-164">Desconectado</span><span class="sxs-lookup"><span data-stu-id="43215-164">Unconnected</span></span>

<span data-ttu-id="43215-165">44,1 ou 48</span><span class="sxs-lookup"><span data-stu-id="43215-165">44.1 or 48</span></span>

<span data-ttu-id="43215-166">16</span><span class="sxs-lookup"><span data-stu-id="43215-166">16</span></span>

<span data-ttu-id="43215-167">Estéreo</span><span class="sxs-lookup"><span data-stu-id="43215-167">Stereo</span></span>

<span data-ttu-id="43215-168">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="43215-168">SD 2 Channel</span></span>

<span data-ttu-id="43215-169">32</span><span class="sxs-lookup"><span data-stu-id="43215-169">32</span></span>

<span data-ttu-id="43215-170">16</span><span class="sxs-lookup"><span data-stu-id="43215-170">16</span></span>

<span data-ttu-id="43215-171">Mono</span><span class="sxs-lookup"><span data-stu-id="43215-171">Mono</span></span>

<span data-ttu-id="43215-172">32</span><span class="sxs-lookup"><span data-stu-id="43215-172">32</span></span>

<span data-ttu-id="43215-173">16</span><span class="sxs-lookup"><span data-stu-id="43215-173">16</span></span>

<span data-ttu-id="43215-174">Mono</span><span class="sxs-lookup"><span data-stu-id="43215-174">Mono</span></span>

<span data-ttu-id="43215-175">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="43215-175">SD 2 Channel</span></span>

<span data-ttu-id="43215-176">32</span><span class="sxs-lookup"><span data-stu-id="43215-176">32</span></span>

<span data-ttu-id="43215-177">16</span><span class="sxs-lookup"><span data-stu-id="43215-177">16</span></span>

<span data-ttu-id="43215-178">Estéreo ou mono\*</span><span class="sxs-lookup"><span data-stu-id="43215-178">Stereo or Mono\*</span></span>

<span data-ttu-id="43215-179">32</span><span class="sxs-lookup"><span data-stu-id="43215-179">32</span></span>

<span data-ttu-id="43215-180">16</span><span class="sxs-lookup"><span data-stu-id="43215-180">16</span></span>

<span data-ttu-id="43215-181">Estéreo ou mono\*</span><span class="sxs-lookup"><span data-stu-id="43215-181">Stereo or Mono\*</span></span>

<span data-ttu-id="43215-182">Canal SD 4</span><span class="sxs-lookup"><span data-stu-id="43215-182">SD 4 Channel</span></span>

<span data-ttu-id="43215-183">44,1</span><span class="sxs-lookup"><span data-stu-id="43215-183">44.1</span></span>

<span data-ttu-id="43215-184">16</span><span class="sxs-lookup"><span data-stu-id="43215-184">16</span></span>

<span data-ttu-id="43215-185">Mono</span><span class="sxs-lookup"><span data-stu-id="43215-185">Mono</span></span>

<span data-ttu-id="43215-186">44,1</span><span class="sxs-lookup"><span data-stu-id="43215-186">44.1</span></span>

<span data-ttu-id="43215-187">16</span><span class="sxs-lookup"><span data-stu-id="43215-187">16</span></span>

<span data-ttu-id="43215-188">Mono</span><span class="sxs-lookup"><span data-stu-id="43215-188">Mono</span></span>

<span data-ttu-id="43215-189">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="43215-189">SD 2 Channel</span></span>

<span data-ttu-id="43215-190">48</span><span class="sxs-lookup"><span data-stu-id="43215-190">48</span></span>

<span data-ttu-id="43215-191">16</span><span class="sxs-lookup"><span data-stu-id="43215-191">16</span></span>

<span data-ttu-id="43215-192">Mono</span><span class="sxs-lookup"><span data-stu-id="43215-192">Mono</span></span>

<span data-ttu-id="43215-193">48</span><span class="sxs-lookup"><span data-stu-id="43215-193">48</span></span>

<span data-ttu-id="43215-194">16</span><span class="sxs-lookup"><span data-stu-id="43215-194">16</span></span>

<span data-ttu-id="43215-195">Mono</span><span class="sxs-lookup"><span data-stu-id="43215-195">Mono</span></span>

<span data-ttu-id="43215-196">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="43215-196">SD 2 Channel</span></span>

<span data-ttu-id="43215-197">\* Se pelo menos um PIN de entrada for estéreo.</span><span class="sxs-lookup"><span data-stu-id="43215-197">\* If at least one input pin is stereo.</span></span>



 

<span data-ttu-id="43215-198">Para a finalidade desta tabela, o PIN 1 de áudio é definido como o primeiro pino de entrada conectado a uma fonte de áudio, e o PIN de áudio 2 é definido como o segundo PIN de entrada conectado a uma fonte de áudio.</span><span class="sxs-lookup"><span data-stu-id="43215-198">For the purpose of this table, audio pin 1 is defined as the first input pin connected to an audio source, and audio pin 2 is defined as the second input pin connected to an audio source.</span></span> <span data-ttu-id="43215-199">Quando um PIN de áudio estiver conectado, esse esquema de numeração permanecerá em vigor, a menos que ambos os Pins de áudio sejam desconectados.</span><span class="sxs-lookup"><span data-stu-id="43215-199">Once an audio pin is connected, this numbering scheme remains in effect unless both audio pins are disconnected.</span></span> <span data-ttu-id="43215-200">Por exemplo, se você conectar ambos os pinos de áudio e, em seguida, desconectar o PIN de áudio 1, o PIN restante ainda será considerado o PIN 2.</span><span class="sxs-lookup"><span data-stu-id="43215-200">For example, if you connect both audio pins and then disconnect audio pin 1, the remaining pin is still considered pin 2.</span></span>

<span data-ttu-id="43215-201">O áudio fornecido para o pino 1 é registrado no primeiro bloco de áudio dos quadros DV (CH1), e o áudio fornecido para o pino 2 é gravado no segundo bloco de áudio (CH2).</span><span class="sxs-lookup"><span data-stu-id="43215-201">Audio supplied to pin 1 is recorded to the first audio block of the DV frames (CH1), and audio supplied to pin 2 is recorded to the second audio block (CH2).</span></span> <span data-ttu-id="43215-202">Exceção: se o filtro tiver uma entrada estéreo única em 44,1 kHz ou 48 kHz, o canal de áudio à esquerda será gravado no primeiro bloco de áudio e o canal de áudio correto será gravado no segundo bloco de áudio.</span><span class="sxs-lookup"><span data-stu-id="43215-202">Exception: if the filter has a single stereo input at 44.1 kHz or 48 kHz, the left audio channel is recorded to the first audio block, and the right audio channel is recorded to the second audio block.</span></span>

<span data-ttu-id="43215-203">Para a saída do SD 4-Channel: se a entrada for estéreo, a faixa à esquerda será registrada em CHa ou CHc, e a faixa direita será registrada em CHb ou CHd.</span><span class="sxs-lookup"><span data-stu-id="43215-203">For SD 4-channel output: If the input is stereo, the left track is recorded to CHa or CHc, and the right track is recorded to CHb or CHd.</span></span> <span data-ttu-id="43215-204">Se a entrada for mono, o áudio será registrado em CHa ou CHc, e CHb e CHd serão silenciosos.</span><span class="sxs-lookup"><span data-stu-id="43215-204">If the input is mono, the audio is recorded to CHa or CHc, and CHb and CHd are silent.</span></span>

<span data-ttu-id="43215-205">Conectando e desconectando o PIN de áudio 1, é possível alcançar um formato não permitido.</span><span class="sxs-lookup"><span data-stu-id="43215-205">By connecting and disconnecting audio pin 1, it is possible to reach a disallowed format.</span></span> <span data-ttu-id="43215-206">Nesse caso, o método [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) do filtro retorna VFW \_ E \_ não \_ conectado.</span><span class="sxs-lookup"><span data-stu-id="43215-206">In that case, the filter's [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method returns VFW\_E\_NOT\_CONNECTED.</span></span> <span data-ttu-id="43215-207">Essa limitação impede uma situação em que o primeiro bloco de áudio não tem áudio, mas o segundo bloco de áudio tem áudio.</span><span class="sxs-lookup"><span data-stu-id="43215-207">This limitation prevents a situation in which the first audio block has no audio, but the second audio block does have audio.</span></span> <span data-ttu-id="43215-208">O segundo bloco deve ter áudio somente se o primeiro bloco também tiver áudio.</span><span class="sxs-lookup"><span data-stu-id="43215-208">The second block should have audio only if the first block also has audio.</span></span>

<span data-ttu-id="43215-209">O DV Muxer não permite entradas de áudio com taxas de amostragem diferentes.</span><span class="sxs-lookup"><span data-stu-id="43215-209">The DV Muxer does not permit audio inputs with different sampling rates.</span></span> <span data-ttu-id="43215-210">No entanto, os métodos de criação de gráficos, como [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) , normalmente adicionarão o filtro de [invólucro do ACM](acm-wrapper-filter.md) , que converterá o segundo fluxo de áudio para corresponder à taxa de amostragem do primeiro fluxo.</span><span class="sxs-lookup"><span data-stu-id="43215-210">However, graph-building methods such as [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) will typically add the [ACM Wrapper](acm-wrapper-filter.md) filter, which will convert the second audio stream to match the first stream's sampling rate.</span></span>

<span data-ttu-id="43215-211">Se a entrada de áudio for 48 kHz ou 32 kHz, a saída de áudio será bloqueada.</span><span class="sxs-lookup"><span data-stu-id="43215-211">If the audio input is 48 kHz or 32 kHz, the audio output is locked.</span></span> <span data-ttu-id="43215-212">(Não é possível bloquear áudio de 44,1 kHz.)</span><span class="sxs-lookup"><span data-stu-id="43215-212">(It is not possible to lock 44.1-kHz audio.)</span></span>

<span data-ttu-id="43215-213">Se nenhum PIN de áudio estiver conectado, a saída conterá os dados de áudio dos quadros de vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="43215-213">If no audio pins are connected, the output contains the audio data from the incoming DV frames.</span></span> <span data-ttu-id="43215-214">Isso pode ser silêncio ou dados de áudio válidos.</span><span class="sxs-lookup"><span data-stu-id="43215-214">This might be silence, or valid audio data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43215-215">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="43215-215">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43215-216">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="43215-216">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="43215-217">Vídeo digital no DirectShow</span><span class="sxs-lookup"><span data-stu-id="43215-217">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



