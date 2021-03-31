---
title: Enviando mensagens MIDI com buffers de fluxo
description: Enviando mensagens MIDI com buffers de fluxo
ms.assetid: f9e77637-098c-4ee8-bca9-a05ecce0c569
keywords:
- MIDI (interface digital de instrumento musical), buffers de fluxo
- MIDI (interface digital de instrumentos musicais), buffers de fluxo
- executando arquivos MIDI, buffers de fluxo
- buffers de fluxo, enviando mensagens de MIDI
- MIDI (interface digital de instrumento musical), enviando mensagens
- MIDI (interface digital de instrumentos musicais), enviando mensagens
- executando arquivos MIDI, enviando mensagens
- enviando mensagens MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dbe2a2854abf9dd1ba67a93954c0823ac387b86
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640614"
---
# <a name="sending-midi-messages-with-stream-buffers"></a><span data-ttu-id="c401f-111">Enviando mensagens MIDI com buffers de fluxo</span><span class="sxs-lookup"><span data-stu-id="c401f-111">Sending MIDI Messages with Stream Buffers</span></span>

<span data-ttu-id="c401f-112">Quando seu aplicativo funciona com buffers de fluxo, ele usa a função [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) para enviar todas as mensagens de Midi (curto e longo) para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c401f-112">When your application works with stream buffers, it uses the [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function to send all (short and long) MIDI messages to the device.</span></span> <span data-ttu-id="c401f-113">Para especificar blocos de dados de fluxo, use as estruturas [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) e [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) .</span><span class="sxs-lookup"><span data-stu-id="c401f-113">To specify stream data blocks, use the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) and [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structures.</span></span> <span data-ttu-id="c401f-114">A estrutura **MIDIHDR** contém um endereço de um bloco de dados bloqueados, o comprimento do bloco de dados e alguns sinalizadores sortidos.</span><span class="sxs-lookup"><span data-stu-id="c401f-114">The **MIDIHDR** structure contains an address of a locked data block, the data-block length, and some assorted flags.</span></span> <span data-ttu-id="c401f-115">Os dados são armazenados na forma de estruturas **MIDIEVENT** .</span><span class="sxs-lookup"><span data-stu-id="c401f-115">The data is stored in the form of **MIDIEVENT** structures.</span></span> <span data-ttu-id="c401f-116">O sistema impõe um limite de tamanho de 64K em buffers de fluxo.</span><span class="sxs-lookup"><span data-stu-id="c401f-116">The system imposes a size limit of 64K on stream buffers.</span></span>

<span data-ttu-id="c401f-117">Depois de usar o **midiStreamOut** para enviar um buffer de fluxo de dados, você deve aguardar até que o driver de dispositivo seja concluído com o bloco de dados antes de liberá-lo.</span><span class="sxs-lookup"><span data-stu-id="c401f-117">After you use **midiStreamOut** to send a stream buffer of data, you must wait until the device driver is finished with the data block before freeing it.</span></span> <span data-ttu-id="c401f-118">Se você estiver enviando vários blocos de dados, deverá monitorar a conclusão de cada bloco de dados para saber quando enviar blocos adicionais.</span><span class="sxs-lookup"><span data-stu-id="c401f-118">If you are sending multiple data blocks, you must monitor the completion of each data block so you know when to send additional blocks.</span></span> <span data-ttu-id="c401f-119">Para obter informações sobre as diferentes técnicas para o monitoramento da conclusão do bloco de dados, consulte [Gerenciando blocos de dados MIDI](managing-midi-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="c401f-119">For information about different techniques for monitoring data-block completion, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

 

 