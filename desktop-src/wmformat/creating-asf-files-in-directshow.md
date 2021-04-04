---
title: Criando arquivos ASF no DirectShow (SDK do Windows Media Format 11)
description: Criando arquivos ASF no DirectShow
ms.assetid: 8b7af340-934d-43a9-88e9-7bbb2d3a38e0
keywords:
- SDK do Windows Media Format, criando arquivos ASF no DirectShow
- SDK do Windows Media Format, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), criando no DirectShow
- ASF (formato de sistemas avançados), criando no DirectShow
- DirectShow, criando arquivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbe4a6a37a508e5d7c713ae4cf38d771d075cefa
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085055"
---
# <a name="creating-asf-files-in-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="758dc-110">Criando arquivos ASF no DirectShow (SDK do Windows Media Format 11)</span><span class="sxs-lookup"><span data-stu-id="758dc-110">Creating ASF Files in DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="758dc-111">Você pode usar o DirectShow para criar arquivos ASF diretamente de fontes de captura, como camcorders DV, ou para transcodificar outros arquivos no formato de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="758dc-111">You can use DirectShow to create ASF files directly from capture sources such as DV camcorders or to transcode other files into Windows Media Format.</span></span> <span data-ttu-id="758dc-112">Em qualquer cenário, os aplicativos criam gráficos de filtro que incluem o filtro de [gravador ASF do WM](wm-asf-writer-filter.md) como o renderizador.</span><span class="sxs-lookup"><span data-stu-id="758dc-112">In either scenario, applications create filter graphs that include the [WM ASF Writer](wm-asf-writer-filter.md) filter as the renderer.</span></span>

<span data-ttu-id="758dc-113">O gravador ASF do WM fornece um wrapper parcial para o SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="758dc-113">The WM ASF Writer provides a partial wrapper for the Windows Media Format SDK.</span></span> <span data-ttu-id="758dc-114">Os aplicativos podem usar a interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) do filtro para passar um perfil do sistema (versões 4, 7 ou 8) ou usar o SDK do Windows Media Format diretamente para criar um perfil personalizado para passar para o filtro.</span><span class="sxs-lookup"><span data-stu-id="758dc-114">Applications can use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface of the filter to pass in a system profile (versions 4, 7, or 8), or use the Windows Media Format SDK directly to create a custom profile to pass to the filter.</span></span> <span data-ttu-id="758dc-115">Para adicionar metadados e outras informações de cabeçalho, o aplicativo usa a interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) , que pode ser obtida no filtro.</span><span class="sxs-lookup"><span data-stu-id="758dc-115">To add metadata and other header information, the application uses the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface, which can be obtained from the filter.</span></span> <span data-ttu-id="758dc-116">Depois que o perfil e os metadados tiverem sido configurados, o aplicativo poderá simplesmente executar o gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="758dc-116">After the profile and metadata have been configured, the application can simply run the filter graph.</span></span> <span data-ttu-id="758dc-117">Internamente, o filtro usa o Windows Media Format SDK para gravar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="758dc-117">Internally, the filter uses the Windows Media Format SDK to write the file.</span></span> <span data-ttu-id="758dc-118">O filtro manipula todos os detalhes de sincronização de áudio e vídeo, que de outra forma seria a responsabilidade do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="758dc-118">The filter handles all the audio-video synchronization details, which would otherwise be the responsibility of the application.</span></span>

<span data-ttu-id="758dc-119">Esse processo é explicado com mais detalhes nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="758dc-119">This process is explained in more detail in the following sections.</span></span>



| <span data-ttu-id="758dc-120">Seção</span><span class="sxs-lookup"><span data-stu-id="758dc-120">Section</span></span>                                                                                                           | <span data-ttu-id="758dc-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="758dc-121">Description</span></span>                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="758dc-122">Configurando o gravador ASF do WM (QASF)</span><span class="sxs-lookup"><span data-stu-id="758dc-122">Configuring the WM ASF Writer (QASF)</span></span>](configuring-the-wm-asf-writer--qasf.md)                                   | <span data-ttu-id="758dc-123">Descreve como configurar o filtro do gravador ASF do WM.</span><span class="sxs-lookup"><span data-stu-id="758dc-123">Describes how to configure the WM ASF Writer filter.</span></span>                                   |
| [<span data-ttu-id="758dc-124">Criando gráficos de filtro para gravar arquivos ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="758dc-124">Building Filter Graphs to Write ASF Files (QASF)</span></span>](building-filter-graphs-to-write-asf-files--qasf.md)           | <span data-ttu-id="758dc-125">Descreve como criar gráficos de transcodificação e captura de arquivos.</span><span class="sxs-lookup"><span data-stu-id="758dc-125">Describes how to create file-transcoding and capture graphs.</span></span>                           |
| [<span data-ttu-id="758dc-126">Configurando perfis e outras propriedades de arquivo (QASF)</span><span class="sxs-lookup"><span data-stu-id="758dc-126">Configuring Profiles and Other File Properties (QASF)</span></span>](configuring-profiles-and-other-file-properties--qasf.md) | <span data-ttu-id="758dc-127">Descreve como executar várias tarefas de configuração de arquivo ASF usando o gravador ASF do WM.</span><span class="sxs-lookup"><span data-stu-id="758dc-127">Describes how to perform various ASF file-configuration tasks using the WM ASF Writer.</span></span> |



 

 

 
