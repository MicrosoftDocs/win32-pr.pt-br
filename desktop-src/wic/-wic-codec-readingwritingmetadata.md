---
description: Este tópico fornece uma visão geral de como você pode usar as APIs do Windows Imaging Component (WIC) para ler e gravar metadados inseridos em arquivos de imagem.
ms.assetid: b1e0b936-a13a-42dd-8470-957ba1d90423
title: Visão geral da leitura e gravação de metadados de imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 484d562b71184c20adf054f1de2a4203878da9b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921924"
---
# <a name="overview-of-reading-and-writing-image-metadata"></a><span data-ttu-id="ba8e3-103">Visão geral da leitura e gravação de metadados de imagem</span><span class="sxs-lookup"><span data-stu-id="ba8e3-103">Overview of Reading and Writing Image Metadata</span></span>

<span data-ttu-id="ba8e3-104">Este tópico fornece uma visão geral de como você pode usar as APIs do Windows Imaging Component (WIC) para ler e gravar metadados inseridos em arquivos de imagem.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-104">This topic provides an overview of how you can use the Windows Imaging Component (WIC) APIs to read and write metadata that is embedded in image files.</span></span>

<span data-ttu-id="ba8e3-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ba8e3-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="ba8e3-106">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="ba8e3-107">Introdução</span><span class="sxs-lookup"><span data-stu-id="ba8e3-107">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="ba8e3-108">Lendo Metadadata usando um leitor de consulta</span><span class="sxs-lookup"><span data-stu-id="ba8e3-108">Reading Metadadata Using a Query Reader</span></span>](#reading-metadadata-using-a-query-reader)
    -   [<span data-ttu-id="ba8e3-109">Obtendo um leitor de consulta</span><span class="sxs-lookup"><span data-stu-id="ba8e3-109">Obtaining a Query Reader</span></span>](#obtaining-a-query-reader)
    -   [<span data-ttu-id="ba8e3-110">Lendo metadados</span><span class="sxs-lookup"><span data-stu-id="ba8e3-110">Reading Metadata</span></span>](#reading-metadata)
    -   [<span data-ttu-id="ba8e3-111">Métodos adicionais de leitura de consulta</span><span class="sxs-lookup"><span data-stu-id="ba8e3-111">Additional Query Reader Methods</span></span>](#additional-query-reader-methods)
-   [<span data-ttu-id="ba8e3-112">Gravando metadados usando um gravador de consulta</span><span class="sxs-lookup"><span data-stu-id="ba8e3-112">Writing Metadata Using a Query Writer</span></span>](#writing-metadata-using-a-query-writer)
    -   [<span data-ttu-id="ba8e3-113">Obtendo um gravador de consulta</span><span class="sxs-lookup"><span data-stu-id="ba8e3-113">Obtaining a Query Writer</span></span>](#obtaining-a-query-writer)
    -   [<span data-ttu-id="ba8e3-114">Adicionando metadados</span><span class="sxs-lookup"><span data-stu-id="ba8e3-114">Adding Metadata</span></span>](#adding-metadata)
    -   [<span data-ttu-id="ba8e3-115">Removendo metadados</span><span class="sxs-lookup"><span data-stu-id="ba8e3-115">Removing Metadata</span></span>](#removing-metadata)
    -   [<span data-ttu-id="ba8e3-116">Copiando metadados para nova codificação</span><span class="sxs-lookup"><span data-stu-id="ba8e3-116">Copying Metadata for Re-encoding</span></span>](#copying-metadata-for-re-encoding)
-   [<span data-ttu-id="ba8e3-117">Codificação rápida de metadados</span><span class="sxs-lookup"><span data-stu-id="ba8e3-117">Fast Metadata Encoding</span></span>](#fast-metadata-encoding)
    -   [<span data-ttu-id="ba8e3-118">Adicionando preenchimento a blocos de metadados</span><span class="sxs-lookup"><span data-stu-id="ba8e3-118">Adding Padding to Metadata Blocks</span></span>](#adding-padding-to-metadata-blocks)
    -   [<span data-ttu-id="ba8e3-119">Obtendo um codificador de metadados rápido</span><span class="sxs-lookup"><span data-stu-id="ba8e3-119">Obtaining a Fast Metadata Encoder</span></span>](#obtaining-a-fast-metadata-encoder)
    -   [<span data-ttu-id="ba8e3-120">Usando o codificador de metadados rápido</span><span class="sxs-lookup"><span data-stu-id="ba8e3-120">Using the Fast Metadata Encoder</span></span>](#using-the-fast-metadata-encoder)
-   [<span data-ttu-id="ba8e3-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ba8e3-121">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="ba8e3-122">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="ba8e3-122">Prerequisites</span></span>

<span data-ttu-id="ba8e3-123">Para entender este tópico, você deve estar familiarizado com o sistema de metadados do WIC, conforme descrito na [visão geral dos metadados do WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="ba8e3-123">To understand this topic, you should be familiar with the WIC metadata system as described in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="ba8e3-124">Você também deve estar familiarizado com a linguagem de consulta usada para ler e gravar metadados, conforme descrito em [visão geral da linguagem de consulta de metadados](-wic-codec-metadataquerylanguage.md).</span><span class="sxs-lookup"><span data-stu-id="ba8e3-124">You should also be familiar with the query language used to read and write metadata, as described in [Metadata Query Language Overview](-wic-codec-metadataquerylanguage.md).</span></span>

## <a name="introduction"></a><span data-ttu-id="ba8e3-125">Introdução</span><span class="sxs-lookup"><span data-stu-id="ba8e3-125">Introduction</span></span>

<span data-ttu-id="ba8e3-126">O WIC fornece aos desenvolvedores de aplicativos componentes de Component Object Model (COM) para ler e gravar metadados inseridos em arquivos de imagem.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-126">WIC provides application developers with Component Object Model (COM) components to read and write metadata embedded in image files.</span></span> <span data-ttu-id="ba8e3-127">Há duas maneiras de ler e gravar metadados:</span><span class="sxs-lookup"><span data-stu-id="ba8e3-127">There are two ways to read and write metadata:</span></span>

-   <span data-ttu-id="ba8e3-128">Usando um leitor de consulta/gravador e uma expressão de consulta para consultar blocos de metadados para blocos aninhados ou metadados específicos em um bloco.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-128">Using a query reader/writer and a query expression to query metadata blocks for nested blocks or specific metadata within a block.</span></span>
-   <span data-ttu-id="ba8e3-129">Usar um manipulador de metadados (um leitor de metadados ou um gravador de metadados) para acessar os blocos de metadados aninhados ou metadados específicos nos blocos de metadados.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-129">Using a metadata handler (a metadata reader or a metadata writer) to access the nested metadata blocks or specific metadata within the metadata blocks.</span></span>

<span data-ttu-id="ba8e3-130">O mais fácil é usar um leitor de consulta/gravador e uma expressão de consulta para acessar os metadados.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-130">The easiest of these is to use a query reader/writer and a query expression to access the metadata.</span></span> <span data-ttu-id="ba8e3-131">Um leitor de consulta ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) é usado para ler metadados enquanto um gravador de consulta ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) é usado para gravar metadados.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-131">A query reader ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) is used to read metadata while a query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) is used to write metadata.</span></span> <span data-ttu-id="ba8e3-132">Ambos usam uma expressão de consulta para ler ou gravar os metadados desejados.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-132">Both of these use a query expression to read or write the desired metadata.</span></span> <span data-ttu-id="ba8e3-133">Nos bastidores, um leitor de consulta (e gravador) usa um manipulador de metadados para acessar os metadados descritos pela expressão de consulta.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-133">Behind the scenes, a query reader (and writer) uses a metadata handler to access the metadata described by the query expression.</span></span>

<span data-ttu-id="ba8e3-134">O método mais avançado é acessar diretamente os manipuladores de metadados.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-134">The more advanced method is to directly access the metadata handlers.</span></span> <span data-ttu-id="ba8e3-135">Um manipulador de metadados é obtido dos quadros individuais usando um leitor de bloco ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) ou um gravador de bloco ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)).</span><span class="sxs-lookup"><span data-stu-id="ba8e3-135">A metadata handler is obtained from the individual frames using a block reader ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) or a block writer ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)).</span></span> <span data-ttu-id="ba8e3-136">Os dois tipos de manipuladores de metadados disponíveis são o leitor de metadados ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) e o gravador de metadados ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)).</span><span class="sxs-lookup"><span data-stu-id="ba8e3-136">The two types of metadata handlers available are the metadata reader ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) and the metadata writer ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)).</span></span>

<span data-ttu-id="ba8e3-137">O diagrama a seguir do conteúdo de um arquivo de imagem JPEG é usado em todos os exemplos neste tópico.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-137">The following diagram of the contents of a JPEG image file is used throughout the examples in this topic.</span></span> <span data-ttu-id="ba8e3-138">A imagem representada por este diagrama foi criada usando o Microsoft Paint; os metadados de classificação foram adicionados usando o recurso Galeria de fotos do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-138">The image represented by this diagram was created by using Microsoft Paint; the rating metadata was added by using the Photo Gallery feature of Windows Vista.</span></span>

![ilustração de imagem JPEG com metadados de classificação](graphics/jpeg.png)

## <a name="reading-metadadata-using-a-query-reader"></a><span data-ttu-id="ba8e3-140">Lendo Metadadata usando um leitor de consulta</span><span class="sxs-lookup"><span data-stu-id="ba8e3-140">Reading Metadadata Using a Query Reader</span></span>

<span data-ttu-id="ba8e3-141">A maneira mais fácil de ler metadados é usar a interface do leitor de consulta, [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span><span class="sxs-lookup"><span data-stu-id="ba8e3-141">The easiest way to read metadata is to use the query reader interface, [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span></span> <span data-ttu-id="ba8e3-142">O leitor de consulta permite que você leia blocos de metadados e itens dentro de blocos de metadados usando uma expressão de consulta.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-142">The query reader enables you to read metadata blocks and items within metadata blocks using a query expression.</span></span>

<span data-ttu-id="ba8e3-143">Há três maneiras de obter um leitor de consulta: por meio de um decodificador de bitmap ([**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)), por meio de seus quadros individuais ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) ou por meio de um gravador de consulta ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span><span class="sxs-lookup"><span data-stu-id="ba8e3-143">There are three ways to obtain a query reader: through a bitmap decoder ([**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)), through its individual frames ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)), or through a query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span></span>

### <a name="obtaining-a-query-reader"></a><span data-ttu-id="ba8e3-144">Obtendo um leitor de consulta</span><span class="sxs-lookup"><span data-stu-id="ba8e3-144">Obtaining a Query Reader</span></span>

<span data-ttu-id="ba8e3-145">O código de exemplo a seguir mostra como obter um decodificador de bitmap do alocador de imagens e recuperar um quadro de bitmap individual.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-145">The following example code shows how to obtain a bitmap decoder from the imaging factory and retrieve an individual bitmap frame.</span></span> <span data-ttu-id="ba8e3-146">Esse código também executa o trabalho de configuração necessário para obter um leitor de consulta de um quadro decodificado.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-146">This code also performs setup work needed to obtain a query reader from a decoded frame.</span></span>


```
IWICImagingFactory *pFactory = NULL;
IWICBitmapDecoder *pDecoder = NULL;
IWICBitmapFrameDecode *pFrameDecode = NULL;
IWICMetadataQueryReader *pQueryReader = NULL;
IWICMetadataQueryReader *pEmbedReader = NULL;
PROPVARIANT value;

// Initialize COM
CoInitialize(NULL);

// Initialize PROPVARIANT
PropVariantInit(&value);

//Create the COM imaging factory
HRESULT hr = CoCreateInstance(
    CLSID_WICImagingFactory,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_IWICImagingFactory,
    (LPVOID*)&pFactory);

// Create the decoder
if (SUCCEEDED(hr))
{
    hr = pFactory->CreateDecoderFromFilename(
        L"test.jpg",
        NULL,
        GENERIC_READ,
        WICDecodeMetadataCacheOnDemand,
        &pDecoder);
}

// Get a single frame from the image
if (SUCCEEDED(hr))
{
    hr = pDecoder->GetFrame(
         0,  //JPEG has only one frame.
         &pFrameDecode); 
}
```



<span data-ttu-id="ba8e3-147">O decodificador de bitmap para o arquivo de test.jpg é obtido usando o método **CreateDecoderFromFilename** da fábrica de imagens.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-147">The bitmap decoder for the test.jpg file is obtained by using the **CreateDecoderFromFilename** method of the imaging factory.</span></span> <span data-ttu-id="ba8e3-148">Nesse método, o quarto parâmetro é definido como o valor WICDecodeMetadataCacheOnDemand da enumeração [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) .</span><span class="sxs-lookup"><span data-stu-id="ba8e3-148">In this method, the fourth parameter is set to the value WICDecodeMetadataCacheOnDemand from the [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) enumeration.</span></span> <span data-ttu-id="ba8e3-149">Isso informa ao decodificador para armazenar em cache os metadados quando os metadados são necessários; seja obtendo um leitor de consulta ou o leitor de metadados subjacente.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-149">This tells the decoder to cache the metadata when the metadata is needed; either by obtaining a query reader or the underlying metadata reader.</span></span> <span data-ttu-id="ba8e3-150">O uso dessa opção permite que você retenha o fluxo para os metadados necessários para a codificação de metadados rápida e permite a decodificação sem perdas da imagem JPEG.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-150">Using this option enables you to retain the stream to the metadata required for fast metadata encoding and enables lossless decoding of the JPEG image.</span></span> <span data-ttu-id="ba8e3-151">Como alternativa, você pode usar o outro valor **WICDecodeOptions** , WICDecodeMetadataCacheOnLoad, que armazena em cache os metadados da imagem inserida assim que a imagem é carregada.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-151">Alternatively, you could use the other **WICDecodeOptions** value, WICDecodeMetadataCacheOnLoad, which caches the embedded image metadata as soon as the image is loaded.</span></span>

<span data-ttu-id="ba8e3-152">Para obter o leitor de consulta do quadro, faça uma chamada simples para o método **GetMetadataQueryReader** do quadro.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-152">To obtain the frame's query reader, make a simple call to the frame's **GetMetadataQueryReader** method.</span></span> <span data-ttu-id="ba8e3-153">O código a seguir demonstra essa chamada.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-153">The following code demonstrates this call.</span></span>


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



<span data-ttu-id="ba8e3-154">Da mesma forma, um leitor de consulta também pode ser obtido no nível do decodificador.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-154">Similarly, a query reader can also be obtained at the decoder level.</span></span> <span data-ttu-id="ba8e3-155">Uma chamada simples para o método **GetMetadataQueryReader** do decodificador Obtém o leitor de consulta do decodificador.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-155">A simple call to the decoder's **GetMetadataQueryReader** method gets the decoder's query reader.</span></span> <span data-ttu-id="ba8e3-156">O leitor de consulta de um decodificador, diferente do leitor de consulta de um quadro, lê os metadados de uma imagem que está fora dos quadros individuais.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-156">An decoder's query reader, unlike a frame's query reader, reads metadata for an image that is outside of the individual frames.</span></span> <span data-ttu-id="ba8e3-157">No entanto, esse cenário não é comum e os formatos de imagem nativa não oferecem suporte a esse recurso.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-157">However, this scenario is not common, and the native image formats do not support this capability.</span></span> <span data-ttu-id="ba8e3-158">Os CODECs de imagem nativa fornecidos pelos metadados de leitura e gravação do WIC no nível do quadro, mesmo para formatos de quadro único, como JPEG.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-158">The native image CODECS provided by WIC read and write metadata at the frame level even for single-frame formats such as JPEG.</span></span>

### <a name="reading-metadata"></a><span data-ttu-id="ba8e3-159">Lendo metadados</span><span class="sxs-lookup"><span data-stu-id="ba8e3-159">Reading Metadata</span></span>

<span data-ttu-id="ba8e3-160">Antes de prosseguir para realmente ler os metadados, examine o diagrama a seguir de um arquivo JPEG que inclui blocos de metadados incorporados e dados reais a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-160">Before you move on to actually reading metadata, look at the following diagram of a JPEG file that includes embedded metadata blocks and actual data to retrieve.</span></span> <span data-ttu-id="ba8e3-161">Este diagrama fornece textos explicativos para blocos de metadados específicos e itens dentro da imagem, fornecendo a expressão de consulta de metadados para cada bloco ou item.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-161">This diagram provides callouts to specific metadata blocks and items within the image providing the metadata query expression to each block or item.</span></span>

![ilustração de imagem JPEG com textos explicativos de metadados](graphics/jpegwithcallouts.png)

<span data-ttu-id="ba8e3-163">Para consultar blocos de metadados inseridos ou itens específicos por nome, chame o método **GetMetadataByName** .</span><span class="sxs-lookup"><span data-stu-id="ba8e3-163">To query for embedded metadata blocks or specific items by name, call the **GetMetadataByName** method.</span></span> <span data-ttu-id="ba8e3-164">Esse método usa uma expressão de consulta e um [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) no qual o item de metadados é retornado.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-164">This method takes a query expression and a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) in which the metadata item is returned.</span></span> <span data-ttu-id="ba8e3-165">O código a seguir consulta um bloco de metadados aninhado e converte o componente [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) fornecido pelo valor PROPVARIANT em um leitor de consulta, se encontrado.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-165">The following code queries for a nested metadata block and converts the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) component provided by the PROPVARIANT value to a query reader if found.</span></span>


```
if (SUCCEEDED(hr))
{
    // Get the nested IFD reader
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd", &value);
    if (value.vt == VT_UNKNOWN)
    {
        hr = value.punkVal->QueryInterface(IID_IWICMetadataQueryReader, (void **)&pEmbedReader);
    }
    PropVariantClear(&value); // Clear value for new query
}
```



<span data-ttu-id="ba8e3-166">A expressão de consulta "/app1/IFD" está consultando o bloco IFD aninhado no bloco App1.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-166">The query expression "/app1/ifd" is querying for the IFD block nested in the App1 block.</span></span> <span data-ttu-id="ba8e3-167">O arquivo de imagem JPEG contém o bloco de metadados aninhado IFD, portanto, o [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) é retornado com um tipo de variável (VT) de `VT_UNKNOWN` e um ponteiro para uma interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) (punkVal).</span><span class="sxs-lookup"><span data-stu-id="ba8e3-167">The JPEG image file contains the IFD nested metadata block, so the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) is returned with a variable type (vt) of `VT_UNKNOWN` and a pointer to an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface (punkVal).</span></span> <span data-ttu-id="ba8e3-168">Em seguida, você consulta a interface IUnknown para um leitor de consulta.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-168">You then query the IUnknown interface for a query reader.</span></span>

<span data-ttu-id="ba8e3-169">O código a seguir demonstra uma nova consulta com base no novo leitor de consulta relativo ao bloco de IFD aninhado.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-169">The following code demonstrates a new query based on the new query reader relative to the nested IFD block.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetMetadataByName(L"/{ushort=18249}", &value);
    PropVariantClear(&value); // Clear value for new query
}
```



<span data-ttu-id="ba8e3-170">A expressão de consulta "/{UShort = 18249}" consulta o bloco IFD para a classificação MicrosoftPhoto inserida na marca 18249.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-170">The query expression "/{ushort=18249}" queries the IFD block for the MicrosoftPhoto rating embedded under tag 18249.</span></span> <span data-ttu-id="ba8e3-171">O valor de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) agora conterá um tipo de valor de `VT_UI2` e um valor de dados de 50.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-171">The [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) value will now contain a value type of `VT_UI2` and a data value of 50.</span></span>

<span data-ttu-id="ba8e3-172">No entanto, não é necessário obter um bloco aninhado antes de consultar valores de dados específicos.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-172">However, it is not necessary to obtain a nested block before querying for specific data values.</span></span> <span data-ttu-id="ba8e3-173">Por exemplo, em vez de consultar a IFD aninhada e, em seguida, para a classificação MicrosoftPhoto, você pode usar o bloco de metadados raiz e a consulta mostrada no código a seguir para obter as mesmas informações.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-173">For instance, instead of querying for the nested IFD and then for the MicrosoftPhoto rating, you can instead use the root metadata block and the query shown in the following code to obtain the same information.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);
    PropVariantClear(&value);
}
```



<span data-ttu-id="ba8e3-174">Além de consultar itens de metadados específicos em um bloco de metadados, você também pode enumerar todos os itens de metadados em um bloco de metadados (não incluindo itens de metadados em blocos de metadados aninhados).</span><span class="sxs-lookup"><span data-stu-id="ba8e3-174">In addition to querying for specific metadata items in a metadata block, you can also enumerate all the metadata items in a metadata block (not including metadata items in nested metadata blocks).</span></span> <span data-ttu-id="ba8e3-175">Para enumerar os itens de metadados no bloco atual, o método **Getenumeration** do leitor de consulta é usado.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-175">To enumerate the metadata items in the current block, the query reader's **GetEnumeration** method is used.</span></span> <span data-ttu-id="ba8e3-176">Esse método obtém uma interface **IEnumString** populada com os itens de metadados no bloco atual.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-176">This method obtains an **IEnumString** interface populated with the metadata items in the current block.</span></span> <span data-ttu-id="ba8e3-177">Por exemplo, o código a seguir enumera a classificação XMP e a classificação MicrosoftPhoto para o bloco de IFD aninhado que foi obtido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-177">For example, the following code enumerates the XMP rating and MicrosoftPhoto rating for the nested IFD block that was obtained earlier.</span></span>


```
IEnumString *metadataItems = NULL;

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetEnumerator(&metadataItems);
}
```



<span data-ttu-id="ba8e3-178">Para obter mais informações sobre como identificar marcas apropriadas para vários formatos de imagem e formatos de metadados, consulte [consultas de metadados de formato de imagem nativa](-wic-native-image-format-metadata-queries.md).</span><span class="sxs-lookup"><span data-stu-id="ba8e3-178">For more information on identifying appropriate tags for various image formats and metadata formats, see [Native Image Format Metadata Queries](-wic-native-image-format-metadata-queries.md).</span></span>

### <a name="additional-query-reader-methods"></a><span data-ttu-id="ba8e3-179">Métodos adicionais de leitura de consulta</span><span class="sxs-lookup"><span data-stu-id="ba8e3-179">Additional Query Reader Methods</span></span>

<span data-ttu-id="ba8e3-180">Além de ler metadados, você também pode obter informações adicionais sobre o leitor de consulta e obter metadados por meio de outros meios.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-180">In addition to reading metadata, you can also obtain additional information about the query reader and obtain metadata through other means.</span></span> <span data-ttu-id="ba8e3-181">O leitor de consulta fornece dois métodos que fornecem informações sobre o leitor de consulta, **GetContainerFormat** e **getLocation**.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-181">The query reader provides two methods that provide information about the query reader, **GetContainerFormat** and **GetLocation**.</span></span>

<span data-ttu-id="ba8e3-182">Com o leitor de consulta incorporado, você pode usar **GetContainerFormat** para determinar o tipo de bloco de metadados e pode chamar **getLocation** para obter o caminho relativo ao bloco de metadados raiz.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-182">With the embedded query reader, you can use **GetContainerFormat** to determine the type of metadata block, and you can call **GetLocation** to obtain the path relative to the root metadata block.</span></span> <span data-ttu-id="ba8e3-183">O código a seguir consulta o leitor de consulta inserido para sua localização.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-183">The following code queries the embedded query reader for its location.</span></span>


```
// Determine the metadata block format

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetContainerFormat(&containerGUID);
}

// Determine the query reader's location
if (SUCCEEDED(hr))
{
    UINT length;
    WCHAR readerNamespace[100];
    hr = pEmbedReader->GetLocation(100, readerNamespace, &length);
}
```



<span data-ttu-id="ba8e3-184">A chamada para **GetContainerFormat** para o leitor de consulta inserida retorna o GUID do formato de metadados IFD.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-184">The call to **GetContainerFormat** for the embedded query reader returns the IFD metadata format GUID.</span></span> <span data-ttu-id="ba8e3-185">A chamada para **getLocation** retorna um namespace de "/app1/IFD"; fornecendo o caminho relativo do qual as consultas subsequentes para o novo leitor de consulta serão executadas.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-185">The call to **GetLocation** returns a namespace of "/app1/ifd"; providing you with the relative path from which subsequent queries to the new query reader will be executed.</span></span> <span data-ttu-id="ba8e3-186">É claro que o código anterior não é muito útil, mas demonstra como usar o método **getLocation** para localizar blocos de metadados aninhados.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-186">Of course, the preceding code isn't very useful, but it does demonstrate how to use the **GetLocation** method for finding nested metadata blocks.</span></span>

## <a name="writing-metadata-using-a-query-writer"></a><span data-ttu-id="ba8e3-187">Gravando metadados usando um gravador de consulta</span><span class="sxs-lookup"><span data-stu-id="ba8e3-187">Writing Metadata Using a Query Writer</span></span>

> [!Note]  
> <span data-ttu-id="ba8e3-188">Alguns dos exemplos de código fornecidos nesta seção não são mostrados no contexto das etapas reais necessárias para gravar metadados.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-188">Some of the code examples provided in this section are not shown in the context of the actual steps required to write metadata.</span></span> <span data-ttu-id="ba8e3-189">Para exibir os exemplos de código no contexto de um exemplo de trabalho, consulte o tutorial como: codificar novamente uma imagem com metadados.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-189">To view the code examples in the context of a working sample, see the How-to: Re-encode an Image with Metadata tutorial.</span></span>

 

<span data-ttu-id="ba8e3-190">O componente principal para gravar metadados é o gravador de consulta ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span><span class="sxs-lookup"><span data-stu-id="ba8e3-190">The main component for writing metadata is the query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span></span> <span data-ttu-id="ba8e3-191">O gravador de consulta permite que você defina e remova os blocos de metadados e os itens em um bloco de metadados.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-191">The query writer enables you to set and remove metadata blocks and items within a metadata block.</span></span>

<span data-ttu-id="ba8e3-192">Assim como o leitor de consultas, há três maneiras de obter um gravador de consulta: por meio de um codificador de bitmap ([**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)), por meio de seus quadros individuais ([**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)) ou por meio de um [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)(codificador de metadados rápido).</span><span class="sxs-lookup"><span data-stu-id="ba8e3-192">Like the query reader, there are three ways to obtain a query writer: through a bitmap encoder ([**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)), through its individual frames ([**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)), or through a fast metadata encoder ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)).</span></span>

### <a name="obtaining-a-query-writer"></a><span data-ttu-id="ba8e3-193">Obtendo um gravador de consulta</span><span class="sxs-lookup"><span data-stu-id="ba8e3-193">Obtaining a Query Writer</span></span>

<span data-ttu-id="ba8e3-194">O gravador de consulta mais comum é para um quadro individual de um bitmap.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-194">The most common query writer is for an individual frame of a bitmap.</span></span> <span data-ttu-id="ba8e3-195">Esse gravador de consulta define e remove os itens e os blocos de metadados de um quadro de imagem.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-195">This query writer sets and removes an image frame's metadata blocks and items.</span></span> <span data-ttu-id="ba8e3-196">Para obter o gravador de consulta de um quadro de imagem, chame o método **GetMetadataQueryWriter** do quadro.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-196">To obtain an image frame's query writer, call the frame's **GetMetadataQueryWriter** method.</span></span> <span data-ttu-id="ba8e3-197">O código a seguir demonstra a chamada de método simples para obter o gravador de consulta de um quadro.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-197">The following code demonstrates the simple method call to obtain a frame's query writer.</span></span>


```
IWICMetadataQueryWriter &pFrameQWriter = NULL;

//Obtain a query writer from the frame.
hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
```



<span data-ttu-id="ba8e3-198">Da mesma forma, um gravador de consulta também pode ser obtido para o nível do codificador.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-198">Similarly, a query writer can also be obtained for the encoder level.</span></span> <span data-ttu-id="ba8e3-199">Uma chamada simples para o método **GetMetadataQueryWriter** do codificador Obtém o gravador de consulta do codificador.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-199">A simple call to the encoder's **GetMetadataQueryWriter** method gets the encoder's query writer.</span></span> <span data-ttu-id="ba8e3-200">O gravador de consulta de um codificador, diferente do gravador de consulta de um quadro, grava metadados para uma imagem fora do quadro individual.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-200">An encoder's query writer, unlike a frame's query writer, writes metadata for an image outside of the individual frame.</span></span> <span data-ttu-id="ba8e3-201">No entanto, esse cenário não é comum e os formatos de imagem nativa não oferecem suporte a esse recurso.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-201">However, this scenario is not common, and the native image formats do not support this capability.</span></span> <span data-ttu-id="ba8e3-202">Os codecs de imagem nativa fornecidos pelos metadados de leitura e gravação do WIC no nível do quadro, mesmo para formatos de quadro único, como JPEG.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-202">The native image codecs provided by WIC read and write metadata at the frame level even for single-frame formats such as JPEG.</span></span>

<span data-ttu-id="ba8e3-203">Você também pode obter um gravador de consulta diretamente do [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)(Imaging Factory).</span><span class="sxs-lookup"><span data-stu-id="ba8e3-203">You can also obtain a query writer directly from the imaging factory ([**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)).</span></span> <span data-ttu-id="ba8e3-204">Há dois métodos de fábrica de geração de imagens que retornam um gravador de consulta: **CreateQueryWriter** e **CreateQueryWriterFromReader**.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-204">There are two imaging factory methods that return a query writer: **CreateQueryWriter** and **CreateQueryWriterFromReader**.</span></span>

<span data-ttu-id="ba8e3-205">**CreateQueryWriter** cria um gravador de consulta para o formato de metadados e o fornecedor especificados.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-205">**CreateQueryWriter** creates a query writer for the specified metadata format and vendor.</span></span> <span data-ttu-id="ba8e3-206">Esse gravador de consulta permite que você grave metadados para um formato de metadados específico e adicione-os à imagem.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-206">This query writer enables you to write metadata for a specific metadata format and add it to the image.</span></span> <span data-ttu-id="ba8e3-207">O código a seguir demonstra uma chamada **CreateQueryWriter** para criar um gravador de consulta XMP.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-207">The following code demonstrates a **CreateQueryWriter** call to create an XMP query writer.</span></span>


```
IWICMetadataQueryWriter *pXMPWriter = NULL;

// Create XMP block
GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriter(
        GUID_MetadataFormatXMP,
        &vendor,
        &pXMPWriter);
```



<span data-ttu-id="ba8e3-208">Neste exemplo, o nome amigável `GUID_MetadataFormatXMP` é usado como o parâmetro *guidMetadataFormat* .</span><span class="sxs-lookup"><span data-stu-id="ba8e3-208">In this example, the friendly name `GUID_MetadataFormatXMP` is used as the *guidMetadataFormat* parameter.</span></span> <span data-ttu-id="ba8e3-209">Ele representa o GUID do formato de metadados XMP e o fornecedor representa o manipulador criado pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-209">It represents the XMP metadata format GUID, and vendor represents the Microsoft created handler.</span></span> <span data-ttu-id="ba8e3-210">Como alternativa, **NULL** pode ser passado como o parâmetro *pguidVendor* com os mesmos resultados se nenhum outro manipulador XMP existir.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-210">Alternatively, **NULL** can be passed as the *pguidVendor* parameter with the same results if no other XMP handler exists.</span></span> <span data-ttu-id="ba8e3-211">Se um manipulador XMP personalizado for instalado junto com o manipulador XMP nativo, a passagem de **NULL** para o fornecedor resultará no gravador de consultas com o menor GUID sendo retornado.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-211">If a custom XMP handler is installed alongside the native XMP handler, passing **NULL** for the vendor will result in the query writer with the lowest GUID being returned.</span></span>

<span data-ttu-id="ba8e3-212">**CreateQueryWriterFromReader** é semelhante ao método **CreateQueryWriter** , exceto pelo fato de que ele popula o novo gravador de consulta com os dados fornecidos pelo leitor de consultas.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-212">**CreateQueryWriterFromReader** is similar to the **CreateQueryWriter** method except that it prepopulates the new query writer with the data provided by the query reader.</span></span> <span data-ttu-id="ba8e3-213">Isso é útil para codificar novamente uma imagem enquanto mantém os metadados existentes ou para remover metadados indesejados.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-213">This is useful for re-encoding an image while maintaining the existing metadata, or for removing unwanted metadata.</span></span> <span data-ttu-id="ba8e3-214">O código a seguir demonstra uma chamada **CreateQueryWriterFromReader** .</span><span class="sxs-lookup"><span data-stu-id="ba8e3-214">The following code demonstrates a **CreateQueryWriterFromReader** call.</span></span>


```
hr = pFrameDecode->GetMetadataQueryReader(&pFrameQReader);

// Copy metadata using query readers
if(SUCCEEDED(hr) && pFrameQReader)
{
    IWICMetadataQueryWriter *pNewWriter = NULL;

    GUID vendor = GUID_VendorMicrosoft;
    hr = pFactory->CreateQueryWriterFromReader(
        pFrameQReader,
        &vendor,
        &pNewWriter);
```



### <a name="adding-metadata"></a><span data-ttu-id="ba8e3-215">Adicionando metadados</span><span class="sxs-lookup"><span data-stu-id="ba8e3-215">Adding Metadata</span></span>

<span data-ttu-id="ba8e3-216">Depois de obter um gravador de consulta, você pode usá-lo para adicionar itens e blocos de metadados.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-216">After you obtain a query writer, you can use it to add metadata blocks and items.</span></span> <span data-ttu-id="ba8e3-217">Para gravar metadados, use o método **SetMetadataByName** do gravador de consulta.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-217">To write metadata, you use the query writer's **SetMetadataByName** method.</span></span> <span data-ttu-id="ba8e3-218">**SetMetadataByName** usa dois parâmetros: uma expressão de consulta (*wzName*) e um ponteiro para um [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (*pvarValue*).</span><span class="sxs-lookup"><span data-stu-id="ba8e3-218">**SetMetadataByName** takes two parameters: a query expression (*wzName*) and a pointer to a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (*pvarValue*).</span></span> <span data-ttu-id="ba8e3-219">A expressão de consulta define o bloco ou o item a ser definido enquanto o PROPVARIANT fornece o valor de dados real a ser definido.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-219">The query expression defines the block or item to set while the PROPVARIANT provides the actual data value to set.</span></span>

<span data-ttu-id="ba8e3-220">O exemplo a seguir demonstra como adicionar um título usando o gravador de consulta XMP obtido anteriormente usando o método **CreateQueryWriter** .</span><span class="sxs-lookup"><span data-stu-id="ba8e3-220">The following example demonstrates how to add a title by using the XMP query writer previously obtained by using the **CreateQueryWriter** method.</span></span>


```
// Write metadata to the XMP writer
if (SUCCEEDED(hr))
{
    PROPVARIANT value;
    PropVariantInit(&value);

    value.vt = VT_LPWSTR;
    value.pwszVal = L"Metadata Test Image.";
   
    hr = pXMPWriter->SetMetadataByName(L"/dc:title", &value);

    PropVariantClear(&value);
}
```



<span data-ttu-id="ba8e3-221">Neste exemplo, o tipo do valor (VT) é definido como `VT_LPWSTR` , indicando que uma cadeia de caracteres será usada como o valor dos dados.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-221">In this example, value's type (vt) is set to `VT_LPWSTR`, indicating that a string will be used as the data value.</span></span> <span data-ttu-id="ba8e3-222">Como o tipo do *valor* é uma cadeia de caracteres, *pwszVal* é usado para definir o título a ser usado.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-222">Because *value*'s type is a string, *pwszVal* is used to set the title to use.</span></span> <span data-ttu-id="ba8e3-223">Em seguida, **SetMetadataByName** é chamado usando a expressão de consulta "/DC: title" e o [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)definido recentemente.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-223">**SetMetadataByName** is then called using the query expression "/dc:title" and the newly set [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span> <span data-ttu-id="ba8e3-224">A expressão de consulta usada indica que a propriedade Title no esquema de Digital Camera (DC) deve ser definida.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-224">The query expression used indicates that the title property in the digital camera (dc) schema should be set.</span></span> <span data-ttu-id="ba8e3-225">Observe que a expressão não é "/XMP/DC: title"; Isso ocorre porque o gravador de consulta já é específico do XMP e não contém um bloco XMP inserido, que "/XMP/DC: title" sugere.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-225">Note that the expression is not "/xmp/dc:title"; this is because the query writer is already specific to XMP and does not contain an embedded XMP block, which "/xmp/dc:title" would suggest.</span></span>

<span data-ttu-id="ba8e3-226">Até este ponto, você não adicionou nenhum metadado a um quadro de imagem.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-226">Up to this point you haven't actually added any metadata to an image frame.</span></span> <span data-ttu-id="ba8e3-227">Você simplesmente preencheu um gravador de consulta com dados.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-227">You've simply populated a query writer with data.</span></span> <span data-ttu-id="ba8e3-228">Para adicionar a um quadro um bloco de metadados representado pelo gravador de consulta, você chama novamente **SetMetadataByName** usando o gravador de consulta como o valor de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span><span class="sxs-lookup"><span data-stu-id="ba8e3-228">To add to a frame a metadata block represented by the query writer, you again call **SetMetadataByName** using the query writer as the value of the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span> <span data-ttu-id="ba8e3-229">Isso efetivamente copia os metadados no gravador de consulta para o quadro de imagem.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-229">This effectively copies the metadata in the query writer to the image frame.</span></span> <span data-ttu-id="ba8e3-230">O código a seguir demonstra como adicionar os metadados no gravador de consulta XMP obtido anteriormente ao bloco de metadados raiz de um quadro.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-230">The following code demonstrates how to add the metadata in the XMP query writer previously obtained to a frame's root metadata block.</span></span>


```
// Get the frame's query writer and write the XMP query writer to it
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);

    // Copy the metadata in the XMP query writer to the frame
    if (SUCCEEDED(hr))
    {
        PROPVARIANT value;

        PropVariantInit(&value);
        value.vt = VT_UNKNOWN;
        value.punkVal = pXMPWriter;
        value.punkVal->AddRef();

        hr = pFrameQWriter->SetMetadataByName(L"/", &value);

        PropVariantClear(&value);
    }
}
```



<span data-ttu-id="ba8e3-231">Neste exemplo, um tipo de valor (VT) de `VT_UNKOWN` é usado; indicando um tipo de valor de interface com.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-231">In this example, a value type (vt) of `VT_UNKOWN` is used; indicating a COM interface value type.</span></span> <span data-ttu-id="ba8e3-232">O gravador de consulta XMP (piXMPWriter) é usado como o valor de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), adicionando uma referência a ele usando o método AddRef.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-232">The XMP query writer (piXMPWriter) is then used as the value of the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), adding a reference to it by using the AddRef method.</span></span> <span data-ttu-id="ba8e3-233">Por fim, o gravador de consulta XMP é definido chamando o método **SetMetadataByName** do quadro e passando a expressão de consulta "/", indicando o bloco raiz e o PROPVARIANT recentemente definido.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-233">Finally, the XMP query writer is set by calling the frame's **SetMetadataByName** method and passing the query expression "/", indicating the root block, and the newly set PROPVARIANT.</span></span>

> [!Note]  
> <span data-ttu-id="ba8e3-234">Se o quadro já contiver o bloco de metadados que você está tentando adicionar, os metadados que você está adicionando serão adicionados e os metadados existentes são substituídos.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-234">If the frame already contains the metadata block you are trying to add, the metadata you are adding will be added and existing metadata overwritten.</span></span>

 

### <a name="removing-metadata"></a><span data-ttu-id="ba8e3-235">Removendo metadados</span><span class="sxs-lookup"><span data-stu-id="ba8e3-235">Removing Metadata</span></span>

<span data-ttu-id="ba8e3-236">Um gravador de consulta também permite remover metadados chamando o método **RemoveMetadataByName** .</span><span class="sxs-lookup"><span data-stu-id="ba8e3-236">A query writer also enables you to remove metadata by calling the **RemoveMetadataByName** method.</span></span> <span data-ttu-id="ba8e3-237">**RemoveMetadataByName** usa uma expressão de consulta e remove o bloco de metadados ou o item, se ele existir.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-237">**RemoveMetadataByName** takes a query expression and removes the metadata block or item if it exists.</span></span> <span data-ttu-id="ba8e3-238">O código a seguir demonstra como remover o título que foi adicionado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-238">The following code demonstrates how to remove the title that was previously added.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp/dc:title");
}
```



<span data-ttu-id="ba8e3-239">O código a seguir demonstra como remover todo o bloco de metadados XMP.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-239">The following code demonstrates how to remove the entire XMP metadata block.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp");
}
```



### <a name="copying-metadata-for-re-encoding"></a><span data-ttu-id="ba8e3-240">Copiando metadados para nova codificação</span><span class="sxs-lookup"><span data-stu-id="ba8e3-240">Copying Metadata for Re-encoding</span></span>

> [!Note]  
> <span data-ttu-id="ba8e3-241">O código nesta seção é válido somente quando os formatos de imagem de origem e destino são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-241">The code in this section is valid only when the source and destination image formats are the same.</span></span> <span data-ttu-id="ba8e3-242">Você não pode copiar todos os metadados de uma imagem em uma única operação ao codificar para um formato de imagem diferente.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-242">You cannot copy all of an image's metadata in a single operation when encoding to a different image format.</span></span>

 

<span data-ttu-id="ba8e3-243">Para preservar os metadados ao codificar novamente uma imagem no mesmo formato de imagem, há métodos disponíveis para copiar todos os metadados em uma única operação.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-243">To preserve metadata while re-encoding an image to the same image format, there are methods available for copying all the metadata in a single operation.</span></span> <span data-ttu-id="ba8e3-244">Cada uma dessas operações segue um padrão semelhante; cada um define os metadados do quadro decodificado diretamente no novo quadro que está sendo codificado.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-244">Each of these operations follows a similar pattern; each sets the decoded frame's metadata directly into the new frame being encoded.</span></span>

<span data-ttu-id="ba8e3-245">O método preferencial para copiar metadados é inicializar o gravador de bloco do novo quadro com o leitor de bloco do quadro decodificado.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-245">The preferred method to copy metadata is to initialize the new frame's block writer with the decoded frame's block reader.</span></span> <span data-ttu-id="ba8e3-246">O código a seguir demonstra esse método.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-246">The following code demonstrates this method.</span></span>


```
if (SUCCEEDED(hr) && formatsEqual)
{
    // Copy metadata using metadata block reader/writer
    if (SUCCEEDED(hr))
    {
        pFrameDecode->QueryInterface(
            IID_IWICMetadataBlockReader,
            (void**)&pBlockReader);
    }
    if (SUCCEEDED(hr))
    {
        pFrameEncode->QueryInterface(
            IID_IWICMetadataBlockWriter,
            (void**)&pBlockWriter);
    }
    if (SUCCEEDED(hr))
    {
        pBlockWriter->InitializeFromBlockReader(pBlockReader);
    }
}
```



<span data-ttu-id="ba8e3-247">Neste exemplo, o leitor de bloco e o gravador de bloco são obtidos do quadro de origem e do quadro de destino, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-247">In this example, the block reader and the block writer are obtained from the source frame and destination frame, respectively.</span></span> <span data-ttu-id="ba8e3-248">Em seguida, o gravador de bloco é inicializado a partir do leitor de blocos.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-248">The block writer is then initialized from the block reader.</span></span> <span data-ttu-id="ba8e3-249">Isso inicializa o leitor de bloco com os metadados preenchidos previamente do leitor de bloco.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-249">This initializes the block reader with the pre-populated metadata of the block reader.</span></span>

<span data-ttu-id="ba8e3-250">Outro método para copiar metadados é gravar o bloco de metadados referenciado pelo leitor de consulta usando o gravador de consultas do codificador.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-250">Another method to copy metadata is to write the metadata block referenced by the query reader using the encoder's query writer.</span></span> <span data-ttu-id="ba8e3-251">O código a seguir demonstra esse método.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-251">The following code demonstrates this method.</span></span>


```
if (SUCCEEDED(hr) && formatsEqual)
{
    hr = pFrameDecode->GetMetadataQueryReader(&pFrameQReader);

    // Copy metadata using query readers
    if(SUCCEEDED(hr))
    {
        hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
        if (SUCCEEDED(hr))
        {
            PropVariantClear(&value);
            value.vt=VT_UNKNOWN;
            value.punkVal=pFrameQReader;
            value.punkVal->AddRef();
            hr = pFrameQWriter->SetMetadataByName(L"/", &value);
            PropVariantClear(&value);
        }
    }
}
```



<span data-ttu-id="ba8e3-252">Aqui, um leitor de consulta é obtido do quadro decodificado e, em seguida, usado como o valor da Propriedade do [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) com um tipo de valor definido como VT \_ desconhecido.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-252">Here, a query reader is obtained from the decoded frame and then used as the property value of the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) with a value type set to VT\_UNKNOWN.</span></span> <span data-ttu-id="ba8e3-253">O gravador de consulta para o codificador é obtido e a expressão de consulta "/" é usada para definir os metadados no caminho de navegação raiz.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-253">The query writer for the encoder is obtained and the query expression "/" is used to set the metadata at the root navigation path.</span></span> <span data-ttu-id="ba8e3-254">Você também pode usar esse método ao definir blocos de metadados aninhados, ajustando a expressão de consulta para o local desejado.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-254">You can also use this method when setting nested metadata blocks, by adjusting the query expression to the desired location.</span></span>

<span data-ttu-id="ba8e3-255">Da mesma forma, você pode criar um gravador de consulta baseado no leitor de consulta do quadro decodificado usando o método **CreateQueryWriterFromReader** do Imaging Factory.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-255">Similarly, you can create a query writer based on the decoded frame's query reader by using the imaging factory's **CreateQueryWriterFromReader** method.</span></span> <span data-ttu-id="ba8e3-256">O gravador de consulta criado nesta operação será preenchido previamente com os metadados do leitor de consulta e, em seguida, poderá ser definido no quadro.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-256">The query writer created in this operation will be prepopulated with the metadata from the query reader and can then be set in the frame.</span></span> <span data-ttu-id="ba8e3-257">O código a seguir demonstra a operação de cópia **CreateQueryWriterFromReader** .</span><span class="sxs-lookup"><span data-stu-id="ba8e3-257">The following code demonstrates the **CreateQueryWriterFromReader** copy operation.</span></span>


```
IWICMetadataQueryWriter *pNewWriter = NULL;

GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriterFromReader(
    pFrameQReader,
    &vendor,
    &pNewWriter);

if (SUCCEEDED(hr))
{
    // Get the frame's query writer
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
}

// Set the query writer to the frame.
if (SUCCEEDED(hr))
{
    PROPVARIANT value;

    PropVariantInit(&value);
    value.vt = VT_UNKNOWN;
    value.punkVal = pNewWriter;
    value.punkVal->AddRef();
    hr = pFrameQWriter->SetMetadataByName(L"/",&value);
}
```



<span data-ttu-id="ba8e3-258">Esse método usa um gravador de consulta separado criado com base nos dados do leitor de consulta.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-258">This method uses a separate query writer is created that is based on the data of the query reader.</span></span> <span data-ttu-id="ba8e3-259">Esse novo gravador de consulta, em seguida, é definido no quadro.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-259">This new query writer then set in the frame.</span></span>

<span data-ttu-id="ba8e3-260">Novamente, essas operações para copiar metadados só funcionam quando as imagens de origem e destino têm o mesmo formato.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-260">Again, these operations to copy metadata only work when the source and destination images have the same format.</span></span> <span data-ttu-id="ba8e3-261">Isso ocorre porque diferentes formatos de imagem armazenam os blocos de metadados em locais diferentes.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-261">This is because different image formats store the metadata blocks in different locations.</span></span> <span data-ttu-id="ba8e3-262">Por exemplo, JPEG e TIFF dão suporte a blocos de metadados XMP.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-262">For instance, both JPEG and TIFF support XMP metadata blocks.</span></span> <span data-ttu-id="ba8e3-263">Em imagens JPEG, o bloco XMP está no bloco de metadados raiz, conforme ilustrado na [visão geral dos metadados do WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="ba8e3-263">In JPEG images, the XMP block is at the root metadata block as illustrated in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="ba8e3-264">No entanto, em uma imagem TIFF, o bloco XMP é aninhado em um bloco de IFD raiz.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-264">However, in a TIFF image, the XMP block is nested in a root IFD block.</span></span> <span data-ttu-id="ba8e3-265">O diagrama a seguir ilustra as diferenças entre uma imagem JPEG e uma imagem TIFF com os mesmos metadados de classificação.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-265">The following diagram illustrates the differences between a JPEG image and a TIFF image with the same rating metadata.</span></span>

![comparação de JPEG e TIFF.](graphics/jpgvstiff.png)

## <a name="fast-metadata-encoding"></a><span data-ttu-id="ba8e3-267">Codificação rápida de metadados</span><span class="sxs-lookup"><span data-stu-id="ba8e3-267">Fast Metadata Encoding</span></span>

<span data-ttu-id="ba8e3-268">Nem sempre é necessário codificar novamente uma imagem para gravar novos metadados nela.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-268">It is not always necessary to re-encode an image to write new metadata to it.</span></span> <span data-ttu-id="ba8e3-269">Os metadados também podem ser gravados usando um codificador de metadados rápido.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-269">Metadata can also be written by using a fast metadata encoder.</span></span> <span data-ttu-id="ba8e3-270">Um codificador de metadados rápido pode gravar uma quantidade limitada de metadados em uma imagem sem codificar novamente a imagem.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-270">A fast metadata encoder can write a limited amount of metadata to an image without re-encoding the image.</span></span> <span data-ttu-id="ba8e3-271">Isso é feito escrevendo-se os novos metadados dentro do preenchimento vazio fornecido por alguns formatos de metadados.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-271">This is accomplished by writing the new metadata within the empty padding provided by some metadata formats.</span></span> <span data-ttu-id="ba8e3-272">Os formatos de metadados nativos que dão suporte ao preenchimento de metadados são EXIF, IFD, GPS e XMP.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-272">The native metadata formats that support metadata padding are Exif, IFD, GPS and XMP.</span></span>

### <a name="adding-padding-to-metadata-blocks"></a><span data-ttu-id="ba8e3-273">Adicionando preenchimento a blocos de metadados</span><span class="sxs-lookup"><span data-stu-id="ba8e3-273">Adding Padding to Metadata Blocks</span></span>

<span data-ttu-id="ba8e3-274">Antes que você possa executar a codificação de metadados rápida, deve haver espaço no bloco de metadados para gravar mais metadados.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-274">Before you can perform fast metadata encoding, there must be room within the metadata block to write more metadata.</span></span> <span data-ttu-id="ba8e3-275">Se não houver espaço suficiente no preenchimento existente para gravar os novos metadados, a codificação rápida de metadados falhará.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-275">If there is not enough room within the existing padding to write the new metadata, the fast metadata encoding will fail.</span></span> <span data-ttu-id="ba8e3-276">Para adicionar o preenchimento de metadados a uma imagem, a imagem deve ser codificada novamente.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-276">To add metadata padding to an image, the image must be re-encoded.</span></span> <span data-ttu-id="ba8e3-277">Você pode adicionar o preenchimento da mesma maneira que adicionaria qualquer outro item de metadados, usando uma expressão de consulta, se o bloco de metadados que você está preenchendo oferecer suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-277">You can add padding the same way you would add any other metadata item, by using a query expression, if the metadata block you are padding supports it.</span></span> <span data-ttu-id="ba8e3-278">O exemplo a seguir demonstra como adicionar o preenchimento a um bloco IFD inserido em um bloco App1.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-278">The following example demonstrates how to add padding to an IFD block embedded in an App1 block.</span></span>


```
if (SUCCEEDED(hr))
{
    // Add metadata padding
    PROPVARIANT padding;

    PropVariantInit(&padding);
    padding.vt = VT_UI4;
    padding.uiVal = 4096; // 4KB

    hr = pFrameQWriter->SetMetadataByName(L"/app1/ifd/PaddingSchema:padding", &padding);

    PropVariantClear(&padding);
}
```



<span data-ttu-id="ba8e3-279">Para adicionar o preenchimento, crie um PROPVARIANT do tipo VT \_ UI4 e um valor correspondente ao número de bytes de preenchimento a serem adicionados.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-279">To add padding, create a PROPVARIANT of type VT\_UI4 and a value corresponding to the number of bytes of padding to add.</span></span> <span data-ttu-id="ba8e3-280">Um valor típico é 4096 bytes.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-280">A typical value is 4096 bytes.</span></span> <span data-ttu-id="ba8e3-281">As consultas de metadados para JPEG, TIFF e JPEG-XR estão nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-281">The metadata queries for JPEG, TIFF, and JPEG-XR are in this table.</span></span>



| <span data-ttu-id="ba8e3-282">Formato de metadados</span><span class="sxs-lookup"><span data-stu-id="ba8e3-282">Metadata format</span></span> | <span data-ttu-id="ba8e3-283">Consulta de metadados JPEG</span><span class="sxs-lookup"><span data-stu-id="ba8e3-283">JPEG metadata query</span></span>                  | <span data-ttu-id="ba8e3-284">TIFF, consulta de metadados de JPEG-XR</span><span class="sxs-lookup"><span data-stu-id="ba8e3-284">TIFF, JPEG-XR metadata query</span></span>    |
|-----------------|--------------------------------------|---------------------------------|
| <span data-ttu-id="ba8e3-285">IFD</span><span class="sxs-lookup"><span data-stu-id="ba8e3-285">IFD</span></span>             | <span data-ttu-id="ba8e3-286">/app1/ifd/PaddingSchema: preenchimento</span><span class="sxs-lookup"><span data-stu-id="ba8e3-286">/app1/ifd/PaddingSchema:Padding</span></span>      | <span data-ttu-id="ba8e3-287">/ifd/PaddingSchema: preenchimento</span><span class="sxs-lookup"><span data-stu-id="ba8e3-287">/ifd/PaddingSchema:Padding</span></span>      |
| <span data-ttu-id="ba8e3-288">EXIF</span><span class="sxs-lookup"><span data-stu-id="ba8e3-288">EXIF</span></span>            | <span data-ttu-id="ba8e3-289">/app1/ifd/exif/PaddingSchema: preenchimento</span><span class="sxs-lookup"><span data-stu-id="ba8e3-289">/app1/ifd/exif/PaddingSchema:Padding</span></span> | <span data-ttu-id="ba8e3-290">/ifd/exif/PaddingSchema: preenchimento</span><span class="sxs-lookup"><span data-stu-id="ba8e3-290">/ifd/exif/PaddingSchema:Padding</span></span> |
| <span data-ttu-id="ba8e3-291">XMP</span><span class="sxs-lookup"><span data-stu-id="ba8e3-291">XMP</span></span>             | <span data-ttu-id="ba8e3-292">/xmp/PaddingSchema: preenchimento</span><span class="sxs-lookup"><span data-stu-id="ba8e3-292">/xmp/PaddingSchema:Padding</span></span>           | <span data-ttu-id="ba8e3-293">/ifd/xmp/PaddingSchema: preenchimento</span><span class="sxs-lookup"><span data-stu-id="ba8e3-293">/ifd/xmp/PaddingSchema:Padding</span></span>  |
| <span data-ttu-id="ba8e3-294">GPS</span><span class="sxs-lookup"><span data-stu-id="ba8e3-294">GPS</span></span>             | <span data-ttu-id="ba8e3-295">/app1/ifd/gps/PaddingSchema: preenchimento</span><span class="sxs-lookup"><span data-stu-id="ba8e3-295">/app1/ifd/gps/PaddingSchema:Padding</span></span>  | <span data-ttu-id="ba8e3-296">/ifd/gps/PaddingSchema: preenchimento</span><span class="sxs-lookup"><span data-stu-id="ba8e3-296">/ifd/gps/PaddingSchema:Padding</span></span>  |



 

### <a name="obtaining-a-fast-metadata-encoder"></a><span data-ttu-id="ba8e3-297">Obtendo um codificador de metadados rápido</span><span class="sxs-lookup"><span data-stu-id="ba8e3-297">Obtaining a Fast Metadata Encoder</span></span>

<span data-ttu-id="ba8e3-298">Quando você tem uma imagem com preenchimento de metadados, um codificador de metadados rápido pode ser obtido usando os métodos **CreateFastMetadataEncoderFromDecoder** e **CreateFastMetadataEncoderFromFrameDecode** do Imaging Factory.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-298">When you have an image with metadata padding, a fast metadata encoder can be obtained by using the imaging factory methods **CreateFastMetadataEncoderFromDecoder** and **CreateFastMetadataEncoderFromFrameDecode**.</span></span>

<span data-ttu-id="ba8e3-299">Como o nome indica, o **CreateFastMetadataEncoderFromDecoder** cria um codificador de metadados rápido para metadados no nível do decodificador.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-299">As the name implies, **CreateFastMetadataEncoderFromDecoder** creates a fast metadata encoder for decoder-level metadata.</span></span> <span data-ttu-id="ba8e3-300">Os formatos de imagem nativa fornecidos pelo WIC não dão suporte a metadados em nível de decodificador, mas esse método é fornecido no caso de um formato de imagem ser desenvolvido no futuro.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-300">The native image formats provided by WIC do not support decoder-level metadata but this method is provided in case such an image format is developed in the future.</span></span>

<span data-ttu-id="ba8e3-301">O cenário mais comum é obter um codificador de metadados rápido de um quadro de imagem usando **CreateFastMetadataEncoderFromFrameDecode**.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-301">The more common scenario is to obtain a fast metadata encoder from an image frame by using **CreateFastMetadataEncoderFromFrameDecode**.</span></span> <span data-ttu-id="ba8e3-302">O código a seguir obtém um codificador de metadados rápidos de um quadro decodificado e altera o valor de classificação no bloco App1.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-302">The following code obtains a decoded frame's fast metadata encoder and changes the rating value in the App1 block.</span></span>


```
if (SUCCEEDED(hr))
{
    IWICFastMetadataEncoder *pFME = NULL;
    IWICMetadataQueryWriter *pFMEQW = NULL;

    hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(
        pFrameDecode, 
        &pFME);
}
```



### <a name="using-the-fast-metadata-encoder"></a><span data-ttu-id="ba8e3-303">Usando o codificador de metadados rápido</span><span class="sxs-lookup"><span data-stu-id="ba8e3-303">Using the Fast Metadata Encoder</span></span>

<span data-ttu-id="ba8e3-304">No codificador de metadados rápido, você pode obter um gravador de consulta.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-304">From the fast metadata encoder, you can obtain a query writer.</span></span> <span data-ttu-id="ba8e3-305">Isso permite que você grave metadados usando uma expressão de consulta como demonstrado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-305">This enables you to write metadata by using a query expression as previously demonstrated.</span></span> <span data-ttu-id="ba8e3-306">Depois que os metadados tiverem sido definidos no gravador de consultas, confirme o codificador de metadados rápidos para finalizar a atualização de metadados.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-306">After metadata has been set in the query writer, commit the fast metadata encoder to finalize the metadata update.</span></span> <span data-ttu-id="ba8e3-307">O código a seguir demonstra como configurar e confirmar as alterações de metadados</span><span class="sxs-lookup"><span data-stu-id="ba8e3-307">The following code demonstrates setting and committing the metadata changes</span></span>


```
    if (SUCCEEDED(hr))
    {
        hr = pFME->GetMetadataQueryWriter(&pFMEQW);
    }

    if (SUCCEEDED(hr))
    {
        // Add additional metadata
        PROPVARIANT value;

        PropVariantInit(&value);

        value.vt = VT_UI4;
        value.uiVal = 99;
        hr = pFMEQW->SetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);

        PropVariantClear(&value);
    }

    if (SUCCEEDED(hr))
    {
        hr = pFME->Commit();
    }
}
```



<span data-ttu-id="ba8e3-308">Se a **confirmação** falhar por algum motivo, será necessário codificar novamente a imagem para garantir que os novos metadados sejam adicionados à imagem.</span><span class="sxs-lookup"><span data-stu-id="ba8e3-308">If **Commit** fails for any reason, you will need to re-encode the image to ensure the new metadata is added to the image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba8e3-309">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ba8e3-309">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ba8e3-310">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="ba8e3-310">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ba8e3-311">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="ba8e3-311">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="ba8e3-312">Visão geral dos metadados do WIC</span><span class="sxs-lookup"><span data-stu-id="ba8e3-312">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="ba8e3-313">Visão geral da linguagem de consulta de metadados</span><span class="sxs-lookup"><span data-stu-id="ba8e3-313">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="ba8e3-314">Visão geral da extensibilidade de metadados</span><span class="sxs-lookup"><span data-stu-id="ba8e3-314">Metadata Extensibility Overview</span></span>](-wic-codec-metadatahandlers.md)
</dt> <dt>

[<span data-ttu-id="ba8e3-315">Como: codificar novamente uma imagem JPEG com metadados</span><span class="sxs-lookup"><span data-stu-id="ba8e3-315">How-to: Re-encode a JPEG Image with Metadata</span></span>](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 
