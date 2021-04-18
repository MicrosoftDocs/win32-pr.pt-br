---
description: Configurando o gravador ASF
ms.assetid: 5708c4a0-6197-4a42-adfd-01c6dfe86302
title: Configurando o gravador ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a6dfc1827743dce946188ebf9e050226b5c484
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105757026"
---
# <a name="configuring-the-asf-writer"></a><span data-ttu-id="77ecd-103">Configurando o gravador ASF</span><span class="sxs-lookup"><span data-stu-id="77ecd-103">Configuring the ASF Writer</span></span>

<span data-ttu-id="77ecd-104">Quando o filtro do [gravador ASF do WM](wm-asf-writer-filter.md) é criado, ele é configurado automaticamente com o \_ perfil WMProfile V80 \_ 256Video.</span><span class="sxs-lookup"><span data-stu-id="77ecd-104">When the [WM ASF Writer](wm-asf-writer-filter.md) filter is created, it is configured automatically with the WMProfile\_V80\_256Video profile.</span></span> <span data-ttu-id="77ecd-105">Esse perfil usa os codecs de áudio do Windows Media e Windows Media Video versão 8, que não são tão recentes quanto os codecs do Windows Media 9 Series.</span><span class="sxs-lookup"><span data-stu-id="77ecd-105">This profile uses the Windows Media Audio and Windows Media Video version 8 codecs, which are not as recent as the Windows Media 9 Series codecs.</span></span> <span data-ttu-id="77ecd-106">É recomendável criar um perfil personalizado que usa os codecs da série Windows Media 9 e configurar o gravador ASF do WM com o perfil personalizado, conforme descrito em [Configurando perfis e outras propriedades de arquivo ASF](configuring-profiles-and-other-asf-file-properties.md).</span><span class="sxs-lookup"><span data-stu-id="77ecd-106">It is recommended to create a custom profile that uses the Windows Media 9 Series codecs, and configure the WM ASF Writer with the custom profile, as described in [Configuring Profiles and Other ASF File Properties](configuring-profiles-and-other-asf-file-properties.md).</span></span> <span data-ttu-id="77ecd-107">Você deve adicionar o filtro do gravador ASF do WM ao grafo de filtro antes de configurar o filtro e configurar o filtro antes de conectá-lo a qualquer outro filtro.</span><span class="sxs-lookup"><span data-stu-id="77ecd-107">You must add the WM ASF Writer filter to the filter graph before configuring the filter, and configure the filter before connecting it to any other filters.</span></span>

<span data-ttu-id="77ecd-108">Todos os dados de entrada devem ter carimbo de data/hora e todos os Pins de entrada devem ser conectados antes que o filtro possa ser executado ou pausado.</span><span class="sxs-lookup"><span data-stu-id="77ecd-108">All input data must be time-stamped, and all input pins must be connected before the filter can be run or paused.</span></span> <span data-ttu-id="77ecd-109">Portanto, se você configurar o filtro com um perfil que tenha um fluxo de áudio e um fluxo de vídeo, o filtro criará um áudio e um pino de entrada de vídeo, e ambos os Pins deverão ser conectados antes que o filtro possa ser executado.</span><span class="sxs-lookup"><span data-stu-id="77ecd-109">Therefore, if you configure the filter with a profile that has an audio stream and a video stream, the filter will create an audio and a video input pin, and both pins must be connected before the filter can be run.</span></span> <span data-ttu-id="77ecd-110">Como o SDK do Windows Media format requer um fluxo de áudio para funcionar, o gravador ASF do WM sempre deve ter um PIN de áudio de entrada, mesmo se for para um fluxo fictício, ou seja, um fluxo de áudio com baixa taxa de bits sem áudio.</span><span class="sxs-lookup"><span data-stu-id="77ecd-110">Because the Windows Media Format SDK requires an audio stream to work, the WM ASF Writer must always have an input audio pin, even if it is for a dummy stream—that is, a muted, low-bit-rate audio stream.</span></span>

<span data-ttu-id="77ecd-111">Adicionando extensões de unidade de dados</span><span class="sxs-lookup"><span data-stu-id="77ecd-111">Adding Data Unit Extensions</span></span>

<span data-ttu-id="77ecd-112">Você pode configurar um fluxo de perfil para extensões de unidade de dados, como códigos de tempo SMPTE, antes ou depois que o filtro está conectado, desde que você siga esta ordem de operações:</span><span class="sxs-lookup"><span data-stu-id="77ecd-112">You can configure a profile stream for data unit extensions, such as SMPTE time codes, either before or after the filter is connected, as long as you follow this order of operations:</span></span>

1.  <span data-ttu-id="77ecd-113">Adicione uma ou mais extensões de unidade de dados ao fluxo usando **IWMStreamConfig2:: AddDataUnitExtension**.</span><span class="sxs-lookup"><span data-stu-id="77ecd-113">Add one or more data unit extensions to the stream using **IWMStreamConfig2::AddDataUnitExtension**.</span></span>
2.  <span data-ttu-id="77ecd-114">Chame **IWMProfile:: ReconfigStream** para atualizar o perfil.</span><span class="sxs-lookup"><span data-stu-id="77ecd-114">Call **IWMProfile::ReconfigStream** to update the profile.</span></span>
3.  <span data-ttu-id="77ecd-115">Chame [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) com o objeto de perfil atualizado.</span><span class="sxs-lookup"><span data-stu-id="77ecd-115">Call [**IConfigAsfWriter::ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) with the updated profile object.</span></span>
4.  <span data-ttu-id="77ecd-116">Localize o PIN de entrada de vídeo e chame o método [**IAMWMBufferPass:: setnotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) para registrar sua interface [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="77ecd-116">Find the video input pin, and call its [**IAMWMBufferPass::SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) method to register your application-defined [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) interface.</span></span>

<span data-ttu-id="77ecd-117">Quando o grafo for executado, o método [**IAMWMBufferPassCallback:: Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) será chamado para cada quadro e você poderá obter e definir propriedades no exemplo usando seus métodos de interface **INSSBuffer3** .</span><span class="sxs-lookup"><span data-stu-id="77ecd-117">When the graph runs, your [**IAMWMBufferPassCallback::Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) method will be called for each frame, and you will be able to get and set properties on the sample using its **INSSBuffer3** interface methods.</span></span>

> [!Note]  
> <span data-ttu-id="77ecd-118">Em alguns cenários com uso intensivo de processador, como o telecineon inverso, o gravador ASF do WM pode exigir mais buffers de saída do que alguns filtros downstream podem dar suporte.</span><span class="sxs-lookup"><span data-stu-id="77ecd-118">In some processor-intensive scenarios such as inverse telecine, the WM ASF Writer may require more output buffers than some downstream filters can support.</span></span> <span data-ttu-id="77ecd-119">O codificador DV, por exemplo, não aceitará mais de um buffer para seu pino de saída e o mesmo será verdadeiro para o descompactador AVI em determinadas condições.</span><span class="sxs-lookup"><span data-stu-id="77ecd-119">The DV Decoder, for example, will not accept more than one buffer for its output pin and the same is true for the AVI Decompressor in certain conditions.</span></span> <span data-ttu-id="77ecd-120">Se você encontrar problemas ao tentar se conectar a esses filtros, ou possivelmente ao executar o grafo, pode ser necessário gravar um filtro intermediário que aceite qualquer número de buffers em seu pino de saída.</span><span class="sxs-lookup"><span data-stu-id="77ecd-120">If you encounter problems when attempting to connect to these filters, or possibly when running the graph, it may be necessary to write an intermediary filter that accepts any number of buffers on its output pin.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="77ecd-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="77ecd-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77ecd-122">Criando arquivos ASF no DirectShow</span><span class="sxs-lookup"><span data-stu-id="77ecd-122">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



