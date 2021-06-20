---
title: Criando arquivos ASF no DirectShow (Windows Media Format SDK 11)
description: Saiba mais sobre como criar arquivos ASF no DirectShow usando o SDK Windows Media Format 11. ASF é um formato de contêiner que pode conter qualquer tipo de dados.
ms.assetid: 8b7af340-934d-43a9-88e9-7bbb2d3a38e0
keywords:
- Windows Media Format SDK, criando arquivos ASF no DirectShow
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), criando no DirectShow
- ASF (Formato de Sistemas Avançados), criando no DirectShow
- DirectShow, criando arquivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e06b6deb6dc9f07115f8143309d32dcf4a58a0f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406179"
---
# <a name="creating-asf-files-in-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="7094c-111">Criando arquivos ASF no DirectShow (Windows Media Format SDK 11)</span><span class="sxs-lookup"><span data-stu-id="7094c-111">Creating ASF Files in DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="7094c-112">Você pode usar o DirectShow para criar arquivos ASF diretamente de fontes de captura, como gravações DV ou para transcodificar outros arquivos em Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="7094c-112">You can use DirectShow to create ASF files directly from capture sources such as DV camcorders or to transcode other files into Windows Media Format.</span></span> <span data-ttu-id="7094c-113">Em qualquer cenário, os aplicativos criam grafos de filtro que incluem o filtro [Wm ASF Writer](wm-asf-writer-filter.md) como o renderdor.</span><span class="sxs-lookup"><span data-stu-id="7094c-113">In either scenario, applications create filter graphs that include the [WM ASF Writer](wm-asf-writer-filter.md) filter as the renderer.</span></span>

<span data-ttu-id="7094c-114">O Wm ASF Writer fornece um wrapper parcial para Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="7094c-114">The WM ASF Writer provides a partial wrapper for the Windows Media Format SDK.</span></span> <span data-ttu-id="7094c-115">Os aplicativos podem usar a interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) do filtro para passar um perfil do sistema (versões 4, 7 ou 8) ou usar o SDK do Windows Media Format diretamente para criar um perfil personalizado para passar para o filtro.</span><span class="sxs-lookup"><span data-stu-id="7094c-115">Applications can use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface of the filter to pass in a system profile (versions 4, 7, or 8), or use the Windows Media Format SDK directly to create a custom profile to pass to the filter.</span></span> <span data-ttu-id="7094c-116">Para adicionar metadados e outras informações de header, o aplicativo usa a interface [**IWMHeaderInfo,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) que pode ser obtida do filtro.</span><span class="sxs-lookup"><span data-stu-id="7094c-116">To add metadata and other header information, the application uses the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface, which can be obtained from the filter.</span></span> <span data-ttu-id="7094c-117">Depois que o perfil e os metadados foram configurados, o aplicativo pode simplesmente executar o grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="7094c-117">After the profile and metadata have been configured, the application can simply run the filter graph.</span></span> <span data-ttu-id="7094c-118">Internamente, o filtro usa o Windows Media Format SDK para gravar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="7094c-118">Internally, the filter uses the Windows Media Format SDK to write the file.</span></span> <span data-ttu-id="7094c-119">O filtro lida com todos os detalhes de sincronização de áudio e vídeo, que, de outra forma, seriam de responsabilidade do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7094c-119">The filter handles all the audio-video synchronization details, which would otherwise be the responsibility of the application.</span></span>

<span data-ttu-id="7094c-120">Esse processo é explicado mais detalhadamente nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="7094c-120">This process is explained in more detail in the following sections.</span></span>



| <span data-ttu-id="7094c-121">Seção</span><span class="sxs-lookup"><span data-stu-id="7094c-121">Section</span></span>                                                                                                           | <span data-ttu-id="7094c-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="7094c-122">Description</span></span>                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="7094c-123">Configurando o WM ASF Writer (QASF)</span><span class="sxs-lookup"><span data-stu-id="7094c-123">Configuring the WM ASF Writer (QASF)</span></span>](configuring-the-wm-asf-writer--qasf.md)                                   | <span data-ttu-id="7094c-124">Descreve como configurar o filtro Wm ASF Writer.</span><span class="sxs-lookup"><span data-stu-id="7094c-124">Describes how to configure the WM ASF Writer filter.</span></span>                                   |
| [<span data-ttu-id="7094c-125">Criando grafos de filtro para gravar arquivos ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="7094c-125">Building Filter Graphs to Write ASF Files (QASF)</span></span>](building-filter-graphs-to-write-asf-files--qasf.md)           | <span data-ttu-id="7094c-126">Descreve como criar grafos de transcodificação e captura de arquivo.</span><span class="sxs-lookup"><span data-stu-id="7094c-126">Describes how to create file-transcoding and capture graphs.</span></span>                           |
| [<span data-ttu-id="7094c-127">Configurando perfis e outras propriedades de arquivo (QASF)</span><span class="sxs-lookup"><span data-stu-id="7094c-127">Configuring Profiles and Other File Properties (QASF)</span></span>](configuring-profiles-and-other-file-properties--qasf.md) | <span data-ttu-id="7094c-128">Descreve como executar várias tarefas de configuração de arquivo ASF usando o Wm ASF Writer.</span><span class="sxs-lookup"><span data-stu-id="7094c-128">Describes how to perform various ASF file-configuration tasks using the WM ASF Writer.</span></span> |



 

 

 
