---
description: O coletor de arquivos ASF é uma implementação de IMFMediaSink fornecida pelo Media Foundation que um aplicativo pode usar para arquivar dados de mídia ASF em um arquivo. Para obter informações sobre o modelo de objeto de coletor de mídia ASF e uso geral, consulte coletores de mídia ASF.
ms.assetid: 21cbde27-a2ca-4298-9197-43bcaf05588d
title: Adicionando informações de fluxo ao coletor de arquivo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e08c6997d9c77836f379d4ca7b75720ddea245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814505"
---
# <a name="adding-stream-information-to-the-asf-file-sink"></a><span data-ttu-id="a4759-104">Adicionando informações de fluxo ao coletor de arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="a4759-104">Adding Stream Information to the ASF File Sink</span></span>

<span data-ttu-id="a4759-105">O coletor de arquivos ASF é uma implementação de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fornecida pelo Media Foundation que um aplicativo pode usar para arquivar dados de mídia ASF em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a4759-105">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span> <span data-ttu-id="a4759-106">Para obter informações sobre o modelo de objeto do coletor de mídia ASF e o uso geral, consulte [coletores de mídia ASF](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="a4759-106">For information about ASF Media Sinks' object model and general usage, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

<span data-ttu-id="a4759-107">Depois de instanciar o coletor de arquivos, ele deve ser configurado antes da criação da topologia.</span><span class="sxs-lookup"><span data-stu-id="a4759-107">After instantiating the file sink, it must be configured before building the topology.</span></span> <span data-ttu-id="a4759-108">O coletor de arquivos precisa saber sobre os fluxos no arquivo de saída, as informações do modo de codificação e os metadados.</span><span class="sxs-lookup"><span data-stu-id="a4759-108">The file sink needs to know about the streams in the output file, the encoding mode information, and the metadata.</span></span> <span data-ttu-id="a4759-109">Este tópico descreve o processo de adição de fluxo no coletor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a4759-109">This topic describes the process of adding stream in the file sink.</span></span>

-   [<span data-ttu-id="a4759-110">Adicionando fluxos no coletor de arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="a4759-110">Adding Streams in the ASF File Sink</span></span>](#adding-streams-in-the-asf-file-sink)
-   [<span data-ttu-id="a4759-111">Enumerando coletores de fluxo</span><span class="sxs-lookup"><span data-stu-id="a4759-111">Enumerating Stream Sinks</span></span>](#enumerating-stream-sinks)
-   [<span data-ttu-id="a4759-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a4759-112">Related topics</span></span>](#related-topics)

## <a name="adding-streams-in-the-asf-file-sink"></a><span data-ttu-id="a4759-113">Adicionando fluxos no coletor de arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="a4759-113">Adding Streams in the ASF File Sink</span></span>

<span data-ttu-id="a4759-114">O coletor de arquivos deve conhecer os fluxos de saída e suas propriedades para que possa gerar amostras de saída de forma adequada e adicioná-las ao arquivo ASF de saída.</span><span class="sxs-lookup"><span data-stu-id="a4759-114">The file sink must know of the output streams and their properties so that it can generate output samples accordingly and add them to the output ASF file.</span></span> <span data-ttu-id="a4759-115">Essas configurações são gravadas no objeto de cabeçalho ASF final.</span><span class="sxs-lookup"><span data-stu-id="a4759-115">These settings are written to the final ASF Header Object.</span></span>

<span data-ttu-id="a4759-116">Para definir informações de fluxo, você deve ter uma referência ao objeto ASF ContentInfo do coletor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a4759-116">To set stream information, you must have a reference to the file sink's ASF ContentInfo object.</span></span> <span data-ttu-id="a4759-117">Para obter informações, consulte [criando o coletor de arquivo ASF](creating-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="a4759-117">For information, see [Creating the ASF File Sink](creating-the-asf-file-sink.md).</span></span>

<span data-ttu-id="a4759-118">O procedimento a seguir resume as etapas gerais para configurar o Stream usando o objeto de perfil ASF.</span><span class="sxs-lookup"><span data-stu-id="a4759-118">The following procedure summarizes the general steps for configuring stream by using the ASF profile object.</span></span>

<span data-ttu-id="a4759-119">**Para configurar as informações de fluxo no coletor de arquivo ASF**</span><span class="sxs-lookup"><span data-stu-id="a4759-119">**To configure stream information in the ASF file sink**</span></span>

1.  <span data-ttu-id="a4759-120">Crie um objeto de perfil ASF chamando [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile).</span><span class="sxs-lookup"><span data-stu-id="a4759-120">Create an ASF profile object by calling [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile).</span></span>
2.  <span data-ttu-id="a4759-121">Para cada fluxo no arquivo de saída, crie um tipo de mídia para o fluxo de destino a ser adicionado no coletor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a4759-121">For each stream in the output file, create a media type for the target stream to be added in the file sink.</span></span> <span data-ttu-id="a4759-122">O tipo de mídia deve ser compatível com os tipos de saída com suporte dos codificadores de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="a4759-122">The media type must be compatible with the output types supported by the Windows Media encoders.</span></span>

    <span data-ttu-id="a4759-123">Para obter informações sobre como adicionar fluxos de áudio ao perfil, consulte Criando fluxos de áudio para codificação ASF.</span><span class="sxs-lookup"><span data-stu-id="a4759-123">For information about adding audio streams to the profile, see Creating Audio Streams for ASF Encoding.</span></span>

    <span data-ttu-id="a4759-124">Para obter informações sobre como adicionar fluxos de vídeo ao perfil, consulte Criando fluxos de vídeo para codificação ASF.</span><span class="sxs-lookup"><span data-stu-id="a4759-124">For information about adding video streams to the profile, see Creating Video Streams for ASF Encoding.</span></span>

3.  <span data-ttu-id="a4759-125">Crie fluxos com base nos tipos de mídia criados na etapa 2 chamando [**IMFASFProfile:: CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).</span><span class="sxs-lookup"><span data-stu-id="a4759-125">Create streams based on the media types created in step 2 by calling [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).</span></span>
4.  <span data-ttu-id="a4759-126">Atribua um número de fluxo para o fluxo recém-criado chamando o ponteiro de interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) recebido na etapa 3.</span><span class="sxs-lookup"><span data-stu-id="a4759-126">Assign a stream number for the newly created stream by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface pointer received in step 3.</span></span>
5.  <span data-ttu-id="a4759-127">Opcionalmente, configure o fluxo com as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="a4759-127">Optionally configure the stream with the following information:</span></span>
    -   <span data-ttu-id="a4759-128">Parâmetros de Bucket vazado definindo os atributos: [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) ou [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="a4759-128">Leaky bucket parameters by setting the attributes: [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) or [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)</span></span>
    -   <span data-ttu-id="a4759-129">Extensão de carga, exclusão mútua chamando métodos [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="a4759-129">Payload extension, mutual exclusion by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) methods.</span></span>
6.  <span data-ttu-id="a4759-130">Opcionalmente, defina o tamanho do pacote de dados para o perfil definindo os atributos [**MF \_ ASFPROFILE \_ MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) e [**MF \_ ASFPROFILE \_ MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="a4759-130">Optionally set data packet size for the profile by setting [**MF\_ASFPROFILE\_MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) and [**MF\_ASFPROFILE\_MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) attributes.</span></span> <span data-ttu-id="a4759-131">O perfil ASF expõe a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , à qual um aplicativo pode obter referência chamando **IMFASFProfile:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="a4759-131">The ASF profile exposes the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface, which an application can get reference to by calling **IMFASFProfile::QueryInterface**.</span></span>
7.  <span data-ttu-id="a4759-132">Defina as informações de codificação para o fluxo no coletor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a4759-132">Set encoding information for the stream in the file sink.</span></span> <span data-ttu-id="a4759-133">Discutido na [configuração de propriedades no coletor de arquivos](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="a4759-133">Discussed in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>
8.  <span data-ttu-id="a4759-134">Adicione o fluxo ao perfil chamando [**IMFASFProfile:: SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream).</span><span class="sxs-lookup"><span data-stu-id="a4759-134">Add the stream to the profile by calling [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream).</span></span>
9.  <span data-ttu-id="a4759-135">Associe o perfil ao objeto ContentInfo chamando [**IMFASFContentInfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span><span class="sxs-lookup"><span data-stu-id="a4759-135">Associate the profile with the ContentInfo object by calling [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span></span>

<span data-ttu-id="a4759-136">Para modificar um fluxo existente, o aplicativo pode obter uma referência à interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) do fluxo e reconfigurá-lo de acordo com os requisitos.</span><span class="sxs-lookup"><span data-stu-id="a4759-136">To modify an existing stream, the application can get a reference to the stream's [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface and reconfigure it according to the requirements.</span></span> <span data-ttu-id="a4759-137">Para adicionar ou remover fluxos, o aplicativo deve chamar [**IMFASFProfile:: RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream).</span><span class="sxs-lookup"><span data-stu-id="a4759-137">To add or remove streams, the application must call [**IMFASFProfile::RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream).</span></span> <span data-ttu-id="a4759-138">Para aplicar essas alterações, as modificações ou a remoção do fluxo, você deve definir o perfil novamente no objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="a4759-138">To apply these changes, stream modifications or removal, you must set the profile again in the ContentInfo object.</span></span> <span data-ttu-id="a4759-139">Isso substitui o perfil existente que já está associado ao objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="a4759-139">This overwrites the existing profile that is already associated with the ContentInfo object.</span></span>


```C++
//-------------------------------------------------------------------
//  CreateVideoStream
//  Create an video stream and add it to the profile.
//
//  pProfile: A pointer to the ASF profile.
//  wStreamNumber: Stream number to assign for the new stream.
//    pType: A pointer to the source's video media type.
//-------------------------------------------------------------------

HRESULT CreateVideoStream(IMFASFProfile* pProfile, WORD wStreamNumber, IMFMediaType* pType)
{
    if (!pProfile)
    {
        return E_INVALIDARG;
    }
    if (wStreamNumber < 1 || wStreamNumber > 127 )
    {
        return MF_E_INVALIDSTREAMNUMBER;
    }

    HRESULT hr = S_OK;

    
    IMFMediaType* pVideoType = NULL;
    IMFASFStreamConfig* pVideoStream = NULL;

    UINT32 dwBitRate = 0;
        
    //Create a new video type from the source type
    hr = CreateCompressedVideoType(pType, &pVideoType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create a new stream with the video type
    hr = pProfile->CreateStream(pVideoType, &pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }
    

    //Set a valid stream number
    hr = pVideoStream->SetStreamNumber(wStreamNumber);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the stream to the profile
    hr = pProfile->SetStream(pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }

    wprintf_s(L"Video Stream created. Stream Number: %d .\n", wStreamNumber);

done:

    SafeRelease(&pVideoStream);
    SafeRelease(&pVideoType);

    return hr;
}
```



## <a name="enumerating-stream-sinks"></a><span data-ttu-id="a4759-140">Enumerando coletores de fluxo</span><span class="sxs-lookup"><span data-stu-id="a4759-140">Enumerating Stream Sinks</span></span>

<span data-ttu-id="a4759-141">Para cada fluxo no perfil do qual o objeto ContentInfo está ciente, o coletor de arquivo ASF cria e adiciona um coletor de fluxo que contém todas as propriedades do fluxo codificado.</span><span class="sxs-lookup"><span data-stu-id="a4759-141">For each stream in the profile that the ContentInfo object is aware of, the ASF file sink creates and adds a stream sink that contains all the properties of the encoded stream.</span></span> <span data-ttu-id="a4759-142">O coletor de arquivos ASF foi projetado para conter fluxos fixos.</span><span class="sxs-lookup"><span data-stu-id="a4759-142">The ASF file sink is designed to contain fixed streams.</span></span> <span data-ttu-id="a4759-143">Isso significa que você não pode adicionar ou remover fluxos chamando [**IMFMediaSink:: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) ou [**IMFMediaSink:: RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink).</span><span class="sxs-lookup"><span data-stu-id="a4759-143">This means that you cannot add or remove streams by calling [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) or [**IMFMediaSink::RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink).</span></span> <span data-ttu-id="a4759-144">Essas chamadas no coletor de arquivos falham com o \_ \_ código de \_ erro fixo MF E STREAMSINKS.</span><span class="sxs-lookup"><span data-stu-id="a4759-144">These calls on the file sink fail with the MF\_E\_STREAMSINKS\_FIXED error code.</span></span> <span data-ttu-id="a4759-145">Adicionar ou remover fluxos no perfil não adiciona ou remove automaticamente os coletores de fluxo no coletor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a4759-145">Adding or removing streams in the profile does not automatically add or remove the stream sinks in the file sink.</span></span> <span data-ttu-id="a4759-146">Você deve descartar a instância existente do arquivo e recriá-la com novas informações de fluxo se os fluxos no perfil tiverem sido alterados.</span><span class="sxs-lookup"><span data-stu-id="a4759-146">You must discard the existing instance of the file and recreate it with new stream information if your streams in the profile have changed.</span></span>

<span data-ttu-id="a4759-147">O procedimento a seguir resume as etapas gerais para enumerar coletores de fluxo no coletor de arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="a4759-147">The following procedure summarizes the general steps for enumerating stream sinks in the ASF file sink.</span></span>

<span data-ttu-id="a4759-148">**Para enumerar coletores de fluxo**</span><span class="sxs-lookup"><span data-stu-id="a4759-148">**To enumerate stream sinks**</span></span>

1.  <span data-ttu-id="a4759-149">Chame [**IMFMediaSink:: GetStreamSinkCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) para obter o número total de coletores de fluxo no coletor de arquivo asf.</span><span class="sxs-lookup"><span data-stu-id="a4759-149">Call [**IMFMediaSink::GetStreamSinkCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) to get the total number of stream sinks in the ASF file sink.</span></span>
2.  <span data-ttu-id="a4759-150">O loop pelos coletores de fluxo ang Obtém uma referência à interface [**GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) do coletor de fluxo.</span><span class="sxs-lookup"><span data-stu-id="a4759-150">Loop through the stream sinks ang get a reference to the stream sink's [**GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) interface.</span></span>

    <span data-ttu-id="a4759-151">– ou –</span><span class="sxs-lookup"><span data-stu-id="a4759-151">-or-</span></span>

    <span data-ttu-id="a4759-152">Chame [**IMFMediaSink:: GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) para obter o coletor de fluxo especificando o número do fluxo.</span><span class="sxs-lookup"><span data-stu-id="a4759-152">Call [**IMFMediaSink::GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) to get the stream sink by specifying the stream number.</span></span> <span data-ttu-id="a4759-153">Cada coletor de fluxo é identificado com o número de fluxo definido durante a criação do fluxo no perfil.</span><span class="sxs-lookup"><span data-stu-id="a4759-153">Each stream sink is identified with the stream number you set while creating the stream in the profile.</span></span>

<span data-ttu-id="a4759-154">Se você estiver criando uma topologia parcial para codificar um arquivo de mídia, deverá adicionar o coletor de arquivo à topologia como um nó de topologia de saída.</span><span class="sxs-lookup"><span data-stu-id="a4759-154">If you are building a partial topology for encoding a media file, you must add the file sink to the topology as an output topology node.</span></span> <span data-ttu-id="a4759-155">Você pode fazer isso especificando cada coletor de fluxo no coletor de arquivos ou definindo o objeto de ativação do coletor de arquivos e os identificadores do coletor de fluxo.</span><span class="sxs-lookup"><span data-stu-id="a4759-155">You can do so either by specifying each steam sink in the file sink or by setting the file sink activation object and the stream sink identifiers.</span></span> <span data-ttu-id="a4759-156">Para obter mais informações e um exemplo de código, consulte [criando nós de saída](creating-output-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="a4759-156">For more information and code example, see [Creating Output Nodes](creating-output-nodes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4759-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a4759-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4759-158">Coletores de mídia ASF</span><span class="sxs-lookup"><span data-stu-id="a4759-158">ASF Media Sinks</span></span>](asf-media-sinks.md)
</dt> <dt>

[<span data-ttu-id="a4759-159">Suporte a ASF no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a4759-159">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



