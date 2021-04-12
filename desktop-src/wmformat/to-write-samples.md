---
title: Para escrever exemplos
description: Para escrever exemplos
ms.assetid: 9ce10a77-9e80-45e0-a7e7-2ffdf8b57773
keywords:
- ASF (Advanced Systems Format), exemplos de gravação
- ASF (formato de sistemas avançados), escrevendo exemplos
- ASF (Advanced Systems Format), passando amostras para o gravador
- ASF (formato de sistemas avançados), passando amostras para o gravador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 738014b3c42441e878105d12a8ebf23ce4b266f7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365555"
---
# <a name="to-write-samples"></a><span data-ttu-id="482aa-107">Para escrever exemplos</span><span class="sxs-lookup"><span data-stu-id="482aa-107">To Write Samples</span></span>

<span data-ttu-id="482aa-108">Quando você tiver identificado e configurado as entradas para o arquivo que está gravando, poderá começar a passar amostras para o gravador.</span><span class="sxs-lookup"><span data-stu-id="482aa-108">When you have identified and configured the inputs for the file you are writing, you can begin passing samples to the writer.</span></span> <span data-ttu-id="482aa-109">Você deve passar os exemplos na ordem de tempo de apresentação, se possível, para tornar o processo de gravação mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="482aa-109">You should pass samples in presentation-time order, if possible, to make the writing process more efficient.</span></span>

<span data-ttu-id="482aa-110">Antes de passar qualquer amostra, você deve definir o gravador para aceitá-las chamando [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span><span class="sxs-lookup"><span data-stu-id="482aa-110">Before passing any samples, you must set the writer to accept them by calling [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

<span data-ttu-id="482aa-111">Para passar um exemplo para o gravador, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="482aa-111">To pass a sample to the writer, perform the following steps:</span></span>

1.  <span data-ttu-id="482aa-112">Aloque um buffer e recupere um ponteiro para a interface [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) chamando [**IWMWriter:: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).</span><span class="sxs-lookup"><span data-stu-id="482aa-112">Allocate a buffer and retrieve a pointer to the [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) interface by calling [**IWMWriter::AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).</span></span>
2.  <span data-ttu-id="482aa-113">Recupere o endereço do buffer criado na etapa 1 chamando [**INSSBuffer:: GetBuffer**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbuffer).</span><span class="sxs-lookup"><span data-stu-id="482aa-113">Retrieve the address of the buffer created in step 1 by calling [**INSSBuffer::GetBuffer**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbuffer).</span></span>
3.  <span data-ttu-id="482aa-114">Copie os dados de exemplo para o local do buffer, certificando-se de que o exemplo passado caiba no buffer alocado.</span><span class="sxs-lookup"><span data-stu-id="482aa-114">Copy your sample data to the buffer location, making sure that the sample passed will fit in the allocated buffer.</span></span> <span data-ttu-id="482aa-115">Você pode usar qualquer função de cópia de memória para copiar seus dados.</span><span class="sxs-lookup"><span data-stu-id="482aa-115">You can use any memory copying function to copy your data.</span></span> <span data-ttu-id="482aa-116">Uma opção comum é o memcpy, que está incluído na biblioteca padrão de tempo de execução do C.</span><span class="sxs-lookup"><span data-stu-id="482aa-116">A common choice is memcpy, which is included in the standard C run-time library.</span></span>
4.  <span data-ttu-id="482aa-117">Atualize a quantidade de dados usados no buffer para refletir o tamanho real do exemplo chamando [**INSSBuffer:: SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).</span><span class="sxs-lookup"><span data-stu-id="482aa-117">Update the amount of data used in the buffer to reflect the actual size of the sample by calling [**INSSBuffer::SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).</span></span>
5.  <span data-ttu-id="482aa-118">Passe a interface de buffer para o gravador junto com o número de entrada e o tempo de amostra usando o método [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) .</span><span class="sxs-lookup"><span data-stu-id="482aa-118">Pass the buffer interface to the writer along with the input number and sample time using the [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) method.</span></span> <span data-ttu-id="482aa-119">Todos os exemplos de áudio de uma entrada representam a mesma duração do conteúdo, de modo que você pode calcular o tempo de amostra adicionando a duração de amostra a um total em execução.</span><span class="sxs-lookup"><span data-stu-id="482aa-119">All audio samples for an input represent the same duration of content, so you can figure the sample time by adding the sample duration to a running total.</span></span> <span data-ttu-id="482aa-120">Para vídeo, você precisa calcular a hora com base na taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="482aa-120">For video, you need to calculate the time based on the frame rate.</span></span>

<span data-ttu-id="482aa-121">O **WriteSample** funciona de forma assíncrona e pode não terminar de gravar os dados do buffer antes que seu aplicativo esteja pronto para chamar o método novamente.</span><span class="sxs-lookup"><span data-stu-id="482aa-121">**WriteSample** works asynchronously and might not finish writing the data from the buffer before your application is ready to call the method again.</span></span> <span data-ttu-id="482aa-122">Portanto, é importante chamar **AllocateSample** uma vez para cada chamada para **WriteSample**.</span><span class="sxs-lookup"><span data-stu-id="482aa-122">Therefore, it is important to call **AllocateSample** once for each call to **WriteSample**.</span></span> <span data-ttu-id="482aa-123">No entanto, você pode liberar a interface **INSSBuffer** imediatamente após chamar **WriteSample**.</span><span class="sxs-lookup"><span data-stu-id="482aa-123">However, you can release the **INSSBuffer** interface immediately after calling **WriteSample**.</span></span>

<span data-ttu-id="482aa-124">Quando terminar de passar amostras, chame [**IWMWriter:: redação**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting).</span><span class="sxs-lookup"><span data-stu-id="482aa-124">When you have finished passing samples, call [**IWMWriter::EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting).</span></span>

<span data-ttu-id="482aa-125">**Observação** É importante que amostras de todos os fluxos no arquivo sejam passadas para o gravador em sincronização entre si.</span><span class="sxs-lookup"><span data-stu-id="482aa-125">**Note** It is important that samples from all streams in the file are passed to the writer in synchronization with one another.</span></span> <span data-ttu-id="482aa-126">Ou seja, sempre que possível, você deve passar amostras para o gravador em ordem de tempo de apresentação dentro da tolerância de sincronização especificada em [**IWMWriterAdvanced:: SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).</span><span class="sxs-lookup"><span data-stu-id="482aa-126">That is, whenever possible you should pass samples to the writer in presentation-time order within the sync tolerance specified in [**IWMWriterAdvanced::SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).</span></span> <span data-ttu-id="482aa-127">Os melhores resultados são obtidos quando os dados são entregues a cada fluxo em unidades de um segundo ou menos.</span><span class="sxs-lookup"><span data-stu-id="482aa-127">Best results are achieved when data is delivered to each stream in units of one second or less.</span></span>

<span data-ttu-id="482aa-128">Os fluxos também devem terminar quase ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="482aa-128">Streams should also end at approximately the same time.</span></span> <span data-ttu-id="482aa-129">Por exemplo, você não deve gravar um arquivo com um fluxo de áudio com 45 segundos de comprimento e um fluxo de vídeo que tenha 50 segundos de comprimento.</span><span class="sxs-lookup"><span data-stu-id="482aa-129">For example, you should not write a file with an audio stream that is 45 seconds long and a video stream that is 50 seconds long.</span></span> <span data-ttu-id="482aa-130">Se você codificar esse arquivo com entradas inalteradas, alguns dos dados de áudio no final do fluxo serão descartados (mesmo que seja o fluxo mais curto).</span><span class="sxs-lookup"><span data-stu-id="482aa-130">If you encode such a file with unaltered inputs, some of the audio data at the end of the stream will be dropped (even though it is the shorter stream).</span></span> <span data-ttu-id="482aa-131">Para fazer com que a codificação do arquivo funcione, você deve adicionar 5 segundos de silêncio à entrada de áudio para que um fluxo não termine vários segundos antes de outro.</span><span class="sxs-lookup"><span data-stu-id="482aa-131">To make the file encoding work, you should add 5 seconds of silence to the audio input so that one stream does not end several seconds before another.</span></span> <span data-ttu-id="482aa-132">Não é necessário que os tipos de fluxo com amostras intermitentes, como fluxos de texto ou de imagem, sejam preenchidos dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="482aa-132">It is not necessary for stream types with intermittent samples, like text or image streams, to be padded in this way.</span></span> <span data-ttu-id="482aa-133">Fluxos de comando de script também devem seguir todas essas regras.</span><span class="sxs-lookup"><span data-stu-id="482aa-133">Script command streams should also follow all these rules.</span></span>

## <a name="related-topics"></a><span data-ttu-id="482aa-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="482aa-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="482aa-135">**Interface INSSBuffer**</span><span class="sxs-lookup"><span data-stu-id="482aa-135">**INSSBuffer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[<span data-ttu-id="482aa-136">**Interface IWMWriter**</span><span class="sxs-lookup"><span data-stu-id="482aa-136">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="482aa-137">**Gravando arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="482aa-137">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




