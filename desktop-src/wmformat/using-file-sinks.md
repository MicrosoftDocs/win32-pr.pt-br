---
title: Uso de coletores de arquivos
description: Uso de coletores de arquivos
ms.assetid: 0cc4320a-c975-452d-bd1c-394d43bd4585
keywords:
- ASF (Advanced Systems Format), coletores de arquivos
- ASF (formato de sistemas avançados), coletores de arquivo
- ASF (Advanced Systems Format), coletores
- ASF (formato de sistemas avançados), coletores
- coletores, coletores de arquivos
- coletores de arquivos, sobre
- coletores de arquivos, criando
- coletores de arquivos, parando
- coletores de arquivos, iniciando
- coletores de arquivos, fechando
- coletores, estatísticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7a7f09a08788128719ea80a2a06d339f6398e6
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104084395"
---
# <a name="using-file-sinks"></a><span data-ttu-id="0ddec-114">Uso de coletores de arquivos</span><span class="sxs-lookup"><span data-stu-id="0ddec-114">Using File Sinks</span></span>

<span data-ttu-id="0ddec-115">Em circunstâncias normais, você pode simplesmente passar o gravador um nome de arquivo de saída usando o método [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) e o objeto gravador gravará o arquivo em disco automaticamente.</span><span class="sxs-lookup"><span data-stu-id="0ddec-115">Under normal circumstances, you can simply pass the writer an output file name using the [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) method, and the writer object will write the file to disk automatically.</span></span> <span data-ttu-id="0ddec-116">Nesse caso, o gravador está, na verdade, criando e controlando um objeto de coletor de arquivo do gravador que manipula a gravação do arquivo em disco.</span><span class="sxs-lookup"><span data-stu-id="0ddec-116">In this case, the writer is actually creating and controlling a writer file sink object that handles writing the file to disk.</span></span> <span data-ttu-id="0ddec-117">Um objeto de coletor de arquivo do gravador controla o fluxo de dados do objeto gravador para um único arquivo.</span><span class="sxs-lookup"><span data-stu-id="0ddec-117">A writer file sink object controls the flow of data from the writer object to a single file.</span></span>

<span data-ttu-id="0ddec-118">Você pode criar seus próprios coletores de arquivos para obter mais controle sobre como o coletor grava o arquivo.</span><span class="sxs-lookup"><span data-stu-id="0ddec-118">You can create your own file sinks to get more control over how the sink writes the file.</span></span> <span data-ttu-id="0ddec-119">Você também pode acessar o coletor de arquivo de gravador padrão criado pelo gravador em resposta a uma chamada para **SetOutputFilename**.</span><span class="sxs-lookup"><span data-stu-id="0ddec-119">You can also access the default writer file sink created by the writer in response to a call to **SetOutputFilename**.</span></span>

## <a name="creating-file-sinks"></a><span data-ttu-id="0ddec-120">Criando coletores de arquivo</span><span class="sxs-lookup"><span data-stu-id="0ddec-120">Creating File Sinks</span></span>

<span data-ttu-id="0ddec-121">Para criar um coletor de arquivos e adicioná-lo ao gravador, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="0ddec-121">To create a file sink and add it to the writer, perform the following steps.</span></span>

1.  <span data-ttu-id="0ddec-122">Crie um novo coletor chamando a função [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink) .</span><span class="sxs-lookup"><span data-stu-id="0ddec-122">Create a new sink by calling the [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink) function.</span></span>
2.  <span data-ttu-id="0ddec-123">Forneça um nome de arquivo para o coletor chamando [**IWMWriterFileSink:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open).</span><span class="sxs-lookup"><span data-stu-id="0ddec-123">Supply a file name for the sink by calling [**IWMWriterFileSink::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open).</span></span>
3.  <span data-ttu-id="0ddec-124">Adicione o coletor de arquivo ao gravador chamando [**IWMWriterAdvanced:: addsink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink).</span><span class="sxs-lookup"><span data-stu-id="0ddec-124">Add the file sink to the writer by calling [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink).</span></span>
4.  <span data-ttu-id="0ddec-125">Execute escrita da maneira usual.</span><span class="sxs-lookup"><span data-stu-id="0ddec-125">Perform writing in the usual way.</span></span>
5.  <span data-ttu-id="0ddec-126">Depois que a gravação for concluída, o coletor fechará o arquivo automaticamente.</span><span class="sxs-lookup"><span data-stu-id="0ddec-126">After writing is completed, the sink will close the file automatically.</span></span>

## <a name="stopping-and-starting-file-sinks"></a><span data-ttu-id="0ddec-127">Parando e iniciando coletores de arquivo</span><span class="sxs-lookup"><span data-stu-id="0ddec-127">Stopping and Starting File Sinks</span></span>

<span data-ttu-id="0ddec-128">Depois que as operações de gravação começam, você pode parar de gravar em um coletor de arquivos chamando [**IWMWriterFileSink2:: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop).</span><span class="sxs-lookup"><span data-stu-id="0ddec-128">After writing operations begin, you can stop writing to a file sink by calling [**IWMWriterFileSink2::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop).</span></span>

<span data-ttu-id="0ddec-129">Há muitas razões possíveis pelas quais você desejaria parar de gravar em um coletor.</span><span class="sxs-lookup"><span data-stu-id="0ddec-129">There are many potential reasons why you would want to stop writing to a sink.</span></span> <span data-ttu-id="0ddec-130">Por exemplo, se você estiver gravando de uma fonte dinâmica, você só poderá estar interessado em parte do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="0ddec-130">For example, if you are recording from a live source, you may only be interested in some of the content.</span></span>

<span data-ttu-id="0ddec-131">Você pode retomar a gravação em um coletor de arquivos chamando [**IWMWriterFileSink2:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start).</span><span class="sxs-lookup"><span data-stu-id="0ddec-131">You can resume writing to a file sink by calling [**IWMWriterFileSink2::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start).</span></span> <span data-ttu-id="0ddec-132">Ambos **param** e **começam** a usar os tempos de apresentação para controlar aproximadamente quando o comando é executado.</span><span class="sxs-lookup"><span data-stu-id="0ddec-132">Both **Stop** and **Start** use presentation times to control approximately when the command is executed.</span></span> <span data-ttu-id="0ddec-133">Você pode usar os métodos [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) para obter mais controle sobre os horários de início e de parada.</span><span class="sxs-lookup"><span data-stu-id="0ddec-133">You can use the [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) methods to gain more control over start and stop times.</span></span>

## <a name="closing-file-sinks"></a><span data-ttu-id="0ddec-134">Fechando coletores de arquivo</span><span class="sxs-lookup"><span data-stu-id="0ddec-134">Closing File Sinks</span></span>

<span data-ttu-id="0ddec-135">Normalmente, um coletor de arquivos é fechado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="0ddec-135">Normally, a file sink is closed automatically.</span></span> <span data-ttu-id="0ddec-136">Se você terminar de gravar em um coletor, mas a gravação de operações em outros coletores estiver continuando, você deverá fechar explicitamente o coletor para conservar os recursos.</span><span class="sxs-lookup"><span data-stu-id="0ddec-136">If you are finished writing to a sink, but writing operations to other sinks are continuing, you should explicitly close the sink to conserve resources.</span></span> <span data-ttu-id="0ddec-137">Para fechar um coletor de arquivos, chame [**IWMWriterFileSink2:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close).</span><span class="sxs-lookup"><span data-stu-id="0ddec-137">To close a file sink, call [**IWMWriterFileSink2::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close).</span></span>

## <a name="getting-sink-statistics"></a><span data-ttu-id="0ddec-138">Obtendo estatísticas do coletor</span><span class="sxs-lookup"><span data-stu-id="0ddec-138">Getting Sink Statistics</span></span>

<span data-ttu-id="0ddec-139">Você pode obter o tamanho do arquivo e a duração de um coletor aberto chamando [**IWMWriterFileSink2:: GetFiles**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) e [**IWMWriterFileSink2:: GetFileDuration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration) respectivamente.</span><span class="sxs-lookup"><span data-stu-id="0ddec-139">You can get the file size and duration for an open sink by calling [**IWMWriterFileSink2::GetFileSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) and [**IWMWriterFileSink2::GetFileDuration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration) respectively.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ddec-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0ddec-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ddec-141">**Interface IWMWriterFileSink**</span><span class="sxs-lookup"><span data-stu-id="0ddec-141">**IWMWriterFileSink Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)
</dt> <dt>

[<span data-ttu-id="0ddec-142">**Interface IWMWriterFileSink2**</span><span class="sxs-lookup"><span data-stu-id="0ddec-142">**IWMWriterFileSink2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)
</dt> <dt>

[<span data-ttu-id="0ddec-143">**Interface IWMWriterFileSink3**</span><span class="sxs-lookup"><span data-stu-id="0ddec-143">**IWMWriterFileSink3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)
</dt> <dt>

[<span data-ttu-id="0ddec-144">**Objeto de coletor de arquivo do gravador**</span><span class="sxs-lookup"><span data-stu-id="0ddec-144">**Writer File Sink Object**</span></span>](writer-file-sink-object.md)
</dt> <dt>

[<span data-ttu-id="0ddec-145">**Gravando arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="0ddec-145">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




