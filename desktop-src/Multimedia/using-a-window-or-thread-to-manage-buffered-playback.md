---
title: Usando uma janela ou thread para gerenciar a reprodução em buffer
description: Usando uma janela ou thread para gerenciar a reprodução em buffer
ms.assetid: 3c8145a8-e56a-449d-ad45-2ae016f79697
keywords:
- MIDI (interface digital de instrumento musical), reprodução em buffer
- MIDI (interface digital de instrumentos musicais), reprodução em buffer
- executando arquivos MIDI, reprodução em buffer
- reprodução em buffer
- MM_MOM_CLOSE mensagem
- MM_MOM_DONE mensagem
- MM_MOM_OPEN mensagem
- MIDI (interface digital de instrumento musical), enviando mensagens
- MIDI (interface digital de instrumentos musicais), enviando mensagens
- executando arquivos MIDI, enviando mensagens
- enviando mensagens MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c8c120504a4a25ddcf01474db341a367a2e9854
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294019"
---
# <a name="using-a-window-or-thread-to-manage-buffered-playback"></a><span data-ttu-id="5c92e-114">Usando uma janela ou thread para gerenciar a reprodução em buffer</span><span class="sxs-lookup"><span data-stu-id="5c92e-114">Using a Window or Thread to Manage Buffered Playback</span></span>

<span data-ttu-id="5c92e-115">As mensagens a seguir podem ser enviadas para uma janela ou thread para gerenciar a reprodução de mensagens exclusivas do sistema MIDI ou buffers de fluxo.</span><span class="sxs-lookup"><span data-stu-id="5c92e-115">The following messages can be sent to a window or thread for managing playback of MIDI system-exclusive messages or stream buffers.</span></span>



| <span data-ttu-id="5c92e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5c92e-116">Value</span></span>                                  | <span data-ttu-id="5c92e-117">Significado</span><span class="sxs-lookup"><span data-stu-id="5c92e-117">Meaning</span></span>                                                                                                                                                                  |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c92e-118">**\_fechamento do MOM mm \_**</span><span class="sxs-lookup"><span data-stu-id="5c92e-118">**MM\_MOM\_CLOSE**</span></span>](mm-mom-close.md) | <span data-ttu-id="5c92e-119">Enviado quando o dispositivo é fechado usando a função [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) .</span><span class="sxs-lookup"><span data-stu-id="5c92e-119">Sent when the device is closed by using the [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) function.</span></span>                                                                               |
| [<span data-ttu-id="5c92e-120">**\_Mom mm \_ concluído**</span><span class="sxs-lookup"><span data-stu-id="5c92e-120">**MM\_MOM\_DONE**</span></span>](mm-mom-done.md)   | <span data-ttu-id="5c92e-121">Enviado quando o driver de dispositivo é concluído com um bloco de dados enviado usando a função [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) ou [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) .</span><span class="sxs-lookup"><span data-stu-id="5c92e-121">Sent when the device driver is finished with a data block sent by using the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) or [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function.</span></span> |
| [<span data-ttu-id="5c92e-122">**\_Mom mm \_ aberto**</span><span class="sxs-lookup"><span data-stu-id="5c92e-122">**MM\_MOM\_OPEN**</span></span>](mm-mom-open.md)   | <span data-ttu-id="5c92e-123">Enviado quando o dispositivo é aberto usando a função [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="5c92e-123">Sent when the device is opened by using the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>                                                                                 |



 

<span data-ttu-id="5c92e-124">Um parâmetro *wParam* e um parâmetro *lParam* são associados a cada uma dessas mensagens.</span><span class="sxs-lookup"><span data-stu-id="5c92e-124">A *wParam* parameter and an *lParam* parameter are associated with each of these messages.</span></span> <span data-ttu-id="5c92e-125">O parâmetro *wParam* sempre especifica o identificador de um dispositivo MIDI aberto.</span><span class="sxs-lookup"><span data-stu-id="5c92e-125">The *wParam* parameter always specifies the handle of an open MIDI device.</span></span> <span data-ttu-id="5c92e-126">Para [**o \_ Mom mm \_ concluído**](mm-mom-done.md), *lParam* especifica um endereço de uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) identificando o bloco de dados concluído.</span><span class="sxs-lookup"><span data-stu-id="5c92e-126">For [**MM\_MOM\_DONE**](mm-mom-done.md), *lParam* specifies an address of a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the completed data block.</span></span> <span data-ttu-id="5c92e-127">O parâmetro *lParam* não é usado para Mom [**mm do MOM de \_ \_ fechamento**](mm-mom-close.md) e [**mm \_ \_ aberto**](mm-mom-open.md).</span><span class="sxs-lookup"><span data-stu-id="5c92e-127">The *lParam* parameter is unused for [**MM\_MOM\_CLOSE**](mm-mom-close.md) and [**MM\_MOM\_OPEN**](mm-mom-open.md).</span></span>

<span data-ttu-id="5c92e-128">A mensagem mais útil é provavelmente MM \_ Mom \_ concluído.</span><span class="sxs-lookup"><span data-stu-id="5c92e-128">The most useful message is probably MM\_MOM\_DONE.</span></span> <span data-ttu-id="5c92e-129">A menos que você precise alocar memória ou inicializar variáveis, provavelmente não precisa processar MM \_ Mom \_ Open e mm \_ Mom \_ Close.</span><span class="sxs-lookup"><span data-stu-id="5c92e-129">Unless you need to allocate memory or initialize variables, you probably do not need to process MM\_MOM\_OPEN and MM\_MOM\_CLOSE.</span></span> <span data-ttu-id="5c92e-130">Quando a reprodução de um bloco de dados é concluída, você pode limpar e liberar o bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="5c92e-130">When playback of a data block is complete, you can clean up and free the data block.</span></span>

 

 