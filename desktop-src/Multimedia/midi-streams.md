---
title: Fluxos de MIDI
description: Fluxos de MIDI
ms.assetid: 622472d9-2888-407f-bdaa-4943896c0bac
keywords:
- MIDI (interface digital de instrumento musical), fluxos
- MIDI (interface digital de instrumentos musicais), fluxos
- buffers de fluxo, fluxos de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4237e1590f3af2e15a3b0b9fedea2fea4c9c40fc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084521"
---
# <a name="midi-streams"></a><span data-ttu-id="4f18f-106">Fluxos de MIDI</span><span class="sxs-lookup"><span data-stu-id="4f18f-106">MIDI Streams</span></span>

<span data-ttu-id="4f18f-107">Os eventos MIDI ocorrem no contexto de um fluxo de dados MIDI.</span><span class="sxs-lookup"><span data-stu-id="4f18f-107">MIDI events occur in the context of a stream of MIDI data.</span></span> <span data-ttu-id="4f18f-108">Embora um aplicativo possa usar vários fluxos para definir dados musicais, o mapeador de MIDI não reconhece vários fluxos.</span><span class="sxs-lookup"><span data-stu-id="4f18f-108">Although an application can use several streams to define musical data, the MIDI mapper does not recognize multiple streams.</span></span> <span data-ttu-id="4f18f-109">A maioria dos aplicativos que usam fluxos usa um fluxo de MIDI único.</span><span class="sxs-lookup"><span data-stu-id="4f18f-109">Most applications that use streams use a single MIDI stream.</span></span>

<span data-ttu-id="4f18f-110">As funções a seguir funcionam com fluxos.</span><span class="sxs-lookup"><span data-stu-id="4f18f-110">The following functions work with streams.</span></span>



| <span data-ttu-id="4f18f-111">Valor</span><span class="sxs-lookup"><span data-stu-id="4f18f-111">Value</span></span>                                            | <span data-ttu-id="4f18f-112">Significado</span><span class="sxs-lookup"><span data-stu-id="4f18f-112">Meaning</span></span>                                                                 |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="4f18f-113">**midiStreamClose**</span><span class="sxs-lookup"><span data-stu-id="4f18f-113">**midiStreamClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)       | <span data-ttu-id="4f18f-114">Fecha um fluxo de MIDI.</span><span class="sxs-lookup"><span data-stu-id="4f18f-114">Closes a MIDI stream.</span></span>                                                   |
| [<span data-ttu-id="4f18f-115">**midiStreamOpen**</span><span class="sxs-lookup"><span data-stu-id="4f18f-115">**midiStreamOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)         | <span data-ttu-id="4f18f-116">Abre um fluxo de MIDI e recupera um identificador.</span><span class="sxs-lookup"><span data-stu-id="4f18f-116">Opens a MIDI stream and retrieves a handle.</span></span>                             |
| [<span data-ttu-id="4f18f-117">**midiStreamOut**</span><span class="sxs-lookup"><span data-stu-id="4f18f-117">**midiStreamOut**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)           | <span data-ttu-id="4f18f-118">Reproduz ou enfileira um fluxo (buffer) de dados MIDI para um dispositivo de saída MIDI.</span><span class="sxs-lookup"><span data-stu-id="4f18f-118">Plays or queues a stream (buffer) of MIDI data to a MIDI output device.</span></span> |
| [<span data-ttu-id="4f18f-119">**midiStreamPause**</span><span class="sxs-lookup"><span data-stu-id="4f18f-119">**midiStreamPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)       | <span data-ttu-id="4f18f-120">Pausa a reprodução de um fluxo MIDI especificado.</span><span class="sxs-lookup"><span data-stu-id="4f18f-120">Pauses playback of a specified MIDI stream.</span></span>                             |
| [<span data-ttu-id="4f18f-121">**midiStreamPosition**</span><span class="sxs-lookup"><span data-stu-id="4f18f-121">**midiStreamPosition**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) | <span data-ttu-id="4f18f-122">Recupera a posição atual em um fluxo de MIDI.</span><span class="sxs-lookup"><span data-stu-id="4f18f-122">Retrieves the current position in a MIDI stream.</span></span>                        |
| [<span data-ttu-id="4f18f-123">**midiStreamProperty**</span><span class="sxs-lookup"><span data-stu-id="4f18f-123">**midiStreamProperty**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty) | <span data-ttu-id="4f18f-124">Define e recupera propriedades de fluxo.</span><span class="sxs-lookup"><span data-stu-id="4f18f-124">Sets and retrieves stream properties.</span></span>                                   |
| [<span data-ttu-id="4f18f-125">**midiStreamRestart**</span><span class="sxs-lookup"><span data-stu-id="4f18f-125">**midiStreamRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)   | <span data-ttu-id="4f18f-126">Reinicia a reprodução de um fluxo de MIDI em pausa.</span><span class="sxs-lookup"><span data-stu-id="4f18f-126">Restarts playback of a paused MIDI stream.</span></span>                              |
| [<span data-ttu-id="4f18f-127">**midiStreamStop**</span><span class="sxs-lookup"><span data-stu-id="4f18f-127">**midiStreamStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)         | <span data-ttu-id="4f18f-128">Desativa todas as notas em todos os canais MIDI para o fluxo MIDI especificado.</span><span class="sxs-lookup"><span data-stu-id="4f18f-128">Turns off all notes on all MIDI channels for the specified MIDI stream.</span></span> |



 

 

 