---
title: Processando dados MIDI de duas fontes MIDI
description: Processando dados MIDI de duas fontes MIDI
ms.assetid: d8b605d9-a12a-4830-8f29-ea700aefb41d
keywords:
- Multimídia do Windows, processamento de dados MIDI de duas fontes
- multimídia, processamento de dados MIDI de duas fontes
- áudio multimídia, processamento de dados MIDI de duas fontes
- áudio, processamento de dados MIDI de duas fontes
- MIDI (interface digital de instrumento musical), processamento de dados de duas fontes
- MIDI (interface digital de instrumentos musicais), processamento de dados de duas fontes
- processando dados MIDI de duas fontes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513dcd16036f6f833aec6813f75c6c082925f666
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007482"
---
# <a name="processing-midi-data-from-two-midi-sources"></a><span data-ttu-id="7c590-110">Processando dados MIDI de duas fontes MIDI</span><span class="sxs-lookup"><span data-stu-id="7c590-110">Processing MIDI Data from Two MIDI Sources</span></span>

<span data-ttu-id="7c590-111">O subsistema MIDI pode rotear mensagens MIDI de duas fontes de dados para um único dispositivo de saída de MIDI para reprodução simultânea.</span><span class="sxs-lookup"><span data-stu-id="7c590-111">The MIDI subsystem can route MIDI messages from two data sources to a single MIDI output device for concurrent playback.</span></span> <span data-ttu-id="7c590-112">Por exemplo, uma fonte pode ser uma música em segundo plano ou uma linha de baixo que tenha sido previamente registrada e armazenada em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="7c590-112">For example, one source can be background music or a bass line that has been pre-recorded and stored in a file.</span></span> <span data-ttu-id="7c590-113">A segunda fonte pode ser dados dinâmicos de um instrumento MIDI, como um teclado ou uma guitarra.</span><span class="sxs-lookup"><span data-stu-id="7c590-113">The second source can be live data from a MIDI instrument, such as a keyboard or guitar.</span></span>

<span data-ttu-id="7c590-114">Ambas as fontes de dados enviam dados MIDI para um único dispositivo MIDI identificado com um identificador.</span><span class="sxs-lookup"><span data-stu-id="7c590-114">Both data sources send MIDI data to a single MIDI device that is identified with one handle.</span></span> <span data-ttu-id="7c590-115">Envie um fluxo de dados usando a função [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) e um ou mais buffers de fluxo.</span><span class="sxs-lookup"><span data-stu-id="7c590-115">Send one data stream by using the [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function and one or more stream buffers.</span></span> <span data-ttu-id="7c590-116">Esse fluxo de dados normalmente contém dados pré-gravados que são empacotados no buffer.</span><span class="sxs-lookup"><span data-stu-id="7c590-116">This data stream typically contains prerecorded data that is packed into the buffer.</span></span>

<span data-ttu-id="7c590-117">Envie o segundo fluxo de dados (normalmente de um instrumento MIDI) de forma assíncrona usando a função [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) .</span><span class="sxs-lookup"><span data-stu-id="7c590-117">Send the second data stream (typically from a MIDI instrument) asynchronously by using the [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) function.</span></span> <span data-ttu-id="7c590-118">O status de execução de um buffer de fluxo não será afetado negativamente pelas chamadas assíncronas feitas pelo segundo fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="7c590-118">The running status of a stream buffer will not be adversely affected by the asynchronous calls made by the second data stream.</span></span>

<span data-ttu-id="7c590-119">Cada mensagem curta enviada com **midiOutShortMsg** deve ser uma mensagem MIDI completa, com um byte de status e o número apropriado de bytes de dados.</span><span class="sxs-lookup"><span data-stu-id="7c590-119">Each short message sent with **midiOutShortMsg** must be a complete MIDI message, with a status byte and the appropriate number of data bytes.</span></span> <span data-ttu-id="7c590-120">Se o byte de status for omitido, **midiOutShortMsg** retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="7c590-120">If the status byte is omitted, **midiOutShortMsg** returns an error.</span></span> <span data-ttu-id="7c590-121">(No entanto, não há nenhum status de execução com saída de fluxo.)</span><span class="sxs-lookup"><span data-stu-id="7c590-121">(However, there is no running status with stream output.)</span></span>

 

 