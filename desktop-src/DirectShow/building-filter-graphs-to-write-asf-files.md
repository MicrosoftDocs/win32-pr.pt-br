---
description: Criando gráficos de filtro para gravar arquivos ASF
ms.assetid: c4885152-d7d2-4749-a79a-e0effd38837d
title: Criando gráficos de filtro para gravar arquivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0581672f9fd3e4bfa5e2c678c3bd3c0d3ea22fa0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456762"
---
# <a name="building-filter-graphs-to-write-asf-files"></a><span data-ttu-id="c4937-103">Criando gráficos de filtro para gravar arquivos ASF</span><span class="sxs-lookup"><span data-stu-id="c4937-103">Building Filter Graphs to Write ASF Files</span></span>

<span data-ttu-id="c4937-104">Ao criar conteúdo baseado no Windows Media, os aplicativos normalmente usam um dos seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="c4937-104">When creating Windows Media–based content, applications typically use one of the following scenarios:</span></span>

-   <span data-ttu-id="c4937-105">Conversão ou transcodificação de conteúdo de outro formato para o Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="c4937-105">Converting or transcoding content from some other format into Windows Media Format.</span></span>
-   <span data-ttu-id="c4937-106">Inserção de conteúdo que não é baseado no Windows Media (formatos de fluxo nativos) em arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="c4937-106">Inserting content that is not Windows Media-based (native stream formats) into ASF files.</span></span>
-   <span data-ttu-id="c4937-107">Capturar dados dinâmicos e codificá-los imediatamente no formato de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="c4937-107">Capturing live data and encoding it immediately into Windows Media Format.</span></span>

<span data-ttu-id="c4937-108">Transcodificação de arquivos ASF</span><span class="sxs-lookup"><span data-stu-id="c4937-108">Transcoding ASF Files</span></span>

<span data-ttu-id="c4937-109">Você pode criar um grafo de filtro de transcodificação de arquivo usando o [gravador ASF do WM](wm-asf-writer-filter.md) de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="c4937-109">You can build a file-transcoding filter graph using the [WM ASF Writer](wm-asf-writer-filter.md) in various ways.</span></span> <span data-ttu-id="c4937-110">A maneira mais fácil é adicionar o gravador ASF do WM ao grafo de filtro e, em seguida, usar o método IGraphBuilder:: RenderFile para criar o grafo automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c4937-110">The easiest way is to add the WM ASF Writer to the filter graph and then use the IGraphBuilder::RenderFile method to build the graph automatically.</span></span>

<span data-ttu-id="c4937-111">Uma maneira alternativa é adicionar cada filtro manualmente ao grafo e conectar os Pins.</span><span class="sxs-lookup"><span data-stu-id="c4937-111">An alternative way is to add each filter manually to the graph and connect the pins.</span></span> <span data-ttu-id="c4937-112">Depois de adicionar o gravador ASF do WM, configure-o usando os métodos IConfigAsfWriter se o perfil padrão não for adequado e conecte os Pins de entrada do gravador ASF do WM aos pins de saída correspondentes nos filtros upstream.</span><span class="sxs-lookup"><span data-stu-id="c4937-112">After adding the WM ASF Writer, configure it by using the IConfigAsfWriter methods if the default profile is not suitable, and connect the WM ASF Writer input pins to the corresponding output pins on the upstream filters.</span></span>

<span data-ttu-id="c4937-113">A ilustração a seguir mostra as configurações típicas de gráfico de filtro de transcodificação do gravador ASF do WM.</span><span class="sxs-lookup"><span data-stu-id="c4937-113">The following illustration shows typical WM ASF Writer transcoding filter graph configurations.</span></span>

![transcodificação do grafo de filtro](images/asf-transcode.png)

<span data-ttu-id="c4937-115">Inserindo formatos de fluxo nativos em arquivos ASF</span><span class="sxs-lookup"><span data-stu-id="c4937-115">Inserting Native Stream Formats Into ASF Files</span></span>

<span data-ttu-id="c4937-116">Por padrão, o filtro do gravador ASF do WM espera fluxos de áudio e vídeo descompactados em seus PINs de entrada e usa os codecs de vídeo do Windows Media Audio e Windows Media para compactar os fluxos.</span><span class="sxs-lookup"><span data-stu-id="c4937-116">By default, the WM ASF Writer filter expects uncompressed audio and video streams on its input pins, and uses the Windows Media Audio and Windows Media Video codecs to compress the streams.</span></span> <span data-ttu-id="c4937-117">No entanto, o contêiner do arquivo ASF pode ser usado para qualquer tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c4937-117">However, the ASF file container can be used for any type of data.</span></span> <span data-ttu-id="c4937-118">Ao colocar dados de mídia digital em um contêiner de arquivo ASF, você pode adicionar recursos fornecidos pelo ASF, como metadados e DRM (gerenciamento de direitos digitais), sem a necessidade de transcodificar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c4937-118">By placing digital media data into an ASF file container, you can add features provided by ASF, such as metadata and digital rights management (DRM), without having to transcode your content.</span></span>

<span data-ttu-id="c4937-119">Para criar um arquivo ASF que contém conteúdo que não é baseado no Windows Media, o aplicativo deve compactar o fluxo no fluxo do grafo de filtro do gravador ASF do WM e ignorar o mecanismo de compactação do gravador ASF do WM chamando [**IConfigAsfWriter2:: SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c4937-119">To create an ASF file that contains content that is not Windows Media–based, the application must compress the stream in the filter graph upstream of the WM ASF Writer and bypass the WM ASF Writer's compression mechanism by calling [**IConfigAsfWriter2::SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) as follows:</span></span>


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)
```



<span data-ttu-id="c4937-120">Em seguida, configure o filtro com o perfil desejado.</span><span class="sxs-lookup"><span data-stu-id="c4937-120">Then configure the filter with the desired profile.</span></span> <span data-ttu-id="c4937-121">É essencial que o tipo de mídia do fluxo de entrada corresponda exatamente ao formato no perfil.</span><span class="sxs-lookup"><span data-stu-id="c4937-121">It is essential that the media type of the input stream exactly matches the format in the profile.</span></span> <span data-ttu-id="c4937-122">Em alguns casos, pode ser necessário examinar o formato do fluxo de entrada e criar um perfil personalizado para fazer a correspondência.</span><span class="sxs-lookup"><span data-stu-id="c4937-122">In some cases, it may be necessary to examine the input stream's format, and create a custom profile to match it.</span></span>

<span data-ttu-id="c4937-123">Ao conectar o gravador ASF do WM ao filtro upstream, use o método IGraphBuilder:: ConnectDirect.</span><span class="sxs-lookup"><span data-stu-id="c4937-123">When you connect the WM ASF Writer to the upstream filter, use the IGraphBuilder::ConnectDirect method.</span></span> <span data-ttu-id="c4937-124">Não use nenhum método de "conexão inteligente" como IGraphBuilder:: Connect ou IGraphBuilder:: RenderFile para conectar o filtro, pois isso desabilitará o modo "ignorar compactação" do filtro.</span><span class="sxs-lookup"><span data-stu-id="c4937-124">Do not use any "intelligent connect" methods such as IGraphBuilder::Connect or IGraphBuilder::RenderFile to connect the filter because this will disable the filter's "bypass compression" mode.</span></span>

<span data-ttu-id="c4937-125">Capturando diretamente de um dispositivo para um arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="c4937-125">Capturing Directly from a Device to an ASF File</span></span>

<span data-ttu-id="c4937-126">Ao capturar áudio ou vídeo diretamente em um arquivo ASF, o grafo de filtro será semelhante ao seguinte, dependendo do tipo de dispositivo de captura que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="c4937-126">When capturing audio or video directly to an ASF file, the filter graph will look similar to the following, depending on the type of capture device being used.</span></span>

![Grafo de captura de vídeo do Windows Media](images/asf-webcam.png)

<span data-ttu-id="c4937-128">Para obter mais informações sobre como criar gráficos de captura de áudio e vídeo, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="c4937-128">For more information about creating video and audio capture graphs, see the following topics:</span></span>

-   [<span data-ttu-id="c4937-129">Captura de áudio</span><span class="sxs-lookup"><span data-stu-id="c4937-129">Audio Capture</span></span>](audio-capture.md)
-   [<span data-ttu-id="c4937-130">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="c4937-130">Video Capture</span></span>](video-capture.md)

<span data-ttu-id="c4937-131">O gravador ASF do WM não será executado, a menos que todos os seus PINs estejam conectados.</span><span class="sxs-lookup"><span data-stu-id="c4937-131">The WM ASF Writer will not run unless all of its pins are connected.</span></span> <span data-ttu-id="c4937-132">Se você configurar o gravador ASF do WM com o perfil de sistema padrão (não recomendado) ou qualquer perfil com fluxos de áudio e vídeo, ele criará um PIN de entrada para cada fluxo e cada um desses Pins deverá ser conectado.</span><span class="sxs-lookup"><span data-stu-id="c4937-132">If you configure the WM ASF Writer with the default system profile (not recommended), or any profile with audio and video streams, then it will create an input pin for each stream and each of those pins must be connected.</span></span> <span data-ttu-id="c4937-133">Se você não pretende capturar áudio, por exemplo, certifique-se de configurar o filtro com um perfil somente de vídeo para que nenhum PIN de áudio seja criado.</span><span class="sxs-lookup"><span data-stu-id="c4937-133">If you do not intend to capture audio, for example, then be sure to configure the filter with a video-only profile so that no audio pin is created.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4937-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c4937-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4937-135">Criando arquivos ASF no DirectShow</span><span class="sxs-lookup"><span data-stu-id="c4937-135">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



