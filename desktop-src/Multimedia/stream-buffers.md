---
title: Buffers de fluxo
description: Buffers de fluxo
ms.assetid: d73209a3-4b9d-4405-9e62-8ecfb94c0bd5
keywords:
- Multimídia do Windows, buffers de fluxo
- multimídia, buffers de fluxo
- áudio de multimídia, buffers de fluxo
- áudio, buffers de fluxo
- MIDI (interface digital de instrumento musical), buffers de fluxo
- MIDI (interface digital de instrumentos musicais), buffers de fluxo
- buffers de fluxo, sobre
- Estrutura MIDIHDR
- Estrutura MIDIEVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a01862a8a8e6b7846cbe445737bd13422cf0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640612"
---
# <a name="stream-buffers"></a><span data-ttu-id="0fac6-112">Buffers de fluxo</span><span class="sxs-lookup"><span data-stu-id="0fac6-112">Stream Buffers</span></span>

<span data-ttu-id="0fac6-113">Os aplicativos podem usar buffers de fluxo para enviar fluxos de eventos MIDI para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0fac6-113">Applications can use stream buffers to send streams of MIDI events to a device.</span></span> <span data-ttu-id="0fac6-114">Cada buffer de fluxo é um bloco de memória apontado por uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) .</span><span class="sxs-lookup"><span data-stu-id="0fac6-114">Each stream buffer is a block of memory pointed to by a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure.</span></span> <span data-ttu-id="0fac6-115">Esse bloco de memória contém dados para um ou mais eventos de MIDI, cada um deles definido por uma estrutura [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) .</span><span class="sxs-lookup"><span data-stu-id="0fac6-115">This block of memory contains data for one or more MIDI events, each of which is defined by a [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure.</span></span> <span data-ttu-id="0fac6-116">Um aplicativo controla o buffer chamando as funções de manipulação de fluxo, como [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen), [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)e [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose).</span><span class="sxs-lookup"><span data-stu-id="0fac6-116">An application controls the buffer by calling the stream-manipulation functions, such as [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen), [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout), and [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose).</span></span>

-   [<span data-ttu-id="0fac6-117">Formato de buffer de fluxo</span><span class="sxs-lookup"><span data-stu-id="0fac6-117">Stream Buffer Format</span></span>](stream-buffer-format.md)
-   [<span data-ttu-id="0fac6-118">Informações de tempo</span><span class="sxs-lookup"><span data-stu-id="0fac6-118">Timing Information</span></span>](timing-information.md)
-   [<span data-ttu-id="0fac6-119">Tipos de evento MIDI</span><span class="sxs-lookup"><span data-stu-id="0fac6-119">MIDI Event Types</span></span>](midi-event-types.md)
-   [<span data-ttu-id="0fac6-120">Fluxos de MIDI</span><span class="sxs-lookup"><span data-stu-id="0fac6-120">MIDI Streams</span></span>](midi-streams.md)

 

 