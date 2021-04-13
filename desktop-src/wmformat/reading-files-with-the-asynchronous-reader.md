---
title: Lendo arquivos com o leitor assíncrono
description: Lendo arquivos com o leitor assíncrono
ms.assetid: 3cc72f8d-bf1f-416d-bc90-21dfb92a55aa
keywords:
- SDK do Windows Media Format, lendo arquivos
- SDK do Windows Media Format, leitores assíncronos
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- ASF (Advanced Systems Format), lendo arquivos
- ASF (formato de sistemas avançados), lendo arquivos
- leitores assíncronos, interface IWMReaderCallback
- IWMReaderCallback, leitores assíncronos
- leitores assíncronos, lendo arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0807c0701dd596f943010ad613b08ef9fe2c415c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365544"
---
# <a name="reading-files-with-the-asynchronous-reader"></a><span data-ttu-id="aa918-112">Lendo arquivos com o leitor assíncrono</span><span class="sxs-lookup"><span data-stu-id="aa918-112">Reading Files with the Asynchronous Reader</span></span>

<span data-ttu-id="aa918-113">O leitor assíncrono lê o conteúdo de arquivos ASF usando vários threads e chamadas assíncronas.</span><span class="sxs-lookup"><span data-stu-id="aa918-113">The asynchronous reader reads the content from ASF files using multiple threads and asynchronous calls.</span></span> <span data-ttu-id="aa918-114">Os recursos com suporte do leitor assíncrono o tornam adequado para aplicativos que processam o conteúdo para os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="aa918-114">The features supported by the asynchronous reader make it well suited for applications that render content to end users.</span></span>

<span data-ttu-id="aa918-115">A funcionalidade mais básica do objeto leitor pode ser dividida nas etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa918-115">The most basic functionality of the reader object can be broken down into the following steps.</span></span> <span data-ttu-id="aa918-116">Nestas etapas, "o aplicativo" se refere ao programa que você escreve usando o SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="aa918-116">In these steps "the application" refers to the program you write using the Windows Media Format SDK.</span></span>

1.  <span data-ttu-id="aa918-117">O aplicativo implementa a interface [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) para lidar com mensagens do leitor.</span><span class="sxs-lookup"><span data-stu-id="aa918-117">The application implements the [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) interface to handle messages from the reader.</span></span> <span data-ttu-id="aa918-118">Isso inclui dois métodos de retorno de chamada: **OnStatus**, que recebe mensagens relacionadas ao status de vários aspectos do leitor e da **amostra**, que recebe amostras descompactadas do leitor.</span><span class="sxs-lookup"><span data-stu-id="aa918-118">This includes two callback methods: **OnStatus**, which receives messages relating to the status of various aspects of the reader and **OnSample**, which receives uncompressed samples from the reader.</span></span>
2.  <span data-ttu-id="aa918-119">O aplicativo passa para o leitor o nome de um arquivo a ser lido.</span><span class="sxs-lookup"><span data-stu-id="aa918-119">The application passes to the reader the name of a file to read.</span></span> <span data-ttu-id="aa918-120">Quando o leitor abre o arquivo, ele atribui um número de saída a cada fluxo.</span><span class="sxs-lookup"><span data-stu-id="aa918-120">When the reader opens the file, it assigns an output number to each stream.</span></span> <span data-ttu-id="aa918-121">Se o arquivo usar a exclusão mútua, o leitor atribuirá uma única saída para todos os fluxos mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="aa918-121">If the file uses mutual exclusion, the reader assigns a single output for all of the mutually exclusive streams.</span></span>
3.  <span data-ttu-id="aa918-122">O aplicativo obtém informações sobre a configuração das várias saídas do leitor.</span><span class="sxs-lookup"><span data-stu-id="aa918-122">The application gets information about the configuration of the various outputs from the reader.</span></span> <span data-ttu-id="aa918-123">As informações coletadas permitirão que o aplicativo processe amostras de mídia corretamente.</span><span class="sxs-lookup"><span data-stu-id="aa918-123">The information gathered will enable the application to properly render media samples.</span></span>
4.  <span data-ttu-id="aa918-124">O aplicativo instrui o leitor a começar a ler dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="aa918-124">The application instructs the reader to begin reading data from the file.</span></span> <span data-ttu-id="aa918-125">O leitor começa a fornecer amostras descompactadas para o retorno de chamada **onsample** , um por vez, em buffers encapsulados em objetos de buffer.</span><span class="sxs-lookup"><span data-stu-id="aa918-125">The reader begins delivering uncompressed samples to the **OnSample** callback one at a time in buffers wrapped in buffer objects.</span></span> <span data-ttu-id="aa918-126">Os exemplos entregues pelo leitor estão em ordem de tempo de apresentação.</span><span class="sxs-lookup"><span data-stu-id="aa918-126">The samples delivered by the reader are in presentation-time order.</span></span> <span data-ttu-id="aa918-127">O leitor continuará fornecendo amostras até que seja interrompido pelo aplicativo ou até que o final do arquivo seja atingido.</span><span class="sxs-lookup"><span data-stu-id="aa918-127">The reader will continue delivering samples until stopped by the application or until the end of the file is reached.</span></span>
5.  <span data-ttu-id="aa918-128">O aplicativo é responsável por renderizar dados depois que eles são entregues pelo leitor.</span><span class="sxs-lookup"><span data-stu-id="aa918-128">The application is responsible for rendering data after it is delivered by the reader.</span></span> <span data-ttu-id="aa918-129">O Windows Media Format SDK não fornece nenhuma rotina de renderização.</span><span class="sxs-lookup"><span data-stu-id="aa918-129">The Windows Media Format SDK does not provide any rendering routines.</span></span> <span data-ttu-id="aa918-130">Normalmente, os aplicativos usarão outros SDKs para renderizar dados, como o Microsoft DirectX® SDK ou as funções de multimídia do SDK da plataforma Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="aa918-130">Typically, applications will use other SDKs to render data, such as the Microsoft DirectX® SDK, or the multimedia functions of the Microsoft Windows Platform SDK.</span></span>
6.  <span data-ttu-id="aa918-131">Quando a leitura estiver concluída, o aplicativo instruirá o leitor a fechar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="aa918-131">When reading is complete, the application instructs the reader to close the file.</span></span>

<span data-ttu-id="aa918-132">Essas etapas são ilustradas no aplicativo de exemplo AudioPlayer, entre outras.</span><span class="sxs-lookup"><span data-stu-id="aa918-132">These steps are illustrated in the AudioPlayer sample application, among others.</span></span> <span data-ttu-id="aa918-133">Para obter mais informações, consulte [aplicativos de exemplo](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="aa918-133">For more information, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="aa918-134">O leitor também dá suporte à funcionalidade mais avançada.</span><span class="sxs-lookup"><span data-stu-id="aa918-134">The reader also supports more advanced functionality.</span></span> <span data-ttu-id="aa918-135">O leitor permite que você faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="aa918-135">The reader enables you to do the following:</span></span>

-   <span data-ttu-id="aa918-136">Pausar reprodução de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="aa918-136">Pause playback of a file.</span></span>
-   <span data-ttu-id="aa918-137">Recuperar estatísticas de desempenho do leitor.</span><span class="sxs-lookup"><span data-stu-id="aa918-137">Retrieve reader performance statistics.</span></span>
-   <span data-ttu-id="aa918-138">Seleção de fluxo de controle para fluxos mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="aa918-138">Control stream selection for mutually exclusive streams.</span></span>
-   <span data-ttu-id="aa918-139">Aloque manualmente os buffers para saída.</span><span class="sxs-lookup"><span data-stu-id="aa918-139">Manually allocate buffers for output.</span></span>
-   <span data-ttu-id="aa918-140">Forneça seu próprio relógio.</span><span class="sxs-lookup"><span data-stu-id="aa918-140">Provide your own clock.</span></span>
-   <span data-ttu-id="aa918-141">Recupere o status das operações de arquivo (buffer, download ou salvamento).</span><span class="sxs-lookup"><span data-stu-id="aa918-141">Retrieve the status of file operations (buffering, download, or save).</span></span>
-   <span data-ttu-id="aa918-142">Abra um arquivo usando a interface COM padrão, **IStream**.</span><span class="sxs-lookup"><span data-stu-id="aa918-142">Open a file using the standard COM interface, **IStream**.</span></span>
-   <span data-ttu-id="aa918-143">Buscar pontos específicos em um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="aa918-143">Seek to specific points in an ASF file.</span></span>
-   <span data-ttu-id="aa918-144">Ler dados de perfil do cabeçalho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="aa918-144">Read profile data from the header of the file.</span></span>

<span data-ttu-id="aa918-145">As seções a seguir descrevem o uso do objeto leitor em detalhes.</span><span class="sxs-lookup"><span data-stu-id="aa918-145">The following sections describe the use of the reader object in detail.</span></span>

-   [<span data-ttu-id="aa918-146">Para implementar mensagens de leitor no retorno de chamada OnStatus</span><span class="sxs-lookup"><span data-stu-id="aa918-146">To Implement Reader Messages in the OnStatus Callback</span></span>](to-implement-reader-messages-in-the-onstatus-callback.md)
-   [<span data-ttu-id="aa918-147">Para implementar o retorno de chamada onsample</span><span class="sxs-lookup"><span data-stu-id="aa918-147">To Implement the OnSample Callback</span></span>](to-implement-the-onsample-callback.md)
-   [<span data-ttu-id="aa918-148">Para criar um leitor e abrir um arquivo</span><span class="sxs-lookup"><span data-stu-id="aa918-148">To Create a Reader and Open a File</span></span>](to-create-a-reader-and-open-a-file.md)
-   [<span data-ttu-id="aa918-149">Para recuperar amostras de mídia com o leitor assíncrono</span><span class="sxs-lookup"><span data-stu-id="aa918-149">To Retrieve Media Samples with the Asynchronous Reader</span></span>](to-retrieve-media-samples-with-the-asynchronous-reader.md)
-   [<span data-ttu-id="aa918-150">Para procurar por tempo usando o leitor assíncrono</span><span class="sxs-lookup"><span data-stu-id="aa918-150">To Seek By Time Using the Asynchronous Reader</span></span>](to-seek-by-time-using-the-asynchronous-reader.md)
-   [<span data-ttu-id="aa918-151">Para buscar por número de quadro usando o leitor assíncrono</span><span class="sxs-lookup"><span data-stu-id="aa918-151">To Seek By Frame Number Using the Asynchronous Reader</span></span>](to-seek-by-frame-number-using-the-asynchronous-reader.md)
-   [<span data-ttu-id="aa918-152">Para buscar pelo código de tempo SMPTE usando o leitor assíncrono</span><span class="sxs-lookup"><span data-stu-id="aa918-152">To Seek By SMPTE Time Code Using the Asynchronous Reader</span></span>](to-seek-by-smpte-time-code-using-the-asynchronous-reader.md)
-   [<span data-ttu-id="aa918-153">Para buscar marcadores</span><span class="sxs-lookup"><span data-stu-id="aa918-153">To Seek to Markers</span></span>](to-seek-to-markers.md)
-   [<span data-ttu-id="aa918-154">Para pausar ou parar a reprodução</span><span class="sxs-lookup"><span data-stu-id="aa918-154">To Pause or Stop Playback</span></span>](to-pause-or-stop-playback.md)
-   [<span data-ttu-id="aa918-155">Para obter estatísticas de desempenho do leitor</span><span class="sxs-lookup"><span data-stu-id="aa918-155">To Get Reader Performance Statistics</span></span>](to-get-reader-performance-statistics.md)
-   [<span data-ttu-id="aa918-156">Para usar a seleção de fluxo manual</span><span class="sxs-lookup"><span data-stu-id="aa918-156">To Use Manual Stream Selection</span></span>](to-use-manual-stream-selection.md)
-   [<span data-ttu-id="aa918-157">Para fornecer amostras compactadas com o leitor assíncrono</span><span class="sxs-lookup"><span data-stu-id="aa918-157">To Deliver Compressed Samples with the Asynchronous Reader</span></span>](to-deliver-compressed-samples-with-the-asynchronous-reader.md)

## <a name="related-topics"></a><span data-ttu-id="aa918-158">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa918-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa918-159">**Lendo arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="aa918-159">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="aa918-160">**Objeto de leitor**</span><span class="sxs-lookup"><span data-stu-id="aa918-160">**Reader Object**</span></span>](reader-object.md)
</dt> </dl>

 

 




