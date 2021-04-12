---
title: Formato de buffer de fluxo
description: Formato de buffer de fluxo
ms.assetid: 4b24c12e-b43f-492e-a000-af4f59d5e16f
keywords:
- MIDI (interface digital de instrumento musical), buffers de fluxo
- MIDI (interface digital de instrumentos musicais), buffers de fluxo
- buffers de fluxo, formato
- Estrutura MIDIHDR
- Estrutura MIDIEVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801a7f0dbeabd0d7aebeae0387af415a831e4658
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365843"
---
# <a name="stream-buffer-format"></a><span data-ttu-id="e822a-108">Formato de buffer de fluxo</span><span class="sxs-lookup"><span data-stu-id="e822a-108">Stream Buffer Format</span></span>

<span data-ttu-id="e822a-109">O membro **lpData** da estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) aponta para um buffer de fluxo e o membro **dwBufferLength** especifica o tamanho real desse buffer.</span><span class="sxs-lookup"><span data-stu-id="e822a-109">The **lpData** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure points to a stream buffer, and the **dwBufferLength** member specifies the actual size of this buffer.</span></span> <span data-ttu-id="e822a-110">O membro **dwBytesRecorded** de **MIDIHDR** especifica o número de bytes no buffer que são realmente usados pelos eventos de Midi; Esse valor deve ser menor ou igual ao valor especificado por **dwBufferLength**.</span><span class="sxs-lookup"><span data-stu-id="e822a-110">The **dwBytesRecorded** member of **MIDIHDR** specifies the number of bytes in the buffer that are actually used by the MIDI events; this value must be less than or equal to the value specified by **dwBufferLength**.</span></span>

<span data-ttu-id="e822a-111">Cada um dos eventos de MIDI no buffer de fluxo é especificado por uma estrutura [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) , que contém a hora do evento, um identificador de fluxo, um código de evento e, quando apropriado, os parâmetros para o evento.</span><span class="sxs-lookup"><span data-stu-id="e822a-111">Each of the MIDI events in the stream buffer is specified by a [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure, which contains the time for the event, a stream identifier, an event code, and, when appropriate, parameters for the event.</span></span> <span data-ttu-id="e822a-112">Cada uma dessas estruturas **MIDIEVENT** deve começar em um limite de doubleword.</span><span class="sxs-lookup"><span data-stu-id="e822a-112">Each of these **MIDIEVENT** structures must begin on a doubleword boundary.</span></span> <span data-ttu-id="e822a-113">Se necessário, os bytes de preenchimento devem ser adicionados ao final da estrutura para garantir que o próximo seja iniciado em um limite de doubleword.</span><span class="sxs-lookup"><span data-stu-id="e822a-113">If necessary, pad bytes must be added to the end of the structure to ensure that the next one starts on a doubleword boundary.</span></span>

 

 