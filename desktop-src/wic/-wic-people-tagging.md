---
description: Este tópico apresenta o novo esquema XMP (Extensible Metadata Platform) e o sistema de propriedades de fotos do Windows 7. photos. Peoples que habilita a marcação de indivíduos em uma foto digital.
ms.assetid: 557c3e9a-1756-4abb-8465-b12195ecbc91
title: Visão geral de marcação de pessoas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64f2080e51d4d340474e0610fcce9512fc72429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091743"
---
# <a name="people-tagging-overview"></a><span data-ttu-id="4bbe3-103">Visão geral de marcação de pessoas</span><span class="sxs-lookup"><span data-stu-id="4bbe3-103">People Tagging Overview</span></span>

<span data-ttu-id="4bbe3-104">Este tópico apresenta o novo esquema XMP (Extensible Metadata Platform) e o sistema de propriedades de fotos do Windows 7 [. photos. Peoples](../properties/props-system-photo-peoplenames.md) que habilita a marcação de indivíduos em uma foto digital.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-104">This topic introduces the new Extensible Metadata Platform (XMP) schema and the Windows 7 photo property [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) that enables the tagging of individuals in a digital photo.</span></span> <span data-ttu-id="4bbe3-105">Este tópico também aborda como usar a API do Windows Imaging Component (WIC) para ler e gravar os metadados necessários para a marcação de pessoas.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-105">This topic also discusses how to use the Windows Imaging Component (WIC) API to both read and write the metadata needed for people tagging.</span></span>

<span data-ttu-id="4bbe3-106">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="4bbe3-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="4bbe3-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="4bbe3-108">Introdução</span><span class="sxs-lookup"><span data-stu-id="4bbe3-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="4bbe3-109">Marcação de pessoas</span><span class="sxs-lookup"><span data-stu-id="4bbe3-109">People Tagging</span></span>](#people-tagging-overview)
    -   [<span data-ttu-id="4bbe3-110">Nomes de pessoas</span><span class="sxs-lookup"><span data-stu-id="4bbe3-110">People Names</span></span>](#people-names)
    -   [<span data-ttu-id="4bbe3-111">Retângulos de pessoas</span><span class="sxs-lookup"><span data-stu-id="4bbe3-111">People Rectangles</span></span>](#people-rectangles)
-   [<span data-ttu-id="4bbe3-112">Referência de esquema</span><span class="sxs-lookup"><span data-stu-id="4bbe3-112">Schema Reference</span></span>](#schema-reference)
    -   [<span data-ttu-id="4bbe3-113">Esquema do Microsoft Photo 1,2</span><span class="sxs-lookup"><span data-stu-id="4bbe3-113">Microsoft Photo 1.2 Schema</span></span>](#microsoft-photo-12-schema)
    -   [<span data-ttu-id="4bbe3-114">Esquema do Microsoft Photo RegionInfo</span><span class="sxs-lookup"><span data-stu-id="4bbe3-114">Microsoft Photo RegionInfo Schema</span></span>](#microsoft-photo-regioninfo-schema)
    -   [<span data-ttu-id="4bbe3-115">Esquema de região fotográfica da Microsoft</span><span class="sxs-lookup"><span data-stu-id="4bbe3-115">Microsoft Photo Region Schema</span></span>](#microsoft-photo-regioninfo-schema)
    -   [<span data-ttu-id="4bbe3-116">Metadados de exemplo</span><span class="sxs-lookup"><span data-stu-id="4bbe3-116">Sample Metadata</span></span>](#sample-metadata)
-   [<span data-ttu-id="4bbe3-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4bbe3-117">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="4bbe3-118">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="4bbe3-118">Prerequisites</span></span>

<span data-ttu-id="4bbe3-119">Para entender este tópico, você deve estar familiarizado com as interfaces do decodificador do WIC e seus componentes COM (Component Object Model) relacionados, conforme descrito no [visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="4bbe3-119">To understand this topic, you should be familiar with the WIC decoder interfaces and its related Component Object Model (COM) components, as described in the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span> <span data-ttu-id="4bbe3-120">Também ajuda a ter uma familiaridade geral com metadados de geração de imagens, especialmente XMP.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-120">It also helps to have a general familiarity with imaging metadata, especially XMP.</span></span>

## <a name="introduction"></a><span data-ttu-id="4bbe3-121">Introdução</span><span class="sxs-lookup"><span data-stu-id="4bbe3-121">Introduction</span></span>

<span data-ttu-id="4bbe3-122">A Microsoft criou um novo esquema XMP para marcar pessoas em uma imagem digital.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-122">Microsoft has created a new XMP schema for tagging people within a digital image.</span></span> <span data-ttu-id="4bbe3-123">Esse esquema permite que os aplicativos armazenem os nomes e locais de indivíduos que estão na imagem como metadados dentro da imagem.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-123">This schema enables applications to store the names and locations of individuals who are in the image as metadata within the image.</span></span> <span data-ttu-id="4bbe3-124">Além do novo esquema, a nova propriedade de foto [System. Photo. peoplenames](../properties/props-system-photo-peoplenames.md) está disponível no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-124">In addition to the new schema, the new photo property [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) is available in Windows 7.</span></span> <span data-ttu-id="4bbe3-125">Essa nova propriedade permite que os aplicativos leiam os nomes de indivíduo armazenados nos metadados da imagem.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-125">This new property enables applications to read the individual's names stored in the image metadata.</span></span> <span data-ttu-id="4bbe3-126">O WIC utiliza esses novos recursos, permitindo que os aplicativos leiam e gravem facilmente os metadados de marcação de pessoas em fotos digitais.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-126">WIC utilizes these new features by enabling applications to easily read and write people tagging metadata to digital photos.</span></span>

## <a name="people-tagging"></a><span data-ttu-id="4bbe3-127">Marcação de pessoas</span><span class="sxs-lookup"><span data-stu-id="4bbe3-127">People Tagging</span></span>

<span data-ttu-id="4bbe3-128">O WIC fornece aos desenvolvedores de aplicativos com componentes COM que lêem dados de imagem, bem como metadados de imagem.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-128">WIC provides application developers with COM components which read image data as well as image metadata.</span></span> <span data-ttu-id="4bbe3-129">Para ler e gravar metadados, como o novo recurso de marcação de pessoas, o WIC fornece as interfaces [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) e [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="4bbe3-129">For reading and writing metadata, such as the new people tagging feature, WIC provides the [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) and [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) interfaces.</span></span> <span data-ttu-id="4bbe3-130">Essas interfaces permitem que os aplicativos usem a [linguagem de consulta de metadados](-wic-codec-metadataquerylanguage.md) para gravar metadados em quadros individuais de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-130">These interfaces enable applications to use the [metadata query language](-wic-codec-metadataquerylanguage.md) to write metadata to the individual frames of an image.</span></span> <span data-ttu-id="4bbe3-131">A seção a seguir demonstra como ler e gravar os metadados de marcação de pessoas em metadados de uma imagem usando leitores de consulta do WIC e gravadores.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-131">The following section demonstrates how to read and write the people-tagging metadata into an image's metadata by using WIC query readers and writers.</span></span>

### <a name="people-names"></a><span data-ttu-id="4bbe3-132">Nomes de pessoas</span><span class="sxs-lookup"><span data-stu-id="4bbe3-132">People Names</span></span>

<span data-ttu-id="4bbe3-133">Parte do recurso de marcação de pessoas é a capacidade de simplesmente obter uma lista dos nomes das pessoas marcadas na imagem.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-133">Part of the people-tagging feature is the ability to simply get a list the names of the people tagged within the image.</span></span> <span data-ttu-id="4bbe3-134">Esta parte do recurso é suportada pelos manipuladores de metadados [System. Photo. People](../properties/props-system-photo-peoplenames.md) e WIC.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-134">This part of the feature is supported by the [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) and WIC's metadata handlers.</span></span> <span data-ttu-id="4bbe3-135">A interface [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) , em conjunto com a propriedade System. Photo. peoplenames, é usada para ler os nomes das pessoas identificadas em uma imagem e armazenadas nos metadados da imagem.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-135">The [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) interface, in conjunction with the System.Photo.PeopleNames property, are used to read the names of people identified in an image and stored in the image metadata.</span></span>

<span data-ttu-id="4bbe3-136">O exemplo de código a seguir demonstra um leitor de consulta obtido de um quadro de imagem para consultar os metadados de uma imagem em busca de nomes marcados da propriedade [System. Photo. peoplenames](../properties/props-system-photo-peoplenames.md) .</span><span class="sxs-lookup"><span data-stu-id="4bbe3-136">The following code example demonstrates a query reader obtained from an image frame to query an image's metadata for tagged names of the [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) property.</span></span>


```C++
// Not shown: image decoding, retrieving an image frame. 
...
PROPVARIANT value;
IWICMetadataQueryReader *pQueryReader = NULL;
...
// Get the query reader.
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}

// Query for the System.Photo.PeopleNames property.
if (SUCCEEDED(hr))
{
    // Get the property metadata by property name.
    hr = pQueryReader->GetMetadataByName(L"System.Photo.PeopleNames", &value);
}
```



<span data-ttu-id="4bbe3-137">A expressão de consulta "System. Photo. Peoplenames" consulta o quadro para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-137">The query expression "System.Photo.PeopleNames" queries the frame for the property.</span></span> <span data-ttu-id="4bbe3-138">Se os metadados de marcação de pessoas existirem e contiverem nomes de pessoas, o valor [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) será definido como VT \_ LPWSTR e o valor dos dados conterá a lista de nomes marcados.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-138">If the people-tagging metadata exists and contains people's names, the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) value will be set to VT\_LPWSTR and the data value will contain the list of tagged names.</span></span> <span data-ttu-id="4bbe3-139">Para obter mais informações sobre como ler metadados de imagem, consulte [visão geral da leitura e gravação de metadados de imagem](-wic-codec-readingwritingmetadata.md).</span><span class="sxs-lookup"><span data-stu-id="4bbe3-139">For more information on reading image metadata, see [Overview of Reading and Writing Image Metadata](-wic-codec-readingwritingmetadata.md).</span></span>

<span data-ttu-id="4bbe3-140">Consultar a marca nomes de pessoas só será útil se a imagem contiver realmente os metadados de marcação de pessoas.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-140">Querying for the people names tag is only useful if the image actually contains the people-tagging metadata.</span></span> <span data-ttu-id="4bbe3-141">Para que isso ocorra, um aplicativo deve primeiro tê-lo gravado.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-141">For this to occur, an application must first have written it.</span></span> <span data-ttu-id="4bbe3-142">Para gravar os metadados de nomes de pessoas, use um [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) e o caminho XMP explícito dos metadados.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-142">To write the people names metadata, use an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) and the explicit XMP path of the metadata.</span></span> <span data-ttu-id="4bbe3-143">O exemplo de código a seguir demonstra como usar um gravador de consulta para gravar um nome no caminho de consulta.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-143">The following code example demonstrates using a query writer to write a name to the query path.</span></span>


```C++
// Not shown: image encoding, retrieving/creating the image frame,
// creating the IWICImagingFactory 
...
IWICImagingFactory *pFactory = NULL;
IWICMetadataQueryWriter *pQueryWriter = NULL;
...
// Get the query writer from the image frame.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pQueryWriter);
}

// A query writer specifically for this person's XMP struct
IWICMetadataQueryWriter *pXMPStructQueryWriter = NULL;

// Create a query writer specifically for an XMP Struct
hr = pFactory->CreateQueryWriter(
    GUID_MetadataFormatXMPStruct,
    NULL,
    &pXMPStructQueryWriter
    );

// Create a variant representing the structure created above
PROPVARIANT xmpStruct;
PropVariantInit(&xmpStruct);

// VT_UNKNOWN indicates that we're setting a COM object, in this case a XMPStruct
// which will hold the name and rectangle
xmpStruct.vt = VT_UNKNOWN; 
xmpStruct.punkVal = pXMPStructQueryWriter;

if(SUCCEEDED(hr))
{
    // WIC will automatically create the xmp base, the RegionInfo struct, and the Regions
    // bag (an unordered array) but structs within that bag need to be explicitly created.
    // The {ulong=0} in the query means to insert the new struct at the start of the bag,
    // {} could also be used to insert at the end of the bag.
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions/{ulong=0}",
        &xmpStruct
        );
}

// Set up the PROPVARIANT with the name information
PROPVARIANT personName;
PropVariantInit(&personName);
personName.vt = VT_LPWSTR;
personName.pwszVal = L"John Doe";

if(SUCCEEDED(hr))
{
    // Set the name metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:PersonDisplayName",
        &personName
        );  
}
```



<span data-ttu-id="4bbe3-144">Observe a etapa que constrói a estrutura XMP e a define em `MPRI:Regions/{ulong=0}` .</span><span class="sxs-lookup"><span data-stu-id="4bbe3-144">Note the step constructing the XMP structure and setting it under `MPRI:Regions/{ulong=0}`.</span></span> <span data-ttu-id="4bbe3-145">Sem essa etapa, o WIC não pode identificar onde colocá-lo `PersonDisplayName` mais tarde.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-145">Without this step, the WIC can't identify where to place the `PersonDisplayName` later on.</span></span> <span data-ttu-id="4bbe3-146">Observe também que o caminho de consulta explícito é usado em vez de [System. Photo. peoplenames](-wic-photoprop-system-photo-peoplenames.md), cuja política de metadados não dá suporte à gravação de metadados.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-146">Also note that the explicit query path is used instead of [System.Photo.PeopleNames](-wic-photoprop-system-photo-peoplenames.md), whose metadata policy does not support writing metadata.</span></span>

### <a name="people-rectangles"></a><span data-ttu-id="4bbe3-147">Retângulos de pessoas</span><span class="sxs-lookup"><span data-stu-id="4bbe3-147">People Rectangles</span></span>

<span data-ttu-id="4bbe3-148">No entanto, os nomes das pessoas são apenas parte do recurso de marcação de pessoas.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-148">People's names however, are only part of the people-tagging feature.</span></span> <span data-ttu-id="4bbe3-149">Além de armazenar nomes de pessoas nos metadados, o esquema também oferece suporte a informações de região que identificam a área específica (um retângulo) que a pessoa é mostrada na imagem.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-149">In addition to storing people's names in the metadata, the schema also supports region information that identifies the specific area (a rectangle) the person is shown in the image.</span></span>

<span data-ttu-id="4bbe3-150">As informações de retângulo são representadas por quatro valores decimais delimitados por vírgula, como "0,25, 0,25, 0,25, 0,25".</span><span class="sxs-lookup"><span data-stu-id="4bbe3-150">The rectangle information is represented by four comma-delimited decimal values, such as "0.25, 0.25, 0.25, 0.25".</span></span> <span data-ttu-id="4bbe3-151">Os dois primeiros valores especificam a coordenada superior esquerda; os dois finais especificam a altura e a largura do retângulo.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-151">The first two values specify the top-left coordinate; the final two specify the height and width of the rectangle.</span></span> <span data-ttu-id="4bbe3-152">As dimensões da imagem para fins de definição de retângulos de pessoas são normalizadas para 1, o que significa que, no exemplo "0,25, 0,25, 0,25, 0,25", o retângulo começa a 1/4 da distância da parte superior e da 1/4 da distância à esquerda da imagem.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-152">The dimensions of the image for the purposes of defining people rectangles are normalized to 1, which means that in the "0.25, 0.25, 0.25, 0.25" example, the rectangle starts 1/4 of the distance from the top and 1/4 of the distance from the left of the image.</span></span> <span data-ttu-id="4bbe3-153">A altura e a largura do retângulo são 1/4 do tamanho de suas respectivas dimensões de imagem.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-153">Both the height and width of the rectangle are 1/4 of the size of their respective image dimensions.</span></span>

<span data-ttu-id="4bbe3-154">As informações de retângulo que identificam indivíduos são escritas da mesma forma que os nomes das pessoas são escritas, dentro da mesma estrutura.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-154">The rectangle information that identifies individuals is written in the same way people's names are written, within the same structure.</span></span> <span data-ttu-id="4bbe3-155">Para gravar os metadados de retângulo, use um [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) e o caminho XMP explícito dos metadados.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-155">To write the rectangle metadata, use an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) and the explicit XMP path of the metadata.</span></span> <span data-ttu-id="4bbe3-156">O exemplo de código a seguir continua o exemplo anterior e adiciona um retângulo representando ' João doe ' aos metadados da imagem.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-156">The following code example continues the previous example and adds a rectangle representing 'John Doe' to the image's metadata.</span></span> <span data-ttu-id="4bbe3-157">Observe que ele usa o mesmo `{ulong=0}` índice para associar este retângulo a ' João doe '.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-157">Note that it uses the same `{ulong=0}` index to associate this rectangle with 'John Doe'.</span></span>


```C++
// Set up the PROPVARIANT with the rectangle information
PROPVARIANT rectangle;
PropVariantInit(&rectangle);
rectangle.vt = VT_LPWSTR;
rectangle.pwszVal = L"0.0,0.0,0.25,0.25";

if(SUCCEEDED(hr))
{
    // Set the rectangle metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:Rectangle",
        &rectangle
        );
}
```



## <a name="schema-reference"></a><span data-ttu-id="4bbe3-158">Referência de esquema</span><span class="sxs-lookup"><span data-stu-id="4bbe3-158">Schema Reference</span></span>

<span data-ttu-id="4bbe3-159">Os esquemas XMP da Microsoft para marcação de pessoas definem um conjunto de propriedades para marcar indivíduos em fotos digitais.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-159">The Microsoft XMP schemas for people tagging define a set of properties to tag individuals in digital photos.</span></span>

<span data-ttu-id="4bbe3-160">As seções a seguir fornecem as definições de esquema necessárias para a marcação de pessoas.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-160">The following sections provide the schema definitions needed for people tagging.</span></span> <span data-ttu-id="4bbe3-161">Sempre que possível, as definições de esquema usam as convenções fornecidas pelas [especificações XMP (Extensible Metadata Platform) da Adobe](https://www.adobe.com/devnet/xmp/).</span><span class="sxs-lookup"><span data-stu-id="4bbe3-161">Wherever possible, the schema definitions use the conventions provided by [Adobe's Extensible Metadata Platform (XMP) Specifications](https://www.adobe.com/devnet/xmp/).</span></span> <span data-ttu-id="4bbe3-162">As definições de esquema neste tópico mostram o XML namespace Uniform Resource Identifier (URI) que identifica o esquema e o prefixo de namespace de esquema preferencial, seguido por uma tabela que lista todas as propriedades definidas para o esquema.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-162">The schema definitions in this topic show the XML namespace Uniform Resource Identifier (URI) that identifies the schema and the preferred schema namespace prefix, followed by a table that lists all properties defined for the schema.</span></span> <span data-ttu-id="4bbe3-163">Cada tabela tem as seguintes colunas:</span><span class="sxs-lookup"><span data-stu-id="4bbe3-163">Each table has the following columns:</span></span>

-   <span data-ttu-id="4bbe3-164">**Property** -o nome da propriedade, incluindo o prefixo de namespace preferencial.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-164">**Property** - The name of the property, including the preferred namespace prefix.</span></span>

-   <span data-ttu-id="4bbe3-165">**Tipo de valor** -o tipo de valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-165">**Value type** - The value type of the property.</span></span> <span data-ttu-id="4bbe3-166">Os esquemas de suporte à marcação de pessoas usam os tipos de valor XMP sempre que possível, incluindo data e texto.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-166">The people-tagging support schemas use the XMP value types whenever possible, including Date and Text.</span></span> <span data-ttu-id="4bbe3-167">Os tipos de matriz são precedidos pelo tipo de contêiner: `alt` , `bag` ou `seq` .</span><span class="sxs-lookup"><span data-stu-id="4bbe3-167">Array types are preceded by the container type: `alt`, `bag`, or `seq`.</span></span>

-   <span data-ttu-id="4bbe3-168">**Categoria** -as propriedades de esquema são internas ou externas:</span><span class="sxs-lookup"><span data-stu-id="4bbe3-168">**Category** - Schema properties are internal or external:</span></span>

    -   <span data-ttu-id="4bbe3-169">Os metadados internos devem ser definidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-169">Internal metadata must be set by the application.</span></span>

    -   <span data-ttu-id="4bbe3-170">Os metadados externos devem ser definidos pelo usuário e são independentes do conteúdo do documento.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-170">External metadata must be set by the user and is independent of the contents of the document.</span></span>

-   <span data-ttu-id="4bbe3-171">**Descrição** -a descrição da propriedade.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-171">**Description** - The description of the property.</span></span>

### <a name="microsoft-photo-12-schema"></a><span data-ttu-id="4bbe3-172">Esquema do Microsoft Photo 1,2</span><span class="sxs-lookup"><span data-stu-id="4bbe3-172">Microsoft Photo 1.2 Schema</span></span>

<span data-ttu-id="4bbe3-173">O esquema do Microsoft Photo 1,2 fornece um conjunto de propriedades para regiões de imagem.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-173">The Microsoft Photo 1.2 schema provides a set of properties for image regions.</span></span>

-   <span data-ttu-id="4bbe3-174">O URI do namespace do esquema é `https://ns.microsoft.com/photo/1.2/` .</span><span class="sxs-lookup"><span data-stu-id="4bbe3-174">The schema namespace URI is `https://ns.microsoft.com/photo/1.2/`.</span></span>
-   <span data-ttu-id="4bbe3-175">O prefixo de namespace de esquema preferencial é `MP` .</span><span class="sxs-lookup"><span data-stu-id="4bbe3-175">The preferred schema namespace prefix is `MP`.</span></span>



| <span data-ttu-id="4bbe3-176">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4bbe3-176">Property</span></span>      | <span data-ttu-id="4bbe3-177">Tipo de valor</span><span class="sxs-lookup"><span data-stu-id="4bbe3-177">Value type</span></span> | <span data-ttu-id="4bbe3-178">Categoria</span><span class="sxs-lookup"><span data-stu-id="4bbe3-178">Category</span></span> | <span data-ttu-id="4bbe3-179">Descrição</span><span class="sxs-lookup"><span data-stu-id="4bbe3-179">Description</span></span>                                                                                                                     |
|---------------|------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bbe3-180">MP: RegionInfo</span><span class="sxs-lookup"><span data-stu-id="4bbe3-180">MP:RegionInfo</span></span> | <span data-ttu-id="4bbe3-181">RegionInfo</span><span class="sxs-lookup"><span data-stu-id="4bbe3-181">RegionInfo</span></span> | <span data-ttu-id="4bbe3-182">Interna</span><span class="sxs-lookup"><span data-stu-id="4bbe3-182">Internal</span></span> | <span data-ttu-id="4bbe3-183">**obrigatório** : armazena a raiz dos metadados de marcação de pessoas.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-183">**required** : Stores the root of the people-tagging metadata.</span></span> <span data-ttu-id="4bbe3-184">Consulte a seção esquema do Microsoft Photo RegionInfo que segue.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-184">See the Microsoft Photo RegionInfo Schema section which follows.</span></span> |



 

### <a name="microsoft-photo-regioninfo-schema"></a><span data-ttu-id="4bbe3-185">Esquema do Microsoft Photo RegionInfo</span><span class="sxs-lookup"><span data-stu-id="4bbe3-185">Microsoft Photo RegionInfo Schema</span></span>

<span data-ttu-id="4bbe3-186">O esquema Microsoft Photo RegionInfo 1,2 fornece um conjunto de propriedades para informações de região.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-186">The Microsoft Photo RegionInfo 1.2 schema provides a set of properties for region info.</span></span>

-   <span data-ttu-id="4bbe3-187">O URI do namespace do esquema é `https://ns.microsoft.com/photo/1.2/t/RegionInfo#` .</span><span class="sxs-lookup"><span data-stu-id="4bbe3-187">The schema namespace URI is `https://ns.microsoft.com/photo/1.2/t/RegionInfo#`.</span></span>
-   <span data-ttu-id="4bbe3-188">O prefixo de namespace de esquema preferencial é `MPRI` .</span><span class="sxs-lookup"><span data-stu-id="4bbe3-188">The preferred schema namespace prefix is `MPRI`.</span></span>



| <span data-ttu-id="4bbe3-189">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4bbe3-189">Property</span></span>              | <span data-ttu-id="4bbe3-190">Tipo de valor</span><span class="sxs-lookup"><span data-stu-id="4bbe3-190">Value type</span></span> | <span data-ttu-id="4bbe3-191">Categoria</span><span class="sxs-lookup"><span data-stu-id="4bbe3-191">Category</span></span> | <span data-ttu-id="4bbe3-192">Descrição</span><span class="sxs-lookup"><span data-stu-id="4bbe3-192">Description</span></span>                                                                                                    |
|-----------------------|------------|----------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bbe3-193">MPRI:DateRegionsValid</span><span class="sxs-lookup"><span data-stu-id="4bbe3-193">MPRI:DateRegionsValid</span></span> | <span data-ttu-id="4bbe3-194">Data</span><span class="sxs-lookup"><span data-stu-id="4bbe3-194">Date</span></span>       | <span data-ttu-id="4bbe3-195">Externo</span><span class="sxs-lookup"><span data-stu-id="4bbe3-195">External</span></span> | <span data-ttu-id="4bbe3-196">**opcional** : data em que a última região foi criada.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-196">**optional** : Date that the last region was created.</span></span>                                                          |
| <span data-ttu-id="4bbe3-197">MPRI: regiões</span><span class="sxs-lookup"><span data-stu-id="4bbe3-197">MPRI:Regions</span></span>          | <span data-ttu-id="4bbe3-198">Região da bolsa</span><span class="sxs-lookup"><span data-stu-id="4bbe3-198">bag Region</span></span> | <span data-ttu-id="4bbe3-199">Externo</span><span class="sxs-lookup"><span data-stu-id="4bbe3-199">External</span></span> | <span data-ttu-id="4bbe3-200">**obrigatório** : armazena as regiões de marcação de pessoas.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-200">**required** : Stores the people tagging regions.</span></span> <span data-ttu-id="4bbe3-201">Consulte a seção esquema de região fotográfica da Microsoft que segue.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-201">See the Microsoft Photo Region Schema section which follows.</span></span> |



 

### <a name="microsoft-photo-region-schema"></a><span data-ttu-id="4bbe3-202">Esquema de região fotográfica da Microsoft</span><span class="sxs-lookup"><span data-stu-id="4bbe3-202">Microsoft Photo Region Schema</span></span>

<span data-ttu-id="4bbe3-203">O esquema da região 1,2 do Microsoft Photo fornece um conjunto de propriedades para regiões de imagem.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-203">The Microsoft Photo Region 1.2 schema provides a set of properties for image regions.</span></span>

-   <span data-ttu-id="4bbe3-204">O URI do namespace do esquema é `https://ns.microsoft.com/photo/1.2/t/Region#` .</span><span class="sxs-lookup"><span data-stu-id="4bbe3-204">The schema namespace URI is `https://ns.microsoft.com/photo/1.2/t/Region#`.</span></span>
-   <span data-ttu-id="4bbe3-205">O prefixo de namespace de esquema preferencial é `MPReg` .</span><span class="sxs-lookup"><span data-stu-id="4bbe3-205">The preferred schema namespace prefix is `MPReg`.</span></span>



| <span data-ttu-id="4bbe3-206">MPReg: Propriedade</span><span class="sxs-lookup"><span data-stu-id="4bbe3-206">MPReg:Property</span></span>          | <span data-ttu-id="4bbe3-207">Tipo de valor</span><span class="sxs-lookup"><span data-stu-id="4bbe3-207">Value type</span></span> | <span data-ttu-id="4bbe3-208">Categoria</span><span class="sxs-lookup"><span data-stu-id="4bbe3-208">Category</span></span> | <span data-ttu-id="4bbe3-209">Descrição</span><span class="sxs-lookup"><span data-stu-id="4bbe3-209">Description</span></span>                                                                                                                                                                                                                                                                                                     |
|-------------------------|------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bbe3-210">MPReg:PersonDisplayName</span><span class="sxs-lookup"><span data-stu-id="4bbe3-210">MPReg:PersonDisplayName</span></span> | <span data-ttu-id="4bbe3-211">Texto</span><span class="sxs-lookup"><span data-stu-id="4bbe3-211">Text</span></span>       | <span data-ttu-id="4bbe3-212">Externo</span><span class="sxs-lookup"><span data-stu-id="4bbe3-212">External</span></span> | <span data-ttu-id="4bbe3-213">**obrigatório** : armazena o nome da pessoa no retângulo fornecido.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-213">**required** : Stores the name of the person in the given rectangle.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="4bbe3-214">MPReg: retângulo</span><span class="sxs-lookup"><span data-stu-id="4bbe3-214">MPReg:Rectangle</span></span>         | <span data-ttu-id="4bbe3-215">Texto</span><span class="sxs-lookup"><span data-stu-id="4bbe3-215">Text</span></span>       | <span data-ttu-id="4bbe3-216">Externo</span><span class="sxs-lookup"><span data-stu-id="4bbe3-216">External</span></span> | <span data-ttu-id="4bbe3-217">**opcional** : armazena o retângulo que identifica a pessoa na foto.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-217">**optional** : Stores the rectangle that identifies the person within the photo.</span></span> <span data-ttu-id="4bbe3-218">O retângulo é armazenado como quatro valores decimais delimitados por vírgula.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-218">The rectangle is stored as four comma-delimited decimal values.</span></span> <span data-ttu-id="4bbe3-219">Os dois primeiros valores especificam a coordenada superior esquerda; os dois finais especificam a altura e a largura do retângulo.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-219">The first two values specify the top left coordinate; the final two specify the height and width of the rectangle.</span></span> <span data-ttu-id="4bbe3-220">Os valores decimais devem ser normalizados para 1.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-220">The decimal values must be normalized to 1.</span></span> |
| <span data-ttu-id="4bbe3-221">MPReg:PersonEmailDigest</span><span class="sxs-lookup"><span data-stu-id="4bbe3-221">MPReg:PersonEmailDigest</span></span> | <span data-ttu-id="4bbe3-222">Texto</span><span class="sxs-lookup"><span data-stu-id="4bbe3-222">Text</span></span>       | <span data-ttu-id="4bbe3-223">Externo</span><span class="sxs-lookup"><span data-stu-id="4bbe3-223">External</span></span> | <span data-ttu-id="4bbe3-224">**opcional** : armazena o hash de mensagem criptografada SHA-1 do endereço de email ao vivo da pessoa.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-224">**optional** : Stores the SHA-1 encrypted message hash of the person's Live e-mail address.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="4bbe3-225">MPReg:PersonLiveIdCID</span><span class="sxs-lookup"><span data-stu-id="4bbe3-225">MPReg:PersonLiveIdCID</span></span>   | <span data-ttu-id="4bbe3-226">Texto</span><span class="sxs-lookup"><span data-stu-id="4bbe3-226">Text</span></span>       | <span data-ttu-id="4bbe3-227">Externo</span><span class="sxs-lookup"><span data-stu-id="4bbe3-227">External</span></span> | <span data-ttu-id="4bbe3-228">**opcional** : armazena a representação decimal assinada da CID ao vivo da pessoa, um inteiro de 64 bits que identifica publicamente uma identidade ao vivo.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-228">**optional** :Stores the signed decimal representation of the person's Live CID, a 64-bit integer that publicly identifies a Live identity.</span></span>                                                                                                                                                                     |



 

### <a name="sample-metadata"></a><span data-ttu-id="4bbe3-229">Metadados de exemplo</span><span class="sxs-lookup"><span data-stu-id="4bbe3-229">Sample Metadata</span></span>

<span data-ttu-id="4bbe3-230">Veja a seguir uma representação dos metadados XMP para marcação de pessoas.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-230">The following is a representation of the XMP metadata for people tagging.</span></span>

``` syntax
<rdf:Description rdf:about="" xmlns:MP="https://ns.microsoft.com/photo/1.2/">
<MP:RegionInfo> 
<rdf:Description xmlns:MPRI="https://ns.microsoft.com/photo/1.2/t/RegionInfo#">
   <MPRI:Regions> 
       <rdf:Bag> 
          <rdf:li> 
       <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#"> 
           <MPReg:Rectangle>0.790650, 0.441734, 0.209350, 0.279133
           </MPReg:Rectangle>
           <MPReg:PersonDisplayName>John Doe</MPReg:PersonDisplayName> 
           <MPReg:PersonEmailDigest>2FD4E1C67A2D28FCED849EE1BB76E7391B93EB13</MPReg:PersonEmailDigest> 
           <MPReg:PersonLiveIdCID>1234567890123456789</MPReg:PersonLiveIdCID> 
       </rdf:Description> 
         </rdf:li> 
         <rdf:li>
             <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#">
                  <MPReg:Rectangle>0.222656, 0.302083, 0.378906, 0.505208</MPReg:Rectangle> 
                  <MPReg:PersonDisplayName>Jane Doe</MPReg:PersonDisplayName> 
              </rdf:Description> 
         </rdf:li> 
<!-- Addition Regions --> ... 
<rdf:li>...
</rdf:li> 
</rdf:Bag> 
</MPRI:Regions> </rdf:Description> </MP:RegionInfo> </rdf:Description>
```

## <a name="related-topics"></a><span data-ttu-id="4bbe3-231">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4bbe3-231">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4bbe3-232">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="4bbe3-232">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4bbe3-233">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="4bbe3-233">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="4bbe3-234">Visão geral dos metadados do WIC</span><span class="sxs-lookup"><span data-stu-id="4bbe3-234">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="4bbe3-235">Visão geral da leitura e gravação de metadados de imagem</span><span class="sxs-lookup"><span data-stu-id="4bbe3-235">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="4bbe3-236">Visão geral da linguagem de consulta de metadados</span><span class="sxs-lookup"><span data-stu-id="4bbe3-236">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> </dl>

 

 
