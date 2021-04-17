---
description: Gravando um arquivo de mídia do Windows no DES
ms.assetid: 741ebcbc-62fb-4c7f-845f-a361f5b63f8c
title: Gravando um arquivo de mídia do Windows no DES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0626a3ef609dee87d90a6d3c2caa023e9ac9a29a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105761745"
---
# <a name="writing-a-windows-media-file-in-des"></a><span data-ttu-id="063ae-103">Gravando um arquivo de mídia do Windows no DES</span><span class="sxs-lookup"><span data-stu-id="063ae-103">Writing a Windows Media File in DES</span></span>

<span data-ttu-id="063ae-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="063ae-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="063ae-105">Esta seção descreve como gravar um arquivo do Windows Media usando o des ( [serviços de edição do DirectShow](directshow-editing-services.md) ).</span><span class="sxs-lookup"><span data-stu-id="063ae-105">This section describes how to write a Windows Media file using [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="063ae-106">Não use o mecanismo de processamento inteligente para gravar arquivos de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="063ae-106">Do not use the Smart Render Engine to write Windows Media files.</span></span> <span data-ttu-id="063ae-107">Sempre use o mecanismo de processamento básico (CLSID \_ RenderEngine).</span><span class="sxs-lookup"><span data-stu-id="063ae-107">Always use the Basic Render Engine (CLSID\_RenderEngine).</span></span>

 

<span data-ttu-id="063ae-108">Para gravar um arquivo do Windows Media, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="063ae-108">To write a Windows Media file, do the following:</span></span>

1.  <span data-ttu-id="063ae-109">Chame **SetSite** no mecanismo de processamento, com um ponteiro para o provedor de chave.</span><span class="sxs-lookup"><span data-stu-id="063ae-109">Call **SetSite** on the render engine, with a pointer to your key provider.</span></span>
2.  <span data-ttu-id="063ae-110">Crie o front-end do grafo.</span><span class="sxs-lookup"><span data-stu-id="063ae-110">Build the front end of the graph.</span></span> <span data-ttu-id="063ae-111">(Consulte [renderizando um projeto](rendering-a-project.md).)</span><span class="sxs-lookup"><span data-stu-id="063ae-111">(See [Rendering a Project](rendering-a-project.md).)</span></span>
3.  <span data-ttu-id="063ae-112">Crie o filtro do [gravador ASF do WM](wm-asf-writer-filter.md) e adicione-o ao grafo.</span><span class="sxs-lookup"><span data-stu-id="063ae-112">Create the [WM ASF Writer](wm-asf-writer-filter.md) filter and add it to the graph.</span></span>
4.  <span data-ttu-id="063ae-113">Use a interface [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) no filtro do gravador ASF do WM para definir o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="063ae-113">Use the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface on the WM ASF Writer filter to set the file name.</span></span>
5.  <span data-ttu-id="063ae-114">Configure o gravador ASF do WM para usar um perfil do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="063ae-114">Configure the WM ASF Writer to use a Windows Media profile.</span></span> <span data-ttu-id="063ae-115">Cada perfil tem um número predefinido de fluxos.</span><span class="sxs-lookup"><span data-stu-id="063ae-115">Each profile has a predefined number of streams.</span></span> <span data-ttu-id="063ae-116">Você deve escolher um perfil que corresponda aos grupos em seu projeto.</span><span class="sxs-lookup"><span data-stu-id="063ae-116">You must choose a profile that matches the groups in your project.</span></span>

    <span data-ttu-id="063ae-117">A interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) contém alguns métodos diferentes para definir o perfil.</span><span class="sxs-lookup"><span data-stu-id="063ae-117">The [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) interface contains a few different methods for setting the profile.</span></span> <span data-ttu-id="063ae-118">Por exemplo, o método **ConfigureFilterUsingProfileGuid** especifica um perfil de sistema como um GUID.</span><span class="sxs-lookup"><span data-stu-id="063ae-118">For example, the **ConfigureFilterUsingProfileGuid** method specifies a system profile as a GUID.</span></span> <span data-ttu-id="063ae-119">Ou, você pode usar os métodos de formato de mídia do Windows para obter um ponteiro **IWMProfile** e, em seguida, chamar [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile).</span><span class="sxs-lookup"><span data-stu-id="063ae-119">Or, you can use Windows Media Format methods to get an **IWMProfile** pointer and then call [**IConfigAsfWriter::ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile).</span></span> <span data-ttu-id="063ae-120">Para obter mais informações, consulte [Configurando o gravador ASF](configuring-the-asf-writer.md).</span><span class="sxs-lookup"><span data-stu-id="063ae-120">For more information, see [Configuring the ASF Writer](configuring-the-asf-writer.md).</span></span>

6.  <span data-ttu-id="063ae-121">Conecte o front-end ao gravador ASF.</span><span class="sxs-lookup"><span data-stu-id="063ae-121">Connect the front end to the ASF Writer.</span></span> <span data-ttu-id="063ae-122">O front-end do grafo contém um pino de saída para cada grupo.</span><span class="sxs-lookup"><span data-stu-id="063ae-122">The front end of the graph contains one output pin for each group.</span></span> <span data-ttu-id="063ae-123">Supondo que você especificou um perfil compatível, o gravador ASF deve ter um conjunto correspondente de Pins de entrada.</span><span class="sxs-lookup"><span data-stu-id="063ae-123">Assuming that you specified a compatible profile, the ASF Writer should have a matching set of input pins.</span></span> <span data-ttu-id="063ae-124">Conecte cada pino de saída ao PIN de entrada correspondente.</span><span class="sxs-lookup"><span data-stu-id="063ae-124">Connect each output pin to the corresponding input pin.</span></span> <span data-ttu-id="063ae-125">A maneira mais fácil de fazer isso é usando o método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) .</span><span class="sxs-lookup"><span data-stu-id="063ae-125">The easiest way to do this is using the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method.</span></span> <span data-ttu-id="063ae-126">Primeiro, crie uma nova instância do [construtor do grafo de captura](capture-graph-builder.md) e inicialize-a com um ponteiro para o Gerenciador do grafo de filtro:</span><span class="sxs-lookup"><span data-stu-id="063ae-126">First, create a new instance of the [Capture Graph Builder](capture-graph-builder.md) and initialize it with a pointer to the Filter Graph Manager:</span></span>

    ```C++
    ICaptureGraphBuilder2 *pBuild = 0;
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 0, CLSCTX_INPROC_SERVER,
        IID_ICaptureGraphBuilder2, (void**)&pBuild);
    pBuild->SetFiltergraph(pGraph); 
    ```

    

    <span data-ttu-id="063ae-127">Em seguida, recupere o pino de saída para cada grupo chamando o método [**IRenderEngine:: GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="063ae-127">Next, retrieve the output pin for each group by calling the [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) method.</span></span> <span data-ttu-id="063ae-128">Chame **RenderStream** para conectar o PIN ao gravador ASF:</span><span class="sxs-lookup"><span data-stu-id="063ae-128">Call **RenderStream** to connect the pin to the ASF Writer:</span></span>

    ```C++
    long cGroups = 0;
    hr = pTimeline->GetGroupCount(&cGroups);
    for (long i = 0; i < cGroups; i++)
    {
        IPin *pPin;
        hr = pRenderEngine->GetGroupOutputPin(i, &pPin);
        if (SUCCEEDED(hr))
        {
            hr = pBuild->RenderStream(0, 0, pPin, 0, pASF);
        }
        pPin->Release();
    }
    pBuild->Release
    ```

    

## <a name="related-topics"></a><span data-ttu-id="063ae-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="063ae-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="063ae-130">Usando o Windows Media com os serviços de edição do DirectShow</span><span class="sxs-lookup"><span data-stu-id="063ae-130">Using Windows Media With DirectShow Editing Services</span></span>](using-windows-media-with-directshow-editing-services.md)
</dt> </dl>

 

 



