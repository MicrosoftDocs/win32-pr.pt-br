---
description: Gerando amostras de fluxo de um objeto de dados ASF existente
ms.assetid: eb27f122-d958-495d-98ea-8befd105a9a8
title: Gerando amostras de fluxo de um objeto de dados ASF existente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee612c9352e3295d6b4957922e385de40a9a1fa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089738"
---
# <a name="generating-stream-samples-from-an-existing-asf-data-object"></a><span data-ttu-id="ec5ee-103">Gerando amostras de fluxo de um objeto de dados ASF existente</span><span class="sxs-lookup"><span data-stu-id="ec5ee-103">Generating Stream Samples from an Existing ASF Data Object</span></span>

<span data-ttu-id="ec5ee-104">O objeto *divisor* de ASF é um componente de camada WMContainer que analisa o objeto de dados ASF de um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="ec5ee-104">The ASF *splitter* object is a WMContainer layer component that parses the ASF Data Object of an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="ec5ee-105">Antes de passar pacotes de dados para o separador, o aplicativo deve inicializar, configurar e selecionar fluxos no divisor para prepará-lo para o processo de análise.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-105">Before passing data packets to the splitter, the application must initialize, configure, and select streams on the splitter in order to prepare it for the parsing process.</span></span> <span data-ttu-id="ec5ee-106">Para obter informações, consulte [criando o objeto divisor de ASF](creating-the-asf-splitter-object.md) e [Configurando o objeto divisor de ASF](configuring-the-asf-splitter-object.md).</span><span class="sxs-lookup"><span data-stu-id="ec5ee-106">For information, see [Creating the ASF Splitter Object](creating-the-asf-splitter-object.md) and [Configuring the ASF Splitter Object](configuring-the-asf-splitter-object.md).</span></span>

<span data-ttu-id="ec5ee-107">Os métodos necessários para analisar o objeto de dados ASF são:</span><span class="sxs-lookup"><span data-stu-id="ec5ee-107">The methods required for parsing the ASF Data Object are:</span></span>

-   <span data-ttu-id="ec5ee-108">[**IMFASFSplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) que inicia o processo de análise enviando por push o buffer que contém os pacotes de dados para o divisor.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-108">[**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) that starts the parsing process by pushing the buffer containing data packets to the splitter.</span></span>
-   <span data-ttu-id="ec5ee-109">[**IMFASFSplitter:: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) que coleta amostras de fluxo que foram geradas do buffer passado para o divisor.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-109">[**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) that collects stream samples that were generated from the buffer passed to splitter.</span></span>

## <a name="finding-the-data-offset"></a><span data-ttu-id="ec5ee-110">Localizando o deslocamento de dados</span><span class="sxs-lookup"><span data-stu-id="ec5ee-110">Finding the Data Offset</span></span>

<span data-ttu-id="ec5ee-111">Antes de iniciar o processo de análise, o aplicativo deve localizar o objeto de dados no arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-111">Before starting the parsing process, the application must locate the Data Object within the ASF file.</span></span> <span data-ttu-id="ec5ee-112">Há duas maneiras de obter o deslocamento do objeto de dados a partir do início do arquivo:</span><span class="sxs-lookup"><span data-stu-id="ec5ee-112">There are two ways to get the offset of the Data Object from the start of the file:</span></span>

-   <span data-ttu-id="ec5ee-113">Antes de inicializar o objeto ContentInfo, você pode chamar o método [**IMFASFContentInfo:: Getheaders**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) .</span><span class="sxs-lookup"><span data-stu-id="ec5ee-113">Before you have initialized the ContentInfo object, you can call the [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) method.</span></span> <span data-ttu-id="ec5ee-114">Esse método requer um buffer que contém os primeiros 30 bytes do cabeçalho ASF.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-114">This method requires a buffer that contains the first 30 bytes of the ASF header.</span></span> <span data-ttu-id="ec5ee-115">Ele retorna o tamanho do cabeçalho inteiro que indica o deslocamento para o primeiro pacote de dados.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-115">It returns the size of the entire header that indicates the offset to the first data packet.</span></span> <span data-ttu-id="ec5ee-116">Esse valor também inclui o tamanho do cabeçalho do objeto de dados de 50 bytes.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-116">This value also includes the Data Object header size of 50 bytes.</span></span>
-   <span data-ttu-id="ec5ee-117">Depois de inicializar o objeto ContentInfo, você pode obter o descritor de apresentação chamando [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)e consultando o descritor de apresentação para o atributo de [**deslocamento de início de \_ dados MF PD \_ ASF \_ \_ \_**](mf-pd-asf-data-start-offset-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="ec5ee-117">After you have initialized the ContentInfo object, you can get the presentation descriptor by calling [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor), and then querying the presentation descriptor for the [**MF\_PD\_ASF\_DATA\_START\_OFFSET**](mf-pd-asf-data-start-offset-attribute.md) attribute.</span></span> <span data-ttu-id="ec5ee-118">O valor desse atributo é o tamanho do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-118">The value of this attribute is the header size.</span></span>
    > [!Note]  
    > <span data-ttu-id="ec5ee-119">O atributo de [**\_ comprimento de dados MF PD \_ ASF \_ \_**](mf-pd-asf-data-length-attribute.md) no descritor de apresentação especifica o comprimento do objeto de dados ASF.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-119">The [**MF\_PD\_ASF\_DATA\_LENGTH**](mf-pd-asf-data-length-attribute.md) attribute on the presentation descriptor specifies the length of the ASF Data Object.</span></span>

     

<span data-ttu-id="ec5ee-120">Em ambos os casos, o valor retornado é o tamanho do objeto de cabeçalho mais o tamanho da seção de cabeçalho do objeto de dados.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-120">In both cases, the returned value is the size of the Header Object plus the size of the header section of the Data Object.</span></span> <span data-ttu-id="ec5ee-121">Portanto, o valor resultante é o deslocamento para o início dos pacotes de dados no objeto de dados ASF.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-121">Therefore, the resulting value is the offset to the start of the data packets in the ASF Data Object.</span></span> <span data-ttu-id="ec5ee-122">Quando você começa a enviar dados para o separador, os dados devem começar com esse deslocamento desde o início do arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-122">When you begin sending data to the splitter, the data must start at this offset from the beginning of the ASF file.</span></span>

<span data-ttu-id="ec5ee-123">O valor de deslocamento é passado como um parâmetro para **ParseData** que inicia o processo de análise.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-123">The offset value is passed as a parameter to **ParseData** that starts the parsing process.</span></span>

<span data-ttu-id="ec5ee-124">O objeto de dados é dividido em pacotes de dados.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-124">The Data Object is divided into data packets.</span></span> <span data-ttu-id="ec5ee-125">Cada pacote de dados contém um cabeçalho de pacote de dados que fornece informações de análise de pacotes e os dados de carga — os dados de mídia digital reais.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-125">Each data packet contains a data packet header that provides packet parsing information and the payload data—the actual digital media data.</span></span> <span data-ttu-id="ec5ee-126">Em um cenário de busca, o aplicativo pode querer que o divisor inicie a análise em um pacote de dados específico.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-126">In a seeking scenario, the application might want the splitter to start parsing at a particular data packet.</span></span> <span data-ttu-id="ec5ee-127">Para fazer isso, você pode usar o indexador ASF é usado para recuperar o deslocamento.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-127">To do this, you can use the ASF Indexer is used to retrieve the offset.</span></span> <span data-ttu-id="ec5ee-128">O indexador retorna um valor de deslocamento que começa no limite do pacote.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-128">The indexer returns an offset value that starts at the packet boundary.</span></span> <span data-ttu-id="ec5ee-129">Se você não estiver usando o indexador, verifique se o deslocamento começa no início do cabeçalho do pacote de dados.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-129">If you are not using the indexer, make sure that the offset starts at the start of the data packet header.</span></span> <span data-ttu-id="ec5ee-130">Se um deslocamento inválido for passado para o separador, como o valor não aponta para o limite do pacote, as chamadas **ParseHeader** e **GetNextSample** são bem sucedidos, mas **GetNextSample** não recupera quaisquer amostras e **NULL** é recebido no parâmetro *pSample* .</span><span class="sxs-lookup"><span data-stu-id="ec5ee-130">If an invalid offset is passed to the splitter, such as the value does not point at the packet boundary, **ParseHeader** and **GetNextSample** calls succeed but **GetNextSample** does not retrieve any samples and **NULL** is received in the *pSample* parameter.</span></span>

<span data-ttu-id="ec5ee-131">Se o divisor estiver configurado para analisar na direção inversa, o divisor sempre iniciará a análise no final do buffer de mídia que é passado para **ParseData**.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-131">If the splitter is configured to parse in the reverse direction, then the splitter always starts parsing at the end of the media buffer that is passed to **ParseData**.</span></span> <span data-ttu-id="ec5ee-132">Portanto, para a análise reversa na chamada para **ParseData**, passe o deslocamento no parâmetro *cbLength* , que especifica o comprimento dos dados e defina *cbBufferOffset* como zero.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-132">Therefore, for reverse parsing in the call to **ParseData**, pass the offset in the *cbLength* parameter, which specifies the length of the data and set *cbBufferOffset* to zero.</span></span>

## <a name="generating-samples-for-asf-data-packets"></a><span data-ttu-id="ec5ee-133">Gerando amostras para pacotes de dados ASF</span><span class="sxs-lookup"><span data-stu-id="ec5ee-133">Generating Samples for ASF Data Packets</span></span>

<span data-ttu-id="ec5ee-134">Um aplicativo inicia o processo de análise passando os pacotes de dados para o divisor.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-134">An application starts the parsing process by passing the data packets to the splitter.</span></span> <span data-ttu-id="ec5ee-135">A entrada para o separador é uma série de buffers de mídia que contêm todo ou fragmentos do objeto de dados.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-135">The input to the splitter is a series of media buffers that contain the entire or fragments of the Data Object.</span></span> <span data-ttu-id="ec5ee-136">A saída do divisor é uma série de amostras de mídia que contêm os dados do pacote.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-136">The output from the splitter is a series of media samples that contain the packet data.</span></span>

<span data-ttu-id="ec5ee-137">Para passar dados de entrada para o separador, crie um buffer de mídia e preencha-o com dados da seção objeto de dados do arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-137">To pass input data to the splitter, create a media buffer and fill it with data from the Data Object section of the ASF file.</span></span> <span data-ttu-id="ec5ee-138">(Para obter mais informações sobre buffers de mídia, consulte [buffers de mídia](media-buffers.md).) Em seguida, passe o buffer de mídia para o método [**IMFASFSplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) .</span><span class="sxs-lookup"><span data-stu-id="ec5ee-138">(For more information about media buffers, see [Media Buffers](media-buffers.md).) Then, pass the media buffer to the [**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) method.</span></span> <span data-ttu-id="ec5ee-139">Você também pode especificar:</span><span class="sxs-lookup"><span data-stu-id="ec5ee-139">You can also specify:</span></span>

-   <span data-ttu-id="ec5ee-140">O deslocamento no buffer em que o divisor deve iniciar a análise.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-140">The offset into the buffer where the splitter should start parsing.</span></span> <span data-ttu-id="ec5ee-141">Se o deslocamento for zero, a análise começará no início do buffer.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-141">If the offset is zero, parsing begins at the start of the buffer.</span></span> <span data-ttu-id="ec5ee-142">Para obter informações sobre como definir o deslocamento de dados, consulte a seção "Localizando o deslocamento de dados" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-142">For information about setting the data offset, see the "Finding the Data Offset" section in this topic.</span></span>
-   <span data-ttu-id="ec5ee-143">A quantidade de dados a ser analisada.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-143">The amount of data to parse.</span></span> <span data-ttu-id="ec5ee-144">Se esse valor for zero, o separador analisa até atingir o final do buffer, conforme especificado pelo método [**IMFMediaBuffer:: GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) .</span><span class="sxs-lookup"><span data-stu-id="ec5ee-144">If this value is zero, the splitter parses until it reaches the end of the buffer, as specified by the [**IMFMediaBuffer::GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) method.</span></span>

<span data-ttu-id="ec5ee-145">O divisor gera amostras de mídia referenciando os dados nos buffers de mídia.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-145">The splitter generates media samples by referencing the data in the media buffers.</span></span> <span data-ttu-id="ec5ee-146">O cliente pode recuperar os exemplos de saída chamando [**IMFASFSplitter:: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) em um loop até que não haja mais dados a serem analisados.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-146">The client can retrieve the output samples by calling [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in a loop until there is no more data to parse.</span></span> <span data-ttu-id="ec5ee-147">Se **GetNextSample** retornar o \_ sinalizador ASF STATUSFLAGS \_ incompleto no parâmetro *pdwStatusFlags* , significa que há mais exemplos a serem recuperados e o aplicativo pode chamar **GetNextSample** novamente.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-147">If **GetNextSample** returns the ASF\_STATUSFLAGS\_INCOMPLETE flag in the *pdwStatusFlags* parameter, it means there are more samples to retrieve, and the application can call **GetNextSample** again.</span></span> <span data-ttu-id="ec5ee-148">Caso contrário, chame **ParseData** para passar mais dados para o divisor.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-148">Otherwise, call **ParseData** to pass more data to the splitter.</span></span> <span data-ttu-id="ec5ee-149">Para os exemplos gerados, o divisor define as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="ec5ee-149">For the generated samples, the splitter sets the following information:</span></span>

-   <span data-ttu-id="ec5ee-150">O divisor define um carimbo de data/hora em todos os exemplos que ele gera.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-150">The splitter sets a time stamp on all the samples that it generates.</span></span> <span data-ttu-id="ec5ee-151">O tempo de amostra representa a hora da apresentação e não inclui o tempo de preversão.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-151">The sample time represents the presentation time and does not include the preroll time.</span></span> <span data-ttu-id="ec5ee-152">O aplicativo pode chamar [**IMFSample:: Getsampletime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) para obter o tempo de apresentação, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-152">The application can call [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) to get the presentation time, in 100-nanosecond units.</span></span>
-   <span data-ttu-id="ec5ee-153">Se ocorrer uma interrupção durante a geração de amostra, o divisor definirá o atributo de [**\_ descontinuidade MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) no primeiro exemplo após a descontinuidade.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-153">If a break occurs during sample generation, the splitter sets the [**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute on the first sample after the discontinuity.</span></span> <span data-ttu-id="ec5ee-154">Descontinuidades geralmente são causados por pacotes descartados em uma conexão de rede, dados de arquivo corrompidos ou o divisor alternando de um fluxo de origem para outro.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-154">Discontinuities are usually caused by dropped packets on a network connection, corrupt file data, or the splitter switching from one source stream to another.</span></span>
-   <span data-ttu-id="ec5ee-155">Para vídeo, o divisor verifica se o exemplo contém um quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-155">For video, the splitter checks whether the sample contains a key frame.</span></span> <span data-ttu-id="ec5ee-156">Se tiver, o divisor definirá o atributo [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) no exemplo.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-156">If it does, the splitter sets the [**MFSampleExtension\_CleanPoint**](mfsampleextension-cleanpoint-attribute.md) attribute on the sample.</span></span>

<span data-ttu-id="ec5ee-157">Se o divisor estiver analisando pacotes de dados que são recebidos de um servidor de mídia, é possível que o tamanho do pacote seja variável.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-157">If the splitter is parsing data packets that are received from a media server, it is possible that the packet length is variable.</span></span> <span data-ttu-id="ec5ee-158">Nesse caso, o cliente deve chamar **ParseData** para cada pacote e definir o atributo [**de \_ \_ limite de pacote MFASFSPLITTER**](mfasfsplitter-packet-boundary-attribute.md) em cada buffer que é enviado ao divisor.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-158">In this case, the client must call **ParseData** for each packet and set the [**MFASFSPLITTER\_PACKET\_BOUNDARY**](mfasfsplitter-packet-boundary-attribute.md) attribute on each buffer that is sent to the splitter.</span></span> <span data-ttu-id="ec5ee-159">Esse atributo indica ao divisor se o buffer de mídia contém o início de um pacote ASF.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-159">This attribute indicates to the splitter whether the media buffer contains the start of an ASF packet.</span></span> <span data-ttu-id="ec5ee-160">Defina o atributo como **true** se o buffer contiver o início de um novo pacote.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-160">Set the attribute to **TRUE** if the buffer contains the start of a new packet.</span></span> <span data-ttu-id="ec5ee-161">Se o buffer contiver uma continuação do pacote anterior, defina o atributo como **false**.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-161">If the buffer contains a continuation of the previous packet, set the attribute to **FALSE**.</span></span> <span data-ttu-id="ec5ee-162">Os buffers não podem abranger vários pacotes.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-162">The buffers cannot span multiple packets.</span></span>

<span data-ttu-id="ec5ee-163">Antes de passar novos buffers de mídia para o divisor, o aplicativo deve chamar [**IMFASFSplitter:: flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-flush).</span><span class="sxs-lookup"><span data-stu-id="ec5ee-163">Before passing new media buffers to the splitter, the application must call [**IMFASFSplitter::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-flush).</span></span> <span data-ttu-id="ec5ee-164">Esse método redefine o divisor e limpa qualquer quadro parcial que esteja aguardando para ser concluído.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-164">This method resets the splitter and clears any partial frame that is waiting to be completed.</span></span> <span data-ttu-id="ec5ee-165">Isso é útil em um cenário de busca em que o deslocamento está em um local diferente.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-165">This is useful in a seeking scenario where the offset is at a different location.</span></span>

### <a name="example"></a><span data-ttu-id="ec5ee-166">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ec5ee-166">Example</span></span>

<span data-ttu-id="ec5ee-167">O exemplo de código a seguir mostra como analisar pacotes de dados.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-167">The following code example shows how to parse data packets.</span></span> <span data-ttu-id="ec5ee-168">Este exemplo analisa desde o início do objeto de dados até o final do fluxo e exibe informações sobre os exemplos que contêm quadros-chave.</span><span class="sxs-lookup"><span data-stu-id="ec5ee-168">This example parses from the beginning of the Data Object to the end of the stream and displays information about the samples that contain key frames.</span></span> <span data-ttu-id="ec5ee-169">Para obter um exemplo completo que usa esse código, consulte [tutorial: lendo um arquivo ASF](tutorial--reading-an-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="ec5ee-169">For a complete example that uses this code, see [Tutorial: Reading an ASF File](tutorial--reading-an-asf-file.md).</span></span>


```C++
// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="ec5ee-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ec5ee-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec5ee-171">Divisor de ASF</span><span class="sxs-lookup"><span data-stu-id="ec5ee-171">ASF Splitter</span></span>](asf-splitter.md)
</dt> </dl>

 

 



