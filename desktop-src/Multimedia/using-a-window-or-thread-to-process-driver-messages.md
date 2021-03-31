---
title: Usando uma janela ou thread para processar mensagens do driver
description: Usando uma janela ou thread para processar mensagens do driver
ms.assetid: 7a9eaaa1-d3b0-400e-8fbf-ee5fe59efc32
keywords:
- áudio de onda, retorno de chamada de janela
- blocos de dados de áudio, retorno de chamada de janela
- áudio de onda, retorno de chamada de thread
- blocos de dados de áudio, retorno de chamada de thread
- áudio de onda, mensagens de driver de processamento
- blocos de dados de áudio, processando mensagens de driver
- Processando mensagens do driver
- função waveInOpen
- função waveOutOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a147bd86b3c8045456ef9961039f645fd4023f13
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917298"
---
# <a name="using-a-window-or-thread-to-process-driver-messages"></a><span data-ttu-id="33f67-112">Usando uma janela ou thread para processar mensagens do driver</span><span class="sxs-lookup"><span data-stu-id="33f67-112">Using a Window or Thread to Process Driver Messages</span></span>

<span data-ttu-id="33f67-113">Para usar uma função de retorno de chamada de janela, especifique o sinalizador de janela de retorno de chamada \_ no parâmetro *fdwOpen* e um identificador de janela na palavra de ordem inferior do parâmetro *dwCallback* da função [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) ou [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .</span><span class="sxs-lookup"><span data-stu-id="33f67-113">To use a window callback function, specify the CALLBACK\_WINDOW flag in the *fdwOpen* parameter and a window handle in the low-order word of the *dwCallback* parameter of the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) or [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function.</span></span> <span data-ttu-id="33f67-114">As mensagens de driver serão enviadas para o procedimento de janela para a janela identificada pelo identificador em *dwCallback*.</span><span class="sxs-lookup"><span data-stu-id="33f67-114">Driver messages will be sent to the window procedure for the window identified by the handle in *dwCallback*.</span></span>

<span data-ttu-id="33f67-115">Da mesma forma, para usar um retorno de chamada de thread, especifique o thread de retorno de chamada \_ e um identificador de thread na chamada para **WaveInOpen** ou **waveOutOpen**.</span><span class="sxs-lookup"><span data-stu-id="33f67-115">Similarly, to use a thread callback, specify CALLBACK\_THREAD and a thread handle in the call to **waveInOpen** or **waveOutOpen**.</span></span> <span data-ttu-id="33f67-116">Nesse caso, as mensagens são postadas no thread especificado em vez de em uma janela.</span><span class="sxs-lookup"><span data-stu-id="33f67-116">In this case, messages are posted to the specified thread instead of to a window.</span></span>

<span data-ttu-id="33f67-117">As mensagens enviadas para a janela ou retorno de chamada de thread são específicas para o tipo de dispositivo de áudio usado.</span><span class="sxs-lookup"><span data-stu-id="33f67-117">Messages sent to the window or thread callback are specific to the audio device type used.</span></span> <span data-ttu-id="33f67-118">Para obter mais informações sobre essas mensagens, consulte [reproduzindo arquivos de Waveform-Audio](playing-waveform-audio-files.md).</span><span class="sxs-lookup"><span data-stu-id="33f67-118">For more information about these messages, see [Playing Waveform-Audio Files](playing-waveform-audio-files.md).</span></span>

 

 