---
title: Gerenciando a gravação de MIDI
description: Gerenciando a gravação de MIDI
ms.assetid: 48b2d815-72cf-4c96-8d93-247d2426b8f2
keywords:
- MIDI (interface digital de instrumento musical), gravação
- MIDI (interface digital de instrumentos musicais), gravação
- gravando áudio MIDI, gerenciando
- Gravação de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0edfb81976e1f5333798c9705640e7676281968a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104453979"
---
# <a name="managing-midi-recording"></a><span data-ttu-id="6339e-107">Gerenciando a gravação de MIDI</span><span class="sxs-lookup"><span data-stu-id="6339e-107">Managing MIDI Recording</span></span>

<span data-ttu-id="6339e-108">Depois de abrir um dispositivo MIDI, você pode começar a gravar dados MIDI.</span><span class="sxs-lookup"><span data-stu-id="6339e-108">After you open a MIDI device, you can begin recording MIDI data.</span></span> <span data-ttu-id="6339e-109">O Windows fornece as seguintes funções para gerenciar a gravação de MIDI.</span><span class="sxs-lookup"><span data-stu-id="6339e-109">Windows provides the following functions for managing MIDI recording.</span></span>



| <span data-ttu-id="6339e-110">Valor</span><span class="sxs-lookup"><span data-stu-id="6339e-110">Value</span></span>                                      | <span data-ttu-id="6339e-111">Significado</span><span class="sxs-lookup"><span data-stu-id="6339e-111">Meaning</span></span>                                                                                           |
|--------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6339e-112">**midiInAddBuffer**</span><span class="sxs-lookup"><span data-stu-id="6339e-112">**midiInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) | <span data-ttu-id="6339e-113">Envia um buffer para o driver de dispositivo para que ele possa ser preenchido com dados de MIDI exclusivos do sistema gravados.</span><span class="sxs-lookup"><span data-stu-id="6339e-113">Sends a buffer to the device driver so it can be filled with recorded system-exclusive MIDI data.</span></span> |
| [<span data-ttu-id="6339e-114">**midiInReset**</span><span class="sxs-lookup"><span data-stu-id="6339e-114">**midiInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)         | <span data-ttu-id="6339e-115">Interrompe a gravação de MIDI e marca todos os buffers pendentes como concluído.</span><span class="sxs-lookup"><span data-stu-id="6339e-115">Stops MIDI recording and marks all pending buffers as done.</span></span>                                       |
| [<span data-ttu-id="6339e-116">**midiInStart**</span><span class="sxs-lookup"><span data-stu-id="6339e-116">**midiInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)         | <span data-ttu-id="6339e-117">Inicia a gravação de MIDI e redefine o carimbo de data/hora como zero.</span><span class="sxs-lookup"><span data-stu-id="6339e-117">Starts MIDI recording and resets the time stamp to zero.</span></span>                                          |
| [<span data-ttu-id="6339e-118">**midiInStop**</span><span class="sxs-lookup"><span data-stu-id="6339e-118">**midiInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)           | <span data-ttu-id="6339e-119">Interrompe a gravação de MIDI.</span><span class="sxs-lookup"><span data-stu-id="6339e-119">Stops MIDI recording.</span></span>                                                                             |



 

<span data-ttu-id="6339e-120">Para enviar buffers para o driver de dispositivo para gravar mensagens exclusivas do sistema, use [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer).</span><span class="sxs-lookup"><span data-stu-id="6339e-120">To send buffers to the device driver for recording system-exclusive messages, use [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer).</span></span> <span data-ttu-id="6339e-121">O aplicativo é notificado, pois os buffers são preenchidos com dados registrados exclusivos do sistema.</span><span class="sxs-lookup"><span data-stu-id="6339e-121">The application is notified as the buffers are filled with system-exclusive recorded data.</span></span> <span data-ttu-id="6339e-122">Para obter mais informações sobre as técnicas de notificação, consulte [Managing MIDI data Blocks](managing-midi-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="6339e-122">For more information about the notification techniques, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

<span data-ttu-id="6339e-123">A função [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) inicia o processo de gravação.</span><span class="sxs-lookup"><span data-stu-id="6339e-123">The [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function begins the recording process.</span></span> <span data-ttu-id="6339e-124">Ao registrar mensagens exclusivas do sistema, envie pelo menos um buffer para o driver antes de iniciar a gravação.</span><span class="sxs-lookup"><span data-stu-id="6339e-124">When recording system-exclusive messages, send at least one buffer to the driver before starting recording.</span></span> <span data-ttu-id="6339e-125">Para interromper a gravação, use [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop).</span><span class="sxs-lookup"><span data-stu-id="6339e-125">To stop recording, use [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop).</span></span> <span data-ttu-id="6339e-126">Antes de fechar o dispositivo usando a função [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) , marque todos os blocos de dados pendentes como sendo feitos chamando [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset).</span><span class="sxs-lookup"><span data-stu-id="6339e-126">Before closing the device by using the [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) function, mark any pending data blocks as being done by calling [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset).</span></span>

<span data-ttu-id="6339e-127">Os aplicativos que exigem dados com carimbo de data/hora usam uma função de retorno de chamada para receber dados MIDI.</span><span class="sxs-lookup"><span data-stu-id="6339e-127">Applications that require time-stamped data use a callback function to receive MIDI data.</span></span> <span data-ttu-id="6339e-128">Se os requisitos de tempo não forem estritos, você poderá usar uma janela ou um retorno de chamada de thread.</span><span class="sxs-lookup"><span data-stu-id="6339e-128">If your timing requirements are not strict, you can use a window or thread callback.</span></span> <span data-ttu-id="6339e-129">No entanto, você não pode usar um retorno de chamada de evento para receber dados MIDI.</span><span class="sxs-lookup"><span data-stu-id="6339e-129">However, you cannot use an event callback to receive MIDI data.</span></span>

<span data-ttu-id="6339e-130">Para registrar mensagens exclusivas do sistema com aplicativos que não usam buffers de fluxo, você deve fornecer o driver de dispositivo com buffers.</span><span class="sxs-lookup"><span data-stu-id="6339e-130">To record system-exclusive messages with applications that do not use stream buffers, you must supply the device driver with buffers.</span></span> <span data-ttu-id="6339e-131">Esses buffers são especificados usando uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) .</span><span class="sxs-lookup"><span data-stu-id="6339e-131">These buffers are specified by using a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6339e-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6339e-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6339e-133">Gravando áudio MIDI</span><span class="sxs-lookup"><span data-stu-id="6339e-133">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 