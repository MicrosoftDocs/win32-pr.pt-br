---
description: Configurar perfis e outras propriedades de arquivo ASF
ms.assetid: c43df556-9d8a-4010-9ed6-f84d8ac6d9bc
title: Configurar perfis e outras propriedades de arquivo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e26dcbb49cb5ff8309dccafc3f1d8d66397871
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370255"
---
# <a name="configuring-profiles-and-other-asf-file-properties"></a><span data-ttu-id="00c56-103">Configurar perfis e outras propriedades de arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="00c56-103">Configuring Profiles and Other ASF File Properties</span></span>

<span data-ttu-id="00c56-104">Os itens a seguir descrevem como executar várias tarefas relacionadas à criação de arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="00c56-104">The following items describe how to perform various tasks related to the creation of ASF files.</span></span> <span data-ttu-id="00c56-105">Algumas das interfaces mencionadas neste tópico estão documentadas na documentação do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="00c56-105">Some of the interfaces mentioned in this topic are documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="00c56-106">Criando um perfil</span><span class="sxs-lookup"><span data-stu-id="00c56-106">Creating a Profile</span></span>

<span data-ttu-id="00c56-107">Os perfis ASF são discutidos em detalhes no SDK do Windows Media Format; essencialmente, eles descrevem atributos de um arquivo de formato de mídia do Windows, como taxa de bits, número e tipo de fluxos e qualidade de compactação.</span><span class="sxs-lookup"><span data-stu-id="00c56-107">ASF profiles are discussed in detail in the Windows Media Format SDK; essentially, they describe attributes of a Windows Media Format file such as bit rate, number and type of streams, and compression quality.</span></span> <span data-ttu-id="00c56-108">O filtro usa o perfil para determinar que tipo de arquivo de formato de mídia do Windows gravar, quantos Pins de entrada devem ser configurados e quais tipos de mídia eles podem aceitar.</span><span class="sxs-lookup"><span data-stu-id="00c56-108">The filter uses the profile to determine what kind of Windows Media Format file to write, how many input pins it must set up, and what media types they can accept.</span></span>

<span data-ttu-id="00c56-109">Para criar um perfil personalizado, use o SDK do Windows Media Format diretamente para criar um objeto do Gerenciador de perfis usando a função **WMCreateProfileManager** .</span><span class="sxs-lookup"><span data-stu-id="00c56-109">To create a custom profile, use the Windows Media Format SDK directly to create a profile manager object by using the **WMCreateProfileManager** function.</span></span> <span data-ttu-id="00c56-110">Em seguida, crie o perfil e passe-o para o [gravador ASF do WM](wm-asf-writer-filter.md) usando o método [**IConfigASFWriter:: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) .</span><span class="sxs-lookup"><span data-stu-id="00c56-110">Next, create the profile, and pass it to the [WM ASF Writer](wm-asf-writer-filter.md) by using the [**IConfigASFWriter::ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) method.</span></span> <span data-ttu-id="00c56-111">Essa é a única maneira de configurar o filtro com um perfil que usa os codecs de áudio do Windows Media e vídeo 9 Series.</span><span class="sxs-lookup"><span data-stu-id="00c56-111">This is the only way to configure the filter with a profile that uses the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="00c56-112">Os perfis de sistema para versões anteriores desses codecs podem ser adicionados usando o método [**IConfigASFWriter:: ConfigureFilterUsingProfileGuid**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofileguid) .</span><span class="sxs-lookup"><span data-stu-id="00c56-112">System profiles for earlier versions of these codecs can be added by using the [**IConfigASFWriter::ConfigureFilterUsingProfileGuid**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofileguid) method.</span></span>

<span data-ttu-id="00c56-113">Você pode redefinir o perfil enquanto os Pins de entrada do filtro estiverem conectados, desde que o novo perfil não exija nenhum pino de entrada adicional.</span><span class="sxs-lookup"><span data-stu-id="00c56-113">You can reset the profile while the filter's input pins are connected, as long as the new profile does not require any additional input pins.</span></span> <span data-ttu-id="00c56-114">Por exemplo, se você alterar o perfil de um perfil somente de áudio de uma entrada para um perfil de áudio e vídeo de duas entradas, apenas o PIN de áudio será reconectado e nenhum novo PIN será criado para o fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="00c56-114">For example, if you change the profile from a one-input audio-only profile to a two-input audio and video profile, just the audio pin will be reconnected and no new pin will be created for the video stream.</span></span>

<span data-ttu-id="00c56-115">Adicionando metadados</span><span class="sxs-lookup"><span data-stu-id="00c56-115">Adding Metadata</span></span>

<span data-ttu-id="00c56-116">Para adicionar metadados a um arquivo, consulte o filtro do [gravador ASF do WM](wm-asf-writer-filter.md) para a interface **IWMHeaderInfo** .</span><span class="sxs-lookup"><span data-stu-id="00c56-116">To add metadata to a file, query the [WM ASF Writer](wm-asf-writer-filter.md) filter for the **IWMHeaderInfo** interface.</span></span> <span data-ttu-id="00c56-117">Depois que o filtro receber um perfil, use os métodos de interface **IWMHeaderInfo** para gravar os metadados.</span><span class="sxs-lookup"><span data-stu-id="00c56-117">After the filter has been given a profile, use the **IWMHeaderInfo** interface methods to write the metadata.</span></span>

<span data-ttu-id="00c56-118">Indexando um arquivo</span><span class="sxs-lookup"><span data-stu-id="00c56-118">Indexing a File</span></span>

<span data-ttu-id="00c56-119">O gravador ASF do WM cria arquivos indexados de temporal por padrão.</span><span class="sxs-lookup"><span data-stu-id="00c56-119">The WM ASF Writer creates temporally indexed files by default.</span></span> <span data-ttu-id="00c56-120">Para criar um arquivo indexado por quadro, use o método [**IConfigAsfWriter:: Setindexmode**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-setindexmode) para desabilitar toda a indexação e, em seguida, crie o arquivo.</span><span class="sxs-lookup"><span data-stu-id="00c56-120">To create a frame-indexed file, use the [**IConfigAsfWriter::SetIndexMode**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-setindexmode) method to disable all indexing, then create the file.</span></span> <span data-ttu-id="00c56-121">Quando estiver concluído, use o SDK do Windows Media Format diretamente para criar um índice baseado em quadro para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="00c56-121">When it is complete, use the Windows Media Format SDK directly to create a frame-based index for the file.</span></span>

<span data-ttu-id="00c56-122">Codificação de Two-Pass</span><span class="sxs-lookup"><span data-stu-id="00c56-122">Two-Pass Encoding</span></span>

<span data-ttu-id="00c56-123">Há suporte para codificação de duas passagens apenas em codecs de mídia do Windows da versão 8 e posterior.</span><span class="sxs-lookup"><span data-stu-id="00c56-123">Two-pass encoding is supported only on Windows Media codecs of version 8 and later.</span></span> <span data-ttu-id="00c56-124">Coloque o gravador ASF do WM no modo de pré-processamento chamando [**IConfigAsfWriter2:: SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) e especificando am \_ CONFIGASFWRITER \_ param \_ MultiPASS no parâmetro *dwParam* e **true** no parâmetro *dwParam1* .</span><span class="sxs-lookup"><span data-stu-id="00c56-124">Put the WM ASF Writer into preprocess mode by calling [**IConfigAsfWriter2::SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) and specifying AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS in the *dwParam* parameter and **TRUE** in the *dwParam1* parameter.</span></span>

<span data-ttu-id="00c56-125">Em seguida, execute o gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="00c56-125">Then run the filter graph.</span></span> <span data-ttu-id="00c56-126">Quando todas as passagens de pré-processamento são concluídas (normalmente, apenas uma passagem de pré-processamento será executada), o aplicativo receberá um evento [**de \_ pré- \_ processamento de EC**](ec-preprocess-complete.md) no filtro.</span><span class="sxs-lookup"><span data-stu-id="00c56-126">When all the preprocessing passes are done (typically only one preprocessing pass will be performed), the application will receive an [**EC\_PREPROCESS\_COMPLETE**](ec-preprocess-complete.md) event from the filter.</span></span> <span data-ttu-id="00c56-127">Quando esse evento for recebido, use [**IMediaSeeking:: Setpositiones**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) para redefinir o ponteiro de fluxo de volta ao início e execute o gráfico de filtro novamente.</span><span class="sxs-lookup"><span data-stu-id="00c56-127">When this event is received, use [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) to reset the stream pointer back to the beginning, and run the filter graph again.</span></span> <span data-ttu-id="00c56-128">Após a última passagem (normalmente a segunda passagem), o aplicativo receberá um evento de [**\_ conclusão do EC**](ec-complete.md) para significar que o processo de codificação foi concluído.</span><span class="sxs-lookup"><span data-stu-id="00c56-128">After the last pass (typically the second pass), the application will receive an [**EC\_COMPLETE**](ec-complete.md) event to signify that the encoding process is complete.</span></span> <span data-ttu-id="00c56-129">Se uma passagem de pré-processamento for cancelada antes de o evento de **\_ \_ conclusão de pré-processamento do EC** ser recebido, chame [**IConfigAsfWriter2:: ResetMultiPassState**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-resetmultipassstate) para redefinir o filtro antes de tentar executar outra execução de pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="00c56-129">If a preprocessing pass is canceled before the **EC\_PREPROCESS\_COMPLETE** event is received, call [**IConfigAsfWriter2::ResetMultiPassState**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-resetmultipassstate) to reset the filter before attempting another preprocessing run.</span></span>

<span data-ttu-id="00c56-130">Só é necessário definir o \_ \_ parâmetro CONFIGASFWRITER param \_ MultiPASS como **false** se você quiser colocar o filtro fora do modo de pré-processamento completamente.</span><span class="sxs-lookup"><span data-stu-id="00c56-130">It is only necessary to set the AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS parameter to **FALSE** if you want to put the filter out of preprocessing mode completely.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="00c56-131">É responsabilidade do aplicativo habilitar o modo de pré-processamento com base no perfil que será usado para codificação.</span><span class="sxs-lookup"><span data-stu-id="00c56-131">It is the application's responsibility to enable the preprocessing mode based on the profile that will be used for encoding.</span></span> <span data-ttu-id="00c56-132">Alguns perfis exigem codificação de duas passagens; Se você tentar codificar um arquivo com um perfil como esse, e não definir \_ CONFIGASFWRITER \_ param \_ multipasse para **true**, ocorrerá um erro do [**EC \_ userabort**](ec-userabort.md) .</span><span class="sxs-lookup"><span data-stu-id="00c56-132">Some profiles require two-pass encoding; if you attempt to encode a file with such a profile, and do not set AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS to **TRUE**, an [**EC\_USERABORT**](ec-userabort.md) error will result.</span></span> <span data-ttu-id="00c56-133">Para obter mais informações, consulte a documentação do Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="00c56-133">For more information, see the Windows Media Format SDK documentation.</span></span>

 

<span data-ttu-id="00c56-134">Obter e definir propriedades de buffer em tempo de execução</span><span class="sxs-lookup"><span data-stu-id="00c56-134">Getting and Setting Buffer Properties at Run Time</span></span>

<span data-ttu-id="00c56-135">Em alguns cenários, por exemplo, se você quiser forçar a inserção de quadro-chave ao gravar um arquivo, um aplicativo pode precisar obter ou definir informações sobre um buffer de mídia do Windows em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="00c56-135">In some scenarios, for example if you want to force key-frame insertion when writing a file, an application may need to get or set information about a Windows Media buffer at run time.</span></span> <span data-ttu-id="00c56-136">O [leitor ASF do WM](wm-asf-reader-filter.md) e o [gravador ASF do WM](wm-asf-writer-filter.md) dão suporte a um mecanismo de retorno de chamada que permite que um aplicativo acesse a interface **INSSBuffer3** em cada buffer de mídia individual durante a leitura do arquivo ou a gravação de arquivos.</span><span class="sxs-lookup"><span data-stu-id="00c56-136">The [WM ASF Reader](wm-asf-reader-filter.md) and [WM ASF Writer](wm-asf-writer-filter.md) filters both support a callback mechanism that enables an application to access the **INSSBuffer3** interface on each individual media buffer during file reading or file writing.</span></span> <span data-ttu-id="00c56-137">Os aplicativos podem usar essa interface para designar exemplos específicos como quadros-chave, definir códigos de tempo SMPTE, especificar configurações de entrelaçamento ou adicionar qualquer tipo de dados privados a um fluxo.</span><span class="sxs-lookup"><span data-stu-id="00c56-137">Applications can use this interface to designate specific samples as key frames, set SMPTE time codes, specify interlace settings, or add any type of private data to a stream.</span></span>

<span data-ttu-id="00c56-138">Use a interface [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) para se registrar para retornos de chamada do PIN que está manipulando o fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="00c56-138">Use the [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) interface to register for callbacks from the pin that is handling the video stream.</span></span> <span data-ttu-id="00c56-139">O PIN chamará o método [**IAMWMBufferPassCallback:: Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) para cada buffer.</span><span class="sxs-lookup"><span data-stu-id="00c56-139">The pin will call your [**IAMWMBufferPassCallback::Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) method for each buffer.</span></span>

<span data-ttu-id="00c56-140">Pixels não quadrados</span><span class="sxs-lookup"><span data-stu-id="00c56-140">Non-Square Pixels</span></span>

<span data-ttu-id="00c56-141">O gravador ASF do WM se conecta a um filtro upstream, como o codificador DV, que gera informações de taxa de proporção de pixel.</span><span class="sxs-lookup"><span data-stu-id="00c56-141">The WM ASF Writer connects to an upstream filter, such as the DV Decoder, that outputs pixel aspect ratio information.</span></span> <span data-ttu-id="00c56-142">O gravador ASF do WM gravará essas informações como extensões de unidade de dados para cada exemplo no arquivo.</span><span class="sxs-lookup"><span data-stu-id="00c56-142">The WM ASF Writer will write this information as data unit extensions for every sample in the file.</span></span>

<span data-ttu-id="00c56-143">Quando o leitor ASF do WM encontrar informações de taxa de proporção de pixel no cabeçalho do arquivo ou nas extensões de unidade de dados para os exemplos, ele oferecerá um formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) como uma primeira opção em seu pino de saída.</span><span class="sxs-lookup"><span data-stu-id="00c56-143">When the WM ASF Reader encounters pixel aspect ratio information in the file header or in data unit extensions for the samples, it will offer a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format as a first choice on its output pin.</span></span> <span data-ttu-id="00c56-144">Os membros **dwPictAspectRatioX** e **dwPictAspectRatioY** da estrutura, que descrevem a taxa de proporção do retângulo de vídeo, serão ajustados corretamente para considerar a taxa de proporção de pixel.</span><span class="sxs-lookup"><span data-stu-id="00c56-144">The **dwPictAspectRatioX** and **dwPictAspectRatioY** members of the structure, which describe the video rectangle's aspect ratio, will be correctly adjusted to account for the pixel aspect ratio.</span></span>

<span data-ttu-id="00c56-145">Mantendo o formato entrelaçado</span><span class="sxs-lookup"><span data-stu-id="00c56-145">Maintaining Interlaced Format</span></span>

<span data-ttu-id="00c56-146">Se você capturar vídeo entrelaçado de uma televisão ou de uma câmera de vídeo digital, talvez queira preservar o vídeo original como campos independentes se esperar que o arquivo codificado seja reproduzido em uma televisão ou em outro dispositivo de vídeo entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="00c56-146">If you capture interlaced video from a television or a DV camera, you might wish to preserve the original video as independent fields if you expect the encoded file to be played back on a television or other interlaced display device.</span></span> <span data-ttu-id="00c56-147">(Monitores de computador são dispositivos de verificação progressiva.) Se você desentrelaçar um vídeo e, em seguida, reentrelaçar-o para reprodução em uma televisão, uma perda de dados será incorrida.</span><span class="sxs-lookup"><span data-stu-id="00c56-147">(Computer monitors are progressive scanning devices.) If you deinterlace a video, and then reinterlace it for playback on a television, some loss of data will be incurred.</span></span> <span data-ttu-id="00c56-148">Em um arquivo ASF, as informações de entrelaçamento são armazenadas como extensões de unidade de dados que o aplicativo aplica a cada exemplo usando o método [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="00c56-148">In an ASF file, interlacing information is stored as data unit extensions that the application applies to each sample using the [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) method described previously.</span></span> <span data-ttu-id="00c56-149">Para codificar um arquivo que preserva as configurações de entrelaçamento originais, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="00c56-149">To encode a file that preserves the original interlace settings, follow these steps:</span></span>

1.  <span data-ttu-id="00c56-150">Implemente uma classe que dê suporte a **IAMWMBufferPassCallback** e grave uma função Notify que defina os sinalizadores entrelaçados para cada amostra.</span><span class="sxs-lookup"><span data-stu-id="00c56-150">Implement a class that supports **IAMWMBufferPassCallback** and write a Notify function that sets the interlace flags for each sample.</span></span> <span data-ttu-id="00c56-151">Essa função será chamada pelo gravador ASF do WM antes de processar cada exemplo.</span><span class="sxs-lookup"><span data-stu-id="00c56-151">This function will be called by the WM ASF Writer before it processes each sample.</span></span>
    ```C++
    // Set to WM_CT_TOP_FIELD_FIRST if that is your format.
    BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
    HRESULT hr = S_OK;

    hr = pNSSBuffer3->SetProperty(
        WM_SampleExtensionGUID_ContentType, 
        (void*) &flag, 
        WM_SampleExtension_ContentType_Size
        );         
    ```

    

2.  <span data-ttu-id="00c56-152">Defina as extensões de unidade de dados no perfil antes de passar o perfil para o filtro.</span><span class="sxs-lookup"><span data-stu-id="00c56-152">Set the data unit extensions on the profile before you pass the profile to the filter.</span></span>
    ```C++
    hr = pWMStreamConfig2->AddDataUnitExtension(
        WM_SampleExtensionGUID_ContentType, 
        WM_SampleExtension_ContentType_Size, 
        NULL, 
        0 
        );
    ```

    

3.  <span data-ttu-id="00c56-153">Depois de configurar o filtro com o perfil, obtenha a interface **IWMWriterAdvanced2** do gravador ASF do WM e chame o método **SetInputSettings** .</span><span class="sxs-lookup"><span data-stu-id="00c56-153">After you configure the filter with the profile, obtain the **IWMWriterAdvanced2** interface from the WM ASF Writer and call the **SetInputSettings** method.</span></span>

    ``

    ``

    ```C++
    // Must do this first.
    hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);
      
    CComPtr<IServiceProvider> pProvider;
    CComPtr<IWMWriterAdvanced2> pWMWA2;

    hr = pConfigAsfWriter2->QueryInterface( __uuidof(IServiceProvider),
                                             (void**)&pProvider);
    if (SUCCEEDED(hr))
    {
        hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
            IID_IWMWriterAdvanced2,
            (void**)&pWMWA2);
    }

    BOOL pValue = TRUE;

    // Set the first parameter to your actual input number.
    hr = pWMWA2->SetInputSetting(0, g_wszInterlacedCoding,
        WMT_TYPE_BOOL, (BYTE*) &pValue, sizeof(WMT_TYPE_BOOL));
                
    ```

    

## <a name="related-topics"></a><span data-ttu-id="00c56-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="00c56-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00c56-155">Criando arquivos ASF no DirectShow</span><span class="sxs-lookup"><span data-stu-id="00c56-155">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



