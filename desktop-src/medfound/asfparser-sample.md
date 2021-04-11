---
description: Exemplo de ASFParser
ms.assetid: 6be1e12f-7d4a-4564-88ae-14fd71fd2cf9
title: Exemplo de ASFParser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c159b481e22d77b0bee9adccbbb74073398c12b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164221"
---
# <a name="asfparser-sample"></a><span data-ttu-id="67785-103">Exemplo de ASFParser</span><span class="sxs-lookup"><span data-stu-id="67785-103">ASFParser Sample</span></span>

<span data-ttu-id="67785-104">Mostra como analisar dados de um arquivo ASF (Advanced Systems Format) usando os componentes ASF de baixo nível no Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="67785-104">Shows how to parse data from an Advanced Systems Format (ASF) file by using the low-level ASF components in Media Foundation.</span></span> <span data-ttu-id="67785-105">O exemplo demonstra as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="67785-105">The sample demonstrates the following tasks:</span></span>

-   <span data-ttu-id="67785-106">Enumerando os fluxos de áudio e vídeo em um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="67785-106">Enumerating the audio and video streams in an ASF file.</span></span>
-   <span data-ttu-id="67785-107">Selecionando um fluxo de áudio ou de vídeo para análise.</span><span class="sxs-lookup"><span data-stu-id="67785-107">Selecting an audio or a video stream for parsing.</span></span>
-   <span data-ttu-id="67785-108">Procurando um pacote em um tempo de reprodução desejado.</span><span class="sxs-lookup"><span data-stu-id="67785-108">Seeking to a packet at a desired playback time.</span></span>
-   <span data-ttu-id="67785-109">Gerando amostras compactadas para o fluxo selecionado.</span><span class="sxs-lookup"><span data-stu-id="67785-109">Generating compressed samples for the selected stream.</span></span>
-   <span data-ttu-id="67785-110">Decodificando amostras de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="67785-110">Decoding audio and video samples.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="67785-111">APIs demonstradas</span><span class="sxs-lookup"><span data-stu-id="67785-111">APIs Demonstrated</span></span>

<span data-ttu-id="67785-112">Este exemplo demonstra as seguintes interfaces de Microsoft Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="67785-112">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="67785-113">**IMFASFContentInfo**</span><span class="sxs-lookup"><span data-stu-id="67785-113">**IMFASFContentInfo**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)
-   [<span data-ttu-id="67785-114">**IMFASFIndexer**</span><span class="sxs-lookup"><span data-stu-id="67785-114">**IMFASFIndexer**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer)
-   [<span data-ttu-id="67785-115">**IMFASFSplitter**</span><span class="sxs-lookup"><span data-stu-id="67785-115">**IMFASFSplitter**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter)

## <a name="usage"></a><span data-ttu-id="67785-116">Uso</span><span class="sxs-lookup"><span data-stu-id="67785-116">Usage</span></span>

1.  <span data-ttu-id="67785-117">Para abrir um arquivo ASF, clique no botão **Abrir arquivo de mídia...** .</span><span class="sxs-lookup"><span data-stu-id="67785-117">To open an ASF file, click the **Open Media File...** button.</span></span>
2.  <span data-ttu-id="67785-118">Selecione um arquivo ASF e clique em **abrir**.</span><span class="sxs-lookup"><span data-stu-id="67785-118">Select an ASF file and click **Open**.</span></span> <span data-ttu-id="67785-119">As informações sobre o arquivo são mostradas no painel de **informações** .</span><span class="sxs-lookup"><span data-stu-id="67785-119">Information about the file is shown on the **Information** pane.</span></span>
3.  <span data-ttu-id="67785-120">Em **configuração do analisador**, selecione um fluxo para analisar.</span><span class="sxs-lookup"><span data-stu-id="67785-120">Under **Parser Configuration**, select a stream to parse.</span></span>
4.  <span data-ttu-id="67785-121">Para gerar amostras em ordem inversa, selecione **Reverse**.</span><span class="sxs-lookup"><span data-stu-id="67785-121">To generate samples in reverse, select **Reverse**.</span></span>
5.  <span data-ttu-id="67785-122">Para especificar o ponto de partida, arraste o controle deslizante para o local desejado.</span><span class="sxs-lookup"><span data-stu-id="67785-122">To specify the start point, drag the slider to the desired location.</span></span>
6.  <span data-ttu-id="67785-123">Para iniciar a análise, clique no botão **gerar amostras** .</span><span class="sxs-lookup"><span data-stu-id="67785-123">To begin parsing, click the **Generate Samples** button.</span></span> <span data-ttu-id="67785-124">As informações sobre os exemplos são mostradas no painel de **informações** .</span><span class="sxs-lookup"><span data-stu-id="67785-124">Information about the samples is shown on the **Information** pane.</span></span>
7.  <span data-ttu-id="67785-125">Para testar os exemplos do fluxo de áudio, clique no botão **testar áudio** .</span><span class="sxs-lookup"><span data-stu-id="67785-125">To test the samples for the audio stream, click the **Test Audio** button.</span></span>
8.  <span data-ttu-id="67785-126">Para testar os exemplos do fluxo de vídeo, clique no botão **Mostrar bitmap** .</span><span class="sxs-lookup"><span data-stu-id="67785-126">To test the samples for the video stream, click the **Show Bitmap** button.</span></span>

## <a name="requirements"></a><span data-ttu-id="67785-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67785-127">Requirements</span></span>



| <span data-ttu-id="67785-128">Produto</span><span class="sxs-lookup"><span data-stu-id="67785-128">Product</span></span>                                                        | <span data-ttu-id="67785-129">Versão</span><span class="sxs-lookup"><span data-stu-id="67785-129">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="67785-130">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="67785-130">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="67785-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="67785-131">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="67785-132">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="67785-132">Downloading the Sample</span></span>

<span data-ttu-id="67785-133">Este exemplo está disponível no [repositório GitHub de exemplos clássicos do Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/asfparser).</span><span class="sxs-lookup"><span data-stu-id="67785-133">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/asfparser).</span></span>

## <a name="related-topics"></a><span data-ttu-id="67785-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="67785-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67785-135">Exemplos de SDK do Media Foundation</span><span class="sxs-lookup"><span data-stu-id="67785-135">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="67785-136">Suporte a ASF no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="67785-136">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="67785-137">Tutorial: lendo um arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="67785-137">Tutorial: Reading an ASF File</span></span>](tutorial--reading-an-asf-file.md)
</dt> <dt>

[<span data-ttu-id="67785-138">Componentes ASF WMContainer</span><span class="sxs-lookup"><span data-stu-id="67785-138">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> </dl>

 

 



