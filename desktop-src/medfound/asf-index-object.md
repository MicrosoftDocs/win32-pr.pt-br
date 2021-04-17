---
description: Indexador ASF
ms.assetid: 3f95b0ac-d70f-4bc2-8524-c7de1df34afa
title: Indexador ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c729b547339149ee578a90283c570ec8460b0c57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790503"
---
# <a name="asf-indexer"></a><span data-ttu-id="4e5bc-103">Indexador ASF</span><span class="sxs-lookup"><span data-stu-id="4e5bc-103">ASF Indexer</span></span>

<span data-ttu-id="4e5bc-104">O *indexador* ASF é um componente de camada WMContainer que é usado para ler ou gravar objetos de índice em um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="4e5bc-104">The ASF *indexer* is a WMContainer layer component that is used to read or write Index Objects in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="4e5bc-105">Para obter informações sobre a estrutura de um arquivo ASF, consulte [estrutura de arquivo ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="4e5bc-105">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="4e5bc-106">Um aplicativo pode usar o indexador para executar busca com base no tempo de apresentação ou gerar novas entradas de índice para um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="4e5bc-106">An application can use the indexer to perform seeking based on presentation time or to generate new index entries for an ASF file.</span></span> <span data-ttu-id="4e5bc-107">O indexador ASF implementa a interface [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) .</span><span class="sxs-lookup"><span data-stu-id="4e5bc-107">The ASF indexer implements the [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) interface.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4e5bc-108">Tipo de índice</span><span class="sxs-lookup"><span data-stu-id="4e5bc-108">Index type</span></span></th>
<th><span data-ttu-id="4e5bc-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e5bc-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4e5bc-110">Índice baseado em tempo de apresentação</span><span class="sxs-lookup"><span data-stu-id="4e5bc-110">Presentation time-based Index</span></span></td>
<td><span data-ttu-id="4e5bc-111">Fornece indexação baseada em tempo de apresentação para fluxos de áudio e vídeo em blocos de índice para tornar a indexação mais eficiente de espaço.</span><span class="sxs-lookup"><span data-stu-id="4e5bc-111">Provides presentation time-based indexing for audio and video streams in index blocks to make indexing more space efficient.</span></span> <span data-ttu-id="4e5bc-112">Cada bloco de índice faz referência a entradas de índice que contêm um deslocamento de byte.</span><span class="sxs-lookup"><span data-stu-id="4e5bc-112">Each index block references index entries that contain a byte offset.</span></span> <br/> <span data-ttu-id="4e5bc-113">O deslocamento é a posição do pacote de dados que está sendo buscado, em relação ao início do objeto de dados ASF.</span><span class="sxs-lookup"><span data-stu-id="4e5bc-113">The offset is the position of the data packet being seeked, relative to the start of the ASF Data Object.</span></span><br/> <span data-ttu-id="4e5bc-114">GUID_NULL deve ser usado como o tipo de GUID para o identificador de índice.</span><span class="sxs-lookup"><span data-stu-id="4e5bc-114">GUID_NULL must be used as the GUID type for the index identifier.</span></span> <span data-ttu-id="4e5bc-115">Para obter mais informações, consulte <a href="using-the-indexer-to-write-a-new-index.md">usando o indexador para gravar um novo índice</a>.</span><span class="sxs-lookup"><span data-stu-id="4e5bc-115">For more information; see <a href="using-the-indexer-to-write-a-new-index.md">Using the Indexer to Write a New Index</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e5bc-116">Índice de código de Code</span><span class="sxs-lookup"><span data-stu-id="4e5bc-116">Timecode Index</span></span></td>
<td><span data-ttu-id="4e5bc-117">Facilita a busca por código de meio em fluxos que contêm metadados de código de code.</span><span class="sxs-lookup"><span data-stu-id="4e5bc-117">Facilitates seeking by timecode in streams which contain timecode metadata.</span></span> <span data-ttu-id="4e5bc-118">Os códigos de tempo estão em conformidade com um formato SMPTE (<em>horas: minutos: segundos: quadros</em>).</span><span class="sxs-lookup"><span data-stu-id="4e5bc-118">The timecodes conform to a SMPTE format (<em>Hours:Minutes:Seconds:Frames</em>).</span></span> <span data-ttu-id="4e5bc-119">Cada bloco de índice faz referência a entradas de índice que contêm um deslocamento de byte.</span><span class="sxs-lookup"><span data-stu-id="4e5bc-119">Each index block references index entries that contain a byte offset.</span></span> <br/> <span data-ttu-id="4e5bc-120">O deslocamento é a posição do pacote de dados que está sendo buscado, em relação ao início do objeto de dados ASF.</span><span class="sxs-lookup"><span data-stu-id="4e5bc-120">The offset is the position of the data packet being seeked, relative to the start of the ASF Data Object.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4e5bc-121">No momento, não há suporte para objetos de índice de código de presente.</span><span class="sxs-lookup"><span data-stu-id="4e5bc-121">Timecode index objects are not currently supported.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e5bc-122">Índice baseado em quadros</span><span class="sxs-lookup"><span data-stu-id="4e5bc-122">Frame-based Index</span></span></td>
<td><span data-ttu-id="4e5bc-123">Fornece indexação baseada em quadros para fluxos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4e5bc-123">Provides frame-based indexing for video streams.</span></span> <span data-ttu-id="4e5bc-124">Os índices no índice baseado em quadros estão em termos de números de quadro, com o primeiro quadro para um fluxo no arquivo ASF correspondente à entrada 0 no objeto de índice baseado em quadros.</span><span class="sxs-lookup"><span data-stu-id="4e5bc-124">Indexes into the frame-based index are in terms of frame numbers, with the first frame for a stream in the ASF file corresponding to entry 0 in the frame-based index object.</span></span> <span data-ttu-id="4e5bc-125">Cada bloco de índice faz referência a entradas de índice que contêm um deslocamento de byte.</span><span class="sxs-lookup"><span data-stu-id="4e5bc-125">Each index block references index entries that contain a byte offset.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4e5bc-126">No momento, não há suporte para objetos de índice baseados em quadros.</span><span class="sxs-lookup"><span data-stu-id="4e5bc-126">Frame-based index objects are not currently supported.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4e5bc-127">Esta seção contém os seguintes tópicos.</span><span class="sxs-lookup"><span data-stu-id="4e5bc-127">This section contains the following topics.</span></span>



| <span data-ttu-id="4e5bc-128">Tópico</span><span class="sxs-lookup"><span data-stu-id="4e5bc-128">Topic</span></span>                                                                                | <span data-ttu-id="4e5bc-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e5bc-129">Description</span></span>                                                                                                                      |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e5bc-130">Criação e configuração do indexador</span><span class="sxs-lookup"><span data-stu-id="4e5bc-130">Indexer Creation and Configuration</span></span>](indexer-creation-and-configuration.md)         | <span data-ttu-id="4e5bc-131">Como criar um objeto de indexador e configurá-lo para ler um índice existente ou para gravar um novo objeto de índice ASF para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="4e5bc-131">How to create an indexer object and configure it for reading an existing index or for writing a new ASF Index Object for a file.</span></span> |
| [<span data-ttu-id="4e5bc-132">Usando o indexador para buscar em um arquivo</span><span class="sxs-lookup"><span data-stu-id="4e5bc-132">Using the Indexer to Seek in a File</span></span>](using-the-indexer-to-seek.md)                 | <span data-ttu-id="4e5bc-133">Como usar o indexador para buscar em um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="4e5bc-133">How to use the indexer to seek within an ASF file.</span></span>                                                                               |
| [<span data-ttu-id="4e5bc-134">Usando o indexador para gravar um novo índice</span><span class="sxs-lookup"><span data-stu-id="4e5bc-134">Using the Indexer to Write a New Index</span></span>](using-the-indexer-to-write-a-new-index.md) | <span data-ttu-id="4e5bc-135">Como usar o indexador para gerar entradas de índice e gravar um novo objeto de índice para um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="4e5bc-135">How to use the indexer to generate index entries and write a new Index Object for an ASF file.</span></span>                                   |



 

## <a name="related-topics"></a><span data-ttu-id="4e5bc-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e5bc-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e5bc-137">Componentes ASF WMContainer</span><span class="sxs-lookup"><span data-stu-id="4e5bc-137">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="4e5bc-138">Suporte a ASF no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4e5bc-138">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




