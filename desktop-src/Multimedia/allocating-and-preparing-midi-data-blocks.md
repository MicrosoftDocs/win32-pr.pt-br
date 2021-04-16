---
title: Alocando e preparando blocos de dados MIDI
description: Alocando e preparando blocos de dados MIDI
ms.assetid: b3a70441-e8f9-4886-bf22-426ebd74d045
keywords:
- MIDI (interface digital de instrumento musical), alocando blocos de dados
- MIDI (interface digital de instrumentos musicais), alocando blocos de dados
- Serviços de MIDI, alocando blocos de dados
- alocando blocos de dados MIDI
- MIDI (interface digital de instrumento musical), preparando blocos de dados
- MIDI (interface digital de instrumentos musicais), preparando blocos de dados
- Serviços de MIDI, preparando blocos de dados
- preparando blocos de dados MIDI
- MIDI (interface digital de instrumento musical), blocos de dados
- MIDI (interface digital de instrumentos musicais), blocos de dados
- Serviços de MIDI, blocos de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48b23a72dfd46035a3d23743faa7228e5fe85aaf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105757774"
---
# <a name="allocating-and-preparing-midi-data-blocks"></a><span data-ttu-id="dacc2-114">Alocando e preparando blocos de dados MIDI</span><span class="sxs-lookup"><span data-stu-id="dacc2-114">Allocating and Preparing MIDI Data Blocks</span></span>

<span data-ttu-id="dacc2-115">As funções [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg), [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)e [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) exigem que os aplicativos aloquem blocos de dados para passar para os drivers de dispositivo para fins de reprodução ou gravação.</span><span class="sxs-lookup"><span data-stu-id="dacc2-115">The [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg), [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer), and [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) functions require that applications to allocate data blocks to pass to the device drivers for playback or recording purposes.</span></span> <span data-ttu-id="dacc2-116">Cada uma dessas funções usa uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) para descrever seu bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="dacc2-116">Each of these functions uses a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure to describe its data block.</span></span>

<span data-ttu-id="dacc2-117">Antes de usar uma dessas funções para passar um bloco de dados para um driver de dispositivo, você deve alocar memória para o buffer e a estrutura de cabeçalho que descreve o bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="dacc2-117">Before you use one of these functions to pass a data block to a device driver, you must allocate memory for the buffer and the header structure that describes the data block.</span></span>

<span data-ttu-id="dacc2-118">O Windows fornece as seguintes funções para preparar e limpar os blocos de dados MIDI.</span><span class="sxs-lookup"><span data-stu-id="dacc2-118">Windows provides the following functions for preparing and cleaning up MIDI data blocks.</span></span>



| <span data-ttu-id="dacc2-119">Valor</span><span class="sxs-lookup"><span data-stu-id="dacc2-119">Value</span></span>                                                    | <span data-ttu-id="dacc2-120">Significado</span><span class="sxs-lookup"><span data-stu-id="dacc2-120">Meaning</span></span>                                                |
|----------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="dacc2-121">**midiInPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="dacc2-121">**midiInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)       | <span data-ttu-id="dacc2-122">Prepara um bloco de dados de entrada MIDI.</span><span class="sxs-lookup"><span data-stu-id="dacc2-122">Prepares a MIDI input data block.</span></span>                      |
| [<span data-ttu-id="dacc2-123">**midiInUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="dacc2-123">**midiInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)   | <span data-ttu-id="dacc2-124">Limpa a preparação de um bloco de dados de entrada MIDI.</span><span class="sxs-lookup"><span data-stu-id="dacc2-124">Cleans up the preparation of a MIDI input data block.</span></span>  |
| [<span data-ttu-id="dacc2-125">**midiOutPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="dacc2-125">**midiOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)     | <span data-ttu-id="dacc2-126">Prepara um bloco de dados de saída MIDI.</span><span class="sxs-lookup"><span data-stu-id="dacc2-126">Prepares a MIDI output data block.</span></span>                     |
| [<span data-ttu-id="dacc2-127">**midiOutUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="dacc2-127">**midiOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) | <span data-ttu-id="dacc2-128">Limpa a preparação de um bloco de dados de saída de MIDI.</span><span class="sxs-lookup"><span data-stu-id="dacc2-128">Cleans up the preparation of a MIDI output data block.</span></span> |



 

<span data-ttu-id="dacc2-129">Antes de passar um bloco de dados MIDI para um driver de dispositivo, você deve preparar o buffer passando-o para a função [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) ou [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) .</span><span class="sxs-lookup"><span data-stu-id="dacc2-129">Before you pass a MIDI data block to a device driver, you must prepare the buffer by passing it to the [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) or [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) function.</span></span> <span data-ttu-id="dacc2-130">Quando o driver de dispositivo for concluído com o buffer e o retornar, você deverá limpar essa preparação passando o buffer para a função [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) ou [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) antes que qualquer memória alocada possa ser liberada.</span><span class="sxs-lookup"><span data-stu-id="dacc2-130">When the device driver is finished with the buffer and returns it, you must clean up this preparation by passing the buffer to the [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) or [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) function before any allocated memory can be freed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dacc2-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dacc2-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dacc2-132">Serviços MIDI</span><span class="sxs-lookup"><span data-stu-id="dacc2-132">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 