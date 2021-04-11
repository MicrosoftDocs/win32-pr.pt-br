---
title: Gerenciando a gravação de Waveform-Audio
description: Gerenciando a gravação de Waveform-Audio
ms.assetid: a44f7c33-54d6-4ba7-bc57-b63c8b205392
keywords:
- áudio de onda, gravação
- Wave-interface de áudio, gravação
- gravando áudio de onda, sobre
- Estrutura WAVEHDR
- função waveInAddBuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539f722a705d489064d38eccdf6d89e80ccb1518
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293939"
---
# <a name="managing-waveform-audio-recording"></a><span data-ttu-id="eff41-108">Gerenciando a gravação de Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="eff41-108">Managing Waveform-Audio Recording</span></span>

<span data-ttu-id="eff41-109">Depois de abrir um dispositivo de entrada de wave-áudio, você pode começar a gravar dados de formato de onda-áudio.</span><span class="sxs-lookup"><span data-stu-id="eff41-109">After you open a waveform-audio input device, you can begin recording waveform-audio data.</span></span> <span data-ttu-id="eff41-110">Formato de onda-os dados de áudio são registrados em buffers fornecidos pelo aplicativo especificados por uma estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) .</span><span class="sxs-lookup"><span data-stu-id="eff41-110">Waveform-audio data is recorded into application-supplied buffers specified by a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure.</span></span> <span data-ttu-id="eff41-111">Esses blocos de dados devem ser preparados antes de serem usados; para obter mais informações, consulte [blocos de dados de áudio](audio-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="eff41-111">These data blocks must be prepared before they are used; for more information, see [Audio Data Blocks](audio-data-blocks.md).</span></span>

<span data-ttu-id="eff41-112">O Windows fornece as seguintes funções para gerenciar a gravação de formato wave-áudio.</span><span class="sxs-lookup"><span data-stu-id="eff41-112">Windows provides the following functions to manage waveform-audio recording.</span></span>



| <span data-ttu-id="eff41-113">Função</span><span class="sxs-lookup"><span data-stu-id="eff41-113">Function</span></span>                                   | <span data-ttu-id="eff41-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="eff41-114">Description</span></span>                                                                                |
|--------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eff41-115">**waveInAddBuffer**</span><span class="sxs-lookup"><span data-stu-id="eff41-115">**waveInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) | <span data-ttu-id="eff41-116">Envia um buffer para o driver de dispositivo para que ele possa ser preenchido com dados gravados de onda de áudio.</span><span class="sxs-lookup"><span data-stu-id="eff41-116">Sends a buffer to the device driver so it can be filled with recorded waveform-audio data.</span></span> |
| [<span data-ttu-id="eff41-117">**waveInReset**</span><span class="sxs-lookup"><span data-stu-id="eff41-117">**waveInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)         | <span data-ttu-id="eff41-118">Interrompe a gravação de wave-áudio e marca todos os buffers pendentes como concluído.</span><span class="sxs-lookup"><span data-stu-id="eff41-118">Stops waveform-audio recording and marks all pending buffers as done.</span></span>                      |
| [<span data-ttu-id="eff41-119">**waveInStart**</span><span class="sxs-lookup"><span data-stu-id="eff41-119">**waveInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)         | <span data-ttu-id="eff41-120">Inicia a onda-gravação de áudio.</span><span class="sxs-lookup"><span data-stu-id="eff41-120">Starts waveform-audio recording.</span></span>                                                           |
| [<span data-ttu-id="eff41-121">**waveInStop**</span><span class="sxs-lookup"><span data-stu-id="eff41-121">**waveInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)           | <span data-ttu-id="eff41-122">Interrompe a gravação de wave-áudio.</span><span class="sxs-lookup"><span data-stu-id="eff41-122">Stops waveform-audio recording.</span></span>                                                            |



 

<span data-ttu-id="eff41-123">Use a função [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) para enviar buffers para o driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eff41-123">Use the [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) function to send buffers to the device driver.</span></span> <span data-ttu-id="eff41-124">Como os buffers são preenchidos com dados gravados de Wave-Audio, o aplicativo é notificado com uma mensagem de janela, mensagem de retorno de chamada, mensagem de thread ou evento, dependendo do sinalizador especificado quando o dispositivo foi aberto.</span><span class="sxs-lookup"><span data-stu-id="eff41-124">As the buffers are filled with recorded waveform-audio data, the application is notified with a window message, callback message, thread message, or event, depending on the flag specified when the device was opened.</span></span>

<span data-ttu-id="eff41-125">Antes de começar a gravar usando o [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart), você deve enviar pelo menos um buffer para o driver ou os dados de entrada podem ser perdidos.</span><span class="sxs-lookup"><span data-stu-id="eff41-125">Before you begin recording by using [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart), you should send at least one buffer to the driver, or incoming data could be lost.</span></span>

<span data-ttu-id="eff41-126">Antes de fechar o dispositivo usando [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose), chame [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) para marcar os blocos de dados pendentes como sendo feitos.</span><span class="sxs-lookup"><span data-stu-id="eff41-126">Before closing the device using [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose), call [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) to mark any pending data blocks as being done.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eff41-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eff41-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eff41-128">Gravando áudio de onda</span><span class="sxs-lookup"><span data-stu-id="eff41-128">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 