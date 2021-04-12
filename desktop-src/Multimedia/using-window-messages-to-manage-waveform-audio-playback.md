---
title: Usando mensagens de janela para gerenciar Waveform-Audio reprodução
description: Usando mensagens de janela para gerenciar Waveform-Audio reprodução
ms.assetid: 217968fd-4bb3-405d-a371-c129e29637ab
keywords:
- áudio de onda, gerenciamento de reprodução com mensagens
- Wave-interface de áudio, gerenciando a reprodução com mensagens
- reprodução de formato de onda-arquivos de áudio, gerenciamento de reprodução com mensagens
- áudio de onda, mensagens
- Wave-interface de áudio, mensagens
- executando a onda-arquivos de áudio, mensagens
- MM_WOM_CLOSE mensagem
- MM_WOM_DONE mensagem
- MM_WOM_OPEN mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce02794222274e10498e31e0f38939d930ef3745
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293966"
---
# <a name="using-window-messages-to-manage-waveform-audio-playback"></a><span data-ttu-id="a4c52-112">Usando mensagens de janela para gerenciar Waveform-Audio reprodução</span><span class="sxs-lookup"><span data-stu-id="a4c52-112">Using Window Messages to Manage Waveform-Audio Playback</span></span>

<span data-ttu-id="a4c52-113">As mensagens a seguir podem ser enviadas a uma função de procedimento de janela para gerenciar a reprodução de formato wave-áudio.</span><span class="sxs-lookup"><span data-stu-id="a4c52-113">The following messages can be sent to a window procedure function for managing waveform-audio playback.</span></span>



| <span data-ttu-id="a4c52-114">Mensagem</span><span class="sxs-lookup"><span data-stu-id="a4c52-114">Message</span></span>                                | <span data-ttu-id="a4c52-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4c52-115">Description</span></span>                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4c52-116">**MM \_ wom \_ fechar**</span><span class="sxs-lookup"><span data-stu-id="a4c52-116">**MM\_WOM\_CLOSE**</span></span>](mm-wom-close.md) | <span data-ttu-id="a4c52-117">Enviado quando o dispositivo é fechado usando a função [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) .</span><span class="sxs-lookup"><span data-stu-id="a4c52-117">Sent when the device is closed by using the [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) function.</span></span>                                 |
| [<span data-ttu-id="a4c52-118">**MM \_ wom \_ concluído**</span><span class="sxs-lookup"><span data-stu-id="a4c52-118">**MM\_WOM\_DONE**</span></span>](mm-wom-done.md)   | <span data-ttu-id="a4c52-119">Enviado quando o driver de dispositivo é concluído com um bloco de dados enviado usando a função [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) .</span><span class="sxs-lookup"><span data-stu-id="a4c52-119">Sent when the device driver is finished with a data block sent by using the [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) function.</span></span> |
| [<span data-ttu-id="a4c52-120">**MM \_ wom \_ abertos**</span><span class="sxs-lookup"><span data-stu-id="a4c52-120">**MM\_WOM\_OPEN**</span></span>](mm-wom-open.md)   | <span data-ttu-id="a4c52-121">Enviado quando o dispositivo é aberto usando a função [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .</span><span class="sxs-lookup"><span data-stu-id="a4c52-121">Sent when the device is opened by using the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function.</span></span>                                   |



 

<span data-ttu-id="a4c52-122">Um parâmetro *wParam* e *lParam* está associado a cada uma dessas mensagens.</span><span class="sxs-lookup"><span data-stu-id="a4c52-122">A *wParam* and *lParam* parameter is associated with each of these messages.</span></span> <span data-ttu-id="a4c52-123">O parâmetro *wParam* sempre especifica um identificador do dispositivo Open Wave-Audio.</span><span class="sxs-lookup"><span data-stu-id="a4c52-123">The *wParam* parameter always specifies a handle of the open waveform-audio device.</span></span> <span data-ttu-id="a4c52-124">Para a mensagem [**mm \_ wom \_ concluído**](mm-wom-done.md) , *lParam* especifica um ponteiro para uma estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica o bloco de dados concluído.</span><span class="sxs-lookup"><span data-stu-id="a4c52-124">For the [**MM\_WOM\_DONE**](mm-wom-done.md) message, *lParam* specifies a pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the completed data block.</span></span> <span data-ttu-id="a4c52-125">O parâmetro *lParam* não é usado para as mensagens [**mm \_ wom \_ Close**](mm-wom-close.md) e [**mm \_ wom \_ Open**](mm-wom-open.md) .</span><span class="sxs-lookup"><span data-stu-id="a4c52-125">The *lParam* parameter is unused for the [**MM\_WOM\_CLOSE**](mm-wom-close.md) and [**MM\_WOM\_OPEN**](mm-wom-open.md) messages.</span></span>

<span data-ttu-id="a4c52-126">A mensagem mais útil é provavelmente MM \_ wom \_ concluído.</span><span class="sxs-lookup"><span data-stu-id="a4c52-126">The most useful message is probably MM\_WOM\_DONE.</span></span> <span data-ttu-id="a4c52-127">Quando essa mensagem sinaliza que a reprodução de um bloco de dados é concluída, você pode limpar e liberar o bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="a4c52-127">When this message signals that playback of a data block is complete, you can clean up and free the data block.</span></span> <span data-ttu-id="a4c52-128">A menos que você precise alocar memória ou inicializar variáveis, provavelmente não precisará processar as \_ mensagens mm wom \_ abrir e mm \_ wom \_ fechar.</span><span class="sxs-lookup"><span data-stu-id="a4c52-128">Unless you need to allocate memory or initialize variables, you probably do not need to process the MM\_WOM\_OPEN and MM\_WOM\_CLOSE messages.</span></span>

<span data-ttu-id="a4c52-129">A função de retorno de chamada para dispositivos de saída de wave-áudio é fornecida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a4c52-129">The callback function for waveform-audio output devices is supplied by the application.</span></span> <span data-ttu-id="a4c52-130">Para obter informações sobre essa função de retorno de chamada, consulte a função [**waveOutProc**](/previous-versions//dd743869(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a4c52-130">For information about this callback function, see the [**waveOutProc**](/previous-versions//dd743869(v=vs.85)) function.</span></span>

 

 