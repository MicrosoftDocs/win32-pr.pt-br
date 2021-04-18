---
title: Configurando perfis e outras propriedades de arquivo (QASF)
description: Configurando perfis e outras propriedades de arquivo (QASF)
ms.assetid: a462fc8b-5a2e-4c93-828d-177d1965b734
keywords:
- SDK do Windows Media Format, Configurando perfis (QASF)
- SDK do Windows Media Format, Configurando propriedades do arquivo (QASF)
- SDK do Windows Media Format, metadados (QASF)
- ASF (Advanced Systems Format), Configurando perfis (QASF)
- ASF (formato de sistemas avançados), Configurando perfis (QASF)
- ASF (Advanced Systems Format), Configurando propriedades de arquivo (QASF)
- ASF (formato de sistemas avançados), Configurando propriedades de arquivo (QASF)
- Formato de sistema avançado (ASF), metadados (QASF)
- ASF (formato de sistemas avançados), metadados (QASF)
- SDK do Windows Media Format, QASF
- ASF (Advanced Systems Format), QASF
- ASF (formato de sistemas avançados), QASF
- metadados, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebb6afedfa00813e7447e5bcaefe1f251c02575
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454220"
---
# <a name="configuring-profiles-and-other-file-properties-qasf"></a><span data-ttu-id="ea2fb-116">Configurando perfis e outras propriedades de arquivo (QASF)</span><span class="sxs-lookup"><span data-stu-id="ea2fb-116">Configuring Profiles and Other File Properties (QASF)</span></span>

<span data-ttu-id="ea2fb-117">Os itens a seguir descrevem como executar várias tarefas relacionadas à criação de arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-117">The following items describe how to perform various tasks related to the creation of ASF files.</span></span>

## <a name="creating-a-profile-qasf"></a><span data-ttu-id="ea2fb-118">Criando um perfil (QASF)</span><span class="sxs-lookup"><span data-stu-id="ea2fb-118">Creating a Profile (QASF)</span></span>

<span data-ttu-id="ea2fb-119">Para criar um perfil personalizado, use o SDK do Windows Media Format diretamente para criar um objeto do Gerenciador de perfis usando a função [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="ea2fb-119">To create a custom profile, use the Windows Media Format SDK directly to create a profile manager object by using the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span> <span data-ttu-id="ea2fb-120">Em seguida, crie o perfil e passe-o para o [gravador ASF do WM](wm-asf-writer-filter.md) usando o método [**IConfigASFWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="ea2fb-120">Next, create the profile, and pass it to the [WM ASF Writer](wm-asf-writer-filter.md) by using the [**IConfigASFWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) method.</span></span> <span data-ttu-id="ea2fb-121">Essa é a única maneira de configurar o filtro com um perfil que usa os codecs de áudio do Windows Media e vídeo 9 Series.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-121">This is the only way to configure the filter with a profile that uses the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="ea2fb-122">Os perfis de sistema para versões anteriores desses codecs podem ser adicionados usando o método [**IConfigASFWriter:: ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md) .</span><span class="sxs-lookup"><span data-stu-id="ea2fb-122">System profiles for earlier versions of these codecs can be added by using the [**IConfigASFWriter::ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md) method.</span></span>

## <a name="adding-metadata-qasf"></a><span data-ttu-id="ea2fb-123">Adicionando metadados (QASF)</span><span class="sxs-lookup"><span data-stu-id="ea2fb-123">Adding Metadata (QASF)</span></span>

<span data-ttu-id="ea2fb-124">Para adicionar metadados a um arquivo, chame **QueryInterface** da interface **IBASEFILTER** no [gravador ASF do WM](wm-asf-writer-filter.md) para recuperar a interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) .</span><span class="sxs-lookup"><span data-stu-id="ea2fb-124">To add metadata to a file, call **QueryInterface** from the **IBaseFilter** interface on the [WM ASF Writer](wm-asf-writer-filter.md) to retrieve the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface.</span></span> <span data-ttu-id="ea2fb-125">Depois que o filtro receber um perfil, use os métodos de interface **IWMHeaderInfo** para gravar os metadados.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-125">After the filter has been given a profile, use the **IWMHeaderInfo** interface methods to write the metadata.</span></span>

## <a name="indexing-a-file-qasf"></a><span data-ttu-id="ea2fb-126">Indexando um arquivo (QASF)</span><span class="sxs-lookup"><span data-stu-id="ea2fb-126">Indexing a File (QASF)</span></span>

<span data-ttu-id="ea2fb-127">O gravador ASF do WM cria arquivos indexados de temporal por padrão.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-127">The WM ASF Writer creates temporally indexed files by default.</span></span> <span data-ttu-id="ea2fb-128">Para criar um arquivo indexado por quadro, use o método [**IConfigAsfWriter:: Setindexmode**](iconfigasfwriter-setindexmode.md) para desabilitar toda a indexação e, em seguida, crie o arquivo.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-128">To create a frame-indexed file, use the [**IConfigAsfWriter::SetIndexMode**](iconfigasfwriter-setindexmode.md) method to disable all indexing, then create the file.</span></span> <span data-ttu-id="ea2fb-129">Quando estiver concluído, use o SDK do Windows Media Format diretamente para criar um índice baseado em quadro para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-129">When it is complete, use the Windows Media Format SDK directly to create a frame-based index for the file.</span></span>

## <a name="performing-two-pass-encoding-qasf"></a><span data-ttu-id="ea2fb-130">Executando codificação de Two-Pass (QASF)</span><span class="sxs-lookup"><span data-stu-id="ea2fb-130">Performing Two-Pass Encoding (QASF)</span></span>

<span data-ttu-id="ea2fb-131">Há suporte para codificação de duas passagens apenas em codecs de mídia do Windows da versão 8 e posterior.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-131">Two-pass encoding is supported only on Windows Media codecs of version 8 and later.</span></span> <span data-ttu-id="ea2fb-132">Coloque o gravador ASF do WM no modo de pré-processamento chamando [**IConfigAsfWriter2:: SetParam**](iconfigasfwriter2-setparam.md) e especificando am \_ CONFIGASFWRITER \_ param \_ MultiPASS no parâmetro *dwParam* e **true** no parâmetro *dwParam1* .</span><span class="sxs-lookup"><span data-stu-id="ea2fb-132">Put the WM ASF Writer into preprocess mode by calling [**IConfigAsfWriter2::SetParam**](iconfigasfwriter2-setparam.md) and specifying AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS in the *dwParam* parameter and **TRUE** in the *dwParam1* parameter.</span></span>

<span data-ttu-id="ea2fb-133">Em seguida, execute o gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-133">Then run the filter graph.</span></span> <span data-ttu-id="ea2fb-134">Quando todas as passagens de pré-processamento são concluídas (normalmente, apenas uma passagem de pré-processamento será executada), o aplicativo receberá um evento **de \_ pré- \_ processamento de EC** no filtro.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-134">When all the preprocessing passes are done (typically only one preprocessing pass will be performed), the application will receive an **EC\_PREPROCESS\_COMPLETE** event from the filter.</span></span> <span data-ttu-id="ea2fb-135">Quando esse evento for recebido, use **IMediaSeeking:: Setpositiones** para redefinir o ponteiro de fluxo de volta ao início e execute o gráfico de filtro novamente.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-135">When this event is received, use **IMediaSeeking::SetPositions** to reset the stream pointer back to the beginning, and run the filter graph again.</span></span> <span data-ttu-id="ea2fb-136">Após a última passagem (normalmente a segunda passagem), o aplicativo receberá um evento de **\_ conclusão do EC** para significar que o processo de codificação foi concluído.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-136">After the last pass (typically the second pass), the application will receive an **EC\_COMPLETE** event to signify that the encoding process is complete.</span></span> <span data-ttu-id="ea2fb-137">Se uma passagem de pré-processamento for cancelada antes de o evento de **\_ \_ conclusão de pré-processamento do EC** ser recebido, chame [**IConfigAsfWriter2:: ResetMultiPassState**](iconfigasfwriter2-resetmultipassstate.md) para redefinir o filtro antes de tentar executar outra execução de pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-137">If a preprocessing pass is canceled before the **EC\_PREPROCESS\_COMPLETE** event is received, call [**IConfigAsfWriter2::ResetMultiPassState**](iconfigasfwriter2-resetmultipassstate.md) to reset the filter before attempting another preprocessing run.</span></span>

<span data-ttu-id="ea2fb-138">Só é necessário chamar **IConfigAsfWriter:: SetParam**(am \_ CONFIGASFWRITER param All \_ \_ Pass, **false**) se você quiser colocar o filtro fora do modo de pré-processamento completamente.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-138">It is only necessary to call **IConfigAsfWriter::SetParam**(AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS, **FALSE**) if you want to put the filter out of preprocessing mode completely.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ea2fb-139">É responsabilidade do aplicativo habilitar o modo de pré-processamento com base no perfil que será usado para codificação.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-139">It is the application's responsibility to enable preprocessing mode based on the profile that will be used for encoding.</span></span> <span data-ttu-id="ea2fb-140">Alguns perfis exigem codificação de duas passagens; Se você tentar codificar um arquivo com um perfil como esse, e não definir \_ CONFIGASFWRITER \_ param \_ multipasse para **true**, \_ ocorrerá um erro do EC userabort.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-140">Some profiles require two-pass encoding; if you attempt to encode a file with such a profile, and do not set AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS to **TRUE**, an EC\_USERABORT error will result.</span></span> <span data-ttu-id="ea2fb-141">Para obter mais informações sobre como determinar se um determinado perfil requer codificação de duas passagens, consulte [usando Two-Pass codificação](using-two-pass-encoding.md) ou [gravando fluxos de taxa de bits variáveis](writing-variable-bit-rate-streams.md).</span><span class="sxs-lookup"><span data-stu-id="ea2fb-141">For more information on how to determine whether a given profile requires two-pass encoding, see [Using Two-Pass Encoding](using-two-pass-encoding.md) or [Writing Variable Bit Rate Streams](writing-variable-bit-rate-streams.md).</span></span>

 

## <a name="getting-and-setting-buffer-properties-at-run-time-qasf"></a><span data-ttu-id="ea2fb-142">Obter e definir propriedades de buffer em tempo de execução (QASF)</span><span class="sxs-lookup"><span data-stu-id="ea2fb-142">Getting and Setting Buffer Properties at Run Time (QASF)</span></span>

<span data-ttu-id="ea2fb-143">Em alguns cenários, por exemplo, se você quiser forçar a inserção de quadro-chave ao gravar um arquivo, um aplicativo pode precisar obter ou definir informações sobre um buffer de mídia do Windows em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-143">In some scenarios, for example if you want to force key-frame insertion when writing a file, an application may need to get or set information about a Windows Media buffer at run time.</span></span> <span data-ttu-id="ea2fb-144">O [leitor ASF do WM](wm-asf-reader-filter.md) e o [gravador ASF do WM](wm-asf-writer-filter.md) dão suporte a um mecanismo de retorno de chamada que permite que um aplicativo acesse a interface [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) em cada buffer de mídia individual durante a leitura do arquivo ou a gravação de arquivos.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-144">The [WM ASF Reader](wm-asf-reader-filter.md) and [WM ASF Writer](wm-asf-writer-filter.md) filters both support a callback mechanism that enables an application to access the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface on each individual media buffer during file reading or file writing.</span></span> <span data-ttu-id="ea2fb-145">Os aplicativos podem usar essa interface para designar amostras específicas como quadros-chave, ou [*cleanpoints*](wmformat-glossary.md), para definir códigos de tempo SMPTE, especificar configurações de entrelaçamento ou adicionar qualquer tipo de dados privados a um fluxo.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-145">Applications can use this interface to designate specific samples as key frames, or [*cleanpoints*](wmformat-glossary.md), to set SMPTE time codes, to specify interlace settings, or add any type of private data to a stream.</span></span>

<span data-ttu-id="ea2fb-146">Use a interface [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass) para se registrar para retornos de chamada do PIN que está manipulando o fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-146">Use the [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass) interface to register for callbacks from the pin that is handling the video stream.</span></span> <span data-ttu-id="ea2fb-147">Quando o PIN chama o método [**IAMWMBufferPassCallback:: Notify**](iamwmbufferpasscallback-notify.md) , examine os carimbos de data/hora no buffer e, se apropriado, chame [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) para definir a propriedade **OutputCleanPoint do WM \_ SampleExtensionGUID \_** no buffer como **true**.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-147">When the pin calls your [**IAMWMBufferPassCallback::Notify**](iamwmbufferpasscallback-notify.md) method, examine the time stamps on the buffer and, if appropriate, call [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) to set the **WM\_SampleExtensionGUID\_OutputCleanPoint** property on the buffer to **TRUE**.</span></span>

## <a name="non-square-pixel-support-qasf"></a><span data-ttu-id="ea2fb-148">Suporte a pixel não quadrado (QASF)</span><span class="sxs-lookup"><span data-stu-id="ea2fb-148">Non-Square Pixel Support (QASF)</span></span>

<span data-ttu-id="ea2fb-149">O gravador ASF do WM se conecta a um filtro upstream, como o codificador DV, que gera informações de taxa de proporção de pixel.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-149">The WM ASF Writer connects to an upstream filter, such as the DV Decoder, that outputs pixel aspect ratio information.</span></span> <span data-ttu-id="ea2fb-150">O gravador ASF do WM gravará essas informações como extensões de unidade de dados para cada exemplo no arquivo.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-150">The WM ASF Writer will write this information as data unit extensions for every sample in the file.</span></span>

<span data-ttu-id="ea2fb-151">Quando o leitor ASF do WM encontrar informações de taxa de proporção de pixel no cabeçalho do arquivo ou em extensões de unidade de dados para os exemplos, ele oferecerá um tipo de mídia **VIDEOINFOHEADER2** como uma primeira opção em seu pino de saída.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-151">When the WM ASF Reader encounters pixel aspect ratio information in the file header or in data unit extensions for the samples, it will offer a **VIDEOINFOHEADER2** media type as a first choice on its output pin.</span></span> <span data-ttu-id="ea2fb-152">Os membros **dwPictAspectRatioX** e **dwPictAspectRatioY** da estrutura, que descrevem a taxa de proporção do retângulo de vídeo, serão ajustados corretamente para considerar a taxa de proporção de pixel.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-152">The **dwPictAspectRatioX** and **dwPictAspectRatioY** members of the structure, which describe the video rectangle's aspect ratio, will be correctly adjusted to account for the pixel aspect ratio.</span></span>

## <a name="maintaining-interlaced-format"></a><span data-ttu-id="ea2fb-153">Mantendo o formato entrelaçado</span><span class="sxs-lookup"><span data-stu-id="ea2fb-153">Maintaining Interlaced Format</span></span>

<span data-ttu-id="ea2fb-154">Se você capturar vídeo entrelaçado de uma televisão ou de uma câmera de vídeo digital, talvez queira preservar o vídeo original como campos independentes se esperar que o arquivo codificado seja reproduzido em uma televisão ou em outro dispositivo de vídeo entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-154">If you capture interlaced video from a television or a DV camera, you might wish to preserve the original video as independent fields if you expect the encoded file to be played back on a television or other interlaced display device.</span></span> <span data-ttu-id="ea2fb-155">(Monitores de computador são dispositivos de verificação progressiva.) Se você desentrelaçar um vídeo e, em seguida, reentrelaçar-o para reprodução em uma televisão, uma perda de dados será incorrida.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-155">(Computer monitors are progressive scanning devices.) If you deinterlace a video, and then reinterlace it for playback on a television, some loss of data will be incurred.</span></span> <span data-ttu-id="ea2fb-156">Em um arquivo ASF, as informações de entrelaçamento são armazenadas como extensões de unidade de dados que o aplicativo aplica a cada exemplo usando o método **IAMWMBufferPassCallback** descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-156">In an ASF file, interlacing information is stored as data unit extensions that the application applies to each sample using the **IAMWMBufferPassCallback** method described previously.</span></span> <span data-ttu-id="ea2fb-157">Para codificar um arquivo que preserva as configurações de entrelaçamento originais, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="ea2fb-157">To encode a file that preserves the original interlace settings, follow these steps:</span></span>

-   <span data-ttu-id="ea2fb-158">Implemente uma classe que dê suporte a **IAMWMBufferPassCallback** e grave uma função Notify que defina os sinalizadores entrelaçados para cada amostra.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-158">Implement a class that supports **IAMWMBufferPassCallback** and write a Notify function that sets the interlace flags for each sample.</span></span> <span data-ttu-id="ea2fb-159">Essa função será chamada pelo gravador ASF do WM antes de processar cada exemplo.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-159">This function will be called by the WM ASF Writer before it processes each sample.</span></span>


```C++
// Set to WM_CT_TOP_FIELD_FIRST if that is your format.
BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
            HRESULT hr = pNSSBuffer3->SetProperty(WM_SampleExtensionGUID_ContentType, (void*) &flag, WM_SampleExtension_ContentType_Size);
           
```



-   <span data-ttu-id="ea2fb-160">Defina as extensões de unidade de dados no perfil antes de passar o perfil para o filtro.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-160">Set the data unit extensions on the profile before you pass the profile to the filter.</span></span>


```C++
hr = pWMStreamConfig2->AddDataUnitExtension( WM_SampleExtensionGUID_ContentType, WM_SampleExtension_ContentType_Size, NULL, 0 );
```



-   <span data-ttu-id="ea2fb-161">Depois de configurar o filtro com o perfil, obtenha a interface **IWMWriterAdvanced2** do gravador ASF do WM e chame o método **SetInputSettings** .</span><span class="sxs-lookup"><span data-stu-id="ea2fb-161">After you configure the filter with the profile, obtain the **IWMWriterAdvanced2** interface from the WM ASF Writer and call the **SetInputSettings** method.</span></span>

`// Must do this first.`

`hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);`


```C++
  
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



 

 