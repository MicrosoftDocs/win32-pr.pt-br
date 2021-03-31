---
title: Blocos de dados de áudio
description: Blocos de dados de áudio
ms.assetid: 9646e18c-294b-4532-bd5e-709d66ad31f4
keywords:
- áudio de multimídia, blocos de dados
- áudio, blocos de dados
- áudio de onda, blocos de dados
- blocos de dados de áudio, sobre
- Estrutura WAVEHDR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a81a5a29ec9718e7c11306b6bafc1aa20369e5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917190"
---
# <a name="audio-data-blocks"></a><span data-ttu-id="9867c-108">Blocos de dados de áudio</span><span class="sxs-lookup"><span data-stu-id="9867c-108">Audio Data Blocks</span></span>

<span data-ttu-id="9867c-109">As funções [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) e [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) exigem que os aplicativos aloquem blocos de dados para passar para os drivers de dispositivo para fins de gravação ou reprodução.</span><span class="sxs-lookup"><span data-stu-id="9867c-109">The [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) and [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) functions require applications to allocate data blocks to pass to the device drivers for recording or playback purposes.</span></span> <span data-ttu-id="9867c-110">Ambas as funções usam a estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) para descrever seu bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="9867c-110">Both of these functions use the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure to describe its data block.</span></span>

<span data-ttu-id="9867c-111">Antes de usar uma dessas funções para passar um bloco de dados para um driver de dispositivo, você deve alocar memória para o bloco de dados e a estrutura de cabeçalho que descreve o bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="9867c-111">Before using one of these functions to pass a data block to a device driver, you must allocate memory for the data block and the header structure that describes the data block.</span></span> <span data-ttu-id="9867c-112">Os cabeçalhos podem ser preparados e despreparados usando as funções a seguir.</span><span class="sxs-lookup"><span data-stu-id="9867c-112">The headers can be prepared and unprepared by using the following functions.</span></span>



| <span data-ttu-id="9867c-113">Função</span><span class="sxs-lookup"><span data-stu-id="9867c-113">Function</span></span>                                                 | <span data-ttu-id="9867c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="9867c-114">Description</span></span>                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="9867c-115">**waveInPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="9867c-115">**waveInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)       | <span data-ttu-id="9867c-116">Prepara um bloco de dados de entrada de wave-áudio.</span><span class="sxs-lookup"><span data-stu-id="9867c-116">Prepares a waveform-audio input data block.</span></span>                      |
| [<span data-ttu-id="9867c-117">**waveInUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="9867c-117">**waveInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)   | <span data-ttu-id="9867c-118">Limpa a preparação em um bloco de dados de entrada de forma de onda-áudio.</span><span class="sxs-lookup"><span data-stu-id="9867c-118">Cleans up the preparation on a waveform-audio input data block.</span></span>  |
| [<span data-ttu-id="9867c-119">**waveOutPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="9867c-119">**waveOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)     | <span data-ttu-id="9867c-120">Prepara um bloco de dados de saída de wave-áudio.</span><span class="sxs-lookup"><span data-stu-id="9867c-120">Prepares a waveform-audio output data block.</span></span>                     |
| [<span data-ttu-id="9867c-121">**waveOutUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="9867c-121">**waveOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) | <span data-ttu-id="9867c-122">Limpa a preparação em um bloco de dados de saída de wave-áudio.</span><span class="sxs-lookup"><span data-stu-id="9867c-122">Cleans up the preparation on a waveform-audio output data block.</span></span> |



 

<span data-ttu-id="9867c-123">Antes de passar um bloco de dados de áudio para um driver de dispositivo, você deve preparar o bloco de dados passando-o para [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader) ou [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader).</span><span class="sxs-lookup"><span data-stu-id="9867c-123">Before you pass an audio data block to a device driver, you must prepare the data block by passing it to either [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader) or [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader).</span></span> <span data-ttu-id="9867c-124">Quando o driver de dispositivo for concluído com o bloco de dados e o retornar, você deverá limpar essa preparação passando o bloco de dados para [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader) ou [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) antes que qualquer memória alocada possa ser liberada.</span><span class="sxs-lookup"><span data-stu-id="9867c-124">When the device driver is finished with the data block and returns it, you must clean up this preparation by passing the data block to either [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader) or [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) before any allocated memory can be freed.</span></span>

<span data-ttu-id="9867c-125">A menos que os dados de entrada e saída de wave-áudio sejam pequenos o suficiente para serem contidos em um único bloco de dados, os aplicativos devem fornecer continuamente o driver de dispositivo com blocos de dados até que a reprodução ou gravação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="9867c-125">Unless the waveform-audio input and output data is small enough to be contained in a single data block, applications must continually supply the device driver with data blocks until playback or recording is complete.</span></span>

<span data-ttu-id="9867c-126">Mesmo que um único bloco de dados seja usado, um aplicativo deve ser capaz de determinar quando um driver de dispositivo é concluído com o bloco de dados para que o aplicativo possa liberar a memória associada ao bloco de dados e à estrutura de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="9867c-126">Even if a single data block is used, an application must be able to determine when a device driver is finished with the data block so the application can free the memory associated with the data block and header structure.</span></span> <span data-ttu-id="9867c-127">Há várias maneiras de determinar quando um driver de dispositivo é concluído com um bloco de dados:</span><span class="sxs-lookup"><span data-stu-id="9867c-127">There are several ways to determine when a device driver is finished with a data block:</span></span>

-   <span data-ttu-id="9867c-128">Especificando uma função de retorno de chamada para receber uma mensagem enviada pelo driver quando ela é concluída com um bloco de dados</span><span class="sxs-lookup"><span data-stu-id="9867c-128">By specifying a callback function to receive a message sent by the driver when it is finished with a data block</span></span>
-   <span data-ttu-id="9867c-129">Usando um retorno de chamada de evento</span><span class="sxs-lookup"><span data-stu-id="9867c-129">By using an event callback</span></span>
-   <span data-ttu-id="9867c-130">Especificando uma janela ou thread para receber uma mensagem enviada pelo driver quando ele é concluído com um bloco de dados</span><span class="sxs-lookup"><span data-stu-id="9867c-130">By specifying a window or thread to receive a message sent by the driver when it is finished with a data block</span></span>
-   <span data-ttu-id="9867c-131">Sondando o \_ bit WHDR realizado no membro **dwFlags** da estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) enviada com cada bloco de dados</span><span class="sxs-lookup"><span data-stu-id="9867c-131">By polling the WHDR\_DONE bit in the **dwFlags** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure sent with each data block</span></span>

<span data-ttu-id="9867c-132">Se um aplicativo não obtiver um bloco de dados para o driver de dispositivo quando necessário, poderá haver uma lacuna audível na reprodução ou uma perda de informações registradas de entrada.</span><span class="sxs-lookup"><span data-stu-id="9867c-132">If an application does not get a data block to the device driver when needed, there can be an audible gap in playback or a loss of incoming recorded information.</span></span> <span data-ttu-id="9867c-133">Isso requer pelo menos um esquema de buffer duplo — mantendo pelo menos um bloco de dados à frente do driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9867c-133">This requires at least a double-buffering scheme — staying at least one data block ahead of the device driver.</span></span>

<span data-ttu-id="9867c-134">Os tópicos a seguir descrevem maneiras de determinar quando um driver de dispositivo é concluído com um bloco de dados:</span><span class="sxs-lookup"><span data-stu-id="9867c-134">The following topics describe ways to determine when a device driver is finished with a data block:</span></span>

<span data-ttu-id="9867c-135">Usando uma função de retorno de chamada para processar mensagens de driver</span><span class="sxs-lookup"><span data-stu-id="9867c-135">Using a Callback Function to Process Driver Messages</span></span>

-   [<span data-ttu-id="9867c-136">Usando uma função de retorno de chamada para processar mensagens de driver</span><span class="sxs-lookup"><span data-stu-id="9867c-136">Using a Callback Function to Process Driver Messages</span></span>](using-a-callback-function-to-process-driver-messages.md)
-   [<span data-ttu-id="9867c-137">Usando um retorno de chamada de evento para processar mensagens de driver</span><span class="sxs-lookup"><span data-stu-id="9867c-137">Using an Event Callback to Process Driver Messages</span></span>](using-an-callback-to-process-driver-messages.md)
-   [<span data-ttu-id="9867c-138">Usando uma janela ou thread para processar mensagens do driver</span><span class="sxs-lookup"><span data-stu-id="9867c-138">Using a Window or Thread to Process Driver Messages</span></span>](using-a-window-or-thread-to-process-driver-messages.md)
-   [<span data-ttu-id="9867c-139">Gerenciando blocos de dados por sondagem</span><span class="sxs-lookup"><span data-stu-id="9867c-139">Managing Data Blocks by Polling</span></span>](managing-data-blocks-by-polling.md)

 

 