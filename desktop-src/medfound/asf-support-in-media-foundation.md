---
description: Suporte a ASF no Media Foundation
ms.assetid: 4b0c4a83-623a-4378-9436-35ed120316af
title: Suporte a ASF no Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb7774d0ddaee592cb583ffb771c900642ed216
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105784614"
---
# <a name="asf-support-in-media-foundation"></a><span data-ttu-id="d9ac2-103">Suporte a ASF no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d9ac2-103">ASF Support in Media Foundation</span></span>

<span data-ttu-id="d9ac2-104">O Media Foundation dá suporte a arquivos de mídia no ASF (Advanced Systems Format):</span><span class="sxs-lookup"><span data-stu-id="d9ac2-104">Media Foundation supports media files in the Advanced Systems Format (ASF):</span></span>

-   <span data-ttu-id="d9ac2-105">Vídeo do Windows Media (arquivos WMV)</span><span class="sxs-lookup"><span data-stu-id="d9ac2-105">Windows Media Video (WMV files)</span></span>
-   <span data-ttu-id="d9ac2-106">Áudio do Windows Media (arquivos WMA)</span><span class="sxs-lookup"><span data-stu-id="d9ac2-106">Windows Media Audio (WMA files)</span></span>

<span data-ttu-id="d9ac2-107">O Media Foundation fornece vários objetos para ler e gravar arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="d9ac2-107">Media Foundation provides several objects for reading and writing ASF files.</span></span> <span data-ttu-id="d9ac2-108">Esses objetos são fornecidos em duas camadas de arquitetura diferentes.</span><span class="sxs-lookup"><span data-stu-id="d9ac2-108">These objects are provided in two different architectural layers.</span></span>

<span data-ttu-id="d9ac2-109">Primeiro, a camada de *pipeline* contém objetos que funcionam dentro do [pipeline de Media Foundation](media-foundation-pipeline.md) e estão em conformidade com as APIs definidas pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="d9ac2-109">First, the *pipeline* layer contains objects that work inside the [Media Foundation pipeline](media-foundation-pipeline.md) and conform to the APIs defined by the pipeline.</span></span> <span data-ttu-id="d9ac2-110">A camada de pipeline do ASF contém:</span><span class="sxs-lookup"><span data-stu-id="d9ac2-110">The ASF pipeline layer contains:</span></span>

-   <span data-ttu-id="d9ac2-111">[Fonte de mídia ASF](asf-media-source.md): analisa arquivos ASF e entrega os pacotes de dados de áudio/vídeo.</span><span class="sxs-lookup"><span data-stu-id="d9ac2-111">[ASF Media Source](asf-media-source.md): Parses ASF files and delivers the audio/video data packets.</span></span>
-   <span data-ttu-id="d9ac2-112">[Codecs de mídia do Windows](windows-media-codecs.md): decodificar ou codificar fluxos de áudio ou vídeo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d9ac2-112">[Windows Media Codecs](windows-media-codecs.md): Decode or encode Windows Media audio or video streams.</span></span>
-   <span data-ttu-id="d9ac2-113">[Coletor de mídia ASF](asf-media-sinks.md): recebe pacotes de dados e grava um arquivo asf.</span><span class="sxs-lookup"><span data-stu-id="d9ac2-113">[ASF Media Sink](asf-media-sinks.md): Receives data packets and writes an ASF file.</span></span>

<span data-ttu-id="d9ac2-114">Em segundo lugar, a camada de contêiner do WM fornece controle de baixo nível sobre a análise e a gravação de um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="d9ac2-114">Second, the WM Container layer provides low-level control over parsing and writing an ASF file.</span></span> <span data-ttu-id="d9ac2-115">A camada de pipeline usa WMContainer internamente.</span><span class="sxs-lookup"><span data-stu-id="d9ac2-115">The pipeline layer uses WMContainer internally.</span></span> <span data-ttu-id="d9ac2-116">Os aplicativos também podem usar WMContainer para análise e gravação de ASF de baixo nível.</span><span class="sxs-lookup"><span data-stu-id="d9ac2-116">Applications can also use WMContainer for low-level ASF parsing and writing.</span></span>

![diagrama mostrando elementos da camada de pipeline e do contêiner do WM](images/asf-components.png)

## <a name="in-this-section"></a><span data-ttu-id="d9ac2-118">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="d9ac2-118">In this section</span></span>



| <span data-ttu-id="d9ac2-119">Tópico</span><span class="sxs-lookup"><span data-stu-id="d9ac2-119">Topic</span></span>                                                                         | <span data-ttu-id="d9ac2-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="d9ac2-120">Description</span></span>                                                                                                        |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d9ac2-121">Estrutura de arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="d9ac2-121">ASF File Structure</span></span>](asf-file-structure.md)<br/>                       | <span data-ttu-id="d9ac2-122">Visão geral da estrutura do arquivo ASF e dos objetos fornecidos pelo Media Foundation para trabalhar com arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="d9ac2-122">Overview of the ASF file structure and the objects provided by Media Foundation to work with ASF files.</span></span><br/> |
| [<span data-ttu-id="d9ac2-123">Componentes ASF da camada de pipeline</span><span class="sxs-lookup"><span data-stu-id="d9ac2-123">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)<br/> | <span data-ttu-id="d9ac2-124">Descreve como analisar e criar arquivos ASF usando a camada de pipeline.</span><span class="sxs-lookup"><span data-stu-id="d9ac2-124">Describes how to parse and author ASF files using the pipeline layer.</span></span><br/>                                   |
| [<span data-ttu-id="d9ac2-125">Componentes ASF WMContainer</span><span class="sxs-lookup"><span data-stu-id="d9ac2-125">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)<br/>       | <span data-ttu-id="d9ac2-126">Descreve como analisar e criar arquivos ASF usando a camada WMContainer.</span><span class="sxs-lookup"><span data-stu-id="d9ac2-126">Describes how to parse and author ASF files using the WMContainer layer.</span></span><br/>                                |



 

<span data-ttu-id="d9ac2-127">Para obter informações detalhadas sobre a estrutura de um arquivo ASF, consulte a especificação do ASF, que pode ser baixada deste [site da Microsoft](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span><span class="sxs-lookup"><span data-stu-id="d9ac2-127">For detailed information about the structure of an ASF file, see the ASF specification, which can be downloaded from this [Microsoft website](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9ac2-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d9ac2-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9ac2-129">Guia de programação Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d9ac2-129">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 




