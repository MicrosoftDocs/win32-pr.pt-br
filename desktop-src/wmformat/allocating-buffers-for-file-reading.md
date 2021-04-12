---
title: Alocando buffers para leitura de arquivo
description: Alocando buffers para leitura de arquivo
ms.assetid: da66ef5b-ec92-445c-90ba-5ee89e0def36
keywords:
- SDK do Windows Media Format, lendo arquivos ASF
- ASF (Advanced Systems Format), lendo arquivos
- ASF (formato de sistemas avançados), lendo arquivos
- SDK do Windows Media Format, alocando buffers
- ASF (Advanced Systems Format), alocando buffers
- ASF (formato de sistemas avançados), alocando buffers
- ASF (Advanced Systems Format), alocação de buffer
- ASF (formato de sistemas avançados), alocação de buffer
- alocação de buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecdf9ba0a333bbe25c94ec087911237b68f38f74
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365525"
---
# <a name="allocating-buffers-for-file-reading"></a><span data-ttu-id="145a9-112">Alocando buffers para leitura de arquivo</span><span class="sxs-lookup"><span data-stu-id="145a9-112">Allocating Buffers for File Reading</span></span>

<span data-ttu-id="145a9-113">No cenário de leitura de arquivos mais básico, os buffers usados para fornecer exemplos são alocados pelo objeto de leitura (o objeto leitor ou o objeto leitor síncrono).</span><span class="sxs-lookup"><span data-stu-id="145a9-113">In the most basic file-reading scenario, the buffers used to deliver samples are allocated by the reading object (the reader object or the synchronous reader object).</span></span> <span data-ttu-id="145a9-114">No entanto, você pode alocar buffers por conta própria.</span><span class="sxs-lookup"><span data-stu-id="145a9-114">You can, however, allocate buffers yourself.</span></span> <span data-ttu-id="145a9-115">Para obter mais informações sobre os benefícios de alocar seus próprios buffers, consulte [suporte de exemplo alocado pelo usuário](user-allocated-sample-support.md).</span><span class="sxs-lookup"><span data-stu-id="145a9-115">For more information about the benefits of allocating your own buffers, see [User Allocated Sample Support](user-allocated-sample-support.md).</span></span>

<span data-ttu-id="145a9-116">Para usar seus próprios buffers para leitura de arquivos, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="145a9-116">To use your own buffers for file reading, perform the following steps.</span></span>

1.  <span data-ttu-id="145a9-117">Implemente um retorno de chamada ou retornos de chamada para o leitor chamar quando ele precisar de um buffer.</span><span class="sxs-lookup"><span data-stu-id="145a9-117">Implement a callback or callbacks for the reader to call when it needs a buffer.</span></span> <span data-ttu-id="145a9-118">Se você estiver lendo exemplos de saída, use [**IWMReaderAllocatorEx:: AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex).</span><span class="sxs-lookup"><span data-stu-id="145a9-118">If you are reading output samples, use [**IWMReaderAllocatorEx::AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex).</span></span> <span data-ttu-id="145a9-119">Se você estiver lendo exemplos de fluxo, use [**IWMReaderAllocatorEx:: AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).</span><span class="sxs-lookup"><span data-stu-id="145a9-119">If you are reading stream samples, use [**IWMReaderAllocatorEx::AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).</span></span> <span data-ttu-id="145a9-120">Inclua qualquer lógica para o gerenciamento de buffers que atendam ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="145a9-120">Include whatever logic for managing buffers that suits your application.</span></span>
2.  <span data-ttu-id="145a9-121">Aloque um pool de buffers que será usado para a leitura de arquivos.</span><span class="sxs-lookup"><span data-stu-id="145a9-121">Allocate a pool of buffers that you will use for file reading.</span></span>
    -   <span data-ttu-id="145a9-122">Localize o tamanho necessário para seus buffers chamando [**IWMReaderAdvanced:: GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize) ou [**IWMReaderAdvanced:: GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxstreamsamplesize) para cada saída e/ou fluxo para o qual o buffer é usado.</span><span class="sxs-lookup"><span data-stu-id="145a9-122">Find the size required for your buffers by calling [**IWMReaderAdvanced::GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize) or [**IWMReaderAdvanced::GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxstreamsamplesize) for each output and/or stream for which the buffer is used.</span></span> <span data-ttu-id="145a9-123">Se estiver usando o leitor síncrono, use [**IWMSyncReader:: GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxoutputsamplesize) ou [**IWMSyncReader:: GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxstreamsamplesize) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="145a9-123">If using the synchronous reader, use [**IWMSyncReader::GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxoutputsamplesize) or [**IWMSyncReader::GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxstreamsamplesize) instead.</span></span>
    -   <span data-ttu-id="145a9-124">Crie cada buffer para o pool.</span><span class="sxs-lookup"><span data-stu-id="145a9-124">Create each buffer for the pool.</span></span>
3.  <span data-ttu-id="145a9-125">Configure o leitor ou leitor síncrono para leitura.</span><span class="sxs-lookup"><span data-stu-id="145a9-125">Set up the reader or synchronous reader for reading.</span></span> <span data-ttu-id="145a9-126">Para obter mais informações, consulte [lendo arquivos com o leitor assíncrono](reading-files-with-the-asynchronous-reader.md) ou [lendo arquivos com o leitor síncrono](reading-files-with-the-synchronous-reader.md).</span><span class="sxs-lookup"><span data-stu-id="145a9-126">For more information see [Reading Files with the Asynchronous Reader](reading-files-with-the-asynchronous-reader.md) or [Reading Files with the Synchronous Reader](reading-files-with-the-synchronous-reader.md).</span></span>
4.  <span data-ttu-id="145a9-127">Antes de começar a gravar, chame [**IWMReaderAdvanced:: SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforoutput) ou [**IWMReaderAdvanced:: SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforstream) para cada saída e fluxo para o qual você está alocando buffers usando o objeto leitor.</span><span class="sxs-lookup"><span data-stu-id="145a9-127">Before beginning writing, call [**IWMReaderAdvanced::SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforoutput) or [**IWMReaderAdvanced::SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforstream) for each output and stream for which you are allocating buffers using the reader object.</span></span> <span data-ttu-id="145a9-128">Para o leitor síncrono, chame [**IWMSyncReader2:: SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforoutput) ou [**IWMSyncReader2:: SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforstream) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="145a9-128">For the synchronous reader, call [**IWMSyncReader2::SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforoutput) or [**IWMSyncReader2::SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforstream) instead.</span></span>
5.  <span data-ttu-id="145a9-129">Comece a ler o arquivo.</span><span class="sxs-lookup"><span data-stu-id="145a9-129">Begin reading the file.</span></span>

<span data-ttu-id="145a9-130">O objeto de leitura fará chamadas para o retorno de chamada de alocador apropriado e obterá exemplos de seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="145a9-130">The reading object will make calls to the appropriate allocator callback and get samples from your application.</span></span> <span data-ttu-id="145a9-131">A lógica de gerenciamento de buffer deve incluir uma maneira de sinalizar que um buffer está livre para ser usado novamente.</span><span class="sxs-lookup"><span data-stu-id="145a9-131">Your buffer management logic must include a way to signal that a buffer is free to be used again.</span></span> <span data-ttu-id="145a9-132">Normalmente, um buffer é colocado de volta no pool quando seu conteúdo é renderizado.</span><span class="sxs-lookup"><span data-stu-id="145a9-132">Typically, a buffer is put back into the pool when its contents are rendered.</span></span> <span data-ttu-id="145a9-133">Dependendo do seu aplicativo, talvez você precise de apenas alguns buffers no pool ou muitos.</span><span class="sxs-lookup"><span data-stu-id="145a9-133">Depending upon your application, you may need just a few buffers in the pool or many.</span></span>

## <a name="related-topics"></a><span data-ttu-id="145a9-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="145a9-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="145a9-135">**Lendo arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="145a9-135">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




