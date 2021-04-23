---
description: Filtro DV Muxer
ms.assetid: 4dd57202-f4de-40d9-b720-efaba8a60a7c
title: Filtro DV Muxer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013251f2f9c1946aaa0f7b3c95edfd2de81c4d78
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908594"
---
# <a name="dv-muxer-filter"></a><span data-ttu-id="20042-103">Filtro DV Muxer</span><span class="sxs-lookup"><span data-stu-id="20042-103">DV Muxer Filter</span></span>

<span data-ttu-id="20042-104">Esse filtro combina um vídeo digital (DV) – fluxo de vídeo codificado com um ou dois fluxos de áudio para produzir um fluxo de DV intercalado.</span><span class="sxs-lookup"><span data-stu-id="20042-104">This filter combines a digital video (DV)—encoded video stream with one or two audio streams to produce an interleaved DV stream.</span></span> <span data-ttu-id="20042-105">Para gravar o fluxo em um arquivo AVI, conecte esse filtro ao filtro [AVI Mux](avi-mux-filter.md) e conecte o *multiplexador AVI* ao filtro do [gravador de arquivo](file-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="20042-105">To write the stream to an AVI file, connect this filter to the [AVI Mux](avi-mux-filter.md) filter and connect the *AVI Mux* to the [File Writer](file-writer-filter.md) filter.</span></span> <span data-ttu-id="20042-106">Para obter mais informações, consulte [vídeo digital no DirectShow](digital-video-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="20042-106">For more information, see [Digital Video in DirectShow](digital-video-in-directshow.md).</span></span>



| <span data-ttu-id="20042-107">Label</span><span class="sxs-lookup"><span data-stu-id="20042-107">Label</span></span> | <span data-ttu-id="20042-108">Valor</span><span class="sxs-lookup"><span data-stu-id="20042-108">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20042-109">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="20042-109">Filter Interfaces</span></span>                        | <span data-ttu-id="20042-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="20042-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span>                                                             |
| <span data-ttu-id="20042-111">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="20042-111">Input Pin Media Types</span></span>                    | <span data-ttu-id="20042-112">**Vídeo**: \_ vídeo de MediaType, MEDIASUBTYPE \_ Dvsd, Format \_ VIDEOINFO **Audio**: MediaType \_ áudio, MEDIASUBTYPE \_ PCM, Format \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="20042-112">**Video**: MEDIATYPE\_Video, MEDIASUBTYPE\_dvsd, FORMAT\_VideoInfo **Audio**: MEDIATYPE\_Audio, MEDIASUBTYPE\_PCM, FORMAT\_WaveFormatEx</span></span> |
| <span data-ttu-id="20042-113">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="20042-113">Input Pin Interfaces</span></span>                     | <span data-ttu-id="20042-114">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="20042-114">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                 |
| <span data-ttu-id="20042-115">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="20042-115">Output Pin Media Types</span></span>                   | <span data-ttu-id="20042-116">MEDIATYPE \_ intercalado, MEDIASUBTYPE \_ DVSD, formato \_ DvInfo</span><span class="sxs-lookup"><span data-stu-id="20042-116">MEDIATYPE\_Interleaved, MEDIASUBTYPE\_dvsd, FORMAT\_DvInfo</span></span>                                                                             |
| <span data-ttu-id="20042-117">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="20042-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="20042-118">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="20042-118">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                       |
| <span data-ttu-id="20042-119">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="20042-119">Filter CLSID</span></span>                             | <span data-ttu-id="20042-120">\_DVMUX CLSID</span><span class="sxs-lookup"><span data-stu-id="20042-120">CLSID\_DVMux</span></span>                                                                                                                           |
| <span data-ttu-id="20042-121">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="20042-121">Property Page CLSID</span></span>                      | <span data-ttu-id="20042-122">Nenhuma página de propriedades</span><span class="sxs-lookup"><span data-stu-id="20042-122">No property page</span></span>                                                                                                                       |
| <span data-ttu-id="20042-123">Executável</span><span class="sxs-lookup"><span data-stu-id="20042-123">Executable</span></span>                               | <span data-ttu-id="20042-124">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="20042-124">qdv.dll</span></span>                                                                                                                                |
| [<span data-ttu-id="20042-125">Núcleo</span><span class="sxs-lookup"><span data-stu-id="20042-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="20042-126">MÉRITO \_ improvável</span><span class="sxs-lookup"><span data-stu-id="20042-126">MERIT\_UNLIKELY</span></span>                                                                                                                        |
| [<span data-ttu-id="20042-127">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="20042-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="20042-128">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="20042-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="20042-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="20042-129">Remarks</span></span>

<span data-ttu-id="20042-130">O DV Muxer pode criar dois pinos de entrada de áudio.</span><span class="sxs-lookup"><span data-stu-id="20042-130">The DV Muxer can create two audio input pins.</span></span> <span data-ttu-id="20042-131">Ele dá suporte aos formatos de áudio mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="20042-131">It supports the audio formats shown in the following table.</span></span>



<span data-ttu-id="20042-132">PIN de áudio 1</span><span class="sxs-lookup"><span data-stu-id="20042-132">Audio Pin 1</span></span>

<span data-ttu-id="20042-133">PIN de áudio 2</span><span class="sxs-lookup"><span data-stu-id="20042-133">Audio Pin 2</span></span>

<span data-ttu-id="20042-134">Formato de Saída</span><span class="sxs-lookup"><span data-stu-id="20042-134">Output Format</span></span>

<span data-ttu-id="20042-135">Taxa de amostra (kHz)</span><span class="sxs-lookup"><span data-stu-id="20042-135">Sample Rate (kHz)</span></span>

<span data-ttu-id="20042-136">Bits/exemplo</span><span class="sxs-lookup"><span data-stu-id="20042-136">Bits/Sample</span></span>

<span data-ttu-id="20042-137">Canais</span><span class="sxs-lookup"><span data-stu-id="20042-137">Channels</span></span>

<span data-ttu-id="20042-138">Taxa de amostragem</span><span class="sxs-lookup"><span data-stu-id="20042-138">Sample Rate</span></span>

<span data-ttu-id="20042-139">Bits/exemplo</span><span class="sxs-lookup"><span data-stu-id="20042-139">Bits/Sample</span></span>

<span data-ttu-id="20042-140">Canais</span><span class="sxs-lookup"><span data-stu-id="20042-140">Channels</span></span>

<span data-ttu-id="20042-141">32</span><span class="sxs-lookup"><span data-stu-id="20042-141">32</span></span>

<span data-ttu-id="20042-142">16</span><span class="sxs-lookup"><span data-stu-id="20042-142">16</span></span>

<span data-ttu-id="20042-143">Mono</span><span class="sxs-lookup"><span data-stu-id="20042-143">Mono</span></span>

<span data-ttu-id="20042-144">Desconectado</span><span class="sxs-lookup"><span data-stu-id="20042-144">Unconnected</span></span>

<span data-ttu-id="20042-145">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="20042-145">SD 2 Channel</span></span>

<span data-ttu-id="20042-146">32</span><span class="sxs-lookup"><span data-stu-id="20042-146">32</span></span>

<span data-ttu-id="20042-147">16</span><span class="sxs-lookup"><span data-stu-id="20042-147">16</span></span>

<span data-ttu-id="20042-148">Estéreo</span><span class="sxs-lookup"><span data-stu-id="20042-148">Stereo</span></span>

<span data-ttu-id="20042-149">Desconectado</span><span class="sxs-lookup"><span data-stu-id="20042-149">Unconnected</span></span>

<span data-ttu-id="20042-150">Canal SD 4</span><span class="sxs-lookup"><span data-stu-id="20042-150">SD 4 Channel</span></span>

<span data-ttu-id="20042-151">44,1 ou 48</span><span class="sxs-lookup"><span data-stu-id="20042-151">44.1 or 48</span></span>

<span data-ttu-id="20042-152">16</span><span class="sxs-lookup"><span data-stu-id="20042-152">16</span></span>

<span data-ttu-id="20042-153">Estéreo ou mono</span><span class="sxs-lookup"><span data-stu-id="20042-153">Stereo or Mono</span></span>

<span data-ttu-id="20042-154">Desconectado</span><span class="sxs-lookup"><span data-stu-id="20042-154">Unconnected</span></span>

<span data-ttu-id="20042-155">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="20042-155">SD 2 Channel</span></span>

<span data-ttu-id="20042-156">Desconectado</span><span class="sxs-lookup"><span data-stu-id="20042-156">Unconnected</span></span>

<span data-ttu-id="20042-157">32</span><span class="sxs-lookup"><span data-stu-id="20042-157">32</span></span>

<span data-ttu-id="20042-158">16</span><span class="sxs-lookup"><span data-stu-id="20042-158">16</span></span>

<span data-ttu-id="20042-159">Estéreo ou mono</span><span class="sxs-lookup"><span data-stu-id="20042-159">Stereo or Mono</span></span>

<span data-ttu-id="20042-160">Não permitido</span><span class="sxs-lookup"><span data-stu-id="20042-160">Disallowed</span></span>

<span data-ttu-id="20042-161">Desconectado</span><span class="sxs-lookup"><span data-stu-id="20042-161">Unconnected</span></span>

<span data-ttu-id="20042-162">44,1 ou 48</span><span class="sxs-lookup"><span data-stu-id="20042-162">44.1 or 48</span></span>

<span data-ttu-id="20042-163">16</span><span class="sxs-lookup"><span data-stu-id="20042-163">16</span></span>

<span data-ttu-id="20042-164">Mono</span><span class="sxs-lookup"><span data-stu-id="20042-164">Mono</span></span>

<span data-ttu-id="20042-165">Não permitido</span><span class="sxs-lookup"><span data-stu-id="20042-165">Disallowed</span></span>

<span data-ttu-id="20042-166">Desconectado</span><span class="sxs-lookup"><span data-stu-id="20042-166">Unconnected</span></span>

<span data-ttu-id="20042-167">44,1 ou 48</span><span class="sxs-lookup"><span data-stu-id="20042-167">44.1 or 48</span></span>

<span data-ttu-id="20042-168">16</span><span class="sxs-lookup"><span data-stu-id="20042-168">16</span></span>

<span data-ttu-id="20042-169">Estéreo</span><span class="sxs-lookup"><span data-stu-id="20042-169">Stereo</span></span>

<span data-ttu-id="20042-170">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="20042-170">SD 2 Channel</span></span>

<span data-ttu-id="20042-171">32</span><span class="sxs-lookup"><span data-stu-id="20042-171">32</span></span>

<span data-ttu-id="20042-172">16</span><span class="sxs-lookup"><span data-stu-id="20042-172">16</span></span>

<span data-ttu-id="20042-173">Mono</span><span class="sxs-lookup"><span data-stu-id="20042-173">Mono</span></span>

<span data-ttu-id="20042-174">32</span><span class="sxs-lookup"><span data-stu-id="20042-174">32</span></span>

<span data-ttu-id="20042-175">16</span><span class="sxs-lookup"><span data-stu-id="20042-175">16</span></span>

<span data-ttu-id="20042-176">Mono</span><span class="sxs-lookup"><span data-stu-id="20042-176">Mono</span></span>

<span data-ttu-id="20042-177">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="20042-177">SD 2 Channel</span></span>

<span data-ttu-id="20042-178">32</span><span class="sxs-lookup"><span data-stu-id="20042-178">32</span></span>

<span data-ttu-id="20042-179">16</span><span class="sxs-lookup"><span data-stu-id="20042-179">16</span></span>

<span data-ttu-id="20042-180">Estéreo ou mono\*</span><span class="sxs-lookup"><span data-stu-id="20042-180">Stereo or Mono\*</span></span>

<span data-ttu-id="20042-181">32</span><span class="sxs-lookup"><span data-stu-id="20042-181">32</span></span>

<span data-ttu-id="20042-182">16</span><span class="sxs-lookup"><span data-stu-id="20042-182">16</span></span>

<span data-ttu-id="20042-183">Estéreo ou mono\*</span><span class="sxs-lookup"><span data-stu-id="20042-183">Stereo or Mono\*</span></span>

<span data-ttu-id="20042-184">Canal SD 4</span><span class="sxs-lookup"><span data-stu-id="20042-184">SD 4 Channel</span></span>

<span data-ttu-id="20042-185">44,1</span><span class="sxs-lookup"><span data-stu-id="20042-185">44.1</span></span>

<span data-ttu-id="20042-186">16</span><span class="sxs-lookup"><span data-stu-id="20042-186">16</span></span>

<span data-ttu-id="20042-187">Mono</span><span class="sxs-lookup"><span data-stu-id="20042-187">Mono</span></span>

<span data-ttu-id="20042-188">44,1</span><span class="sxs-lookup"><span data-stu-id="20042-188">44.1</span></span>

<span data-ttu-id="20042-189">16</span><span class="sxs-lookup"><span data-stu-id="20042-189">16</span></span>

<span data-ttu-id="20042-190">Mono</span><span class="sxs-lookup"><span data-stu-id="20042-190">Mono</span></span>

<span data-ttu-id="20042-191">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="20042-191">SD 2 Channel</span></span>

<span data-ttu-id="20042-192">48</span><span class="sxs-lookup"><span data-stu-id="20042-192">48</span></span>

<span data-ttu-id="20042-193">16</span><span class="sxs-lookup"><span data-stu-id="20042-193">16</span></span>

<span data-ttu-id="20042-194">Mono</span><span class="sxs-lookup"><span data-stu-id="20042-194">Mono</span></span>

<span data-ttu-id="20042-195">48</span><span class="sxs-lookup"><span data-stu-id="20042-195">48</span></span>

<span data-ttu-id="20042-196">16</span><span class="sxs-lookup"><span data-stu-id="20042-196">16</span></span>

<span data-ttu-id="20042-197">Mono</span><span class="sxs-lookup"><span data-stu-id="20042-197">Mono</span></span>

<span data-ttu-id="20042-198">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="20042-198">SD 2 Channel</span></span>

<span data-ttu-id="20042-199">\* Se pelo menos um PIN de entrada for estéreo.</span><span class="sxs-lookup"><span data-stu-id="20042-199">\* If at least one input pin is stereo.</span></span>



 

<span data-ttu-id="20042-200">Para a finalidade desta tabela, o PIN 1 de áudio é definido como o primeiro pino de entrada conectado a uma fonte de áudio, e o PIN de áudio 2 é definido como o segundo PIN de entrada conectado a uma fonte de áudio.</span><span class="sxs-lookup"><span data-stu-id="20042-200">For the purpose of this table, audio pin 1 is defined as the first input pin connected to an audio source, and audio pin 2 is defined as the second input pin connected to an audio source.</span></span> <span data-ttu-id="20042-201">Quando um PIN de áudio estiver conectado, esse esquema de numeração permanecerá em vigor, a menos que ambos os Pins de áudio sejam desconectados.</span><span class="sxs-lookup"><span data-stu-id="20042-201">Once an audio pin is connected, this numbering scheme remains in effect unless both audio pins are disconnected.</span></span> <span data-ttu-id="20042-202">Por exemplo, se você conectar ambos os pinos de áudio e, em seguida, desconectar o PIN de áudio 1, o PIN restante ainda será considerado o PIN 2.</span><span class="sxs-lookup"><span data-stu-id="20042-202">For example, if you connect both audio pins and then disconnect audio pin 1, the remaining pin is still considered pin 2.</span></span>

<span data-ttu-id="20042-203">O áudio fornecido para o pino 1 é registrado no primeiro bloco de áudio dos quadros DV (CH1), e o áudio fornecido para o pino 2 é gravado no segundo bloco de áudio (CH2).</span><span class="sxs-lookup"><span data-stu-id="20042-203">Audio supplied to pin 1 is recorded to the first audio block of the DV frames (CH1), and audio supplied to pin 2 is recorded to the second audio block (CH2).</span></span> <span data-ttu-id="20042-204">Exceção: se o filtro tiver uma entrada estéreo única em 44,1 kHz ou 48 kHz, o canal de áudio à esquerda será gravado no primeiro bloco de áudio e o canal de áudio correto será gravado no segundo bloco de áudio.</span><span class="sxs-lookup"><span data-stu-id="20042-204">Exception: if the filter has a single stereo input at 44.1 kHz or 48 kHz, the left audio channel is recorded to the first audio block, and the right audio channel is recorded to the second audio block.</span></span>

<span data-ttu-id="20042-205">Para a saída do SD 4-Channel: se a entrada for estéreo, a faixa à esquerda será registrada em CHa ou CHc, e a faixa direita será registrada em CHb ou CHd.</span><span class="sxs-lookup"><span data-stu-id="20042-205">For SD 4-channel output: If the input is stereo, the left track is recorded to CHa or CHc, and the right track is recorded to CHb or CHd.</span></span> <span data-ttu-id="20042-206">Se a entrada for mono, o áudio será registrado em CHa ou CHc, e CHb e CHd serão silenciosos.</span><span class="sxs-lookup"><span data-stu-id="20042-206">If the input is mono, the audio is recorded to CHa or CHc, and CHb and CHd are silent.</span></span>

<span data-ttu-id="20042-207">Conectando e desconectando o PIN de áudio 1, é possível alcançar um formato não permitido.</span><span class="sxs-lookup"><span data-stu-id="20042-207">By connecting and disconnecting audio pin 1, it is possible to reach a disallowed format.</span></span> <span data-ttu-id="20042-208">Nesse caso, o método [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) do filtro retorna VFW \_ E \_ não \_ conectado.</span><span class="sxs-lookup"><span data-stu-id="20042-208">In that case, the filter's [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method returns VFW\_E\_NOT\_CONNECTED.</span></span> <span data-ttu-id="20042-209">Essa limitação impede uma situação em que o primeiro bloco de áudio não tem áudio, mas o segundo bloco de áudio tem áudio.</span><span class="sxs-lookup"><span data-stu-id="20042-209">This limitation prevents a situation in which the first audio block has no audio, but the second audio block does have audio.</span></span> <span data-ttu-id="20042-210">O segundo bloco deve ter áudio somente se o primeiro bloco também tiver áudio.</span><span class="sxs-lookup"><span data-stu-id="20042-210">The second block should have audio only if the first block also has audio.</span></span>

<span data-ttu-id="20042-211">O DV Muxer não permite entradas de áudio com taxas de amostragem diferentes.</span><span class="sxs-lookup"><span data-stu-id="20042-211">The DV Muxer does not permit audio inputs with different sampling rates.</span></span> <span data-ttu-id="20042-212">No entanto, os métodos de criação de gráficos, como [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) , normalmente adicionarão o filtro de [invólucro do ACM](acm-wrapper-filter.md) , que converterá o segundo fluxo de áudio para corresponder à taxa de amostragem do primeiro fluxo.</span><span class="sxs-lookup"><span data-stu-id="20042-212">However, graph-building methods such as [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) will typically add the [ACM Wrapper](acm-wrapper-filter.md) filter, which will convert the second audio stream to match the first stream's sampling rate.</span></span>

<span data-ttu-id="20042-213">Se a entrada de áudio for 48 kHz ou 32 kHz, a saída de áudio será bloqueada.</span><span class="sxs-lookup"><span data-stu-id="20042-213">If the audio input is 48 kHz or 32 kHz, the audio output is locked.</span></span> <span data-ttu-id="20042-214">(Não é possível bloquear áudio de 44,1 kHz.)</span><span class="sxs-lookup"><span data-stu-id="20042-214">(It is not possible to lock 44.1-kHz audio.)</span></span>

<span data-ttu-id="20042-215">Se nenhum PIN de áudio estiver conectado, a saída conterá os dados de áudio dos quadros de vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="20042-215">If no audio pins are connected, the output contains the audio data from the incoming DV frames.</span></span> <span data-ttu-id="20042-216">Isso pode ser silêncio ou dados de áudio válidos.</span><span class="sxs-lookup"><span data-stu-id="20042-216">This might be silence, or valid audio data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20042-217">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="20042-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20042-218">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="20042-218">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="20042-219">Vídeo digital no DirectShow</span><span class="sxs-lookup"><span data-stu-id="20042-219">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



