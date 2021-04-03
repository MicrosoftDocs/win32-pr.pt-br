---
title: Enviando mensagens de System-Exclusive
description: Enviando mensagens de System-Exclusive
ms.assetid: 2bb95e4e-004e-46c8-9c56-25436fcc7f6c
keywords:
- MIDI (interface digital de instrumento musical), enviando mensagens
- MIDI (interface digital de instrumentos musicais), enviando mensagens
- executando arquivos MIDI, enviando mensagens
- enviando mensagens MIDI
- MIDI (interface digital de instrumento musical), mensagens exclusivas do sistema
- MIDI (interface digital de instrumentos musicais), mensagens exclusivas do sistema
- executando arquivos MIDI, mensagens exclusivas do sistema
- mensagens MIDI exclusivas do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073ebc0fe111ef19e2edb098e6bdb170c13abc3e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823680"
---
# <a name="sending-system-exclusive-messages"></a><span data-ttu-id="55897-111">Enviando mensagens de System-Exclusive</span><span class="sxs-lookup"><span data-stu-id="55897-111">Sending System-Exclusive Messages</span></span>

<span data-ttu-id="55897-112">As mensagens exclusivas do sistema MIDI são as únicas mensagens de MIDI que não se ajustarão a um único valor doubleword.</span><span class="sxs-lookup"><span data-stu-id="55897-112">MIDI system-exclusive messages are the only MIDI messages that will not fit into a single doubleword value.</span></span> <span data-ttu-id="55897-113">As mensagens exclusivas do sistema podem ter qualquer comprimento.</span><span class="sxs-lookup"><span data-stu-id="55897-113">System-exclusive messages can be any length.</span></span> <span data-ttu-id="55897-114">O Windows fornece a função [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) para enviar mensagens exclusivas do sistema para dispositivos de saída de Midi.</span><span class="sxs-lookup"><span data-stu-id="55897-114">Windows provides the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) function for sending system-exclusive messages to MIDI output devices.</span></span> <span data-ttu-id="55897-115">Para especificar os blocos de dados exclusivos do sistema MIDI, use a estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) .</span><span class="sxs-lookup"><span data-stu-id="55897-115">To specify MIDI system-exclusive data blocks, use the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure.</span></span>

<span data-ttu-id="55897-116">Depois de enviar um bloco de dados exclusivo do sistema usando o **midiOutLongMsg**, você deve aguardar até que o driver do dispositivo seja concluído com o bloco de dados antes de liberá-lo.</span><span class="sxs-lookup"><span data-stu-id="55897-116">After you send a system-exclusive data block using **midiOutLongMsg**, you must wait until the device driver is finished with the data block before freeing it.</span></span> <span data-ttu-id="55897-117">Se você estiver enviando vários blocos de dados, deverá monitorar a conclusão de cada bloco de dados para saber quando enviar blocos adicionais.</span><span class="sxs-lookup"><span data-stu-id="55897-117">If you are sending multiple data blocks, you must monitor the completion of each data block so you know when to send additional blocks.</span></span> <span data-ttu-id="55897-118">Para obter informações sobre as diferentes técnicas para o monitoramento da conclusão do bloco de dados, consulte [Gerenciando blocos de dados MIDI](managing-midi-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="55897-118">For information about different techniques for monitoring data-block completion, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

> [!Note]  
> <span data-ttu-id="55897-119">Qualquer byte de status de MIDI diferente de uma mensagem de sistema-em tempo real encerrará uma mensagem exclusiva do sistema.</span><span class="sxs-lookup"><span data-stu-id="55897-119">Any MIDI status byte other than a system-real-time message will terminate a system-exclusive message.</span></span> <span data-ttu-id="55897-120">Se você estiver usando vários blocos de dados para enviar uma única mensagem exclusiva do sistema, não envie mensagens MIDI além das mensagens do sistema em tempo real entre os blocos de dados.</span><span class="sxs-lookup"><span data-stu-id="55897-120">If you are using multiple data blocks to send a single system-exclusive message, do not send any MIDI messages other than system-real-time messages between data blocks.</span></span>

 

 

 