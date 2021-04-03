---
title: Implementando um plug-in do DSP de áudio
description: Implementando um plug-in do DSP de áudio
ms.assetid: 93ff0c45-f418-443d-8fba-c0a62f6e4e80
keywords:
- Plug-ins do Windows Media Player, DSP de áudio
- plug-ins, DSP de áudio
- plug-ins de processamento de sinal digital, implementando código
- Plug-ins do DSP, implementando código
- plug-ins de processamento de sinal digital, modificando código de exemplo
- Plug-ins do DSP, modificando código de exemplo
- plug-ins de processamento de sinal digital, implementação de áudio
- Plug-ins do DSP, implementação de áudio
- plug-ins do DSP de áudio, implementando código
- plug-ins do DSP de áudio, modificando código de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdde8e7f00fc9ea3ad9bb8b7adb2d0a8bfba6b32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005835"
---
# <a name="implementing-an-audio-dsp-plug-in"></a><span data-ttu-id="da3eb-113">Implementando um plug-in do DSP de áudio</span><span class="sxs-lookup"><span data-stu-id="da3eb-113">Implementing an Audio DSP Plug-in</span></span>

<span data-ttu-id="da3eb-114">Para criar um plug-in de DSP do Windows Media Player que processa áudio, você precisará modificar o código de exemplo na função chamada **DoProcessOutput**.</span><span class="sxs-lookup"><span data-stu-id="da3eb-114">To create a Windows Media Player DSP plug-in that processes audio, you'll need to modify the sample code in the function named **DoProcessOutput**.</span></span> <span data-ttu-id="da3eb-115">**DoProcessOutput** é chamado cada vez que o Windows Media Player chama com êxito **IMediaObject::P rocessoutput**.</span><span class="sxs-lookup"><span data-stu-id="da3eb-115">**DoProcessOutput** is called each time Windows Media Player successfully calls **IMediaObject::ProcessOutput**.</span></span> <span data-ttu-id="da3eb-116">É a função que executa as tarefas de processamento de sinal digital que produzem o resultado audível que o plug-in do DSP pretende produzir.</span><span class="sxs-lookup"><span data-stu-id="da3eb-116">It is the function that performs the digital signal processing tasks that produce the audible result that the DSP plug-in is intended to produce.</span></span>

<span data-ttu-id="da3eb-117">O processamento de um fluxo de áudio é como lidar com um evento cronometrado.</span><span class="sxs-lookup"><span data-stu-id="da3eb-117">Processing an audio stream is like handling a timed event.</span></span> <span data-ttu-id="da3eb-118">**DoProcessOutput** será chamado repetidamente e em intervalos específicos.</span><span class="sxs-lookup"><span data-stu-id="da3eb-118">**DoProcessOutput** will be called repeatedly and at specific intervals.</span></span> <span data-ttu-id="da3eb-119">Cada vez que seu código for executado, ele precisará processar um número específico de bytes de dados.</span><span class="sxs-lookup"><span data-stu-id="da3eb-119">Each time your code executes, it will need to process a specific number of bytes of data.</span></span> <span data-ttu-id="da3eb-120">**DoProcessOutput** contém os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="da3eb-120">**DoProcessOutput** contains the following parameters:</span></span>



| <span data-ttu-id="da3eb-121">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="da3eb-121">Parameter</span></span>          | <span data-ttu-id="da3eb-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="da3eb-122">Description</span></span>                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da3eb-123">*pbOutputData*</span><span class="sxs-lookup"><span data-stu-id="da3eb-123">*pbOutputData*</span></span>     | <span data-ttu-id="da3eb-124">Esse é um ponteiro de **byte** para o buffer em que sua implementação de **DoProcessOutput** deve copiar seus dados processados.</span><span class="sxs-lookup"><span data-stu-id="da3eb-124">This is a **BYTE** pointer to the buffer where your implementation of **DoProcessOutput** must copy its processed data.</span></span> |
| <span data-ttu-id="da3eb-125">*pbInputData*</span><span class="sxs-lookup"><span data-stu-id="da3eb-125">*pbInputData*</span></span>      | <span data-ttu-id="da3eb-126">Esse é um ponteiro de **byte** constante para o buffer que contém os dados a serem processados.</span><span class="sxs-lookup"><span data-stu-id="da3eb-126">This is a constant **BYTE** pointer to the buffer that contains the data to be processed.</span></span>                               |
| <span data-ttu-id="da3eb-127">*cbBytesToProcess*</span><span class="sxs-lookup"><span data-stu-id="da3eb-127">*cbBytesToProcess*</span></span> | <span data-ttu-id="da3eb-128">Esse é um valor **DWORD** que contém uma contagem do número de bytes no buffer de entrada a ser processado.</span><span class="sxs-lookup"><span data-stu-id="da3eb-128">This is a **DWORD** value that contains a count of the number of bytes in the input buffer to be processed.</span></span>             |



 

<span data-ttu-id="da3eb-129">As seções a seguir fornecem detalhes sobre como modificar o código gerado pelo assistente de plug-in do Windows Media Player para criar seu próprio plug-in de DSP de áudio:</span><span class="sxs-lookup"><span data-stu-id="da3eb-129">The following sections provide details about how to modify the code generated by the Windows Media Player Plug-in Wizard to create your own audio DSP plug-in:</span></span>

-   [<span data-ttu-id="da3eb-130">Implementando DoProcessOutput</span><span class="sxs-lookup"><span data-stu-id="da3eb-130">Implementing DoProcessOutput</span></span>](implementing-doprocessoutput.md)
-   [<span data-ttu-id="da3eb-131">Adicionando propriedades ao plug-in do DSP de áudio de exemplo</span><span class="sxs-lookup"><span data-stu-id="da3eb-131">Adding Properties to the Sample Audio DSP Plug-in</span></span>](adding-properties-to-the-sample-audio-dsp-plug-in.md)
-   [<span data-ttu-id="da3eb-132">Implementando a página de propriedades para um plug-in do DSP</span><span class="sxs-lookup"><span data-stu-id="da3eb-132">Implementing the Property Page for a DSP Plug-in</span></span>](implementing-the-property-page-for-a-dsp-plug-in.md)
-   [<span data-ttu-id="da3eb-133">Alterando a propriedade de plug-in do DSP de áudio de exemplo</span><span class="sxs-lookup"><span data-stu-id="da3eb-133">Changing the Sample Audio DSP Plug-in Property</span></span>](changing-the-sample-audio-dsp-plug-in-property.md)
-   [<span data-ttu-id="da3eb-134">Sobre a descontinuidade</span><span class="sxs-lookup"><span data-stu-id="da3eb-134">About Discontinuity</span></span>](about-discontinuity.md)
-   [<span data-ttu-id="da3eb-135">Sobre a alocação de recursos de streaming</span><span class="sxs-lookup"><span data-stu-id="da3eb-135">About Allocating Streaming Resources</span></span>](about-allocating-streaming-resources.md)

## <a name="related-topics"></a><span data-ttu-id="da3eb-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="da3eb-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da3eb-137">**Sobre plug-ins do DSP**</span><span class="sxs-lookup"><span data-stu-id="da3eb-137">**About DSP Plug-ins**</span></span>](about-dsp-plug-ins.md)
</dt> </dl>

 

 




