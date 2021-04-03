---
title: Configurando o gravador ASF do WM (QASF)
description: Configurando o gravador ASF do WM (QASF)
ms.assetid: 0f49ed5a-c228-456a-9551-8d277adccd0e
keywords:
- SDK do Windows Media Format, configurando o gravador ASF do WM (QASF)
- SDK do Windows Media Format, DirectShow
- SDK do Windows Media Format, gravador ASF do WM
- SDK do Windows Media Format, QASF
- ASF (Advanced Systems Format), configurando o gravador ASF do WM (QASF)
- ASF (formato de sistemas avançados), configurando o gravador ASF do WM (QASF)
- ASF (Advanced Systems Format), gravador ASF do WM
- ASF (formato de sistemas avançados), gravador ASF do WM
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), QASF
- ASF (formato de sistemas avançados), QASF
- DirectShow, configurando o gravador ASF do WM (QASF)
- DirectShow, gravador ASF do WM
- DirectShow, QASF
- Gravador ASF do WM, configurando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72f954522c4acae89e6f6dd001561811088c2a9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084797"
---
# <a name="configuring-the-wm-asf-writer-qasf"></a><span data-ttu-id="68241-119">Configurando o gravador ASF do WM (QASF)</span><span class="sxs-lookup"><span data-stu-id="68241-119">Configuring the WM ASF Writer (QASF)</span></span>

<span data-ttu-id="68241-120">Quando o filtro do [gravador ASF do WM](wm-asf-writer-filter.md) é criado, ele é configurado automaticamente com o \_ perfil WMProfile V80 \_ 256Video como padrão.</span><span class="sxs-lookup"><span data-stu-id="68241-120">When the [WM ASF Writer](wm-asf-writer-filter.md) filter is created, it is configured automatically with the WMProfile\_V80\_256Video profile as a default.</span></span> <span data-ttu-id="68241-121">Como esse perfil usa os codecs de áudio do Windows Media e Windows Media Video versão 8, é recomendável que você crie um perfil personalizado que usa os codecs da série Windows Media 9 e, em seguida, passe o ponteiro [**IWMProfile**](iwmprofile.md) para o filtro usando o método [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="68241-121">Because this profile uses the Windows Media Audio and Windows Media Video version 8 codecs, it is recommended that you create a custom profile that uses the Windows Media 9 Series codecs, and then pass its [**IWMProfile**](iwmprofile.md) pointer to the filter using the [**IConfigAsfWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) method.</span></span> <span data-ttu-id="68241-122">O filtro deve ser adicionado ao grafo antes que o filtro possa ser configurado e deve ser configurado antes que possa ser conectado a filtros upstream.</span><span class="sxs-lookup"><span data-stu-id="68241-122">The filter must be added to the graph before the filter can be configured, and it must be configured before it can be connected to upstream filters.</span></span> <span data-ttu-id="68241-123">O filtro usa o perfil para determinar que tipo de arquivo de formato de mídia do Windows deve ser gravado, quantos Pins de entrada configurar e quais tipos de mídia os Pins podem aceitar.</span><span class="sxs-lookup"><span data-stu-id="68241-123">The filter uses the profile to determine what kind of Windows Media Format file to write, how many input pins to set up, and what media types the pins can accept.</span></span>

<span data-ttu-id="68241-124">O filtro permite que os perfis sejam redefinidos enquanto seus PINs de entrada estão conectados, desde que o novo perfil não exija nenhum pino de entrada adicional.</span><span class="sxs-lookup"><span data-stu-id="68241-124">The filter allows profiles to be reset while its input pins are connected, as long as the new profile does not require any additional input pins.</span></span> <span data-ttu-id="68241-125">Por exemplo, se você alterar o perfil de um perfil somente de áudio de uma entrada para um perfil de áudio e vídeo de duas entradas, apenas o PIN de áudio será reconnectedAll os dados de entrada deverão ser carimbados por hora e todos os Pins de entrada deverão ser conectados antes que o filtro possa ser executado ou pausado.</span><span class="sxs-lookup"><span data-stu-id="68241-125">For example, if you change the profile from a one-input audio-only profile to a two-input audio and video profile, just the audio pin will be reconnectedAll input data must be time-stamped, and all input pins must be connected before the filter can be run or paused.</span></span> <span data-ttu-id="68241-126">Isso significa que, se você configurar o filtro com um perfil que tenha um fluxo de áudio e um fluxo de vídeo, o filtro criará um áudio e um pino de entrada de vídeo, e ambos os Pins deverão ser conectados antes que o filtro possa ser executado.</span><span class="sxs-lookup"><span data-stu-id="68241-126">This means that if you configure the filter with a profile that has an audio stream and a video stream, the filter will create an audio and a video input pin, and both pins must be connected before the filter can be run.</span></span>

<span data-ttu-id="68241-127">Adicionando extensões de unidade de dados</span><span class="sxs-lookup"><span data-stu-id="68241-127">Adding Data Unit Extensions</span></span>

<span data-ttu-id="68241-128">Você pode configurar um fluxo de perfil para extensões de unidade de dados, como códigos de tempo SMPTE, antes ou depois que o filtro está conectado, desde que você siga esta ordem de operações:</span><span class="sxs-lookup"><span data-stu-id="68241-128">You can configure a profile stream for data unit extensions, such as SMPTE time codes, either before or after the filter is connected, as long as you follow this order of operations:</span></span>

1.  <span data-ttu-id="68241-129">Adicione uma ou mais extensões de unidade de dados ao fluxo usando [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).</span><span class="sxs-lookup"><span data-stu-id="68241-129">Add one or more data unit extensions to the stream using [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).</span></span>
2.  <span data-ttu-id="68241-130">Chame [**WMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) para atualizar o perfil.</span><span class="sxs-lookup"><span data-stu-id="68241-130">Call [**WMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) to update the profile.</span></span>
3.  <span data-ttu-id="68241-131">Chame [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) com o objeto de perfil atualizado.</span><span class="sxs-lookup"><span data-stu-id="68241-131">Call [**IConfigAsfWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) with the updated profile object.</span></span>
4.  <span data-ttu-id="68241-132">Localize o PIN de entrada de vídeo e chame o método [**IAMWMBufferPass:: setnotify**](iamwmbufferpass-setnotify.md) para registrar sua interface [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="68241-132">Find the video input pin, and call its [**IAMWMBufferPass::SetNotify**](iamwmbufferpass-setnotify.md) method to register your application-defined [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) interface.</span></span>

<span data-ttu-id="68241-133">Quando o grafo for executado, o método [**IAMWMBufferPassCallback:: Notify**](iamwmbufferpasscallback-notify.md) será chamado para cada quadro e você poderá obter e definir propriedades no exemplo usando seus métodos de interface [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) .</span><span class="sxs-lookup"><span data-stu-id="68241-133">When the graph runs, your [**IAMWMBufferPassCallback::Notify**](iamwmbufferpasscallback-notify.md) method will be called for each frame, and you will be able to get and set properties on the sample using its [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface methods.</span></span>

> [!Note]  
> <span data-ttu-id="68241-134">Em alguns cenários com uso intensivo de processador, como o telecineon inverso, o gravador ASF do WM pode exigir mais buffers de saída do que alguns filtros downstream podem dar suporte.</span><span class="sxs-lookup"><span data-stu-id="68241-134">In some processor-intensive scenarios such as inverse telecine, the WM ASF Writer may require more output buffers than some downstream filters can support.</span></span> <span data-ttu-id="68241-135">O codificador DV, por exemplo, não aceitará mais de um buffer para seu pino de saída e o mesmo será verdadeiro para o descompactador AVI em determinadas condições.</span><span class="sxs-lookup"><span data-stu-id="68241-135">The DV Decoder, for example, will not accept more than one buffer for its output pin and the same is true for the AVI Decompressor in certain conditions.</span></span> <span data-ttu-id="68241-136">Se você encontrar problemas ao tentar se conectar a esses filtros, ou possivelmente ao executar o grafo, pode ser necessário gravar um filtro intermediário que aceite qualquer número de buffers em seu pino de saída.</span><span class="sxs-lookup"><span data-stu-id="68241-136">If you encounter problems when attempting to connect to these filters, or possibly when running the graph, it may be necessary to write an intermediary filter that accepts any number of buffers on its output pin.</span></span>

 

 

 