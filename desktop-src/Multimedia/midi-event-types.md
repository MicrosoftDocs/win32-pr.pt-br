---
title: Tipos de evento MIDI
description: Tipos de evento MIDI
ms.assetid: 0b0984b7-3087-461e-90f2-a899dc1a88c6
keywords:
- MIDI (interface digital de instrumento musical), tipos de evento
- MIDI (interface digital de instrumentos musicais), tipos de evento
- Estrutura MIDIEVENT
- buffers de fluxo, tipos de evento MIDI
- Tipos de evento MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 823ce5ce7af898ca3178e0379fb814c54fbf06b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007527"
---
# <a name="midi-event-types"></a><span data-ttu-id="6eb81-108">Tipos de evento MIDI</span><span class="sxs-lookup"><span data-stu-id="6eb81-108">MIDI Event Types</span></span>

<span data-ttu-id="6eb81-109">O membro **dwEvent** da estrutura [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) descreve o evento MIDI que deve ocorrer.</span><span class="sxs-lookup"><span data-stu-id="6eb81-109">The **dwEvent** member of the [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure describes the MIDI event that is to take place.</span></span> <span data-ttu-id="6eb81-110">Eventos curtos se encaixam totalmente nesse membro.</span><span class="sxs-lookup"><span data-stu-id="6eb81-110">Short events fit entirely into this member.</span></span> <span data-ttu-id="6eb81-111">Eventos longos exigem um ou mais valores doubleword além do membro **dwEvent** para armazenar as descrições de eventos.</span><span class="sxs-lookup"><span data-stu-id="6eb81-111">Long events require one or more doubleword values in addition to the **dwEvent** member to store the event descriptions.</span></span>

<span data-ttu-id="6eb81-112">O byte alto do membro **dwEvent** contém informações sobre se o evento é longo ou curto e se um retorno de chamada é gerado junto com o evento.</span><span class="sxs-lookup"><span data-stu-id="6eb81-112">The high byte of the **dwEvent** member contains information about whether the event is long or short and about whether a callback is generated along with the event.</span></span> <span data-ttu-id="6eb81-113">Além disso, esse byte é usado para descrever o tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="6eb81-113">In addition, this byte is used to describe the event type.</span></span> <span data-ttu-id="6eb81-114">Os 24 bits restantes do membro **dwEvent** são usados para conter os parâmetros de evento (para mensagens curtas) ou para conter o comprimento dos parâmetros de evento (para mensagens longas).</span><span class="sxs-lookup"><span data-stu-id="6eb81-114">The remaining 24 bits of the **dwEvent** member are used either to contain the event parameters (for short messages) or to contain the length of the event parameters (for long messages).</span></span> <span data-ttu-id="6eb81-115">Para extrair informações do membro **dwEvent** , use as macros [**\_ EVENTTYPE MEVT**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype) e [**MEVT \_ EVENTPARM**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm) .</span><span class="sxs-lookup"><span data-stu-id="6eb81-115">To extract information from the **dwEvent** member, use the [**MEVT\_EVENTTYPE**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype) and [**MEVT\_EVENTPARM**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm) macros.</span></span>

<span data-ttu-id="6eb81-116">Para obter uma descrição dos tipos de evento predefinidos, consulte o material de referência para a estrutura **MIDIEVENT** .</span><span class="sxs-lookup"><span data-stu-id="6eb81-116">For a description of the predefined event types, see the reference material for the **MIDIEVENT** structure.</span></span>

 

 