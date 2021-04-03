---
title: Informações de tempo
description: Informações de tempo
ms.assetid: ff9d6fb2-1387-49ce-a4de-1b2f67353628
keywords:
- MIDI (interface digital de instrumento musical), informações de tempo
- MIDI (interface digital de instrumentos musicais), informações de tempo
- buffers de fluxo, informações de tempo
- Estrutura MIDIEVENT
- buffers de fluxo, formato SMPTE
- buffers de fluxo, tempo de nota do trimestre
- buffers de fluxo, tiques
- Formato SMPTE
- hora da nota do trimestre
- ticks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2daf5b1847456e8fb518665521e484118fead79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084468"
---
# <a name="timing-information"></a><span data-ttu-id="c6ea9-113">Informações de tempo</span><span class="sxs-lookup"><span data-stu-id="c6ea9-113">Timing Information</span></span>

<span data-ttu-id="c6ea9-114">As informações de tempo para um evento MIDI são armazenadas no membro **dwDeltaTime** da estrutura [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) .</span><span class="sxs-lookup"><span data-stu-id="c6ea9-114">Timing information for a MIDI event is stored in the **dwDeltaTime** member of the [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure.</span></span> <span data-ttu-id="c6ea9-115">O tempo é fornecido em tiques, conforme definido na especificação *padrão de arquivos MIDI 1,0* .</span><span class="sxs-lookup"><span data-stu-id="c6ea9-115">Time is given in ticks, as defined in the *Standard MIDI Files 1.0* specification.</span></span> <span data-ttu-id="c6ea9-116">O comprimento de um tique é definido pelo formato de hora e possivelmente pelo tempo associado ao fluxo.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-116">The length of a tick is defined by the time format and possibly the tempo associated with the stream.</span></span> <span data-ttu-id="c6ea9-117">Para obter mais informações sobre fluxos, consulte [fluxos de Midi](midi-streams.md).</span><span class="sxs-lookup"><span data-stu-id="c6ea9-117">For more information about streams, see [MIDI Streams](midi-streams.md).</span></span>

<span data-ttu-id="c6ea9-118">Uma escala é expressa como microssegundos por trimestre ou como tiques de hora SMPTE (sociedade de imagem de movimento e engenheiros de televisão).</span><span class="sxs-lookup"><span data-stu-id="c6ea9-118">A tick is expressed either as microseconds per quarter note or as ticks of SMPTE (Society of Motion Picture and Television Engineers) time.</span></span> <span data-ttu-id="c6ea9-119">Os aplicativos que enviam mensagens de MIDI individualmente ou usam mensagens MIDI não processadas usam informações de hora do trimestre e tempo para determinar a duração de um tique.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-119">Applications that send MIDI messages individually or use unprocessed MIDI messages use quarter note time and tempo information to determine the duration of a tick.</span></span> <span data-ttu-id="c6ea9-120">Aplicativos que processam mensagens MIDI podem armazenar o tempo decorrido como uma contagem das unidades SMPTE que estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-120">Applications that preprocess MIDI messages can store the elapsed time as a count of the SMPTE units being used.</span></span>

<span data-ttu-id="c6ea9-121">O tempo de nota de trimestre é indicado com um zero no bit de palavra alta (bit 15) da palavra de divisão de tempo.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-121">Quarter note time is indicated with a zero in the high-word bit (bit 15) of the time-division word.</span></span> <span data-ttu-id="c6ea9-122">O restante da palavra contém as marcações por trimestre.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-122">The remainder of the word contains the ticks per quarter note.</span></span> <span data-ttu-id="c6ea9-123">Um tempo associado a um fluxo de dados MIDI é mantido em unidades (microssegundos por trimestre) consistentes com a especificação *1,0 de arquivos MIDI padrão* .</span><span class="sxs-lookup"><span data-stu-id="c6ea9-123">A tempo associated with a stream of MIDI data is kept in units (microseconds per quarter note) consistent with the *Standard MIDI Files 1.0* specification.</span></span> <span data-ttu-id="c6ea9-124">Por exemplo, um quarto de nota em 4/4 tempo que usa um tempo de 500.000 microssegundos por trimestre de observação é reproduzido à taxa de 120 batidas por minuto.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-124">For example, a quarter note in 4/4 time that uses a tempo of 500,000 microseconds per quarter note plays at the rate of 120 beats per minute.</span></span>

<span data-ttu-id="c6ea9-125">Os formatos de divisão de tempo SMPTE especificam completamente o comprimento de um tique sem a necessidade de informações de tempo.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-125">SMPTE time division formats completely specify the length of a tick without the need for tempo information.</span></span> <span data-ttu-id="c6ea9-126">No uso de formatos de hora SMPTE, as sequências MIDI podem ser sincronizadas com outros eventos SMPTE, como vídeo ou áudio distribuído.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-126">In using SMPTE time formats, MIDI sequences can be synchronized with other SMPTE events, such as video or striped audio.</span></span> <span data-ttu-id="c6ea9-127">O horário SMPTE é indicado com um 1 no bit de ordem superior (bit 15) da palavra de divisão de tempo.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-127">SMPTE time is indicated with a 1 in the high-order bit (bit 15) of the time-division word.</span></span> <span data-ttu-id="c6ea9-128">O restante do byte mais significativo especifica o formato SMPTE em uso como valores negativos.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-128">The rest of the most-significant byte specifies the SMPTE format in use as negative values.</span></span> <span data-ttu-id="c6ea9-129">Os formatos SMPTE com suporte e seus valores correspondentes (entre parênteses) são 24 (-24), 25 (-25), 30 (-30) e 30 Drop (-29).</span><span class="sxs-lookup"><span data-stu-id="c6ea9-129">The supported SMPTE formats and their corresponding values (in parentheses) are 24 (-24), 25 (-25), 30 (-30), and 30 drop (-29).</span></span> <span data-ttu-id="c6ea9-130">O byte inferior da palavra de divisão de tempo especifica o número de tiques por quadro SMPTE.</span><span class="sxs-lookup"><span data-stu-id="c6ea9-130">The low byte of the time-division word specifies the number of ticks per SMPTE frame.</span></span>

 

 