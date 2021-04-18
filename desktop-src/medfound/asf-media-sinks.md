---
description: O coletor de mídia ASF é o componente final no pipeline de codificação que permite que um aplicativo grave um arquivo ASF.
ms.assetid: 65bb8822-5eb0-46a3-ab9e-c55ae466e982
title: Coletores de mídia ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6bcd3e6b91403185342607e8c4374eb32069c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105759159"
---
# <a name="asf-media-sinks"></a><span data-ttu-id="b177f-103">Coletores de mídia ASF</span><span class="sxs-lookup"><span data-stu-id="b177f-103">ASF Media Sinks</span></span>

<span data-ttu-id="b177f-104">O coletor de mídia ASF é o componente final no pipeline de codificação que permite que um aplicativo grave um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="b177f-104">The ASF media sink is the final component in the encoding pipeline that enables an application to write an ASF file.</span></span>

<span data-ttu-id="b177f-105">Media Foundation fornece dois tipos de coletores de mídia ASF:</span><span class="sxs-lookup"><span data-stu-id="b177f-105">Media Foundation provides two types of ASF media sinks:</span></span>

-   <span data-ttu-id="b177f-106">O *coletor de arquivos ASF* é usado para arquivar dados de mídia ASF em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="b177f-106">*ASF file sink* is used to archive ASF media data to a file.</span></span>
-   <span data-ttu-id="b177f-107">O *coletor de streaming ASF* é usado para gravar conteúdo ASF em um fluxo de bytes que pode ser transmitido pela rede.</span><span class="sxs-lookup"><span data-stu-id="b177f-107">*ASF streaming sink* is used to write ASF content in a byte stream that can be streamed across the network.</span></span>

<span data-ttu-id="b177f-108">Os coletores de mídia ASF contêm um ou mais coletores de fluxo, que representam os dados a serem gravados para cada fluxo no arquivo ASF de saída.</span><span class="sxs-lookup"><span data-stu-id="b177f-108">ASF media sinks contain one or more stream sinks, which represents the data to write for each stream in the output ASF file.</span></span> <span data-ttu-id="b177f-109">Para codificar aplicativos executados no Windows Vista, você deve configurar manualmente a topologia de codificação criando e Configurando o coletor de mídia ASF e, em seguida, adicionando-o à topologia.</span><span class="sxs-lookup"><span data-stu-id="b177f-109">For encoding applications that run on Windows Vista, you must manually configure the encoding topology by creating and configuring the ASF media sink and then adding it to the topology.</span></span> <span data-ttu-id="b177f-110">No Windows 7, se você estiver usando os objetos de transcodificação rápida para criar a topologia, você não terá criar o coletor de mídia diretamente e o aplicativo não chamará nenhum método no coletor de mídia ou qualquer um dos coletores de fluxo.</span><span class="sxs-lookup"><span data-stu-id="b177f-110">In Windows 7, if you are using the fast transcode objects to create the topology, you do not have create the media sink directly and the application does not call any methods on the media sink or any of the stream sinks.</span></span> <span data-ttu-id="b177f-111">Os objetos de transcodificação rápida instanciam os coletores de mídia necessários e os adicionam à topologia antes de retornar uma referência ao aplicativo chamador.</span><span class="sxs-lookup"><span data-stu-id="b177f-111">The fast transcode objects instantiate the required media sinks and add it to the topology before returning a reference to the caller application.</span></span> <span data-ttu-id="b177f-112">No entanto, para objetos de transcodificação rápidos, há algumas restrições que se aplicam dependendo do tipo de codificação.</span><span class="sxs-lookup"><span data-stu-id="b177f-112">However for fast transcode objects, there are some restrictions that apply depending on the type of encoding.</span></span>

-   [<span data-ttu-id="b177f-113">Modelo de objeto de coletor de mídia ASF</span><span class="sxs-lookup"><span data-stu-id="b177f-113">ASF Media Sink Object Model</span></span>](#asf-media-sink-object-model)
-   [<span data-ttu-id="b177f-114">Coletor de arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="b177f-114">ASF File Sink</span></span>](#asf-file-sink)
-   [<span data-ttu-id="b177f-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b177f-115">Related topics</span></span>](#related-topics)

## <a name="asf-media-sink-object-model"></a><span data-ttu-id="b177f-116">Modelo de objeto de coletor de mídia ASF</span><span class="sxs-lookup"><span data-stu-id="b177f-116">ASF Media Sink Object Model</span></span>

<span data-ttu-id="b177f-117">Os coletores de mídia ASF implementam a interface [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) e expõem as interfaces a seguir.</span><span class="sxs-lookup"><span data-stu-id="b177f-117">ASF media sinks implement the [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) interface and exposes the following interfaces.</span></span> <span data-ttu-id="b177f-118">Um aplicativo pode obter uma referência a essas interfaces chamando [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no coletor de mídia do ASF que está usando para gerar amostras de saída.</span><span class="sxs-lookup"><span data-stu-id="b177f-118">An application can get a reference to these interfaces by calling [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the ASF media sink it is using for generating output samples.</span></span>



| <span data-ttu-id="b177f-119">Interface</span><span class="sxs-lookup"><span data-stu-id="b177f-119">Interface</span></span>                                                  | <span data-ttu-id="b177f-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="b177f-120">Description</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b177f-121">**IMFMediaSink**</span><span class="sxs-lookup"><span data-stu-id="b177f-121">**IMFMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)                       | <span data-ttu-id="b177f-122">Necessário para todos os coletores de mídia.</span><span class="sxs-lookup"><span data-stu-id="b177f-122">Required for all media sinks.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="b177f-123">**IMFFinalizableMediaSink**</span><span class="sxs-lookup"><span data-stu-id="b177f-123">**IMFFinalizableMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink) | <span data-ttu-id="b177f-124">Implementado pelo coletor de arquivo ASF que grava o conteúdo de mídia gerado em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="b177f-124">Implemented by the ASF file sink that writes the generated media content to a file.</span></span> <span data-ttu-id="b177f-125">Você pode usar os métodos nessa interface para liberar dados e atualizar o objeto de cabeçalho ASF do arquivo de saída final.</span><span class="sxs-lookup"><span data-stu-id="b177f-125">You can use the methods on this interface to flush data and update the ASF Header Object of the final output file.</span></span> |
| [<span data-ttu-id="b177f-126">**IMFClockStateSink**</span><span class="sxs-lookup"><span data-stu-id="b177f-126">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)             | <span data-ttu-id="b177f-127">Recebe notificações de alteração de estado do relógio de apresentação.</span><span class="sxs-lookup"><span data-stu-id="b177f-127">Receives state-change notifications from the presentation clock.</span></span>                                                                                                                                       |
| [<span data-ttu-id="b177f-128">**IMFASFContentInfo**</span><span class="sxs-lookup"><span data-stu-id="b177f-128">**IMFASFContentInfo**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)             | <span data-ttu-id="b177f-129">O objeto ASF ContentInfo é um objeto de nível WMContainer que armazena principalmente informações de objeto de cabeçalho ASF.</span><span class="sxs-lookup"><span data-stu-id="b177f-129">The ASF ContentInfo object is a WMContainer level object that mainly stores ASF Header Object information.</span></span> <span data-ttu-id="b177f-130">Isso é usado para criar coletores de mídia ASF.</span><span class="sxs-lookup"><span data-stu-id="b177f-130">This is used to create ASF media sinks.</span></span>                                                     |
| [<span data-ttu-id="b177f-131">**IMFMetadata**</span><span class="sxs-lookup"><span data-stu-id="b177f-131">**IMFMetadata**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                         | <span data-ttu-id="b177f-132">Usado para descrever os metadados para o arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="b177f-132">Used to describe the metadata for the ASF file.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="b177f-133">**IMFMetadataProvider**</span><span class="sxs-lookup"><span data-stu-id="b177f-133">**IMFMetadataProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)         | <span data-ttu-id="b177f-134">Recupera uma coleção de metadados, seja para uma apresentação inteira ou para um fluxo na apresentação.</span><span class="sxs-lookup"><span data-stu-id="b177f-134">Retrieves a collection of metadata, either for an entire presentation, or for one stream in the presentation.</span></span>                                                                                          |



 

## <a name="asf-file-sink"></a><span data-ttu-id="b177f-135">Coletor de arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="b177f-135">ASF File Sink</span></span>

<span data-ttu-id="b177f-136">O coletor de arquivos ASF é uma implementação de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fornecida pelo Media Foundation que um aplicativo pode usar para arquivar dados de mídia ASF em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="b177f-136">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span>

<span data-ttu-id="b177f-137">Você precisa criar, configurar e chamar métodos no coletor de arquivos ou qualquer um de seus coletores de fluxo se estiver usando os objetos da camada de pipeline para gravar um novo arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="b177f-137">You need to create, configure, and call methods on the file sink or any of its stream sinks if you are using the pipeline layer objects to write a new ASF file.</span></span> <span data-ttu-id="b177f-138">Depois de configurar o coletor de arquivos, você pode adicioná-lo ao pipeline de codificação.</span><span class="sxs-lookup"><span data-stu-id="b177f-138">After configuring the file sink you can then add it to the encoding pipeline.</span></span>

<span data-ttu-id="b177f-139">Aqui estão as etapas gerais para usar o coletor de arquivo ASF:</span><span class="sxs-lookup"><span data-stu-id="b177f-139">Here are the general steps for using the ASF file sink:</span></span>

1.  <span data-ttu-id="b177f-140">Crie o coletor de arquivos em processo ou fora de processo.</span><span class="sxs-lookup"><span data-stu-id="b177f-140">Create the file sink in-process or out-of-process.</span></span>
2.  <span data-ttu-id="b177f-141">Configure o coletor de arquivos com todos os fluxos, propriedades de codificação e informações de metadados.</span><span class="sxs-lookup"><span data-stu-id="b177f-141">Configure the file sink with all the streams, encoding properties, and metadata information.</span></span>
3.  <span data-ttu-id="b177f-142">Associe o coletor de arquivos ao nó de topologia de saída enumerando os coletores de fluxo ou controlando os números de fluxo com no coletor.</span><span class="sxs-lookup"><span data-stu-id="b177f-142">Associate the file sink with the output topology node either by enumerating the stream sinks or by keeping track of the stream numbers with in the sink.</span></span>

<span data-ttu-id="b177f-143">Os tópicos a seguir contêm informações detalhadas sobre como trabalhar com o coletor de arquivos ASF:</span><span class="sxs-lookup"><span data-stu-id="b177f-143">The following topics contain detailed information about working with the ASF file sink:</span></span>

-   [<span data-ttu-id="b177f-144">Criando o coletor de arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="b177f-144">Creating the ASF File Sink</span></span>](creating-the-asf-file-sink.md)
-   [<span data-ttu-id="b177f-145">Adicionando informações de fluxo ao coletor de arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="b177f-145">Adding Stream Information to the ASF File Sink</span></span>](adding-stream-information-to-the-asf-file-sink.md)
-   [<span data-ttu-id="b177f-146">Definindo propriedades no coletor de arquivos</span><span class="sxs-lookup"><span data-stu-id="b177f-146">Setting Properties in the File Sink</span></span>](setting-properties-in-the-file-sink.md)
-   [<span data-ttu-id="b177f-147">Adicionando metadados ao coletor de arquivos</span><span class="sxs-lookup"><span data-stu-id="b177f-147">Adding Metadata to the File Sink</span></span>](adding-metadata-to-the-file-sink.md)
-   [<span data-ttu-id="b177f-148">O modelo de buffer de buckets vazados</span><span class="sxs-lookup"><span data-stu-id="b177f-148">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)

## <a name="related-topics"></a><span data-ttu-id="b177f-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b177f-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b177f-150">Componentes ASF da camada de pipeline</span><span class="sxs-lookup"><span data-stu-id="b177f-150">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="b177f-151">Suporte a ASF no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b177f-151">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
