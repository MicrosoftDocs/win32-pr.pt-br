---
title: Lendo arquivos com o leitor síncrono
description: Lendo arquivos com o leitor síncrono
ms.assetid: 18c6c0cd-478f-4325-b23e-571c33779a96
keywords:
- SDK do Windows Media Format, lendo arquivos
- SDK do Windows Media Format, leitores síncronos
- ASF (Advanced Systems Format), leitores síncronos
- ASF (formato de sistemas avançados), leitores síncronos
- ASF (Advanced Systems Format), lendo arquivos
- ASF (formato de sistemas avançados), lendo arquivos
- leitores síncronos, interface IWMReaderCallback
- IWMReaderCallback, leitores síncronos
- leitores síncronos, lendo arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893a1bd324cdc91968e423f2084bfdba5ef57c8e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365543"
---
# <a name="reading-files-with-the-synchronous-reader"></a><span data-ttu-id="2d34a-112">Lendo arquivos com o leitor síncrono</span><span class="sxs-lookup"><span data-stu-id="2d34a-112">Reading Files with the Synchronous Reader</span></span>

<span data-ttu-id="2d34a-113">Você pode usar o leitor síncrono para ler um arquivo ASF usando chamadas síncronas em vez dos métodos assíncronos no objeto leitor.</span><span class="sxs-lookup"><span data-stu-id="2d34a-113">You can use the synchronous reader to read an ASF file using synchronous calls instead of the asynchronous methods in the reader object.</span></span> <span data-ttu-id="2d34a-114">O uso de chamadas síncronas reduz o número de threads necessários para ler um arquivo.</span><span class="sxs-lookup"><span data-stu-id="2d34a-114">Using synchronous calls reduces the number of threads required to read a file.</span></span> <span data-ttu-id="2d34a-115">O leitor assíncrono usa vários threads para processar fluxos.</span><span class="sxs-lookup"><span data-stu-id="2d34a-115">The asynchronous reader uses multiple threads for processing streams.</span></span> <span data-ttu-id="2d34a-116">Para arquivos com vários fluxos, o número de threads usados pode se tornar muito grande.</span><span class="sxs-lookup"><span data-stu-id="2d34a-116">For files with multiple streams, the number of threads used can become very large.</span></span> <span data-ttu-id="2d34a-117">O leitor síncrono usa apenas um thread.</span><span class="sxs-lookup"><span data-stu-id="2d34a-117">The synchronous reader uses only one thread.</span></span>

<span data-ttu-id="2d34a-118">O leitor síncrono foi projetado para atender às necessidades de criação de conteúdo e aplicativos de edição de arquivos.</span><span class="sxs-lookup"><span data-stu-id="2d34a-118">The synchronous reader was designed to meet the needs of content creation and file editing applications.</span></span> <span data-ttu-id="2d34a-119">Você pode usar o leitor síncrono para outros aplicativos, mas sua funcionalidade é limitada.</span><span class="sxs-lookup"><span data-stu-id="2d34a-119">You can use the synchronous reader for other applications, but its functionality is limited.</span></span>

<span data-ttu-id="2d34a-120">O leitor síncrono pode abrir arquivos que são locais ou arquivos em uma rede usando o nome do caminho UNC (como " \\ \\ someshare \\ somedirectory \\ somefile. wmv").</span><span class="sxs-lookup"><span data-stu-id="2d34a-120">The synchronous reader can open files that are local, or files on a network using the UNC path name (such as "\\\\someshare\\somedirectory\\somefile.wmv").</span></span> <span data-ttu-id="2d34a-121">Não é possível transmitir arquivos para o leitor síncrono ou abrir arquivos de um local da Internet.</span><span class="sxs-lookup"><span data-stu-id="2d34a-121">You cannot stream files to the synchronous reader, or open files from an Internet location.</span></span> <span data-ttu-id="2d34a-122">O leitor síncrono também fornece suporte para usar a interface com de **IStream** como uma origem.</span><span class="sxs-lookup"><span data-stu-id="2d34a-122">The synchronous reader also provides support for using the **IStream** COM interface as a source.</span></span>

<span data-ttu-id="2d34a-123">O leitor síncrono fornece mais versatilidade para recuperar amostras de um arquivo ASF do que o leitor assíncrono.</span><span class="sxs-lookup"><span data-stu-id="2d34a-123">The synchronous reader provides more versatility for retrieving samples from an ASF file than the asynchronous reader.</span></span> <span data-ttu-id="2d34a-124">O leitor síncrono pode fornecer amostras por número de fluxo, bem como por saída.</span><span class="sxs-lookup"><span data-stu-id="2d34a-124">The synchronous reader can deliver samples by stream number as well as by output.</span></span> <span data-ttu-id="2d34a-125">Exemplos entregues por número de fluxo podem ser compactados ou descompactados.</span><span class="sxs-lookup"><span data-stu-id="2d34a-125">Samples delivered by stream number can be compressed or uncompressed.</span></span> <span data-ttu-id="2d34a-126">O leitor síncrono também pode alternar entre entregas compactadas e não compactadas durante a reprodução; Esse recurso é conhecido como "edição rápida".</span><span class="sxs-lookup"><span data-stu-id="2d34a-126">The synchronous reader can also switch between compressed and uncompressed delivery during playback; this feature is known as "fast editing."</span></span> <span data-ttu-id="2d34a-127">Esse recurso permite que um aplicativo de edição Leia o conteúdo baseado no Windows Media e passe-o diretamente para o gravador até que um quadro desejado seja atingido.</span><span class="sxs-lookup"><span data-stu-id="2d34a-127">This feature enables an editing application to read Windows Media-based content and pass it directly through to the writer until a desired frame is reached.</span></span> <span data-ttu-id="2d34a-128">Nesse ponto, o aplicativo pode instruir o leitor a iniciar o fornecimento de conteúdo descompactado, que o aplicativo pode modificar e passar para o gravador para recompactação.</span><span class="sxs-lookup"><span data-stu-id="2d34a-128">At that point the application can tell the reader to start delivering uncompressed content, which the application can then modify and pass to the writer for recompression.</span></span> <span data-ttu-id="2d34a-129">Quando o aplicativo terminar de modificar os quadros especificados, ele poderá instruir o leitor a começar a entregar quadros compactados novamente.</span><span class="sxs-lookup"><span data-stu-id="2d34a-129">When the application has finished modifying the specified frames, it can tell the reader to start delivering compressed frames again.</span></span>

<span data-ttu-id="2d34a-130">A funcionalidade mais básica do objeto leitor síncrono pode ser dividida nas etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="2d34a-130">The most basic functionality of the synchronous reader object can be broken down into the following steps.</span></span> <span data-ttu-id="2d34a-131">Nestas etapas, "o aplicativo" se refere ao programa que você escreve usando o SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="2d34a-131">In these steps "the application" refers to the program you write using the Windows Media Format SDK.</span></span>

1.  <span data-ttu-id="2d34a-132">O aplicativo passa para o leitor síncrono o nome de um arquivo a ser lido.</span><span class="sxs-lookup"><span data-stu-id="2d34a-132">The application passes to the synchronous reader the name of a file to read.</span></span> <span data-ttu-id="2d34a-133">Quando o leitor síncrono abre o arquivo, ele atribui um número de saída a cada fluxo.</span><span class="sxs-lookup"><span data-stu-id="2d34a-133">When the synchronous reader opens the file, it assigns an output number to each stream.</span></span> <span data-ttu-id="2d34a-134">Se o arquivo usar a exclusão mútua, o leitor atribuirá uma única saída para todos os fluxos mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="2d34a-134">If the file uses mutual exclusion, the reader assigns a single output for all of the mutually exclusive streams.</span></span>
2.  <span data-ttu-id="2d34a-135">O aplicativo obtém informações sobre a configuração das várias saídas do leitor.</span><span class="sxs-lookup"><span data-stu-id="2d34a-135">The application gets information about the configuration of the various outputs from the reader.</span></span> <span data-ttu-id="2d34a-136">As informações coletadas permitirão que o aplicativo processe amostras de mídia corretamente.</span><span class="sxs-lookup"><span data-stu-id="2d34a-136">The information gathered will enable the application to properly render media samples.</span></span>
3.  <span data-ttu-id="2d34a-137">O aplicativo começa a solicitar exemplos, um de cada vez, do leitor síncrono.</span><span class="sxs-lookup"><span data-stu-id="2d34a-137">The application begins requesting samples, one at a time, from the synchronous reader.</span></span> <span data-ttu-id="2d34a-138">O leitor síncrono entrega cada exemplo em um objeto de buffer para o qual ele fornece a interface [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) .</span><span class="sxs-lookup"><span data-stu-id="2d34a-138">The synchronous reader delivers each sample in a buffer object for which it delivers the [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) interface.</span></span>
4.  <span data-ttu-id="2d34a-139">O aplicativo é responsável por renderizar dados depois que eles são entregues pelo leitor.</span><span class="sxs-lookup"><span data-stu-id="2d34a-139">The application is responsible for rendering data after it is delivered by the reader.</span></span> <span data-ttu-id="2d34a-140">O Windows Media Format SDK não fornece nenhuma rotina de renderização.</span><span class="sxs-lookup"><span data-stu-id="2d34a-140">The Windows Media Format SDK does not provide any rendering routines.</span></span> <span data-ttu-id="2d34a-141">Normalmente, os aplicativos usarão outros SDKs para renderizar dados, como o SDK do Microsoft Direct X ou as funções de multimídia do SDK da plataforma Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2d34a-141">Typically, applications will use other SDKs to render data, such as the Microsoft Direct X SDK, or the multimedia functions of the Microsoft Windows Platform SDK.</span></span>

<span data-ttu-id="2d34a-142">Essas etapas são ilustradas no aplicativo de exemplo WMSyncReader.</span><span class="sxs-lookup"><span data-stu-id="2d34a-142">These steps are illustrated in the WMSyncReader sample application.</span></span> <span data-ttu-id="2d34a-143">Para obter mais informações, consulte [aplicativos de exemplo](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="2d34a-143">For more information, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="2d34a-144">O leitor síncrono também dá suporte à funcionalidade mais avançada.</span><span class="sxs-lookup"><span data-stu-id="2d34a-144">The synchronous reader also supports more advanced functionality.</span></span> <span data-ttu-id="2d34a-145">O leitor síncrono permite que você faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="2d34a-145">The synchronous reader enables you to do the following:</span></span>

-   <span data-ttu-id="2d34a-146">Especifique um intervalo de amostras para recuperar por hora ou por número de quadro.</span><span class="sxs-lookup"><span data-stu-id="2d34a-146">Specify a range of samples to retrieve by time or by frame number.</span></span>
-   <span data-ttu-id="2d34a-147">Seleção de fluxo de controle para fluxos mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="2d34a-147">Control stream selection for mutually exclusive streams.</span></span>
-   <span data-ttu-id="2d34a-148">Abra um arquivo usando a interface COM padrão, **IStream**.</span><span class="sxs-lookup"><span data-stu-id="2d34a-148">Open a file using the standard COM interface, **IStream**.</span></span>
-   <span data-ttu-id="2d34a-149">Ler dados de perfil do cabeçalho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2d34a-149">Read profile data from the file header.</span></span>
-   <span data-ttu-id="2d34a-150">Ler metadados do cabeçalho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2d34a-150">Read metadata from the file header.</span></span>
-   <span data-ttu-id="2d34a-151">Alternar entre exemplos de fluxo e saída durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="2d34a-151">Switch between stream and output samples during playback.</span></span>
-   <span data-ttu-id="2d34a-152">Alternar entre amostras de fluxo compactadas e não compactadas durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="2d34a-152">Switch between compressed and uncompressed stream samples during playback.</span></span>

<span data-ttu-id="2d34a-153">As seções a seguir descrevem o uso do objeto leitor síncrono em detalhes.</span><span class="sxs-lookup"><span data-stu-id="2d34a-153">The following sections describe the use of the synchronous reader object in detail.</span></span>

-   [<span data-ttu-id="2d34a-154">Para criar um leitor síncrono e abrir um arquivo</span><span class="sxs-lookup"><span data-stu-id="2d34a-154">To Create a Synchronous Reader and Open a File</span></span>](to-create-a-synchronous-reader-and-open-a-file.md)
-   [<span data-ttu-id="2d34a-155">Para localizar números de fluxo e números de saída</span><span class="sxs-lookup"><span data-stu-id="2d34a-155">To Find Stream Numbers and Output Numbers</span></span>](to-find-stream-numbers-and-output-numbers.md)
-   [<span data-ttu-id="2d34a-156">Para recuperar amostras de mídia com o leitor síncrono</span><span class="sxs-lookup"><span data-stu-id="2d34a-156">To Retrieve Media Samples with the Synchronous Reader</span></span>](to-retrieve-media-samples-with-the-synchronous-reader.md)
-   [<span data-ttu-id="2d34a-157">Para buscar por tempo usando o leitor síncrono</span><span class="sxs-lookup"><span data-stu-id="2d34a-157">To Seek By Time Using the Synchronous Reader</span></span>](to-seek-by-time-using-the-synchronous-reader.md)
-   [<span data-ttu-id="2d34a-158">Para buscar por número de quadro usando o leitor síncrono</span><span class="sxs-lookup"><span data-stu-id="2d34a-158">To Seek By Frame Number Using the Synchronous Reader</span></span>](to-seek-by-frame-number-using-the-synchronous-reader.md)
-   [<span data-ttu-id="2d34a-159">Para buscar pelo código de tempo SMPTE usando o leitor síncrono</span><span class="sxs-lookup"><span data-stu-id="2d34a-159">To Seek By SMPTE Time Code Using the Synchronous Reader</span></span>](to-seek-by-smpte-time-code-using-the-synchronous-reader.md)
-   [<span data-ttu-id="2d34a-160">Para recuperar exemplos de fluxo com o leitor síncrono</span><span class="sxs-lookup"><span data-stu-id="2d34a-160">To Retrieve Stream Samples with the Synchronous Reader</span></span>](to-retrieve-stream-samples-with-the-synchronous-reader.md)
-   [<span data-ttu-id="2d34a-161">Para recuperar amostras compactadas com o leitor síncrono</span><span class="sxs-lookup"><span data-stu-id="2d34a-161">To Retrieve Compressed Samples with the Synchronous Reader</span></span>](to-retrieve-compressed-samples-with-the-synchronous-reader.md)

<span data-ttu-id="2d34a-162">**Código de exemplo**</span><span class="sxs-lookup"><span data-stu-id="2d34a-162">**Example Code**</span></span>

<span data-ttu-id="2d34a-163">O código de exemplo a seguir mostra como ler exemplos de um arquivo ASF usando o leitor síncrono.</span><span class="sxs-lookup"><span data-stu-id="2d34a-163">The following example code shows how to read samples from an ASF file using the synchronous reader.</span></span> <span data-ttu-id="2d34a-164">Especifica por número de quadro um intervalo de amostras a serem entregues.</span><span class="sxs-lookup"><span data-stu-id="2d34a-164">It specifies by frame number a range of samples to deliver.</span></span>


```C++
IWMSyncReader* pSyncReader = NULL;
INSSBuffer*    pMyBuffer   = NULL;

QWORD cnsSampleTime = 0;
QWORD cnsSampleDuration = 0;
DWORD dwFlags = 0;
DWORD dwOutputNumber;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a synchronous reader.
hr = WMCreateSyncReader(NULL, WMT_RIGHT_PLAYBACK, &pSyncReader);

// Open an ASF file.
hr = pSyncReader->Open(L"c:\\somefile.wmv");

// TODO: Identify the properties for each output. This works 
// exactly as it does with the asynchronous reader.

// Specify a playback range from frame number 100 of the video 
// stream to the end of the file. Assume that the video stream 
// is stream number 2.
hr = pSyncReader->SetRangeByFrame(2, 100, 0);

// Loop through all the samples in the specified range.
do
{
   // Get the next sample, regardless of its stream number.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

pSyncReader->Release();
pSyncReader = NULL;

```



## <a name="related-topics"></a><span data-ttu-id="2d34a-165">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2d34a-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d34a-166">**Interface IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="2d34a-166">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="2d34a-167">**Lendo arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="2d34a-167">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="2d34a-168">**Objeto de leitor síncrono**</span><span class="sxs-lookup"><span data-stu-id="2d34a-168">**Synchronous Reader Object**</span></span>](synchronous-reader-object.md)
</dt> </dl>

 

 




