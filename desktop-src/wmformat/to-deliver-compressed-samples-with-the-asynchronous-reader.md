---
title: Para fornecer amostras compactadas com o leitor assíncrono
description: Para fornecer amostras compactadas com o leitor assíncrono
ms.assetid: 488baa3c-8863-4afc-89b2-fe55823e5db9
keywords:
- ASF (Advanced Systems Format), fornecendo amostras compactadas
- ASF (formato de sistemas avançados), fornecendo amostras compactadas
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- ASF (Advanced Systems Format), amostras compactadas
- ASF (formato de sistemas avançados), amostras compactadas
- leitores assíncronos, fornecendo amostras compactadas
- leitores assíncronos, amostras compactadas
- amostras compactadas, entregando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ce835075f5bd760014a3b1b776ba3627adb076
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640155"
---
# <a name="to-deliver-compressed-samples-with-the-asynchronous-reader"></a><span data-ttu-id="f7858-112">Para fornecer amostras compactadas com o leitor assíncrono</span><span class="sxs-lookup"><span data-stu-id="f7858-112">To Deliver Compressed Samples with the Asynchronous Reader</span></span>

<span data-ttu-id="f7858-113">O leitor assíncrono pode fornecer amostras compactadas de fluxos em arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="f7858-113">The asynchronous reader can deliver compressed samples from streams in ASF files.</span></span> <span data-ttu-id="f7858-114">Normalmente, os aplicativos fornecem amostras compactadas ao copiar um fluxo de um arquivo para outro.</span><span class="sxs-lookup"><span data-stu-id="f7858-114">Applications usually deliver compressed samples when copying a stream from one file to another.</span></span> <span data-ttu-id="f7858-115">Não é aconselhável recompactar os dados que foram reconstruídos a partir de um fluxo compactado, pois os dados são perdidos no processo de codificação.</span><span class="sxs-lookup"><span data-stu-id="f7858-115">It is not advisable to recompress data that has been reconstructed from a compressed stream, because data is lost in the encoding process.</span></span> <span data-ttu-id="f7858-116">A mídia digital que foi compactada mais de uma vez terá uma diminuição perceptível na qualidade.</span><span class="sxs-lookup"><span data-stu-id="f7858-116">Digital media that has been compressed more than once will have a noticeable decrease in quality.</span></span>

<span data-ttu-id="f7858-117">O Windows Media Format SDK não fornece nenhum método para decodificar dados depois que ele foi extraído de um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="f7858-117">The Windows Media Format SDK does not provide any methods for decoding data after it has been extracted from an ASF file.</span></span> <span data-ttu-id="f7858-118">Se você receber amostras compactadas e, posteriormente, quiser descompactá-las, precisará fornecer seu próprio código para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="f7858-118">If you receive compressed samples and later want to decompress them, you will have to provide your own code to do so.</span></span> <span data-ttu-id="f7858-119">Uma maneira de contornar essa limitação é escrever os exemplos compactados em um novo arquivo ASF e, em seguida, lê-los novamente em amostras normais e descompactadas.</span><span class="sxs-lookup"><span data-stu-id="f7858-119">One way to get around this limitation is to write the compressed samples to a new ASF file and then re-read them into normal, uncompressed samples.</span></span>

<span data-ttu-id="f7858-120">Para receber amostras compactadas com o leitor assíncrono, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="f7858-120">To receive compressed samples with the asynchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="f7858-121">Implemente o retorno de chamada [**IWMReaderCallbackAdvanced:: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) .</span><span class="sxs-lookup"><span data-stu-id="f7858-121">Implement the [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) callback.</span></span> <span data-ttu-id="f7858-122">Esse retorno de chamada é basicamente idêntico na função para [**IWMReaderCallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) , exceto pelo fato de que ele fornece exemplos por número de fluxo e os exemplos ainda são compactados.</span><span class="sxs-lookup"><span data-stu-id="f7858-122">This callback is basically identical in function to [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) except that it delivers samples by stream number and the samples are still compressed.</span></span>
2.  <span data-ttu-id="f7858-123">Antes de iniciar a reprodução, obtenha um ponteiro para a interface [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) do objeto leitor chamando **IWMReader:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="f7858-123">Before starting playback, obtain a pointer to the [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
3.  <span data-ttu-id="f7858-124">Configure o leitor para fornecer amostras compactadas para o fluxo desejado chamando [**IWMReaderAdvanced:: SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples).</span><span class="sxs-lookup"><span data-stu-id="f7858-124">Configure the reader to deliver compressed samples for the desired stream by calling [**IWMReaderAdvanced::SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples).</span></span>
4.  <span data-ttu-id="f7858-125">Repita a etapa 3 para cada fluxo para o qual a entrega de amostra compactada é desejada.</span><span class="sxs-lookup"><span data-stu-id="f7858-125">Repeat step 3 for each stream for which compressed sample delivery is desired.</span></span>

> [!Note]  
> <span data-ttu-id="f7858-126">Fluxos de imagem não são válidos para entrega de fluxo compactado.</span><span class="sxs-lookup"><span data-stu-id="f7858-126">Image streams are not valid for compressed stream delivery.</span></span> <span data-ttu-id="f7858-127">Se você copiar um fluxo de imagem de um arquivo para outro, ele não funcionará no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="f7858-127">If you copy an image stream from one file to another, it will not work in the new file.</span></span> <span data-ttu-id="f7858-128">Para copiar um fluxo de imagem do arquivo para o arquivo, recupere os exemplos de fluxo de imagem por número de saída e inclua-os no novo arquivo como se incluir um novo fluxo de imagem.</span><span class="sxs-lookup"><span data-stu-id="f7858-128">To copy an image stream from file to file, retrieve the image stream samples by output number and include them in the new file as if including a new image stream.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f7858-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7858-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7858-130">**Interface IWMReaderCallbackAdvanced**</span><span class="sxs-lookup"><span data-stu-id="f7858-130">**IWMReaderCallbackAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[<span data-ttu-id="f7858-131">**Lendo arquivos com o leitor assíncrono**</span><span class="sxs-lookup"><span data-stu-id="f7858-131">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




