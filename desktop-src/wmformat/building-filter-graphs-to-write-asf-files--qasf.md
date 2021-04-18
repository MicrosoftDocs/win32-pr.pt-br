---
title: Criando gráficos de filtro para gravar arquivos ASF (QASF)
description: Criando gráficos de filtro para gravar arquivos ASF (QASF)
ms.assetid: 45583c97-4e59-4a6a-987b-5486e6f33990
keywords:
- SDK do Windows Media Format, criando gráficos de filtro (QASF)
- SDK do Windows Media Format, DirectShow
- Windows Media Format SDK, gravando arquivos ASF (QASF)
- ASF (Advanced Systems Format), criando gráficos de filtro (QASF)
- ASF (formato de sistemas avançados), criando gráficos de filtro (QASF)
- ASF (Advanced Systems Format), gravação (QASF)
- ASF (formato de sistemas avançados), gravação (QASF)
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- DirectShow, criação de gráficos de filtro (QASF)
- DirectShow, gravando arquivos ASF (QASF)
- SDK do Windows Media Format, QASF
- ASF (Advanced Systems Format), QASF
- ASF (formato de sistemas avançados), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbf0a261d1502f76cebc0eb2141cd230c509029
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105764236"
---
# <a name="building-filter-graphs-to-write-asf-files-qasf"></a><span data-ttu-id="6b765-118">Criando gráficos de filtro para gravar arquivos ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="6b765-118">Building Filter Graphs to Write ASF Files (QASF)</span></span>

<span data-ttu-id="6b765-119">Aplicativos baseados no DirectShow normalmente usam um dos três tipos básicos de grafos de filtro ao criar conteúdo baseado no Windows Media:</span><span class="sxs-lookup"><span data-stu-id="6b765-119">Applications based on DirectShow typically use one of three basic types of filter graphs when creating Windows Media–based content:</span></span>

-   <span data-ttu-id="6b765-120">Filtrar grafos para converter ou transcodificar conteúdo de outro formato no formato de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="6b765-120">Filter graphs for converting or transcoding content from some other format into Windows Media Format.</span></span>
-   <span data-ttu-id="6b765-121">Filtrar grafos para inserir conteúdo que não seja baseado no Windows Media (formatos de fluxo nativos) em arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="6b765-121">Filter graphs for inserting content that is not Windows Media-based (native stream formats) into ASF files.</span></span>
-   <span data-ttu-id="6b765-122">Filtrar grafos para capturar dados dinâmicos e codificá-los imediatamente no formato de mídia do Windows antes de salvá-los no disco.</span><span class="sxs-lookup"><span data-stu-id="6b765-122">Filter graphs for capturing live data and encoding it immediately into Windows Media Format before saving it to disk.</span></span>

<span data-ttu-id="6b765-123">Cada tipo de grafo de filtro é descrito mais detalhadamente nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="6b765-123">Each type of filter graph is described in more detail in the following sections.</span></span>



| <span data-ttu-id="6b765-124">Seção</span><span class="sxs-lookup"><span data-stu-id="6b765-124">Section</span></span>                                                                                                             | <span data-ttu-id="6b765-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b765-125">Description</span></span>                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b765-126">Transcodificação de arquivos (QASF)</span><span class="sxs-lookup"><span data-stu-id="6b765-126">Transcoding Files (QASF)</span></span>](transcoding-files--qasf.md)                                                             | <span data-ttu-id="6b765-127">Descreve como criar gráficos de filtro de transcodificação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6b765-127">Describes how to create file-transcoding filter graphs.</span></span>                                               |
| [<span data-ttu-id="6b765-128">Inserindo formatos de fluxo nativos em arquivos ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="6b765-128">Inserting Native Stream Formats Into ASF Files (QASF)</span></span>](inserting-native-stream-formats-into-asf-files--qasf.md)   | <span data-ttu-id="6b765-129">Descreve como posicionar qualquer tipo de áudio compactado ou não compactado ou dados de vídeo em um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="6b765-129">Describes how to place any type of compressed or non-compressed audio or video data into an ASF file.</span></span> |
| [<span data-ttu-id="6b765-130">Capturando diretamente de um dispositivo para um arquivo ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="6b765-130">Capturing Directly from a Device to an ASF File (QASF)</span></span>](capturing-directly-from-a-device-to-an-asf-file--qasf.md) | <span data-ttu-id="6b765-131">Descreve como criar gráficos de filtro de captura que geram saída para um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="6b765-131">Describes how to create capture filter graphs that output to an ASF file.</span></span>                             |



 

 

 




