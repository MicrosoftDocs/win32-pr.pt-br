---
title: Transmissão de dados ASF
description: Transmissão de dados ASF
ms.assetid: 1b04f361-8147-4f6a-8c9d-d8eeed28550a
keywords:
- SDK do Windows Media Format, transmitindo dados ASF
- ASF (Advanced Systems Format), dados de difusão
- ASF (formato de sistemas avançados), dados de difusão
- SDK do Windows Media Format, enviando dados do ASF
- ASF (Advanced Systems Format), enviando dados
- ASF (formato de sistemas avançados), enviando dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42339b4a3e60666c1ea0cb69a07dfdc836b19409
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "104007223"
---
# <a name="broadcasting-asf-data"></a><span data-ttu-id="c1393-109">Transmissão de dados ASF</span><span class="sxs-lookup"><span data-stu-id="c1393-109">Broadcasting ASF Data</span></span>

<span data-ttu-id="c1393-110">Este tópico descreve como enviar dados ASF em uma rede usando o protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="c1393-110">This topic describes how to send ASF data across a network using the HTTP protocol.</span></span> <span data-ttu-id="c1393-111">O envio de arquivos por uma rede requer o uso do objeto Writer, portanto, você deve ter uma compreensão geral desse objeto antes de ler este tópico.</span><span class="sxs-lookup"><span data-stu-id="c1393-111">Sending files over a network requires the use of the writer object, so you should have a general understanding of this object before reading this topic.</span></span> <span data-ttu-id="c1393-112">Para obter mais informações, consulte [Writing ASF files](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="c1393-112">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>

<span data-ttu-id="c1393-113">Se você estiver iniciando com dados descompactados, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c1393-113">If you are starting with uncompressed data, do the following:</span></span>

1.  <span data-ttu-id="c1393-114">Crie o objeto gravador chamando a função [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) .</span><span class="sxs-lookup"><span data-stu-id="c1393-114">Create the writer object by calling the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function.</span></span> <span data-ttu-id="c1393-115">Essa função retorna um ponteiro **IWMWriter** .</span><span class="sxs-lookup"><span data-stu-id="c1393-115">This function returns an **IWMWriter** pointer.</span></span>
    ```C++
    IWMWriter *pWriter;
    hr = WMCreateWriter(NULL, &pWriter);
    ```

    

2.  <span data-ttu-id="c1393-116">Crie o objeto de coletor de rede chamando a função [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink) , que retorna um ponteiro **IWMWriterNetworkSink** .</span><span class="sxs-lookup"><span data-stu-id="c1393-116">Create the network sink object by calling the [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink) function, which returns an **IWMWriterNetworkSink** pointer.</span></span>
    ```C++
    IWMWriterNetworkSink *pNetSink;
    hr = WMCreateWriterNetworkSink(&pNetSink);
    ```

    

3.  <span data-ttu-id="c1393-117">Chame [**IWMWriterNetworkSink:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open) no coletor de rede e especifique o número da porta a ser aberta; por exemplo, 8080.</span><span class="sxs-lookup"><span data-stu-id="c1393-117">Call [**IWMWriterNetworkSink::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open) on the network sink and specify the port number to open; for example, 8080.</span></span> <span data-ttu-id="c1393-118">Opcionalmente, chame [**IWMWriterNetworkSink:: GetHostURL**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl) para obter a URL do host.</span><span class="sxs-lookup"><span data-stu-id="c1393-118">Optionally, call [**IWMWriterNetworkSink::GetHostURL**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl) to get the URL of the host.</span></span> <span data-ttu-id="c1393-119">Os clientes acessarão o conteúdo dessa URL.</span><span class="sxs-lookup"><span data-stu-id="c1393-119">Clients will access the content from this URL.</span></span> <span data-ttu-id="c1393-120">Você também pode chamar [**IWMWriterNetworkSink:: SetMaximumClients**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients) para restringir o número de clientes.</span><span class="sxs-lookup"><span data-stu-id="c1393-120">You can also call [**IWMWriterNetworkSink::SetMaximumClients**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients) to restrict the number of clients.</span></span>
    ```C++
    DWORD dwPortNum = 8080;
    hr = pNetSink->Open( &dwPortNum)
    ```

    

4.  <span data-ttu-id="c1393-121">Anexe o coletor de rede ao gravador chamando [**IWMWriterAdvanced:: addsink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) no gravador, com um ponteiro para a interface **IWMWriterNetworkSink** do coletor de rede.</span><span class="sxs-lookup"><span data-stu-id="c1393-121">Attach the network sink to the writer by calling [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) on the writer, with a pointer to the network sink's **IWMWriterNetworkSink** interface.</span></span>
    ```C++
    IWMWriterAdvanced *pWriterAdvanced;
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, ( void** ) pWriterAdvanced );
    if (SUCCEEDED(hr))
    {
        pWriterAdvanced->AddSink(pNetSink);
    }
    ```

    

5.  <span data-ttu-id="c1393-122">Defina o perfil do ASF chamando o método [**IWMWriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) no objeto do gravador, com um ponteiro [**IWMProfile**](iwmprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="c1393-122">Set the ASF profile by calling the [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) method on the writer object, with an [**IWMProfile**](iwmprofile.md) pointer.</span></span> <span data-ttu-id="c1393-123">Para obter informações sobre como criar um perfil, consulte [trabalhando com perfis](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="c1393-123">For information about creating a profile, see [Working with Profiles](working-with-profiles.md).</span></span>
6.  <span data-ttu-id="c1393-124">Opcionalmente, especifique os metadados usando a interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) no gravador.</span><span class="sxs-lookup"><span data-stu-id="c1393-124">Optionally, specify metadata using the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface on the writer.</span></span>
7.  <span data-ttu-id="c1393-125">Chame [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting) no gravador.</span><span class="sxs-lookup"><span data-stu-id="c1393-125">Call [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting) on the writer.</span></span>
    ```C++
    hr = pWriter->BeginWriting();
    ```

    

8.  <span data-ttu-id="c1393-126">Para cada exemplo, chame o método [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) .</span><span class="sxs-lookup"><span data-stu-id="c1393-126">For each sample, call the [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) method.</span></span> <span data-ttu-id="c1393-127">Especifique o número do fluxo, a hora da apresentação, a duração do exemplo e um ponteiro para o buffer de exemplo.</span><span class="sxs-lookup"><span data-stu-id="c1393-127">Specify the stream number, the presentation time, the duration of the sample, and a pointer to the sample buffer.</span></span> <span data-ttu-id="c1393-128">O método **WriteSample** compacta os exemplos.</span><span class="sxs-lookup"><span data-stu-id="c1393-128">The **WriteSample** method compresses the samples.</span></span>
9.  <span data-ttu-id="c1393-129">Quando terminar, chame [**IWMWriter:: redação**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) no gravador.</span><span class="sxs-lookup"><span data-stu-id="c1393-129">When you are done, call [**IWMWriter::EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) on the writer.</span></span>
    ```C++
    hr = pWriter->EndWriting();
    ```

    

10. <span data-ttu-id="c1393-130">Chame [**IWMWriterAdvanced:: RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) no gravador para desanexar o objeto de coletor de rede.</span><span class="sxs-lookup"><span data-stu-id="c1393-130">Call [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) on the writer to detach the network sink object.</span></span>
    ```C++
    hr = pWriterAdvanced->RemoveSink(pNetSink);
    ```

    

11. <span data-ttu-id="c1393-131">Chame [**IWMWriterNetworkSink:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close) no coletor de rede para liberar a porta.</span><span class="sxs-lookup"><span data-stu-id="c1393-131">Call [**IWMWriterNetworkSink::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close) on the network sink to release the port.</span></span>
    ```C++
    hr = pNetSink->Close();
    ```

    

<span data-ttu-id="c1393-132">Outra maneira de transmitir conteúdo ASF por meio de uma rede é lê-lo de um arquivo ASF existente.</span><span class="sxs-lookup"><span data-stu-id="c1393-132">Another way to stream ASF content over a network is to read it from an existing ASF file.</span></span> <span data-ttu-id="c1393-133">O exemplo de WMVNetWrite fornecido no SDK demonstra essa abordagem.</span><span class="sxs-lookup"><span data-stu-id="c1393-133">The WMVNetWrite sample provided in the SDK demonstrates this approach.</span></span> <span data-ttu-id="c1393-134">Além das etapas listadas anteriormente, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c1393-134">In addition to the steps listed previously, do the following:</span></span>

1.  <span data-ttu-id="c1393-135">Crie um objeto leitor e chame o método **Open** com o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="c1393-135">Create a reader object and call the **Open** method with the name of the file.</span></span>
2.  <span data-ttu-id="c1393-136">Chame [**IWMReaderAdvanced:: SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection) no objeto Reader, com o valor **true**.</span><span class="sxs-lookup"><span data-stu-id="c1393-136">Call [**IWMReaderAdvanced::SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection) on the reader object, with the value **TRUE**.</span></span> <span data-ttu-id="c1393-137">Isso permite que o aplicativo Leia cada fluxo no arquivo, incluindo fluxos com exclusão mútua.</span><span class="sxs-lookup"><span data-stu-id="c1393-137">This enables the application to read every stream in the file, including streams with mutual exclusion.</span></span>
3.  <span data-ttu-id="c1393-138">Consulte o leitor para a interface [**IWMProfile**](iwmprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="c1393-138">Query the reader for the [**IWMProfile**](iwmprofile.md) interface.</span></span> <span data-ttu-id="c1393-139">Use esse ponteiro quando você chamar [**IWMWriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) no objeto do gravador (etapa 5 no procedimento anterior).</span><span class="sxs-lookup"><span data-stu-id="c1393-139">Use this pointer when you call [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) on the writer object (step 5 in the previous procedure).</span></span>
4.  <span data-ttu-id="c1393-140">Para cada fluxo definido no perfil, chame [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) para obter o número do fluxo.</span><span class="sxs-lookup"><span data-stu-id="c1393-140">For every stream defined in the profile, call [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) to get the stream number.</span></span> <span data-ttu-id="c1393-141">Passe este número de fluxo para o método [**IWMReaderAdvanced:: SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) do leitor.</span><span class="sxs-lookup"><span data-stu-id="c1393-141">Pass this stream number to the reader's [**IWMReaderAdvanced::SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) method.</span></span> <span data-ttu-id="c1393-142">Esse método informa o leitor para fornecer amostras compactadas, em vez de decodificá-las.</span><span class="sxs-lookup"><span data-stu-id="c1393-142">This method informs the reader to deliver compressed samples, rather than decoding them.</span></span> <span data-ttu-id="c1393-143">Os exemplos serão entregues ao aplicativo por meio do método de retorno de chamada [**IWMReaderCallbackAdvanced:: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1393-143">The samples will be delivered to the application through the application's [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) callback method.</span></span>

    <span data-ttu-id="c1393-144">Você deve obter informações de codec para cada fluxo que ler não compactado e adicioná-lo ao cabeçalho antes da transmissão.</span><span class="sxs-lookup"><span data-stu-id="c1393-144">You must obtain codec information for every stream that you read uncompressed and add it to the header before broadcast.</span></span> <span data-ttu-id="c1393-145">Para obter as informações do codec, chame [**IWMHeaderInfo2:: GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) e [**IWMHeaderInfo2:: GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) para enumerar os codecs associados ao arquivo no leitor.</span><span class="sxs-lookup"><span data-stu-id="c1393-145">To obtain the codec information, call [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) and [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) to enumerate the codecs associated with the file in the reader.</span></span> <span data-ttu-id="c1393-146">Selecione as informações de codec que correspondem à configuração de fluxo.</span><span class="sxs-lookup"><span data-stu-id="c1393-146">Select the codec information that matches the stream configuration.</span></span> <span data-ttu-id="c1393-147">Em seguida, defina as informações do codec no gravador chamando [**IWMHeaderInfo3:: AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passando as informações obtidas do leitor.</span><span class="sxs-lookup"><span data-stu-id="c1393-147">Then set the codec information in the writer by calling [**IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passing the information obtained from the reader.</span></span>

5.  <span data-ttu-id="c1393-148">Depois de definir o perfil no gravador, chame [**IWMWriter:: GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount) no gravador para obter o número de entradas.</span><span class="sxs-lookup"><span data-stu-id="c1393-148">After you set the profile on the writer, call [**IWMWriter::GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount) on the writer to get the number of inputs.</span></span> <span data-ttu-id="c1393-149">Para cada entrada, chame [**IWMWriter:: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) com o valor **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c1393-149">For each input, call [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) with the value **NULL**.</span></span> <span data-ttu-id="c1393-150">Isso indica para o objeto do gravador que o aplicativo fornecerá amostras compactadas, de modo que o gravador não precisa usar nenhum codec para compactar os dados.</span><span class="sxs-lookup"><span data-stu-id="c1393-150">This indicates to the writer object that the application will deliver compressed samples, so the writer does not have to use any codecs to compress the data.</span></span> <span data-ttu-id="c1393-151">Certifique-se de chamar **SetInputProps** antes de chamar **BeginWriting**.</span><span class="sxs-lookup"><span data-stu-id="c1393-151">Make sure to call **SetInputProps** before calling **BeginWriting**.</span></span>
6.  <span data-ttu-id="c1393-152">Opcionalmente, copie os atributos de metadados do leitor para o gravador</span><span class="sxs-lookup"><span data-stu-id="c1393-152">Optionally, copy the metadata attributes from the reader to the writer</span></span>
7.  <span data-ttu-id="c1393-153">Como os exemplos do leitor já estão compactados, use o método [**IWMWriterAdvanced:: WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) para gravar os exemplos, em vez do método **WriteSample** .</span><span class="sxs-lookup"><span data-stu-id="c1393-153">Because the samples from the reader are already compressed, use the [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) method to write the samples, instead of the **WriteSample** method.</span></span> <span data-ttu-id="c1393-154">O método **WriteStreamSample** ignora os procedimentos de compactação usuais do objeto gravador.</span><span class="sxs-lookup"><span data-stu-id="c1393-154">The **WriteStreamSample** method bypasses the writer object's usual compression procedures.</span></span>
8.  <span data-ttu-id="c1393-155">Quando o leitor atinge o final do arquivo, ele envia uma notificação de \_ EOF WMT para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1393-155">When the reader reaches the end of the file, it sends a WMT\_EOF notification to the application.</span></span>

<span data-ttu-id="c1393-156">Além disso, o aplicativo deve orientar o relógio no objeto leitor, para que o leitor receba os dados do arquivo o mais rápido possível.</span><span class="sxs-lookup"><span data-stu-id="c1393-156">In addition, the application should drive the clock on the reader object, so that the reader pulls data from the file as quickly as possible.</span></span> <span data-ttu-id="c1393-157">Para fazer isso, chame o método [**IWMReaderAdvanced:: SetUserProvidedClock**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock) no leitor, com o valor **true**.</span><span class="sxs-lookup"><span data-stu-id="c1393-157">To do this, call the [**IWMReaderAdvanced::SetUserProvidedClock**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock) method on the reader, with the value **TRUE**.</span></span> <span data-ttu-id="c1393-158">Depois que o leitor envia a \_ notificação de WMT iniciado, chame [**IWMReaderAdvanced::D elivertime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime) e especifique o intervalo de tempo que o leitor deve entregar.</span><span class="sxs-lookup"><span data-stu-id="c1393-158">After the reader sends the WMT\_STARTED notification, call [**IWMReaderAdvanced::DeliverTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime) and specify the time interval that the reader should deliver.</span></span> <span data-ttu-id="c1393-159">Depois que o leitor terminar de ler esse intervalo de tempo, ele chamará o método de retorno de chamada [**IWMReaderCallbackAdvanced:: ontime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime) do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1393-159">After the reader is done reading this time interval, it calls the application's [**IWMReaderCallbackAdvanced::OnTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime) callback method.</span></span> <span data-ttu-id="c1393-160">O aplicativo deve chamar o atendimento de **entrega** novamente para ler o próximo intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="c1393-160">The application should call **DeliverTime** again to read the next time interval.</span></span> <span data-ttu-id="c1393-161">Por exemplo, para ler o arquivo em intervalos de um segundo:</span><span class="sxs-lookup"><span data-stu-id="c1393-161">For example, to read from the file in one-second intervals:</span></span>


```C++
// Initial call to DeliverTime.
QWORD m_qwTime = 10000000; // 1 second.
hr = m_pReaderAdvanced->DeliverTime(m_qwTime);

// In the callback:
HRESULT CNetWrite::OnTime(QWORD cnsCurrentTime, void *pvContext)
{
    HRESULT hr = S_OK;
    // Continue calling DeliverTime until the end of the file.
    if(!m_bEOF)
    {
        m_qwTime += 10000000; // 1 second.
        hr = m_pReaderAdvanced->DeliverTime(m_qwTime);
    }
    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="c1393-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c1393-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1393-163">**Enviando dados ASF por meio de uma rede**</span><span class="sxs-lookup"><span data-stu-id="c1393-163">**Sending ASF Data Over a Network**</span></span>](sending-asf-data-over-a-network.md)
</dt> <dt>

[<span data-ttu-id="c1393-164">**Trabalhando com coletores de gravador**</span><span class="sxs-lookup"><span data-stu-id="c1393-164">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




