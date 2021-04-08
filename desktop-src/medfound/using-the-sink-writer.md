---
description: .
ms.assetid: BE89E2E0-711F-4BD5-BB86-AA4CCA2D3E7F
title: Usando o gravador do coletor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46157eae6fe851468515f9d9653adb33918ebb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921348"
---
# <a name="using-the-sink-writer"></a><span data-ttu-id="c2cc3-103">Usando o gravador do coletor</span><span class="sxs-lookup"><span data-stu-id="c2cc3-103">Using the Sink Writer</span></span>

## <a name="overview"></a><span data-ttu-id="c2cc3-104">Visão geral</span><span class="sxs-lookup"><span data-stu-id="c2cc3-104">Overview</span></span>

### <a name="file-container-types"></a><span data-ttu-id="c2cc3-105">Tipos de contêiner de arquivo</span><span class="sxs-lookup"><span data-stu-id="c2cc3-105">File Container Types</span></span>

<span data-ttu-id="c2cc3-106">O gravador do coletor tem suporte interno para vários tipos de contêineres de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-106">The sink writer has built-in support for several file container types.</span></span> <span data-ttu-id="c2cc3-107">Para obter uma lista completa, confira o [ \_ \_ contêiner de codificação MF](mf-transcode-containertype.md).</span><span class="sxs-lookup"><span data-stu-id="c2cc3-107">For a complete list, see [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md).</span></span> <span data-ttu-id="c2cc3-108">Você pode dar suporte a tipos de contêineres adicionais escrevendo um [coletor de mídia](media-sinks.md)personalizado.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-108">You can support additional container types by writing a custom [media sink](media-sinks.md).</span></span> <span data-ttu-id="c2cc3-109">O contêiner de arquivo é especificado quando você cria uma nova instância do gravador de coletor.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-109">The file container is specified when you create a new instance of the sink writer.</span></span>

### <a name="stream-formats"></a><span data-ttu-id="c2cc3-110">Formatos de fluxo</span><span class="sxs-lookup"><span data-stu-id="c2cc3-110">Stream Formats</span></span>

<span data-ttu-id="c2cc3-111">Para cada fluxo, o aplicativo deve especificar o seguinte.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-111">For each stream, the application must specify the following.</span></span>

-   <span data-ttu-id="c2cc3-112">O *formato de entrada* é o formato que o aplicativo envia para o gravador do coletor.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-112">The *input format* is the format that the application sends to the sink writer.</span></span>
-   <span data-ttu-id="c2cc3-113">O *formato de saída* é o formato que será gravado no arquivo.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-113">The *output format* is the format that will be written to the file.</span></span>

<span data-ttu-id="c2cc3-114">Os formatos de entrada e saída podem ser compactados ou descompactados.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-114">The input and output formats can be either compressed or uncompressed.</span></span> <span data-ttu-id="c2cc3-115">O gravador do coletor dá suporte às seguintes combinações:</span><span class="sxs-lookup"><span data-stu-id="c2cc3-115">The sink writer supports the following combinations:</span></span>

-   <span data-ttu-id="c2cc3-116">Entrada não compactada com saída compactada.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-116">Uncompressed input with compressed output.</span></span> <span data-ttu-id="c2cc3-117">Esse é o caso típico e é usado para cenários de codificação ou transcodificação.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-117">This is the typical case, and is used for encoding or transcoding scenarios.</span></span> <span data-ttu-id="c2cc3-118">Um codificador de Microsoft Media Foundation deve estar disponível para aceitar o tipo de entrada e codificar para o tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-118">A Microsoft Media Foundation encoder must be available that accepts the input type and encodes to the output type.</span></span>
-   <span data-ttu-id="c2cc3-119">Entrada compactada com saída idêntica.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-119">Compressed input with identical output.</span></span> <span data-ttu-id="c2cc3-120">Use essa combinação para remux um arquivo sem transcodificação.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-120">Use this combination to remux a file without transcoding.</span></span>
-   <span data-ttu-id="c2cc3-121">Entrada não compactada com saída idêntica.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-121">Uncompressed input with identical output.</span></span> <span data-ttu-id="c2cc3-122">Use essa combinação para gravar áudio ou vídeo não compactado em um contêiner de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-122">Use this combination to write uncompressed audio or video to a file container.</span></span>

<span data-ttu-id="c2cc3-123">O gravador de coletor não dá suporte ao redimensionamento de vídeo, conversão de taxa de quadros ou reamostragem de áudio, a menos que essas funções sejam fornecidas pelo codificador.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-123">The sink writer does not support video resizing, frame-rate conversion, or audio resampling, unless these functions are provided by the encoder.</span></span> <span data-ttu-id="c2cc3-124">Caso contrário, o aplicativo pode usar [processadores de sinal digital](windowsmediadigitalsignalprocessors.md) para converter os dados de entrada, antes de enviar os dados para o</span><span class="sxs-lookup"><span data-stu-id="c2cc3-124">Otherwise, the application can use [Digital Signal Processors](windowsmediadigitalsignalprocessors.md) to convert the input data, before sending the data to the</span></span>

## <a name="creating-the-sink-writer"></a><span data-ttu-id="c2cc3-125">Criando o gravador do coletor</span><span class="sxs-lookup"><span data-stu-id="c2cc3-125">Creating the Sink Writer</span></span>

<span data-ttu-id="c2cc3-126">Há duas funções que criam o gravador de coletor:</span><span class="sxs-lookup"><span data-stu-id="c2cc3-126">There are two functions that create the sink writer:</span></span>

-   <span data-ttu-id="c2cc3-127">[**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) Obtém a URL de um arquivo de saída ou um ponteiro para um fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-127">[**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) takes the URL of an output file or a pointer to a byte stream.</span></span> <span data-ttu-id="c2cc3-128">Essa função cria o coletor de mídia internamente.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-128">This function creates the media sink internally.</span></span>
-   <span data-ttu-id="c2cc3-129">[**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) usa um ponteiro para um coletor de mídia que já foi criado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-129">[**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) takes a pointer to a media sink that has already been created by the application.</span></span>

<span data-ttu-id="c2cc3-130">Se você estiver usando um dos coletores de mídia internos, a função [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) é preferível, pois o chamador não precisa configurar o coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-130">If you are using one of the built-in media sinks, the [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) function is preferable, because the caller does not need to configure the media sink.</span></span>

<span data-ttu-id="c2cc3-131">O método [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) fornece várias opções para especificar o tipo de contêiner de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-131">The [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) method provides several options for specifying the type of file container.</span></span> <span data-ttu-id="c2cc3-132">No caso mais simples, a função usa a extensão de nome de arquivo na URL para selecionar o contêiner de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-132">In the simplest case, the function uses the file name extension in the URL to select the file container.</span></span> <span data-ttu-id="c2cc3-133">Para obter detalhes, consulte a página de referência da função.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-133">For details, refer to the function reference page.</span></span>

<span data-ttu-id="c2cc3-134">Por exemplo, o código a seguir especifica o nome do arquivo "output. wmv" para a URL.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-134">For example, the following code specifies the file name "output.wmv" for the URL.</span></span> <span data-ttu-id="c2cc3-135">Com base na extensão de nome de arquivo, o gravador de coletor carregará o [coletor de mídia ASF](asf-media-sinks.md) para criar um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="c2cc3-135">Based on the file name extension, the sink writer will load the [ASF Media Sink](asf-media-sinks.md) to create an Advanced Systems Format (ASF) file.</span></span>


```C++
    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);
```



<span data-ttu-id="c2cc3-136">No caso do [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink), o tipo de arquivo é determinado pelo coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-136">In the case of [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink), the file type is determined by the media sink.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2cc3-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c2cc3-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2cc3-138">Gravador do coletor</span><span class="sxs-lookup"><span data-stu-id="c2cc3-138">Sink Writer</span></span>](sink-writer.md)
</dt> </dl>

 

 



