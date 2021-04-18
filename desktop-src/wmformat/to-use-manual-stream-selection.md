---
title: Para usar a seleção de fluxo manual
description: Para usar a seleção de fluxo manual
ms.assetid: 49ec283f-670a-4a0e-9477-c60a80919a1e
keywords:
- ASF (Advanced Systems Format), seleção de fluxo manual
- ASF (formato de sistemas avançados), seleção de fluxo manual
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- ASF (Advanced Systems Format), seleção de fluxo
- ASF (formato de sistemas avançados), seleção de fluxo
- ASF (Advanced Systems Format), exclusão mútua
- ASF (formato de sistemas avançados), exclusão mútua
- leitores assíncronos, seleção de fluxo manual
- leitores assíncronos, seleção de fluxo
- fluxos, seleção manual
- exclusão mútua, seleção de fluxo manual
- fluxos, leitores assíncronos
- exclusão mútua, leitores assíncronos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87c493bc8f41bc2a03ba15832ed402939adbeff
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105770649"
---
# <a name="to-use-manual-stream-selection"></a><span data-ttu-id="e4daf-117">Para usar a seleção de fluxo manual</span><span class="sxs-lookup"><span data-stu-id="e4daf-117">To Use Manual Stream Selection</span></span>

<span data-ttu-id="e4daf-118">Ao fornecer exemplos não compactados com o objeto leitor, você pode entregá-los somente pelo número de saída.</span><span class="sxs-lookup"><span data-stu-id="e4daf-118">When delivering uncompressed samples with the reader object, you can deliver them only by output number.</span></span> <span data-ttu-id="e4daf-119">No caso de fluxos mutuamente exclusivos, isso significa que você pode receber amostras somente de um fluxo na exclusão mútua de cada vez.</span><span class="sxs-lookup"><span data-stu-id="e4daf-119">In the case of mutually exclusive streams, this means that you can receive samples only from one stream in the mutual exclusion at a time.</span></span> <span data-ttu-id="e4daf-120">O processo de escolher qual fluxo mutuamente exclusivo a ser entregue é chamado de seleção de fluxo.</span><span class="sxs-lookup"><span data-stu-id="e4daf-120">The process of choosing which mutually exclusive stream to deliver is called stream selection.</span></span>

<span data-ttu-id="e4daf-121">Para a exclusão mútua de taxa de bits, o leitor faz seleções de fluxo automaticamente com base nas condições no computador host na reprodução.</span><span class="sxs-lookup"><span data-stu-id="e4daf-121">For bit-rate mutual exclusion, the reader makes stream selections automatically based on the conditions on the host machine at playback.</span></span> <span data-ttu-id="e4daf-122">Para outros tipos de exclusão mútua, o leitor fornecerá exemplos do fluxo padrão, a menos que você selecione manualmente um fluxo diferente.</span><span class="sxs-lookup"><span data-stu-id="e4daf-122">For other types of mutual exclusion, the reader will deliver samples from the default stream unless you manually select a different stream yourself.</span></span> <span data-ttu-id="e4daf-123">Também pode haver instâncias em que você deseja selecionar um fluxo manualmente de uma exclusão mútua de taxa de bits.</span><span class="sxs-lookup"><span data-stu-id="e4daf-123">There may also be instances when you want to select a stream manually from a bit-rate mutual exclusion.</span></span>

<span data-ttu-id="e4daf-124">A seleção de fluxo manual está ativada ou desativada para o arquivo inteiro.</span><span class="sxs-lookup"><span data-stu-id="e4daf-124">Manual stream selection is either on or off for the entire file.</span></span> <span data-ttu-id="e4daf-125">Se um arquivo contiver exclusão mútua de taxa de bits e algum outro tipo de exclusão mútua, você deverá selecionar manualmente os fluxos com base na taxa de bits.</span><span class="sxs-lookup"><span data-stu-id="e4daf-125">If a file contains bit-rate mutual exclusion and some other mutual exclusion type, you must select the bit rate based streams manually.</span></span>

<span data-ttu-id="e4daf-126">Para selecionar um fluxo mutuamente exclusivo manualmente, você deve executar as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="e4daf-126">To select a mutually exclusive stream manually, you must perform the following steps.</span></span>

1.  <span data-ttu-id="e4daf-127">Recupere um ponteiro para a interface [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) do objeto leitor chamando **IWMReader:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="e4daf-127">Retrieve a pointer to the [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
2.  <span data-ttu-id="e4daf-128">Habilite a seleção de fluxo manual chamando [**IWMReaderAdvanced:: SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection).</span><span class="sxs-lookup"><span data-stu-id="e4daf-128">Enable manual stream selection by calling [**IWMReaderAdvanced::SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection).</span></span>
3.  <span data-ttu-id="e4daf-129">Para descobrir se um fluxo específico está selecionado, chame [**IWMReaderAdvanced:: GetStreamSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected).</span><span class="sxs-lookup"><span data-stu-id="e4daf-129">To find out if a particular stream is selected, call [**IWMReaderAdvanced::GetStreamSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected).</span></span> <span data-ttu-id="e4daf-130">Você deve passar um ponteiro para uma variável do tipo de enumeração de [**\_ \_ seleção de fluxo WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection) .</span><span class="sxs-lookup"><span data-stu-id="e4daf-130">You must pass a pointer to a variable of the [**WMT\_STREAM\_SELECTION**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection) enumeration type.</span></span> <span data-ttu-id="e4daf-131">Quando a chamada retorna, o valor na variável descreverá o tipo de seleção atual do fluxo.</span><span class="sxs-lookup"><span data-stu-id="e4daf-131">When the call returns, the value in the variable will describe the current selection type of the stream.</span></span>
4.  <span data-ttu-id="e4daf-132">Para selecionar um fluxo, chame [**IWMReaderAdvanced:: SetStreamsSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected).</span><span class="sxs-lookup"><span data-stu-id="e4daf-132">To select a stream, call [**IWMReaderAdvanced::SetStreamsSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected).</span></span> <span data-ttu-id="e4daf-133">Esse método permite que você especifique vários fluxos ao mesmo tempo para a alternância de fluxo sincronizada.</span><span class="sxs-lookup"><span data-stu-id="e4daf-133">This method enables you to specify multiple streams at the same time for synchronized stream switching.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4daf-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e4daf-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4daf-135">**Lendo arquivos com o leitor assíncrono**</span><span class="sxs-lookup"><span data-stu-id="e4daf-135">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




