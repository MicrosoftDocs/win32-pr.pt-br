---
description: Este tópico apresenta o suporte a metadados de imagens fornecido pelo Windows Imaging Component (WIC).
ms.assetid: 35727810-3c4c-4c11-a4a2-3ae2cf3b8142
title: Visão geral dos metadados do WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f00e3a77eb74a3fb4a00db05ef9e00028f02ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551280"
---
# <a name="wic-metadata-overview"></a><span data-ttu-id="7cf43-103">Visão geral dos metadados do WIC</span><span class="sxs-lookup"><span data-stu-id="7cf43-103">WIC Metadata Overview</span></span>

<span data-ttu-id="7cf43-104">Este tópico apresenta o suporte a metadados de imagens fornecido pelo Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="7cf43-104">This topic introduces the imaging metadata support provided by the Windows Imaging Component (WIC).</span></span> <span data-ttu-id="7cf43-105">Ele fornece uma introdução à leitura e gravação de metadados de imagem, à linguagem de consulta de metadados e à extensibilidade do manipulador de metadados.</span><span class="sxs-lookup"><span data-stu-id="7cf43-105">It provides an introduction to reading and writing image metadata, the metadata query language, and metadata handler extensibility.</span></span>

<span data-ttu-id="7cf43-106">Metadados de imagem são dados inseridos dentro de um arquivo de imagem que fornece informações adicionais sobre a imagem, como o dispositivo usado para capturar a imagem ou as dimensões da imagem.</span><span class="sxs-lookup"><span data-stu-id="7cf43-106">Image metadata is data embedded inside an image file that provides additional information about the image, such as the device used to capture the image or the dimensions of the image.</span></span> <span data-ttu-id="7cf43-107">Embora esteja contido no próprio arquivo de imagem, esses metadados não fazem parte dos dados de renderização.</span><span class="sxs-lookup"><span data-stu-id="7cf43-107">Although it is contained within the image file itself, this metadata is not part of the rendering data.</span></span> <span data-ttu-id="7cf43-108">O WIC fornece interfaces que permitem que você leia e grave esses metadados para vários formatos de metadados comuns, incluindo XMP (Extensible Metadata Platform), EXIF (arquivo de imagem intercambiável) e dados textuais de png (texto).</span><span class="sxs-lookup"><span data-stu-id="7cf43-108">WIC provides interfaces that enable you to read and write this metadata for several common metadata formats including Extensible Metadata Platform (XMP), Exchangeable Image File (EXIF), and Png Textual Data (tEXt).</span></span>

<span data-ttu-id="7cf43-109">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="7cf43-109">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="7cf43-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="7cf43-110">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="7cf43-111">Introdução</span><span class="sxs-lookup"><span data-stu-id="7cf43-111">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="7cf43-112">Lendo metadados de imagem</span><span class="sxs-lookup"><span data-stu-id="7cf43-112">Reading Image Metadata</span></span>](#reading-image-metadata)
-   [<span data-ttu-id="7cf43-113">Gravando metadados de imagem</span><span class="sxs-lookup"><span data-stu-id="7cf43-113">Writing Image Metadata</span></span>](#writing-image-metadata)
-   [<span data-ttu-id="7cf43-114">Extensibilidade de metadados</span><span class="sxs-lookup"><span data-stu-id="7cf43-114">Metadata Extensibility</span></span>](#metadata-extensibility)
-   [<span data-ttu-id="7cf43-115">Formatos de metadados com suporte</span><span class="sxs-lookup"><span data-stu-id="7cf43-115">Supported Metadata Formats</span></span>](#supported-metadata-formats)
-   [<span data-ttu-id="7cf43-116">Resumo do componente de metadados</span><span class="sxs-lookup"><span data-stu-id="7cf43-116">Metadata Component Summary</span></span>](#metadata-component-summary)
-   [<span data-ttu-id="7cf43-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7cf43-117">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="7cf43-118">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="7cf43-118">Prerequisites</span></span>

<span data-ttu-id="7cf43-119">Para entender este tópico, você deve estar familiarizado com as interfaces do codificador e do codificador do WIC e seus componentes COM (Component Object Model) relacionados, conforme descrito na [visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="7cf43-119">To understand this topic, you should be familiar with the WIC encoder and decoder interfaces and their related Component Object Model (COM) components, as described in the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span> <span data-ttu-id="7cf43-120">Também ajuda a ter uma familiaridade geral com alguns dos formatos de metadados de geração de imagens usados hoje em dia.</span><span class="sxs-lookup"><span data-stu-id="7cf43-120">It also helps to have a general familiarity with some of the imaging metadata formats in use today.</span></span>

## <a name="introduction"></a><span data-ttu-id="7cf43-121">Introdução</span><span class="sxs-lookup"><span data-stu-id="7cf43-121">Introduction</span></span>

<span data-ttu-id="7cf43-122">Metadados fornecem informações estendidas sobre uma imagem.</span><span class="sxs-lookup"><span data-stu-id="7cf43-122">Metadata provides extended information about an image.</span></span> <span data-ttu-id="7cf43-123">Essas informações podem ser usadas de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="7cf43-123">This information can be used in several ways.</span></span> <span data-ttu-id="7cf43-124">Uma imagem pode conter metadados como uma descrição, classificação, marcas de categoria e informações de direitos autorais.</span><span class="sxs-lookup"><span data-stu-id="7cf43-124">An image might contain metadata such as a description, rating, category tags, and copyright information.</span></span> <span data-ttu-id="7cf43-125">O acesso aos metadados facilita a execução de tarefas como o gerenciamento de ativos, o local do arquivo ou a determinação de informações de direitos autorais.</span><span class="sxs-lookup"><span data-stu-id="7cf43-125">Accessing the metadata makes it easier to perform tasks such as asset management, file location, or determining copyright information.</span></span> <span data-ttu-id="7cf43-126">Por exemplo, a Galeria de fotos do Windows no Windows Vista permite que você adicione descrições e marcas de categoria a imagens.</span><span class="sxs-lookup"><span data-stu-id="7cf43-126">For example, the Windows Photo Gallery in Windows Vista enables you to add descriptions and category tags to images.</span></span> <span data-ttu-id="7cf43-127">Isso permite uma melhor descoberta de imagens e uma maneira conveniente de categorizar imagens.</span><span class="sxs-lookup"><span data-stu-id="7cf43-127">This allows for better discoverability of images and a convenient way to categorize images.</span></span> <span data-ttu-id="7cf43-128">Usando as APIs do WIC e os formatos de metadados comuns, os aplicativos podem facilmente escrever ou ler esse tipo de metadados de ou para imagens.</span><span class="sxs-lookup"><span data-stu-id="7cf43-128">Using the WIC APIs and common metadata formats, applications can easily write or read this type of metadata to or from images.</span></span>

<span data-ttu-id="7cf43-129">O diagrama a seguir ilustra o conteúdo de um arquivo JPEG que inclui blocos de metadados incorporados e itens de metadados.</span><span class="sxs-lookup"><span data-stu-id="7cf43-129">The following diagram illustrates the contents of a JPEG file that includes embedded metadata blocks and metadata items.</span></span>

![imagem JPEG com metadados de classificação](graphics/jpeg.png)

<span data-ttu-id="7cf43-131">Nesta imagem de exemplo, os metadados são inseridos no arquivo de imagem dentro de um quadro de imagem.</span><span class="sxs-lookup"><span data-stu-id="7cf43-131">In this example image, the metadata is embedded in the image file within an image frame.</span></span> <span data-ttu-id="7cf43-132">O formato JPEG não dá suporte a vários quadros de imagem, portanto, os metadados são anexados conceitualmente a esse único quadro.</span><span class="sxs-lookup"><span data-stu-id="7cf43-132">The JPEG format does not support multiple image frames, so the metadata is conceptually attached to this single frame.</span></span> <span data-ttu-id="7cf43-133">Formatos que dão suporte a vários quadros, como TIFF, podem ter metadados anexados a cada quadro de imagem, como mostra este diagrama.</span><span class="sxs-lookup"><span data-stu-id="7cf43-133">Formats that support multiple frames, such as TIFF, may have metadata attached to each image frame as this diagram shows.</span></span> <span data-ttu-id="7cf43-134">Embora não seja comum hoje e não tenha suporte dos codecs de imagem nativa, alguns formatos de imagem também podem oferecer suporte a metadados fora de um quadro de imagem.</span><span class="sxs-lookup"><span data-stu-id="7cf43-134">Though not common today and not supported by the native image codecs, some image formats may also support metadata outside of an image frame.</span></span> <span data-ttu-id="7cf43-135">O WIC é flexível o suficiente para lidar com metadados de nível de quadro e metadados fora do quadro individual de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="7cf43-135">WIC is flexible enough to handle both frame-level metadata and metadata outside of an image's individual frame.</span></span>

## <a name="reading-image-metadata"></a><span data-ttu-id="7cf43-136">Lendo metadados de imagem</span><span class="sxs-lookup"><span data-stu-id="7cf43-136">Reading Image Metadata</span></span>

<span data-ttu-id="7cf43-137">As APIs do WIC fornecem componentes COM que tornam mais fácil para os aplicativos ler e gravar metadados de imagem.</span><span class="sxs-lookup"><span data-stu-id="7cf43-137">The WIC APIs provide COM components that make it easy for applications to read and write image metadata.</span></span>

<span data-ttu-id="7cf43-138">A maneira principal de ler metadados é usar um [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)(leitor de consulta de metadados) para acessar itens de metadados específicos.</span><span class="sxs-lookup"><span data-stu-id="7cf43-138">The primary way to read metadata is to use a metadata query reader ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) to access specific metadata items.</span></span> <span data-ttu-id="7cf43-139">O componente leitor de consulta de metadados é implementado pelo codec e pode ser acessado no nível do decodificador ou por meio de quadros de imagem individuais, que é o método mais comum.</span><span class="sxs-lookup"><span data-stu-id="7cf43-139">The metadata query reader component is implemented by the codec and can be accessed at the decoder level or through individual image frames, which is the more common method.</span></span> <span data-ttu-id="7cf43-140">O código a seguir demonstra como acessar um leitor de consulta para um quadro individual usando o método **GetMetadataQueryReader** do leitor de consulta.</span><span class="sxs-lookup"><span data-stu-id="7cf43-140">The following code demonstrates how to access a query reader for an individual frame by using the query reader's **GetMetadataQueryReader** method.</span></span>


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



<span data-ttu-id="7cf43-141">Um leitor de consulta fornece métodos para obter informações sobre metadados específicos e um meio de especificar um item de metadados a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="7cf43-141">A query reader provides methods to obtain information about specific metadata, and a means to specify a metadata item to retrieve.</span></span> <span data-ttu-id="7cf43-142">O código a seguir usa uma expressão de consulta para solicitar um item de metadados específico dentro do bloco de IFD (diretório de arquivos de imagem aninhada) do App1.</span><span class="sxs-lookup"><span data-stu-id="7cf43-142">The following code uses a query expression to request a specific metadata item within the App1 nested image file directory (IFD) block.</span></span> <span data-ttu-id="7cf43-143">Isso é feito usando o método **GetMetadataByName** do leitor de consulta.</span><span class="sxs-lookup"><span data-stu-id="7cf43-143">This is done by using the query reader's **GetMetadataByName** method.</span></span> <span data-ttu-id="7cf43-144">O código a seguir demonstra como usar o leitor de consultas para obter o valor de classificação MicrosoftPhoto.</span><span class="sxs-lookup"><span data-stu-id="7cf43-144">The following code demonstrates using the query reader to obtain the MicrosoftPhoto rating value.</span></span>


```
PROPVARIANT value;
PropVariantInit(&value);

LPCWSTR pwzRatingQuery = L"/app1/ifd/{ushort=18249}";

if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(pwzRatingQuery, &value);
}
```



<span data-ttu-id="7cf43-145">A variável pwzRatingQuery no exemplo anterior é a cadeia de caracteres de consulta para acessar a classificação MicrosoftPhoto do item de metadados.</span><span class="sxs-lookup"><span data-stu-id="7cf43-145">The pwzRatingQuery variable in the preceding example is the query string to access the metadata item MicrosoftPhoto rating.</span></span> <span data-ttu-id="7cf43-146">Essa cadeia de caracteres é criada usando a linguagem de consulta de metadados.</span><span class="sxs-lookup"><span data-stu-id="7cf43-146">This string is created by using the metadata query language.</span></span> <span data-ttu-id="7cf43-147">Para criar essa cadeia de caracteres, é necessário ter conhecimento do formato de metadados e da linguagem de consulta de metadados para recuperar itens de metadados individuais.</span><span class="sxs-lookup"><span data-stu-id="7cf43-147">To create this string, knowledge of the metadata format and the metadata query language is needed to retrieve individual metadata items.</span></span> <span data-ttu-id="7cf43-148">Para obter mais informações sobre a linguagem de consulta de metadados, consulte [visão geral da linguagem de consulta de metadados](-wic-codec-metadataquerylanguage.md).</span><span class="sxs-lookup"><span data-stu-id="7cf43-148">For more information about the metadata query language, see the [Metadata Query Language Overview](-wic-codec-metadataquerylanguage.md).</span></span>

<span data-ttu-id="7cf43-149">Nos bastidores, um leitor de consulta usa um leitor de metadados ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) para acessar os metadados descritos pela expressão de consulta.</span><span class="sxs-lookup"><span data-stu-id="7cf43-149">Behind the scenes, a query reader uses a metadata reader ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) to access the metadata described by the query expression.</span></span> <span data-ttu-id="7cf43-150">Além de usar um leitor de consulta, você também pode acessar um leitor de metadados diretamente para ler os metadados.</span><span class="sxs-lookup"><span data-stu-id="7cf43-150">In addition to using a query reader, you can also access a metadata reader directly to read metadata.</span></span> <span data-ttu-id="7cf43-151">Você pode obter um leitor de metadados do decodificador ou quadros individuais consultando uma interface [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)(leitor de bloco).</span><span class="sxs-lookup"><span data-stu-id="7cf43-151">You can obtain a metadata reader from the decoder or individual frames by querying for a block reader ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) interface.</span></span>

## <a name="writing-image-metadata"></a><span data-ttu-id="7cf43-152">Gravando metadados de imagem</span><span class="sxs-lookup"><span data-stu-id="7cf43-152">Writing Image Metadata</span></span>

<span data-ttu-id="7cf43-153">O processo de gravação de metadados é semelhante ao modo como é lido, exceto pelo fato de que um [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)(gravador de consulta de metadados) é usado.</span><span class="sxs-lookup"><span data-stu-id="7cf43-153">The process of writing metadata is similar to the way it is read except that a metadata query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) is used.</span></span> <span data-ttu-id="7cf43-154">A interface do gravador de consulta é implementada pelo codificador de imagem e, como no leitor de consulta, os metadados são acessados no codificador e em quadros individuais (dependendo do suporte ao formato de imagem).</span><span class="sxs-lookup"><span data-stu-id="7cf43-154">The query writer interface is implemented by the image encoder and, as in the query reader, metadata is accessed both on the encoder and on individual frames (depending on image format support).</span></span>

<span data-ttu-id="7cf43-155">O código a seguir demonstra como obter um gravador de consulta de um quadro de codificador e remover o valor de classificação que foi lido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="7cf43-155">The following code demonstrates how to obtain a query writer from an encoder frame and remove the rating value that was previously read.</span></span>


```
// Get the frame's query writer
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
}

if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/app1/ifd/{ushort=18249}");
}
```



<span data-ttu-id="7cf43-156">Outra maneira de gravar metadados é por meio de atualizações rápidas de metadados.</span><span class="sxs-lookup"><span data-stu-id="7cf43-156">Another way to write metadata is through fast metadata updates.</span></span> <span data-ttu-id="7cf43-157">A codificação rápida de metadados é uma maneira de gravar metadados de imagem sem a necessidade de codificar novamente um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="7cf43-157">Fast metadata encoding is a way to write image metadata without having to re-encode an image file.</span></span> <span data-ttu-id="7cf43-158">Isso é feito com a gravação de novas informações de metadados em uma região preenchida do formato de metadados.</span><span class="sxs-lookup"><span data-stu-id="7cf43-158">This is done by writing new metadata information to a padded region of the metadata format.</span></span> <span data-ttu-id="7cf43-159">O [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)(codificador de metadados rápidos) é obtido da fábrica de componentes, com base no decodificador de imagem.</span><span class="sxs-lookup"><span data-stu-id="7cf43-159">The fast metadata encoder ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)) is obtained from the component factory, based on the image decoder.</span></span> <span data-ttu-id="7cf43-160">O codificador de metadados rápido Obtém um gravador de consulta que é usado para gravar os metadados.</span><span class="sxs-lookup"><span data-stu-id="7cf43-160">The fast metadata encoder then obtains a query writer that is used to write the metadata.</span></span> <span data-ttu-id="7cf43-161">Por fim, o codificador rápido confirma a alteração.</span><span class="sxs-lookup"><span data-stu-id="7cf43-161">Finally, the fast encoder commits the change.</span></span>

<span data-ttu-id="7cf43-162">O código a seguir demonstra como obter um codificador de metadados rápido e usá-lo para gravar o valor de MicrosoftRating.</span><span class="sxs-lookup"><span data-stu-id="7cf43-162">The following code demonstrates how to obtain a fast metadata encoder and use it to write the MicrosoftRating value.</span></span>


```
if (SUCCEEDED(hr))
{
    IWICFastMetadataEncoder *pFME = NULL;
    IWICMetadataQueryWriter *pFMEQW = NULL;

    hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(
        pFrameDecode,
        &pFME);

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



<span data-ttu-id="7cf43-163">Nem todos os formatos de metadados dão suporte a metadados rápidos.</span><span class="sxs-lookup"><span data-stu-id="7cf43-163">Not all metadata formats support fast metadata.</span></span> <span data-ttu-id="7cf43-164">Para ver quais formatos com suporte nativo dão suporte à codificação de metadados rápida, consulte a tabela na seção [formatos de metadados com suporte](#supported-metadata-formats) mais adiante neste documento.</span><span class="sxs-lookup"><span data-stu-id="7cf43-164">To see which natively supported formats support fast metadata encoding, see the table in the [Supported Metadata Formats](#supported-metadata-formats) section later in this document.</span></span>

<span data-ttu-id="7cf43-165">Nos bastidores, um gravador de consulta usa um gravador de metadados ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) para gravar os metadados descritos pela expressão de consulta.</span><span class="sxs-lookup"><span data-stu-id="7cf43-165">Behind the scenes, a query writer uses a metadata writer ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) to write the metadata described by the query expression.</span></span> <span data-ttu-id="7cf43-166">Além de usar um leitor de consulta, você também pode acessar um gravador de metadados diretamente para gravar metadados.</span><span class="sxs-lookup"><span data-stu-id="7cf43-166">In addition to using a query reader, you can also access a metadata writer directly to write metadata.</span></span> <span data-ttu-id="7cf43-167">Você pode obter um gravador de metadados do decodificador ou quadros individuais usando a consulta para uma interface de gravador de bloco ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)).</span><span class="sxs-lookup"><span data-stu-id="7cf43-167">You can obtain a metadata writer from the decoder or individual frames using querying for a block writer ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)) interface.</span></span>

## <a name="metadata-extensibility"></a><span data-ttu-id="7cf43-168">Extensibilidade de metadados</span><span class="sxs-lookup"><span data-stu-id="7cf43-168">Metadata Extensibility</span></span>

<span data-ttu-id="7cf43-169">Conforme mencionado anteriormente, o WIC fornece vários manipuladores de metadados para ler e gravar metadados para formatos de metadados comuns.</span><span class="sxs-lookup"><span data-stu-id="7cf43-169">As mentioned previously, WIC provides several metadata handlers to read and write metadata for common metadata formats.</span></span> <span data-ttu-id="7cf43-170">No entanto, há alguns formatos de metadados que não têm suporte nativo.</span><span class="sxs-lookup"><span data-stu-id="7cf43-170">However, there are some metadata formats that are not natively supported.</span></span> <span data-ttu-id="7cf43-171">Portanto, o WIC fornece APIs para criar manipuladores de metadados adicionais que podem estender o suporte de metadados para outros formatos.</span><span class="sxs-lookup"><span data-stu-id="7cf43-171">Therefore, WIC provides APIs for creating additional metadata handlers that can extend metadata support to other formats.</span></span>

<span data-ttu-id="7cf43-172">Para oferecer suporte total a outros formatos de metadados, dois tipos de manipuladores devem ser desenvolvidos — um leitor de metadados para ler metadados e um gravador de metadados para gravar metadados.</span><span class="sxs-lookup"><span data-stu-id="7cf43-172">To fully support other metadata formats, two types of handlers must be developed — a metadata reader to read metadata and a metadata writer to write metadata.</span></span> <span data-ttu-id="7cf43-173">Embora esses dois manipuladores sejam geralmente implementados em pares para um formato específico, isso não é um requisito.</span><span class="sxs-lookup"><span data-stu-id="7cf43-173">Although these two handlers are usually implemented in pairs for a specific format, that is not a requirement.</span></span> <span data-ttu-id="7cf43-174">Pode haver alguns casos em que apenas a capacidade de leitura ou apenas a capacidade de gravação é necessária.</span><span class="sxs-lookup"><span data-stu-id="7cf43-174">There might be some cases in which only the read ability or only the write ability is needed.</span></span>

<span data-ttu-id="7cf43-175">Para obter mais informações sobre a extensibilidade de metadados usando as APIs do WIC, consulte [visão geral da extensibilidade de metadados](-wic-codec-metadatahandlers.md).</span><span class="sxs-lookup"><span data-stu-id="7cf43-175">For more information on metadata extensibility using the WIC APIs, see the [Metadata Extensibility Overview](-wic-codec-metadatahandlers.md).</span></span>

## <a name="supported-metadata-formats"></a><span data-ttu-id="7cf43-176">Formatos de metadados com suporte</span><span class="sxs-lookup"><span data-stu-id="7cf43-176">Supported Metadata Formats</span></span>

<span data-ttu-id="7cf43-177">O WIC fornece suporte para vários formatos de metadados comuns.</span><span class="sxs-lookup"><span data-stu-id="7cf43-177">WIC provides support for several common metadata formats.</span></span> <span data-ttu-id="7cf43-178">A tabela a seguir lista os formatos de metadados com suporte, suas versões, os formatos de imagem que oferecem suporte ao formato de metadados e se o formato de metadados oferece suporte à codificação de metadados rápida.</span><span class="sxs-lookup"><span data-stu-id="7cf43-178">The following table lists the supported metadata formats, their versions, the image formats that support the metadata format, and whether the metadata format supports fast metadata encoding.</span></span> <span data-ttu-id="7cf43-179">Para obter mais informações sobre a codificação rápida de metadados, consulte a seção [gravando metadados de imagem](#writing-image-metadata) anteriormente neste documento.</span><span class="sxs-lookup"><span data-stu-id="7cf43-179">For more information about fast metadata encoding, see the [Writing Image Metadata](#writing-image-metadata) section earlier in this document.</span></span>



| <span data-ttu-id="7cf43-180">Formatos de metadados com suporte</span><span class="sxs-lookup"><span data-stu-id="7cf43-180">Supported metadata formats</span></span> | <span data-ttu-id="7cf43-181">Versão de especificação de metadados</span><span class="sxs-lookup"><span data-stu-id="7cf43-181">Metadata specification version</span></span> | <span data-ttu-id="7cf43-182">Suporte ao formato de imagem</span><span class="sxs-lookup"><span data-stu-id="7cf43-182">Image format support</span></span> | <span data-ttu-id="7cf43-183">Dá suporte à codificação de metadados rápida</span><span class="sxs-lookup"><span data-stu-id="7cf43-183">Supports fast metadata encoding</span></span> |
|----------------------------|--------------------------------|----------------------|---------------------------------|
| <span data-ttu-id="7cf43-184">App0</span><span class="sxs-lookup"><span data-stu-id="7cf43-184">App0</span></span>                       | <span data-ttu-id="7cf43-185">JFIF 1, 2</span><span class="sxs-lookup"><span data-stu-id="7cf43-185">JFIF 1.02</span></span>                      | <span data-ttu-id="7cf43-186">JPEG</span><span class="sxs-lookup"><span data-stu-id="7cf43-186">JPEG</span></span>                 | <span data-ttu-id="7cf43-187">No</span><span class="sxs-lookup"><span data-stu-id="7cf43-187">No</span></span>                              |
| <span data-ttu-id="7cf43-188">Aplicativo1</span><span class="sxs-lookup"><span data-stu-id="7cf43-188">App1</span></span>                       | <span data-ttu-id="7cf43-189">JFIF 1, 2</span><span class="sxs-lookup"><span data-stu-id="7cf43-189">JFIF 1.02</span></span>                      | <span data-ttu-id="7cf43-190">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="7cf43-190">JPEG, TIFF</span></span>           | <span data-ttu-id="7cf43-191">No</span><span class="sxs-lookup"><span data-stu-id="7cf43-191">No</span></span>                              |
| <span data-ttu-id="7cf43-192">App13</span><span class="sxs-lookup"><span data-stu-id="7cf43-192">App13</span></span>                      | <span data-ttu-id="7cf43-193">Unknown</span><span class="sxs-lookup"><span data-stu-id="7cf43-193">Unknown</span></span>                        | <span data-ttu-id="7cf43-194">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="7cf43-194">JPEG, TIFF</span></span>           | <span data-ttu-id="7cf43-195">No</span><span class="sxs-lookup"><span data-stu-id="7cf43-195">No</span></span>                              |
| <span data-ttu-id="7cf43-196">IFD</span><span class="sxs-lookup"><span data-stu-id="7cf43-196">IFD</span></span>                        | <span data-ttu-id="7cf43-197">TIFF 6,0</span><span class="sxs-lookup"><span data-stu-id="7cf43-197">TIFF 6.0</span></span>                       | <span data-ttu-id="7cf43-198">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="7cf43-198">JPEG, TIFF</span></span>           | <span data-ttu-id="7cf43-199">Yes</span><span class="sxs-lookup"><span data-stu-id="7cf43-199">Yes</span></span>                             |
| <span data-ttu-id="7cf43-200">IRB</span><span class="sxs-lookup"><span data-stu-id="7cf43-200">IRB</span></span>                        | <span data-ttu-id="7cf43-201">Unknown</span><span class="sxs-lookup"><span data-stu-id="7cf43-201">Unknown</span></span>                        | <span data-ttu-id="7cf43-202">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="7cf43-202">JPEG, TIFF</span></span>           | <span data-ttu-id="7cf43-203">No</span><span class="sxs-lookup"><span data-stu-id="7cf43-203">No</span></span>                              |
| <span data-ttu-id="7cf43-204">Exif</span><span class="sxs-lookup"><span data-stu-id="7cf43-204">Exif</span></span>                       | <span data-ttu-id="7cf43-205">EXIF 2,2</span><span class="sxs-lookup"><span data-stu-id="7cf43-205">Exif 2.2</span></span>                       | <span data-ttu-id="7cf43-206">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="7cf43-206">JPEG, TIFF</span></span>           | <span data-ttu-id="7cf43-207">Yes</span><span class="sxs-lookup"><span data-stu-id="7cf43-207">Yes</span></span>                             |
| <span data-ttu-id="7cf43-208">XMP</span><span class="sxs-lookup"><span data-stu-id="7cf43-208">XMP</span></span>                        | <span data-ttu-id="7cf43-209">XMP 1,0 (setembro de 2005)</span><span class="sxs-lookup"><span data-stu-id="7cf43-209">XMP 1.0 (Sept 2005)</span></span>            | <span data-ttu-id="7cf43-210">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="7cf43-210">JPEG, TIFF</span></span>           | <span data-ttu-id="7cf43-211">Yes</span><span class="sxs-lookup"><span data-stu-id="7cf43-211">Yes</span></span>                             |
| <span data-ttu-id="7cf43-212">GPS</span><span class="sxs-lookup"><span data-stu-id="7cf43-212">GPS</span></span>                        | <span data-ttu-id="7cf43-213">EXIF 2,2</span><span class="sxs-lookup"><span data-stu-id="7cf43-213">Exif 2.2</span></span>                       | <span data-ttu-id="7cf43-214">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="7cf43-214">JPEG, TIFF</span></span>           | <span data-ttu-id="7cf43-215">Yes</span><span class="sxs-lookup"><span data-stu-id="7cf43-215">Yes</span></span>                             |
| <span data-ttu-id="7cf43-216">IPTC</span><span class="sxs-lookup"><span data-stu-id="7cf43-216">IPTC</span></span>                       | <span data-ttu-id="7cf43-217">IPTC 4,0</span><span class="sxs-lookup"><span data-stu-id="7cf43-217">IPTC 4.0</span></span>                       | <span data-ttu-id="7cf43-218">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="7cf43-218">JPEG, TIFF</span></span>           | <span data-ttu-id="7cf43-219">Yes</span><span class="sxs-lookup"><span data-stu-id="7cf43-219">Yes</span></span>                             |
| <span data-ttu-id="7cf43-220">Texto</span><span class="sxs-lookup"><span data-stu-id="7cf43-220">tEXt</span></span>                       | <span data-ttu-id="7cf43-221">PNG 1,2</span><span class="sxs-lookup"><span data-stu-id="7cf43-221">PNG 1.2</span></span>                        | <span data-ttu-id="7cf43-222">PNG</span><span class="sxs-lookup"><span data-stu-id="7cf43-222">PNG</span></span>                  | <span data-ttu-id="7cf43-223">No</span><span class="sxs-lookup"><span data-stu-id="7cf43-223">No</span></span>                              |



 

> [!Note]  
> <span data-ttu-id="7cf43-224">O IPTC só dá suporte a FME se os blocos crescerem em tamanho, pois o IPTC não oferece suporte a preenchimento.</span><span class="sxs-lookup"><span data-stu-id="7cf43-224">IPTC only supports FME if the blocks grow in size, as IPTC does not support padding.</span></span>

 

## <a name="metadata-component-summary"></a><span data-ttu-id="7cf43-225">Resumo do componente de metadados</span><span class="sxs-lookup"><span data-stu-id="7cf43-225">Metadata Component Summary</span></span>

<span data-ttu-id="7cf43-226">A tabela a seguir descreve as interfaces WIC que dão suporte a metadados e seus componentes correspondentes.</span><span class="sxs-lookup"><span data-stu-id="7cf43-226">The following table describes the WIC interfaces that support metadata, and their corresponding components.</span></span> <span data-ttu-id="7cf43-227">Esses componentes fornecem o acesso aos metadados de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="7cf43-227">These components provide the access to an image's metadata.</span></span> <span data-ttu-id="7cf43-228">Para obter mais informações sobre esses componentes, consulte [visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="7cf43-228">For more information about these components, see the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7cf43-229">Componente</span><span class="sxs-lookup"><span data-stu-id="7cf43-229">Component</span></span></th>
<th><span data-ttu-id="7cf43-230">Descrição</span><span class="sxs-lookup"><span data-stu-id="7cf43-230">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7cf43-231">Decodificador de bitmap (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="7cf43-231">Bitmap Decoder (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="7cf43-232">Lê um fluxo de imagem e produz uma fonte de bitmap utilizável.</span><span class="sxs-lookup"><span data-stu-id="7cf43-232">Reads an image stream and produces a usable bitmap source.</span></span> <span data-ttu-id="7cf43-233">Associado a um formato de contêiner, como TIFF (Tagged Image File Format) ou JPEG (grupo de especialistas fotográfico) conjunta.</span><span class="sxs-lookup"><span data-stu-id="7cf43-233">Associated with a container format such as Tagged Image File Format (TIFF) or Joint Photographic Experts Group (JPEG).</span></span></li>
<li><span data-ttu-id="7cf43-234">Implementa uma interface <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> para enumerar todos os blocos de metadados no fluxo de dados do decodificador que não estão dentro de um quadro.</span><span class="sxs-lookup"><span data-stu-id="7cf43-234">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> interface to enumerate all of the metadata blocks in the decoder's data stream that are not inside a frame.</span></span></li>
<li><span data-ttu-id="7cf43-235">Expõe um leitor de consulta para ler os metadados associados à imagem que não está dentro de um quadro.</span><span class="sxs-lookup"><span data-stu-id="7cf43-235">Exposes a query reader to read the metadata associated with the image that is not inside a frame.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cf43-236">Decodificação de quadros de bitmap (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="7cf43-236">Bitmap Frame Decode (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="7cf43-237">Acessa quadros individuais do fluxo de imagem mantido pelo decodificador.</span><span class="sxs-lookup"><span data-stu-id="7cf43-237">Accesses individual frames from the image stream held by the decoder.</span></span></li>
<li><span data-ttu-id="7cf43-238">Implementa uma interface <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> para enumerar todos os blocos de metadados no fluxo de dados do quadro.</span><span class="sxs-lookup"><span data-stu-id="7cf43-238">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> interface to enumerate all of the metadata blocks in the frame's data stream.</span></span></li>
<li><span data-ttu-id="7cf43-239">Expõe um leitor de consulta para ler os metadados associados ao quadro, usando expressões de consulta.</span><span class="sxs-lookup"><span data-stu-id="7cf43-239">Exposes a query reader to read the metadata associated with the frame, using query expressions.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cf43-240">Codificador de bitmap (<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="7cf43-240">Bitmap Encoder (<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="7cf43-241">Grava uma origem de bitmap em um fluxo de imagem.</span><span class="sxs-lookup"><span data-stu-id="7cf43-241">Writes a bitmap source to an image stream.</span></span> <span data-ttu-id="7cf43-242">Associado a um formato de contêiner como TIFF ou JPEG.</span><span class="sxs-lookup"><span data-stu-id="7cf43-242">Associated with a container format such as TIFF or JPEG.</span></span></li>
<li><span data-ttu-id="7cf43-243">Implementa uma interface <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> para criar uma lista de blocos de metadados para gravar no fluxo de dados do codificador.</span><span class="sxs-lookup"><span data-stu-id="7cf43-243">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> interface to build up a list of metadata blocks to write into the data stream of the encoder.</span></span></li>
<li><span data-ttu-id="7cf43-244">Expõe um gravador de consulta para gravar os metadados associados à imagem, usando expressões de consulta.</span><span class="sxs-lookup"><span data-stu-id="7cf43-244">Exposes a query writer to write the metadata associated with the image, using query expressions.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cf43-245">Bitma frame Encode (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="7cf43-245">Bitma Frame Encode (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="7cf43-246">Cria um quadro que será codificado no fluxo mantido pelo codificador.</span><span class="sxs-lookup"><span data-stu-id="7cf43-246">Creates a frame that will be encoded into the stream held by the encoder.</span></span></li>
<li><span data-ttu-id="7cf43-247">Implementa uma interface <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> para criar uma lista de blocos de metadados para gravar no fluxo de dados do quadro.</span><span class="sxs-lookup"><span data-stu-id="7cf43-247">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> interface to build up a list of metadata blocks to write into the frame's data stream.</span></span></li>
<li><span data-ttu-id="7cf43-248">Expõe um gravador de consulta para gravar os metadados associados ao quadro, usando expressões de consulta.</span><span class="sxs-lookup"><span data-stu-id="7cf43-248">Exposes a query writer to write the metadata associated with the frame, using query expressions.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7cf43-249">A tabela a seguir descreve os componentes de metadados do WIC.</span><span class="sxs-lookup"><span data-stu-id="7cf43-249">The following table describes the WIC metadata components.</span></span> <span data-ttu-id="7cf43-250">Esses componentes permitem que você leia e grave os metadados em uma imagem exposta pelos componentes listados na tabela anterior.</span><span class="sxs-lookup"><span data-stu-id="7cf43-250">These components enable you to read and write the metadata in an image exposed by the components listed in the previous table.</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7cf43-251">Componente</span><span class="sxs-lookup"><span data-stu-id="7cf43-251">Component</span></span></th>
<th><span data-ttu-id="7cf43-252">Descrição</span><span class="sxs-lookup"><span data-stu-id="7cf43-252">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7cf43-253">Leitor de consulta de metadados (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader"><strong>IWICMetadataQueryReader</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="7cf43-253">Metadata Query Reader (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader"><strong>IWICMetadataQueryReader</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="7cf43-254">Usa uma cadeia de caracteres de consulta e navega pela hierarquia de metadados subjacente para obter metadados.</span><span class="sxs-lookup"><span data-stu-id="7cf43-254">Takes a query string and navigates the underlying metadata hierarchy to get metadata.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cf43-255">Gravador de consulta de metadados (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter"><strong>IWICMetadataQueryWriter</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="7cf43-255">Metadata Query Writer (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter"><strong>IWICMetadataQueryWriter</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="7cf43-256">Usa uma cadeia de caracteres de consulta e navega pela hierarquia de metadados subjacente para obter, definir e remover metadados.</span><span class="sxs-lookup"><span data-stu-id="7cf43-256">Takes a query string and navigates the underlying metadata hierarchy to get, set, and remove metadata.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cf43-257">Iniwicmetadatablockreader (leitor<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong></strong></a>de bloco de metadados)</span><span class="sxs-lookup"><span data-stu-id="7cf43-257">Metadata Block Reader (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="7cf43-258">Gerencia uma coleção somente leitura de objetos <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a> na parte superior da hierarquia de metadados e habilita a enumeração de todos os blocos de metadados.</span><span class="sxs-lookup"><span data-stu-id="7cf43-258">Manages a read-only collection of <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a> objects at the top of the metadata hierarchy and enables enumeration of all metadata blocks.</span></span></li>
<li><span data-ttu-id="7cf43-259">Implementado por um decodificador de bitmap e um quadro de bitmap decodificado.</span><span class="sxs-lookup"><span data-stu-id="7cf43-259">Implemented by a bitmap decoder and a decoded bitmap frame.</span></span></li>
<li><span data-ttu-id="7cf43-260">Implementados por desenvolvedores de componentes de terceiros para codecs personalizados.</span><span class="sxs-lookup"><span data-stu-id="7cf43-260">Implemented by third-party component developers for custom codecs.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cf43-261">Gravador de bloco de metadados (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="7cf43-261">Metadata Block Writer (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="7cf43-262">Gerencia uma coleção de leitura e gravação de objetos <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a> na parte superior da hierarquia de metadados.</span><span class="sxs-lookup"><span data-stu-id="7cf43-262">Manages a read and write collection of <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a> objects at the top of the metadata hierarchy.</span></span></li>
<li><span data-ttu-id="7cf43-263">Implementado por um codificador de bitmap e uma codificação de quadro de bitmap.</span><span class="sxs-lookup"><span data-stu-id="7cf43-263">Implemented by a bitmap encoder and a bitmap frame encode.</span></span></li>
<li><span data-ttu-id="7cf43-264">Implementados por desenvolvedores de componentes de terceiros para codecs personalizados.</span><span class="sxs-lookup"><span data-stu-id="7cf43-264">Implemented by third-party component developers for custom codecs.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cf43-265">Leitor de metadados (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="7cf43-265">Metadata Reader (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="7cf43-266">Analisa um fluxo de metadados e gerencia uma coleção somente leitura dos itens de metadados.</span><span class="sxs-lookup"><span data-stu-id="7cf43-266">Parses a stream of metadata and manages a read-only collection of the metadata items.</span></span> <span data-ttu-id="7cf43-267">Associado a um formato de metadados como EXIF, IFD e XMP.</span><span class="sxs-lookup"><span data-stu-id="7cf43-267">Associated with a metadata format such as EXIF, IFD, and XMP.</span></span></li>
<li><span data-ttu-id="7cf43-268">Atua como um dicionário, retornando um valor quando um par de formato e ID é fornecido.</span><span class="sxs-lookup"><span data-stu-id="7cf43-268">Acts as a dictionary, returning a value when given a format and ID pair.</span></span></li>
<li><span data-ttu-id="7cf43-269">Implementado por desenvolvedores de componentes de terceiros para tipos de metadados personalizados.</span><span class="sxs-lookup"><span data-stu-id="7cf43-269">Implemented by third-party component developers for custom metadata types.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cf43-270">Gravador de metadados (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="7cf43-270">Metadata Writer (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="7cf43-271">Analisa e serializa um fluxo de metadados e gerencia uma coleção de leitura/gravação de itens de metadados.</span><span class="sxs-lookup"><span data-stu-id="7cf43-271">Parses and serializes a stream of metadata and manages a read/write collection of metadata items.</span></span></li>
<li><span data-ttu-id="7cf43-272">Implementado por desenvolvedores de componentes de terceiros para tipos de metadados personalizados.</span><span class="sxs-lookup"><span data-stu-id="7cf43-272">Implemented by third-party component developers for custom metadata types.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cf43-273">IWICFastMetadataEncoder do codificador de metadados rápidos<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder"><strong></strong></a></span><span class="sxs-lookup"><span data-stu-id="7cf43-273">Fast Metadata Encoder<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder"><strong>IWICFastMetadataEncoder</strong></a></span></span></td>
<td><ul>
<li><span data-ttu-id="7cf43-274">Expõe a semântica para gravar em uma hierarquia de metadados que atualizará os metadados no local sem codificar novamente a imagem.</span><span class="sxs-lookup"><span data-stu-id="7cf43-274">Exposes semantics for writing on a metadata hierarchy that will update metadata in place without re-encoding the image.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="7cf43-275">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7cf43-275">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7cf43-276">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="7cf43-276">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7cf43-277">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="7cf43-277">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="7cf43-278">Visão geral da linguagem de consulta de metadados</span><span class="sxs-lookup"><span data-stu-id="7cf43-278">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="7cf43-279">Visão geral da leitura e gravação de metadados de imagem</span><span class="sxs-lookup"><span data-stu-id="7cf43-279">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="7cf43-280">Visão geral da extensibilidade de metadados</span><span class="sxs-lookup"><span data-stu-id="7cf43-280">Metadata Extensibility Overview</span></span>](-wic-codec-metadatahandlers.md)
</dt> <dt>

[<span data-ttu-id="7cf43-281">Como: codificar novamente uma imagem JPEG com metadados</span><span class="sxs-lookup"><span data-stu-id="7cf43-281">How-to: Re-encode a JPEG Image with Metadata</span></span>](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 



