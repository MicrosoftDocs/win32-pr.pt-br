---
title: Inserindo formatos de fluxo nativos em arquivos ASF (QASF)
description: Inserindo formatos de fluxo nativos em arquivos ASF (QASF)
ms.assetid: ec7a69f3-0d4c-43dd-8d4b-fe066329a98f
keywords:
- SDK do Windows Media Format, formatos de fluxo nativos (QASF)
- SDK do Windows Media Format, inserindo formatos de fluxo nativos em arquivos ASF (QASF)
- SDK do Windows Media Format, DirectShow
- Formato de sistema avançado (ASF), inserção de formatos de fluxo nativos (QASF)
- ASF (formato de sistemas avançados), inserindo formatos de fluxo nativos (QASF)
- ASF (Advanced Systems Format), QASF (formatos de fluxo nativos)
- ASF (formato de sistemas avançados), formatos de fluxo nativos (QASF)
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- DirectShow, formatos de fluxo nativos (QASF)
- DirectShow, inserindo formatos de fluxo nativos em arquivos ASF (QASF)
- SDK do Windows Media Format, QASF
- ASF (Advanced Systems Format), QASF
- ASF (formato de sistemas avançados), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4736c450b3620a05fe01dcc1808adc297ebbd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822906"
---
# <a name="inserting-native-stream-formats-into-asf-files-qasf"></a><span data-ttu-id="ca095-118">Inserindo formatos de fluxo nativos em arquivos ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="ca095-118">Inserting Native Stream Formats Into ASF Files (QASF)</span></span>

<span data-ttu-id="ca095-119">Por padrão, o [gravador ASF do WM](wm-asf-writer-filter.md) espera fluxos de áudio e vídeo descompactados em seus PINs de entrada e usa o Windows Media Format SDK para acessar os codecs de vídeo do Windows Media Audio e Windows Media, que compactam os fluxos.</span><span class="sxs-lookup"><span data-stu-id="ca095-119">By default, the [WM ASF Writer](wm-asf-writer-filter.md) expects uncompressed audio and video streams on its input pins, and uses the Windows Media Format SDK to access the Windows Media Audio and Windows Media Video codecs, which compress the streams.</span></span> <span data-ttu-id="ca095-120">Mas o contêiner de arquivo ASF pode ser usado para qualquer tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ca095-120">But the ASF file container can be used for any type of data.</span></span> <span data-ttu-id="ca095-121">Ao colocar dados de mídia digital em um contêiner de arquivo ASF, você pode adicionar recursos fornecidos pelo ASF, como metadados e DRM (gerenciamento de direitos digitais), sem a necessidade de transcodificar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ca095-121">By placing digital media data into an ASF file container, you can add features provided by ASF, such as metadata and digital rights management (DRM), without having to transcode your content.</span></span>

<span data-ttu-id="ca095-122">Para criar um arquivo ASF que contém conteúdo que não é baseado no Windows Media, o aplicativo deve compactar o fluxo no fluxo do grafo de filtro do gravador ASF do WM e ignorar o mecanismo de compactação do gravador ASF do WM chamando [**IConfigAsfWriter2:: SetParam**](iconfigasfwriter2-setparam.md) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="ca095-122">To create an ASF file that contains content that is not Windows Media–based, the application must compress the stream in the filter graph upstream of the WM ASF Writer and bypass the WM ASF Writer's compression mechanism by calling [**IConfigAsfWriter2::SetParam**](iconfigasfwriter2-setparam.md) as follows:</span></span>


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)

```



<span data-ttu-id="ca095-123">Em seguida, configure o filtro com o perfil desejado.</span><span class="sxs-lookup"><span data-stu-id="ca095-123">Then configure the filter with the desired profile.</span></span> <span data-ttu-id="ca095-124">É essencial que o tipo de mídia do fluxo de entrada corresponda exatamente ao formato no perfil.</span><span class="sxs-lookup"><span data-stu-id="ca095-124">It is essential that the media type of the input stream exactly matches the format in the profile.</span></span> <span data-ttu-id="ca095-125">Em alguns casos, pode ser necessário examinar o formato do fluxo de entrada e criar um perfil personalizado para fazer a correspondência.</span><span class="sxs-lookup"><span data-stu-id="ca095-125">In some cases, it may be necessary to examine the input stream's format, and create a custom profile to match it.</span></span> <span data-ttu-id="ca095-126">Para obter mais informações, consulte [para criar arquivos ASF usando codecs de](to-create-asf-files-using-third-party-codecs.md)terceiros.</span><span class="sxs-lookup"><span data-stu-id="ca095-126">For more information, see [To Create ASF Files Using Third-Party Codecs](to-create-asf-files-using-third-party-codecs.md).</span></span>

<span data-ttu-id="ca095-127">Ao conectar o gravador ASF do WM ao filtro upstream, use o método **IGraphBuilder:: ConnectDirect** .</span><span class="sxs-lookup"><span data-stu-id="ca095-127">When you connect the WM ASF Writer to the upstream filter, use the **IGraphBuilder::ConnectDirect** method.</span></span> <span data-ttu-id="ca095-128">Não use nenhum método de "conexão inteligente" como **IGraphBuilder:: Connect** ou **IGraphBuilder:: RenderFile** para conectar o filtro, pois isso desabilitará o modo "ignorar compactação" do filtro.</span><span class="sxs-lookup"><span data-stu-id="ca095-128">Do not use any "intelligent connect" methods such as **IGraphBuilder::Connect** or **IGraphBuilder::RenderFile** to connect the filter because this will disable the filter's "bypass compression" mode.</span></span>

 

 




