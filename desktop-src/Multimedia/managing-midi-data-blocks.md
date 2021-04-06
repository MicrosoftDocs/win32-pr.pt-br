---
title: Gerenciando blocos de dados MIDI
description: Gerenciando blocos de dados MIDI
ms.assetid: f29fbc08-ef67-489c-aedf-5a2bc65233f7
keywords:
- MIDI (interface digital de instrumento musical), gerenciando blocos de dados
- MIDI (interface digital de instrumentos musicais), gerenciando blocos de dados
- Serviços de MIDI, gerenciando blocos de dados
- Gerenciando blocos de dados MIDI
- MIDI (interface digital de instrumento musical), mensagens do driver de processamento
- MIDI (interface digital de instrumentos musicais), processamento de mensagens do driver
- Serviços de MIDI, processando mensagens de driver
- Processando mensagens do driver
- MIDI (interface digital de instrumento musical), blocos de dados
- MIDI (interface digital de instrumentos musicais), blocos de dados
- Serviços de MIDI, blocos de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af348d6c53d2944bf22c026674704baa1fe74e07
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917197"
---
# <a name="managing-midi-data-blocks"></a><span data-ttu-id="59da2-114">Gerenciando blocos de dados MIDI</span><span class="sxs-lookup"><span data-stu-id="59da2-114">Managing MIDI Data Blocks</span></span>

<span data-ttu-id="59da2-115">Aplicativos que usam blocos de dados para passar mensagens exclusivas do sistema (usando as funções [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) e [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) ) e buffers de fluxo (usando a função [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) ) devem fornecer continuamente o driver de dispositivo com blocos de dados até que a reprodução ou gravação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="59da2-115">Applications that use data blocks for passing system-exclusive messages (using the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) and [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) functions) and stream buffers (using the [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function) must continually supply the device driver with data blocks until playback or recording is complete.</span></span>

<span data-ttu-id="59da2-116">Mesmo que um único bloco de dados seja usado, um aplicativo deve ser capaz de determinar quando um driver de dispositivo é concluído com o bloco de dados para que ele possa liberar a memória associada ao bloco de dados e à estrutura de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="59da2-116">Even if a single data block is used, an application must be able to determine when a device driver is finished with the data block so it can free the memory associated with the data block and header structure.</span></span> <span data-ttu-id="59da2-117">Três métodos podem ser usados para determinar quando um driver de dispositivo é concluído com um bloco de dados:</span><span class="sxs-lookup"><span data-stu-id="59da2-117">Three methods can be used to determine when a device driver is finished with a data block:</span></span>

-   <span data-ttu-id="59da2-118">Especifique uma função de retorno de chamada para receber uma mensagem enviada pelo driver quando ela for concluída com um bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="59da2-118">Specify a callback function to receive a message sent by the driver when it is finished with a data block.</span></span> <span data-ttu-id="59da2-119">Para obter dados de entrada MIDI com carimbo de data/hora, você deve usar uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="59da2-119">To get time-stamped MIDI input data, you must use a callback function.</span></span>
-   <span data-ttu-id="59da2-120">Use um retorno de chamada de evento (somente para saída).</span><span class="sxs-lookup"><span data-stu-id="59da2-120">Use an event callback (for output only).</span></span>
-   <span data-ttu-id="59da2-121">Use uma janela ou um retorno de chamada de thread para receber uma mensagem enviada pelo driver quando ele for concluído com um bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="59da2-121">Use a window or thread callback to receive a message sent by the driver when it is finished with a data block.</span></span>

<span data-ttu-id="59da2-122">Se um aplicativo não obtiver um bloco de dados para o driver de dispositivo quando for necessário, uma lacuna audível na reprodução ou uma perda de informações registradas de entrada poderá ocorrer.</span><span class="sxs-lookup"><span data-stu-id="59da2-122">If an application does not get a data block to the device driver when it is needed, an audible gap in playback or a loss of incoming recorded information can occur.</span></span> <span data-ttu-id="59da2-123">No mínimo, um aplicativo deve usar um esquema de buffer duplo para manter pelo menos um bloco de dados à frente do driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="59da2-123">At a minimum, an application should use a double-buffering scheme to stay at least one data block ahead of the device driver.</span></span>

## <a name="using-a-callback-function-to-process-driver-messages"></a><span data-ttu-id="59da2-124">Usando uma função de retorno de chamada para processar mensagens de driver</span><span class="sxs-lookup"><span data-stu-id="59da2-124">Using a Callback Function to Process Driver Messages</span></span>

<span data-ttu-id="59da2-125">Você pode escrever sua própria função de retorno de chamada para processar mensagens enviadas pelo driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="59da2-125">You can write your own callback function to process messages sent by the device driver.</span></span> <span data-ttu-id="59da2-126">Para usar uma função de retorno de chamada, especifique o sinalizador da função de retorno de chamada \_ no parâmetro *dwFlags* e o endereço da função de retorno de chamada no parâmetro *dwCallback* da função [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) ou [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="59da2-126">To use a callback function, specify the CALLBACK\_FUNCTION flag in the *dwFlags* parameter and the address of the callback function in the *dwCallback* parameter of the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) or [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>

<span data-ttu-id="59da2-127">As mensagens enviadas a uma função de retorno de chamada são semelhantes às mensagens enviadas a uma janela, exceto que têm dois parâmetros doubleword em vez de um parâmetro inteiro não assinado e um parâmetro doubleword.</span><span class="sxs-lookup"><span data-stu-id="59da2-127">Messages sent to a callback function are similar to messages sent to a window, except they have two doubleword parameters instead of an unsigned integer parameter and a doubleword parameter.</span></span> <span data-ttu-id="59da2-128">Para obter mais informações sobre essas mensagens, consulte [enviando mensagens System-Exclusive](sending-system-exclusive-messages.md) e [Gerenciando a gravação de Midi](managing-midi-recording.md).</span><span class="sxs-lookup"><span data-stu-id="59da2-128">For more information about these messages, see [Sending System-Exclusive Messages](sending-system-exclusive-messages.md) and [Managing MIDI Recording](managing-midi-recording.md).</span></span>

<span data-ttu-id="59da2-129">Use uma das técnicas a seguir para passar dados de instância de um aplicativo para uma função de retorno de chamada:</span><span class="sxs-lookup"><span data-stu-id="59da2-129">Use one of the following techniques to pass instance data from an application to a callback function:</span></span>

-   <span data-ttu-id="59da2-130">Use o parâmetro *dwCallBackInstance* da função que abre o driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="59da2-130">Use the *dwCallbackInstance* parameter of the function that opens the device driver.</span></span>
-   <span data-ttu-id="59da2-131">Use o membro **dwUser** da estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica um bloco de dados que está sendo enviado a um driver de dispositivo MIDI.</span><span class="sxs-lookup"><span data-stu-id="59da2-131">Use the **dwUser** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure that identifies a data block being sent to a MIDI device driver.</span></span>

<span data-ttu-id="59da2-132">Se você precisar de mais de 32 bits de dados de instância, passe um endereço de uma estrutura que contém as informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="59da2-132">If you need more than 32 bits of instance data, pass an address of a structure containing the additional information.</span></span>

## <a name="using-an-event-callback-to-process-driver-messages"></a><span data-ttu-id="59da2-133">Usando um retorno de chamada de evento para processar mensagens de driver</span><span class="sxs-lookup"><span data-stu-id="59da2-133">Using an Event Callback to Process Driver Messages</span></span>

<span data-ttu-id="59da2-134">Para usar um retorno de chamada de evento, use a função [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) para recuperar o identificador de um evento e especifique o evento de retorno \_ de chamada na chamadas para a função [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="59da2-134">To use an event callback, use the [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to retrieve the handle of an event and specify CALLBACK\_EVENT in the call to the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>

<span data-ttu-id="59da2-135">Um retorno de chamada de evento é definido por qualquer coisa que possa causar um retorno de chamada de função.</span><span class="sxs-lookup"><span data-stu-id="59da2-135">An event callback is set by anything that might cause a function callback.</span></span> <span data-ttu-id="59da2-136">Ao contrário das funções de retorno de chamada e de retornos de chamada de janela ou thread, os retornos de chamada de evento não recebem notificações específicas de fechamento, conclusão ou abertura.</span><span class="sxs-lookup"><span data-stu-id="59da2-136">Unlike callback functions and window or thread callbacks, event callbacks do not receive specific close, done, or open notifications.</span></span> <span data-ttu-id="59da2-137">Portanto, um aplicativo pode precisar verificar o status do processo que está aguardando depois que o evento ocorrer.</span><span class="sxs-lookup"><span data-stu-id="59da2-137">Therefore, an application may have to check the status of the process it is waiting for after the event occurs.</span></span>

<span data-ttu-id="59da2-138">Para obter mais informações sobre retornos de chamada de evento, consulte [usando um retorno de chamada de evento para gerenciar a reprodução em buffer](using-an-callback-to-manage-buffered-playback.md).</span><span class="sxs-lookup"><span data-stu-id="59da2-138">For more information about event callbacks, see [Using an Event Callback to Manage Buffered Playback](using-an-callback-to-manage-buffered-playback.md).</span></span>

## <a name="using-a-window-or-thread-callback-to-process-driver-messages"></a><span data-ttu-id="59da2-139">Usando uma janela ou um retorno de chamada de thread para processar mensagens de driver</span><span class="sxs-lookup"><span data-stu-id="59da2-139">Using a Window or Thread Callback to Process Driver Messages</span></span>

<span data-ttu-id="59da2-140">Para usar um retorno de chamada de janela, especifique o sinalizador de janela de retorno de chamada \_ no parâmetro *dwFlags* e um identificador de janela na palavra de ordem inferior do parâmetro *dwCallback* da função [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) ou [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="59da2-140">To use a window callback, specify the CALLBACK\_WINDOW flag in the *dwFlags* parameter and a window handle in the low-order word of the *dwCallback* parameter of the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) or [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span> <span data-ttu-id="59da2-141">As mensagens de driver serão enviadas para a função de procedimento de janela para a janela identificada pelo identificador em *dwCallback*.</span><span class="sxs-lookup"><span data-stu-id="59da2-141">Driver messages will be sent to the window procedure function for the window identified by the handle in *dwCallback*.</span></span>

<span data-ttu-id="59da2-142">Da mesma forma, para usar um retorno de chamada de thread, especifique o sinalizador de thread de retorno de chamada \_ e um identificador de thread na chamada para **MidiInOpen** ou **midiOutOpen**.</span><span class="sxs-lookup"><span data-stu-id="59da2-142">Similarly, to use a thread callback, specify the CALLBACK\_THREAD flag and a thread identifier in the call to **midiInOpen** or **midiOutOpen**.</span></span> <span data-ttu-id="59da2-143">Nesse caso, as mensagens serão postadas no thread especificado em vez de em uma janela.</span><span class="sxs-lookup"><span data-stu-id="59da2-143">In this case, messages will be posted to the specified thread instead of to a window.</span></span>

<span data-ttu-id="59da2-144">As mensagens enviadas para uma janela ou retorno de chamada de thread são específicas para o dispositivo MIDI usado.</span><span class="sxs-lookup"><span data-stu-id="59da2-144">Messages sent to a window or thread callback are specific to the MIDI device used.</span></span> <span data-ttu-id="59da2-145">Para obter mais informações sobre essas mensagens, consulte [enviando mensagens System-Exclusive](sending-system-exclusive-messages.md) e [Gerenciando a gravação de Midi](managing-midi-recording.md).</span><span class="sxs-lookup"><span data-stu-id="59da2-145">For more information about these messages, see [Sending System-Exclusive Messages](sending-system-exclusive-messages.md) and [Managing MIDI Recording](managing-midi-recording.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="59da2-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="59da2-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59da2-147">Serviços MIDI</span><span class="sxs-lookup"><span data-stu-id="59da2-147">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 