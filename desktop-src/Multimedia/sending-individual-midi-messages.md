---
title: Enviando mensagens individuais de MIDI
description: Enviando mensagens individuais de MIDI
ms.assetid: 9e5b7194-d6d0-40a6-b8c1-ea9442f34bd8
keywords:
- MIDI (interface digital de instrumento musical), enviando mensagens
- MIDI (interface digital de instrumentos musicais), enviando mensagens
- executando arquivos MIDI, enviando mensagens
- enviando mensagens MIDI
- MIDI (interface digital de instrumento musical), mensagens individuais
- MIDI (interface digital de instrumentos musicais), mensagens individuais
- executando arquivos MIDI, mensagens individuais
- mensagens individuais de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5473d1ab7361c26a922683ed7d5021995b0f13ea
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105757505"
---
# <a name="sending-individual-midi-messages"></a><span data-ttu-id="d46ce-111">Enviando mensagens individuais de MIDI</span><span class="sxs-lookup"><span data-stu-id="d46ce-111">Sending Individual MIDI Messages</span></span>

<span data-ttu-id="d46ce-112">Você pode trabalhar com mensagens MIDI individuais usando as funções a seguir.</span><span class="sxs-lookup"><span data-stu-id="d46ce-112">You can work with individual MIDI messages by using the following functions.</span></span>



| <span data-ttu-id="d46ce-113">Valor</span><span class="sxs-lookup"><span data-stu-id="d46ce-113">Value</span></span>                                      | <span data-ttu-id="d46ce-114">Significado</span><span class="sxs-lookup"><span data-stu-id="d46ce-114">Meaning</span></span>                                                                                                                                                                             |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d46ce-115">**midiOutLongMsg**</span><span class="sxs-lookup"><span data-stu-id="d46ce-115">**midiOutLongMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)   | <span data-ttu-id="d46ce-116">Envia um buffer de dados MIDI para o dispositivo de saída MIDI especificado.</span><span class="sxs-lookup"><span data-stu-id="d46ce-116">Sends a buffer of MIDI data to the specified MIDI output device.</span></span> <span data-ttu-id="d46ce-117">Use essa função para enviar mensagens exclusivas do sistema para um dispositivo MIDI.</span><span class="sxs-lookup"><span data-stu-id="d46ce-117">Use this function to send system-exclusive messages to a MIDI device.</span></span>                                              |
| [<span data-ttu-id="d46ce-118">**midiOutReset**</span><span class="sxs-lookup"><span data-stu-id="d46ce-118">**midiOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)       | <span data-ttu-id="d46ce-119">Desativa todas as notas em todos os canais para um dispositivo de saída MIDI especificado.</span><span class="sxs-lookup"><span data-stu-id="d46ce-119">Turns off all notes on all channels for a specified MIDI output device.</span></span> <span data-ttu-id="d46ce-120">Qualquer buffer exclusivo do sistema pendente e buffers de fluxo são marcados como concluídos e retornados para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d46ce-120">Any pending system-exclusive buffers and stream buffers are marked as done and returned to the application.</span></span> |
| [<span data-ttu-id="d46ce-121">**midiOutShortMsg**</span><span class="sxs-lookup"><span data-stu-id="d46ce-121">**midiOutShortMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) | <span data-ttu-id="d46ce-122">Envia uma mensagem MIDI para um dispositivo de saída MIDI especificado.</span><span class="sxs-lookup"><span data-stu-id="d46ce-122">Sends a MIDI message to a specified MIDI output device.</span></span>                                                                                                                             |



 

<span data-ttu-id="d46ce-123">Para enviar qualquer mensagem MIDI (exceto para mensagens exclusivas do sistema), use [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg).</span><span class="sxs-lookup"><span data-stu-id="d46ce-123">To send any MIDI message (except for system-exclusive messages), use [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg).</span></span>

 

 