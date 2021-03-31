---
title: Usando uma função de retorno de chamada para gerenciar a reprodução em buffer
description: Usando uma função de retorno de chamada para gerenciar a reprodução em buffer
ms.assetid: aaaf9c5f-c9b2-4e55-a4c1-28c99cc03945
keywords:
- MIDI (interface digital de instrumento musical), reprodução em buffer
- MIDI (interface digital de instrumentos musicais), reprodução em buffer
- executando arquivos MIDI, reprodução em buffer
- reprodução em buffer
- MOM_CLOSE mensagem
- MOM_DONE mensagem
- MOM_OPEN mensagem
- MIDI (interface digital de instrumento musical), enviando mensagens
- MIDI (interface digital de instrumentos musicais), enviando mensagens
- executando arquivos MIDI, enviando mensagens
- enviando mensagens MIDI
- MIDI (interface digital de instrumento musical), funções de retorno de chamada
- MIDI (interface digital de instrumentos musicais), funções de retorno de chamada
- executando arquivos MIDI, funções de retorno de chamada
- Função de retorno de chamada MidiOutProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bccccd8e5fb052b89e8ca1804b89de6da26cd5b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640848"
---
# <a name="using-a-callback-function-to-manage-buffered-playback"></a><span data-ttu-id="1f5ed-118">Usando uma função de retorno de chamada para gerenciar a reprodução em buffer</span><span class="sxs-lookup"><span data-stu-id="1f5ed-118">Using a Callback Function to Manage Buffered Playback</span></span>

<span data-ttu-id="1f5ed-119">Você pode definir sua própria função de retorno de chamada para gerenciar a reprodução em buffer de dispositivos de saída de MIDI.</span><span class="sxs-lookup"><span data-stu-id="1f5ed-119">You can define your own callback function to manage buffered playback of MIDI output devices.</span></span> <span data-ttu-id="1f5ed-120">A função de retorno de chamada está documentada como [**MidiOutProc**](/previous-versions//dd798478(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1f5ed-120">The callback function is documented as [**MidiOutProc**](/previous-versions//dd798478(v=vs.85)).</span></span>

<span data-ttu-id="1f5ed-121">As mensagens a seguir podem ser enviadas para o parâmetro *wMsg* da função de retorno de chamada **MidiOutProc** .</span><span class="sxs-lookup"><span data-stu-id="1f5ed-121">The following messages can be sent to the *wMsg* parameter of the **MidiOutProc** callback function.</span></span>



| <span data-ttu-id="1f5ed-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1f5ed-122">Value</span></span>                           | <span data-ttu-id="1f5ed-123">Significado</span><span class="sxs-lookup"><span data-stu-id="1f5ed-123">Meaning</span></span>                                                                                                                                                                  |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f5ed-124">**fechamento do MOM \_**</span><span class="sxs-lookup"><span data-stu-id="1f5ed-124">**MOM\_CLOSE**</span></span>](mom-close.md) | <span data-ttu-id="1f5ed-125">Enviado quando o dispositivo é fechado usando a função [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) .</span><span class="sxs-lookup"><span data-stu-id="1f5ed-125">Sent when the device is closed by using the [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) function.</span></span>                                                                               |
| [<span data-ttu-id="1f5ed-126">**MOM \_ concluído**</span><span class="sxs-lookup"><span data-stu-id="1f5ed-126">**MOM\_DONE**</span></span>](mom-done.md)   | <span data-ttu-id="1f5ed-127">Enviado quando o driver de dispositivo é concluído com um bloco de dados enviado usando a função [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) ou [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) .</span><span class="sxs-lookup"><span data-stu-id="1f5ed-127">Sent when the device driver is finished with a data block sent by using the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) or [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function.</span></span> |
| [<span data-ttu-id="1f5ed-128">**MOM \_ aberto**</span><span class="sxs-lookup"><span data-stu-id="1f5ed-128">**MOM\_OPEN**</span></span>](mom-open.md)   | <span data-ttu-id="1f5ed-129">Enviado quando o dispositivo é aberto usando a função [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="1f5ed-129">Sent when the device is opened by using the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>                                                                                 |



 

<span data-ttu-id="1f5ed-130">Essas mensagens são semelhantes àquelas enviadas para funções de procedimento de janela, mas os parâmetros são diferentes.</span><span class="sxs-lookup"><span data-stu-id="1f5ed-130">These messages are similar to those sent to window procedure functions, but the parameters are different.</span></span> <span data-ttu-id="1f5ed-131">Um identificador do dispositivo MIDI aberto é passado como um parâmetro para a função de retorno de chamada, junto com o doubleword dos dados da instância passados usando **midiOutOpen**.</span><span class="sxs-lookup"><span data-stu-id="1f5ed-131">A handle of the open MIDI device is passed as a parameter to the callback function, along with the doubleword of instance data passed by using **midiOutOpen**.</span></span>

<span data-ttu-id="1f5ed-132">Depois que o driver for concluído com um bloco de dados, você poderá limpar e liberar o bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="1f5ed-132">After the driver is finished with a data block, you can clean up and free the data block.</span></span> <span data-ttu-id="1f5ed-133">Devido às restrições sugeridas nas funções de retorno de chamada, é melhor não fazer isso de dentro da função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="1f5ed-133">Because of the suggested restrictions on callback functions, it is better not to do this from within the callback function.</span></span>

 

 