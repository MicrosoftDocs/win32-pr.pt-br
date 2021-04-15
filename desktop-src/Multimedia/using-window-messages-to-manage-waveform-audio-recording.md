---
title: Usando mensagens de janela para gerenciar a gravação de Waveform-Audio
description: Usando mensagens de janela para gerenciar a gravação de Waveform-Audio
ms.assetid: 65637d51-9d30-48db-8681-48332442130e
keywords:
- áudio de formato de onda, gerenciando a gravação com mensagens
- Wave-interface de áudio, gerenciando a gravação com mensagens
- gravando áudio de onda, gerenciando a gravação com mensagens
- áudio de onda, mensagens
- Wave-interface de áudio, mensagens
- gravando áudio de onda, mensagens
- MM_WIM_CLOSE mensagem
- MM_WIM_DATA mensagem
- MM_WIM_OPEN mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70bb1cfe1ed0f7ba6052fc1eb6af8fca8355d87d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104453994"
---
# <a name="using-window-messages-to-manage-waveform-audio-recording"></a><span data-ttu-id="0e2de-112">Usando mensagens de janela para gerenciar a gravação de Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="0e2de-112">Using Window Messages to Manage Waveform-Audio Recording</span></span>

<span data-ttu-id="0e2de-113">As mensagens a seguir podem ser enviadas a uma função de procedimento de janela para gerenciar a gravação de formato wave-áudio.</span><span class="sxs-lookup"><span data-stu-id="0e2de-113">The following messages can be sent to a window procedure function for managing waveform-audio recording.</span></span>



| <span data-ttu-id="0e2de-114">Mensagem</span><span class="sxs-lookup"><span data-stu-id="0e2de-114">Message</span></span>                                | <span data-ttu-id="0e2de-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e2de-115">Description</span></span>                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e2de-116">**MM \_ de \_ fechamento de Wim**</span><span class="sxs-lookup"><span data-stu-id="0e2de-116">**MM\_WIM\_CLOSE**</span></span>](mm-wim-close.md) | <span data-ttu-id="0e2de-117">Enviado quando o dispositivo é fechado usando a função [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose) .</span><span class="sxs-lookup"><span data-stu-id="0e2de-117">Sent when the device is closed by using the [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose) function.</span></span>                                     |
| [<span data-ttu-id="0e2de-118">**\_dados wim \_ mm**</span><span class="sxs-lookup"><span data-stu-id="0e2de-118">**MM\_WIM\_DATA**</span></span>](mm-wim-data.md)   | <span data-ttu-id="0e2de-119">Enviado quando o driver de dispositivo é concluído com um buffer enviado usando a função [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) .</span><span class="sxs-lookup"><span data-stu-id="0e2de-119">Sent when the device driver is finished with a buffer sent by using the [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) function.</span></span> |
| [<span data-ttu-id="0e2de-120">**Wim de MM \_ \_ aberto**</span><span class="sxs-lookup"><span data-stu-id="0e2de-120">**MM\_WIM\_OPEN**</span></span>](mm-wim-open.md)   | <span data-ttu-id="0e2de-121">Enviado quando o dispositivo é aberto usando a função [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) .</span><span class="sxs-lookup"><span data-stu-id="0e2de-121">Sent when the device is opened by using the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function.</span></span>                                       |



 

<span data-ttu-id="0e2de-122">O parâmetro *lParam* de [**\_ \_ dados wim mm**](mm-wim-data.md) especifica um ponteiro para uma estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica o buffer.</span><span class="sxs-lookup"><span data-stu-id="0e2de-122">The *lParam* parameter of [**MM\_WIM\_DATA**](mm-wim-data.md) specifies a pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the buffer.</span></span> <span data-ttu-id="0e2de-123">Esse buffer pode não estar completamente cheio com dados de wave-áudio; a gravação pode parar antes de o buffer ser preenchido.</span><span class="sxs-lookup"><span data-stu-id="0e2de-123">This buffer might not be completely filled with waveform-audio data; recording can stop before the buffer is filled.</span></span> <span data-ttu-id="0e2de-124">Use o membro **dwBytesRecorded** da estrutura **WAVEHDR** para determinar a quantidade de dados válidos presentes no buffer.</span><span class="sxs-lookup"><span data-stu-id="0e2de-124">Use the **dwBytesRecorded** member of the **WAVEHDR** structure to determine the amount of valid data present in the buffer.</span></span>

<span data-ttu-id="0e2de-125">A mensagem mais útil é, provavelmente, [**\_ \_ dados de Wim mm**](mm-wim-data.md).</span><span class="sxs-lookup"><span data-stu-id="0e2de-125">The most useful message is probably [**MM\_WIM\_DATA**](mm-wim-data.md).</span></span> <span data-ttu-id="0e2de-126">Quando o aplicativo terminar de usar o bloco de dados enviado pelo driver de dispositivo, você poderá limpar e liberar o bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="0e2de-126">When your application finishes using the data block sent by the device driver, you can clean up and free the data block.</span></span> <span data-ttu-id="0e2de-127">A menos que você precise alocar memória ou inicializar variáveis, provavelmente não precisará usar as mensagens de [**\_ \_ fechamento**](mm-wim-close.md) do WIM Open e mm do [**\_ \_ wim mm**](mm-wim-open.md) .</span><span class="sxs-lookup"><span data-stu-id="0e2de-127">Unless you need to allocate memory or initialize variables, you probably do not need to use the [**MM\_WIM\_OPEN**](mm-wim-open.md) and [**MM\_WIM\_CLOSE**](mm-wim-close.md) messages.</span></span>

<span data-ttu-id="0e2de-128">A função de retorno de chamada para dispositivos de entrada de wave-áudio é fornecida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0e2de-128">The callback function for waveform-audio input devices is supplied by the application.</span></span> <span data-ttu-id="0e2de-129">Para obter informações sobre essa função de retorno de chamada, consulte a função [**waveInProc**](/previous-versions//dd743849(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0e2de-129">For information about this callback function, see the [**waveInProc**](/previous-versions//dd743849(v=vs.85)) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e2de-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e2de-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e2de-131">Gravando áudio de onda</span><span class="sxs-lookup"><span data-stu-id="0e2de-131">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 