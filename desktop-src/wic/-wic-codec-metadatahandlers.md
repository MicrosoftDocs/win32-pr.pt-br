---
description: Este tópico apresenta os requisitos para a criação de manipuladores de metadados personalizados para o Windows Imaging Component (WIC), incluindo leitores de metadados e gravadores.
ms.assetid: 08f1872b-6e4d-44ee-abc7-48685e435acc
title: Visão geral da extensibilidade de metadados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6576585f7f35628432504086695dd6c64091d3b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170307"
---
# <a name="metadata-extensibility-overview"></a><span data-ttu-id="80a76-103">Visão geral da extensibilidade de metadados</span><span class="sxs-lookup"><span data-stu-id="80a76-103">Metadata Extensibility Overview</span></span>

<span data-ttu-id="80a76-104">Este tópico apresenta os requisitos para a criação de manipuladores de metadados personalizados para o Windows Imaging Component (WIC), incluindo leitores de metadados e gravadores.</span><span class="sxs-lookup"><span data-stu-id="80a76-104">This topic introduces the requirements for creating custom metadata handlers for the Windows Imaging Component (WIC), including both metadata readers and writers.</span></span> <span data-ttu-id="80a76-105">Ele também aborda os requisitos para estender a descoberta de componentes de tempo de execução do WIC para incluir manipuladores de metadados personalizados.</span><span class="sxs-lookup"><span data-stu-id="80a76-105">It also discusses the requirements for extending WIC run-time component discovery to include your custom metadata handlers.</span></span>

<span data-ttu-id="80a76-106">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="80a76-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="80a76-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="80a76-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="80a76-108">Introdução</span><span class="sxs-lookup"><span data-stu-id="80a76-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="80a76-109">Criando um leitor de metadados</span><span class="sxs-lookup"><span data-stu-id="80a76-109">Creating a Metadata Reader</span></span>](#creating-a-metadata-reader)
    -   [<span data-ttu-id="80a76-110">Interface IWICMetadataReader</span><span class="sxs-lookup"><span data-stu-id="80a76-110">IWICMetadataReader Interface</span></span>](#iwicmetadatareader-interface)
    -   [<span data-ttu-id="80a76-111">Interface IWICPersistStream</span><span class="sxs-lookup"><span data-stu-id="80a76-111">IWICPersistStream Interface</span></span>](#iwicpersiststream-interface)
    -   [<span data-ttu-id="80a76-112">Interface IWICStreamProvider</span><span class="sxs-lookup"><span data-stu-id="80a76-112">IWICStreamProvider Interface</span></span>](#iwicstreamprovider-interface)
-   [<span data-ttu-id="80a76-113">Criando um gravador de metadados</span><span class="sxs-lookup"><span data-stu-id="80a76-113">Creating a Metadata Writer</span></span>](#creating-a-metadata-writer)
    -   [<span data-ttu-id="80a76-114">Interface IWICMetadataWriter</span><span class="sxs-lookup"><span data-stu-id="80a76-114">IWICMetadataWriter Interface</span></span>](#iwicmetadatawriter-interface)
    -   [<span data-ttu-id="80a76-115">Interface IWICPersistStream</span><span class="sxs-lookup"><span data-stu-id="80a76-115">IWICPersistStream Interface</span></span>](#iwicpersiststream-interface)
    -   [<span data-ttu-id="80a76-116">Interface IWICStreamProvider</span><span class="sxs-lookup"><span data-stu-id="80a76-116">IWICStreamProvider Interface</span></span>](#iwicstreamprovider-interface)
-   [<span data-ttu-id="80a76-117">Instalando e registrando um manipulador de metadados</span><span class="sxs-lookup"><span data-stu-id="80a76-117">Installing and Registering a Metadata Handler</span></span>](#installing-and-registering-a-metadata-handler)
    -   [<span data-ttu-id="80a76-118">Chaves do registro do manipulador de metadados</span><span class="sxs-lookup"><span data-stu-id="80a76-118">Metadata Handler Registry Keys</span></span>](#metadata-handler-registry-keys)
    -   [<span data-ttu-id="80a76-119">Leitores de metadados</span><span class="sxs-lookup"><span data-stu-id="80a76-119">Metadata Readers</span></span>](#metadata-readers)
    -   [<span data-ttu-id="80a76-120">Gravadores de metadados</span><span class="sxs-lookup"><span data-stu-id="80a76-120">Metadata Writers</span></span>](#metadata-writers)
    -   [<span data-ttu-id="80a76-121">Assinando um manipulador de metadados</span><span class="sxs-lookup"><span data-stu-id="80a76-121">Signing a Metadata Handler</span></span>](#signing-a-metadata-handler)
-   [<span data-ttu-id="80a76-122">Considerações especiais</span><span class="sxs-lookup"><span data-stu-id="80a76-122">Special Considerations</span></span>](#special-considerations)
    -   [<span data-ttu-id="80a76-123">PROPVARIANTS</span><span class="sxs-lookup"><span data-stu-id="80a76-123">PROPVARIANTS</span></span>](#propvariants)
    -   [<span data-ttu-id="80a76-124">Manipuladores 8BIM</span><span class="sxs-lookup"><span data-stu-id="80a76-124">8BIM Handlers</span></span>](#8bim-handlers)
-   [<span data-ttu-id="80a76-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="80a76-125">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="80a76-126">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="80a76-126">Prerequisites</span></span>

<span data-ttu-id="80a76-127">Para entender este tópico, você deve ter uma compreensão aprofundada do WIC, de seus componentes e de metadados para imagens.</span><span class="sxs-lookup"><span data-stu-id="80a76-127">To understand this topic you should have an in-depth understanding of WIC, its components, and metadata for images.</span></span> <span data-ttu-id="80a76-128">Para obter mais informações sobre metadados do WIC, consulte a [visão geral dos metadados do WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="80a76-128">For more information on WIC metadata, see the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="80a76-129">Para obter mais informações sobre os componentes do WIC, consulte [visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="80a76-129">For more information on WIC components, see the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span>

## <a name="introduction"></a><span data-ttu-id="80a76-130">Introdução</span><span class="sxs-lookup"><span data-stu-id="80a76-130">Introduction</span></span>

<span data-ttu-id="80a76-131">Conforme discutido na [visão geral dos metadados do WIC](-wic-about-metadata.md), geralmente há vários blocos de metadados em uma imagem, cada um expondo diferentes tipos de informações em diferentes formatos de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-131">As discussed in the [WIC Metadata Overview](-wic-about-metadata.md), there are often multiple blocks of metadata within an image, each exposing different types of information in different metadata formats.</span></span> <span data-ttu-id="80a76-132">Para interagir com um formato de metadados inserido em uma imagem, um aplicativo deve usar um manipulador de metadados apropriado.</span><span class="sxs-lookup"><span data-stu-id="80a76-132">To interact with a metadata format embedded within an image, an application must use an appropriate metadata handler.</span></span> <span data-ttu-id="80a76-133">O WIC fornece vários manipuladores de metadados (leitores de metadados e gravadores) que permitem que você leia e grave tipos específicos de metadados, como EXIF ou XMP.</span><span class="sxs-lookup"><span data-stu-id="80a76-133">WIC provides several metadata handlers (both metadata readers and writers) that enable you to read and write specific types of metadata such as Exif or XMP.</span></span>

<span data-ttu-id="80a76-134">Além dos manipuladores nativos fornecidos, o WIC fornece APIs que permitem criar novos manipuladores de metadados que participam da descoberta de componente em tempo de execução do WIC.</span><span class="sxs-lookup"><span data-stu-id="80a76-134">In addition to the native handlers provided, WIC provides APIs that enable you to create new metadata handlers that participate in WIC's run-time component discovery.</span></span> <span data-ttu-id="80a76-135">Isso permite que os aplicativos que usam o WIC leiam e gravem seus formatos de metadados personalizados.</span><span class="sxs-lookup"><span data-stu-id="80a76-135">This enables applications that use WIC to read and write your custom metadata formats.</span></span>

<span data-ttu-id="80a76-136">As etapas a seguir permitem que seus manipuladores de metadados participem da descoberta de metadados de tempo de execução do WIC.</span><span class="sxs-lookup"><span data-stu-id="80a76-136">The following steps enable your metadata handlers to participate in WIC's run-time metadata discovery.</span></span>

-   <span data-ttu-id="80a76-137">Implemente uma classe de manipulador de leitor de metadados ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) que expõe as interfaces WIC necessárias para ler seu formato de metadados personalizado.</span><span class="sxs-lookup"><span data-stu-id="80a76-137">Implement a metadata-reader handler class ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) that exposes the required WIC interfaces for reading your custom metadata format.</span></span> <span data-ttu-id="80a76-138">Isso permite que os aplicativos baseados em WIC leiam o formato de metadados da mesma maneira que lêem formatos de metadados nativos.</span><span class="sxs-lookup"><span data-stu-id="80a76-138">This enables WIC-based applications to read your metadata format the same way they read native metadata formats.</span></span>
-   <span data-ttu-id="80a76-139">Implemente uma classe de manipulador de gravador de metadados ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) que expõe as interfaces WIC necessárias para codificar seu formato de metadados personalizado.</span><span class="sxs-lookup"><span data-stu-id="80a76-139">Implement a metadata-writer handler class ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) that exposes the required WIC interfaces for encoding your custom metadata format.</span></span> <span data-ttu-id="80a76-140">Isso permite que aplicativos baseados em WIC serializem seu formato de metadados em formatos de imagem com suporte.</span><span class="sxs-lookup"><span data-stu-id="80a76-140">This enables WIC-based applications to serialize your metadata format into supported image formats.</span></span>
-   <span data-ttu-id="80a76-141">Assine digitalmente e registre seus manipuladores de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-141">Digitally sign and register your metadata handlers.</span></span> <span data-ttu-id="80a76-142">Isso permite que os manipuladores de metadados sejam descobertos em tempo de execução, combinando o padrão de identificação no registro com o padrão inserido no arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="80a76-142">This enables your metadata handlers to be discovered at run time by matching the identifying pattern in the registry with the pattern embedded in the image file.</span></span>

## <a name="creating-a-metadata-reader"></a><span data-ttu-id="80a76-143">Criando um leitor de metadados</span><span class="sxs-lookup"><span data-stu-id="80a76-143">Creating a Metadata Reader</span></span>

<span data-ttu-id="80a76-144">O principal acesso aos blocos de metadados em um codec é por meio da interface [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) implementada por cada codec do WIC.</span><span class="sxs-lookup"><span data-stu-id="80a76-144">The main access to metadata blocks within a codec is through the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) interface that each WIC codec implements.</span></span> <span data-ttu-id="80a76-145">Essa interface enumera cada um dos blocos de metadados inseridos em um formato de imagem para que o manipulador de metadados apropriado possa ser descoberto e instanciado para cada bloco.</span><span class="sxs-lookup"><span data-stu-id="80a76-145">This interface enumerates each of the metadata blocks embedded in an image format so that the appropriate metadata handler can be discovered and instantiated for each block.</span></span> <span data-ttu-id="80a76-146">Os blocos de metadados que não são reconhecidos pelo WIC são considerados desconhecidos e definidos como o CLSID WICUnknownMetadataReader do GUID \_ .</span><span class="sxs-lookup"><span data-stu-id="80a76-146">The metadata blocks that are not recognized by WIC are considered unknown and are defined as the GUID CLSID\_WICUnknownMetadataReader.</span></span> <span data-ttu-id="80a76-147">Para que seu formato de metadados seja reconhecido pelo WIC, você deve criar uma classe que implemente três interfaces: [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)e [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span><span class="sxs-lookup"><span data-stu-id="80a76-147">To have your metadata format recognized by WIC, you must create a class that implements three interfaces: [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream), and [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span></span>

> [!Note]  
> <span data-ttu-id="80a76-148">Se o formato de metadados tiver restrições que processem alguns métodos das interfaces necessárias inadequadas, esses métodos devem retornar WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.</span><span class="sxs-lookup"><span data-stu-id="80a76-148">If your metadata format has restrictions that render some methods of the required interfaces inappropriate, such methods should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

 

### <a name="iwicmetadatareader-interface"></a><span data-ttu-id="80a76-149">Interface IWICMetadataReader</span><span class="sxs-lookup"><span data-stu-id="80a76-149">IWICMetadataReader Interface</span></span>

<span data-ttu-id="80a76-150">A interface [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) deve ser implementada ao criar um leitor de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-150">The [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) interface must be implemented when creating a metadata reader.</span></span> <span data-ttu-id="80a76-151">Essa interface fornece acesso ao sob a lista de itens de metadados dentro do fluxo de dados de um formato de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-151">This interface provides access to the underling metadata items within the data stream of a metadata format.</span></span>

<span data-ttu-id="80a76-152">O código a seguir mostra a definição da interface do leitor de metadados, conforme definido no arquivo wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="80a76-152">The following code shows the definition of the metadata reader interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICMetadataReader : IUnknown
{
    HRESULT GetMetadataFormat(
        [out] GUID *pguidMetadataFormat
        );

    HRESULT GetMetadataHandlerInfo(
        [out] IWICMetadataHandlerInfo **ppIHandler
        );

    HRESULT GetCount(
        [out] UINT *pcCount
        );

    HRESULT GetValueByIndex(
        [in] UINT nIndex,
        [in, out, unique] PROPVARIANT *pvarSchema,
        [in, out, unique] PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetEnumerator(
        [out] IWICEnumMetadataItem **ppIEnumMetadata
        );
};
```

<span data-ttu-id="80a76-153">O método **GetMetadataFormat** retorna o GUID do seu formato de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-153">The **GetMetadataFormat** method returns the GUID of your metadata format.</span></span>

<span data-ttu-id="80a76-154">O método **GetMetadataHandlerInfo** retorna uma interface [**IWICMetadataHandlerInfo**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo) que fornece informações sobre o manipulador de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-154">The **GetMetadataHandlerInfo** method returns an [**IWICMetadataHandlerInfo**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo) interface that provides information about your metadata handler.</span></span> <span data-ttu-id="80a76-155">Isso inclui informações como quais formatos de imagem dão suporte ao formato de metadados e se o leitor de metadados requer acesso ao fluxo de metadados completo.</span><span class="sxs-lookup"><span data-stu-id="80a76-155">This includes information such as what image formats support the metadata format and whether your metadata reader requires access to the full metadata stream.</span></span>

<span data-ttu-id="80a76-156">O método **GetCount** retorna o número de itens de metadados individuais (incluindo blocos de metadados inseridos) encontrados no fluxo de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-156">The **GetCount** method returns the number of individual metadata items (including embedded metadata blocks) found within the metadata stream.</span></span>

<span data-ttu-id="80a76-157">O método **GetValueByIndex** retorna um item de metadados por um valor de índice.</span><span class="sxs-lookup"><span data-stu-id="80a76-157">The **GetValueByIndex** method returns a metadata item by an index value.</span></span> <span data-ttu-id="80a76-158">Esse método permite que os aplicativos executem um loop em cada item de metadados em um bloco de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-158">This method enables applications to loop through each metadata item in a metadata block.</span></span> <span data-ttu-id="80a76-159">O código a seguir demonstra como um aplicativo pode usar esse método para recuperar cada item de metadados em um bloco de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-159">The following code demonstrates how an application can use this method to retrieve each metadata item in a metadata block.</span></span>


```C++
PROPVARIANT readerValue;
IWICMetadataBlockReader *blockReader = NULL;
IWICMetadataReader *reader = NULL;

PropVariantInit(&readerValue);

hr = pFrameDecode->QueryInterface(IID_IWICMetadataBlockReader, (void**)&blockReader);

if (SUCCEEDED(hr))
{
    // Retrieve the third block in the image. This is image specific and
    // ideally you should call this by retrieving the reader count
    // first.
    hr = blockReader->GetReaderByIndex(2, &reader);
}

if (SUCCEEDED(hr))
{
    UINT numValues = 0;

    hr = reader->GetCount(&numValues);

    // Loop through each item and retrieve by index
    for (UINT i = 0; SUCCEEDED(hr) && i < numValues; i++)
    {
        PROPVARIANT id, value;

        PropVariantInit(&id);
        PropVariantInit(&value);

        hr = reader->GetValueByIndex(i, NULL, &id, &value);

        if (SUCCEEDED(hr))
        {
            // Do something with the metadata item.
            //...
        }
        PropVariantClear(&id);
        PropVariantClear(&value);
    }               
}
```



<span data-ttu-id="80a76-160">O método **GetValue** recupera um item de metadados específico por esquema e/ou ID.</span><span class="sxs-lookup"><span data-stu-id="80a76-160">The **GetValue** method retrieves a specific metadata item by schema and/or ID.</span></span> <span data-ttu-id="80a76-161">Esse método é semelhante ao método **GetValueByIndex** , exceto que ele recupera um item de metadados que tem um esquema ou ID específico.</span><span class="sxs-lookup"><span data-stu-id="80a76-161">This method is similar to the **GetValueByIndex** method except that it retrieves a metadata item that has a specific schema or ID.</span></span>

<span data-ttu-id="80a76-162">O método **GetEnumerator** retorna um enumerador de cada item de metadados no bloco de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-162">The **GetEnumerator** method returns an enumerator of each metadata item in the metadata block.</span></span> <span data-ttu-id="80a76-163">Isso permite que os aplicativos usem um enumerador para navegar no formato de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-163">This enables applications to use an enumerator to navigate your metadata format.</span></span>

<span data-ttu-id="80a76-164">Se o formato de metadados não tiver uma noção de esquemas para itens de metadados, o método GetValue... os métodos devem ignorar essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="80a76-164">If your metadata format does not have a notion of schemas for metadata items, the GetValue... methods should ignore this property.</span></span> <span data-ttu-id="80a76-165">No entanto, se o formato der suporte à nomenclatura de esquema, você deverá prever um valor **nulo** .</span><span class="sxs-lookup"><span data-stu-id="80a76-165">If, however, your format supports schema naming, you should anticipate a **NULL** value.</span></span>

<span data-ttu-id="80a76-166">Se um item de metadados for um bloco de metadados inserido, crie um manipulador de metadados do Subfluxo do conteúdo inserido e retorne o novo manipulador de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-166">If a metadata item is an embedded metadata block, create a metadata handler from the substream of the embedded content and return the new metadata handler.</span></span> <span data-ttu-id="80a76-167">Se não houver nenhum leitor de metadados disponível para o bloco aninhado, crie uma instância e retorne um leitor de metadados desconhecido.</span><span class="sxs-lookup"><span data-stu-id="80a76-167">If there is no metadata reader available for the nested block, instantiate and return an unknown metadata reader.</span></span> <span data-ttu-id="80a76-168">Para criar um novo leitor de metadados para o bloco inserido, chame os métodos **CreateMetadataReaderFromContainer** ou **CreateMetadataReader** da fábrica de componentes ou chame a função [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent) .</span><span class="sxs-lookup"><span data-stu-id="80a76-168">To create a new metadata reader for the embedded block, call the component factory's **CreateMetadataReaderFromContainer** or **CreateMetadataReader** methods, or call the [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent) function.</span></span>

<span data-ttu-id="80a76-169">Se o fluxo de metadados contiver conteúdo big endian, o leitor de metadados será responsável por trocar os valores de dados que ele processa.</span><span class="sxs-lookup"><span data-stu-id="80a76-169">If the metadata stream contains big-endian content, the metadata reader is responsible for swapping any data values it processes.</span></span> <span data-ttu-id="80a76-170">Também é responsável por informar quaisquer leitores de metadados aninhados que estejam trabalhando com o fluxo de dados big-endian.</span><span class="sxs-lookup"><span data-stu-id="80a76-170">It is also responsible for informing any nested metadata readers that they are working with big-endian data stream.</span></span> <span data-ttu-id="80a76-171">No entanto, todos os valores devem ser retornados no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="80a76-171">However, all values should be returned in little-endian format.</span></span>

<span data-ttu-id="80a76-172">Implemente o suporte para navegação de namespace ao dar suporte a consultas em que a ID do item de metadados é um `VT_CLSID` (um GUID) correspondente a um formato de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-172">Implement support for namespace navigation by supporting queries where the metadata item ID is a `VT_CLSID` (a GUID) corresponding to a metadata format.</span></span> <span data-ttu-id="80a76-173">Se um leitor de metadados aninhado para esse formato for identificado durante a análise, ele deverá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="80a76-173">If a nested metadata reader for that format is identified during parsing, it must be returned.</span></span> <span data-ttu-id="80a76-174">Isso permite que os aplicativos usem um leitor de consulta de metadados para pesquisar o formato de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-174">This enables applications to use a metadata query reader to search your metadata format.</span></span>

<span data-ttu-id="80a76-175">Ao obter um item de metadados por ID, você deve usar a [função PropVariantChangeType](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) para forçar a ID para o tipo esperado.</span><span class="sxs-lookup"><span data-stu-id="80a76-175">When getting a metadata item by ID, you should use [PropVariantChangeType Function](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) to coerce the ID into the expected type.</span></span> <span data-ttu-id="80a76-176">Por exemplo, o leitor IFD forçará uma ID a digitar `VT_UI2` para coincidir com o tipo de dados de uma ID de etiqueta IFD ushort.</span><span class="sxs-lookup"><span data-stu-id="80a76-176">For example, the IFD reader will coerce an ID to type `VT_UI2` to coincide with the data type of an IFD tag ID USHORT.</span></span> <span data-ttu-id="80a76-177">O tipo de entrada e o tipo esperado devem ser [PROPVARIANTdos](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="80a76-177">The input type and expected type must both be [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) to do this.</span></span> <span data-ttu-id="80a76-178">Isso não é necessário, mas fazer essa coerção simplifica o código que chama o leitor para consultar itens de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-178">This is not required, but doing this coercion simplifies code that calls the reader to query for metadata items.</span></span>

### <a name="iwicpersiststream-interface"></a><span data-ttu-id="80a76-179">Interface IWICPersistStream</span><span class="sxs-lookup"><span data-stu-id="80a76-179">IWICPersistStream Interface</span></span>

<span data-ttu-id="80a76-180">A interface [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) herda de **IPersistStream** e fornece métodos adicionais para salvar e carregar objetos usando a enumeração [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .</span><span class="sxs-lookup"><span data-stu-id="80a76-180">The [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface inherits from **IPersistStream** and provides additional methods for saving and loading objects by using the [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) enumeration.</span></span>

<span data-ttu-id="80a76-181">O código a seguir mostra a definição da interface [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) , conforme definido no arquivo wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="80a76-181">The following code shows the definition of the [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

<span data-ttu-id="80a76-182">O método **LoadEx** fornece o leitor de metadados com um fluxo de dados que contém o seu bloco de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-182">The **LoadEx** method provides your metadata reader with a data stream containing your metadata block.</span></span> <span data-ttu-id="80a76-183">Seu leitor analisa esse fluxo para acessar os itens de metadados subjacentes.</span><span class="sxs-lookup"><span data-stu-id="80a76-183">Your reader parses this stream to access the underlying metadata items.</span></span> <span data-ttu-id="80a76-184">O leitor de metadados é inicializado com um subfluxo que está posicionado no início do conteúdo de metadados brutos.</span><span class="sxs-lookup"><span data-stu-id="80a76-184">Your metadata reader is initialized with a substream that is positioned at the beginning of the raw metadata content.</span></span> <span data-ttu-id="80a76-185">Se o leitor não exigir o fluxo completo, o Subfluxo será limitado no intervalo para apenas o conteúdo do bloco de metadados; caso contrário, o fluxo de metadados completo é fornecido com a posição definida no início do seu bloco de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-185">If your reader does not require the full stream, the substream is limited in range to only the content of the metadata block; otherwise, the full metadata stream is provided with the position set at the beginning of your metadata block.</span></span>

<span data-ttu-id="80a76-186">O método **SaveEx** é usado pelos gravadores de metadados para serializar o bloco de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-186">The **SaveEx** method is used by metadata writers to serialize your metadata block.</span></span> <span data-ttu-id="80a76-187">Quando **SaveEx** é usado em um leitor de metadados, ele deve retornar WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.</span><span class="sxs-lookup"><span data-stu-id="80a76-187">When **SaveEx** is used in a metadata reader, it should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

### <a name="iwicstreamprovider-interface"></a><span data-ttu-id="80a76-188">Interface IWICStreamProvider</span><span class="sxs-lookup"><span data-stu-id="80a76-188">IWICStreamProvider Interface</span></span>

<span data-ttu-id="80a76-189">A interface [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) permite que o leitor de metadados forneça referências ao seu fluxo de conteúdo, forneça informações sobre o fluxo e atualize as versões em cache do fluxo.</span><span class="sxs-lookup"><span data-stu-id="80a76-189">The [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) interface enables your metadata reader to provide references to its content stream, provide information about the stream, and refresh cached versions of the stream.</span></span>

<span data-ttu-id="80a76-190">O código a seguir mostra a definição da interface [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) , conforme definido no arquivo wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="80a76-190">The following code shows the definition of the [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICStreamProvider : IUnknown
{
    HRESULT GetStream(
        [out] IStream **ppIStream
        );

    HRESULT GetPersistOptions(
        [out] DWORD *pdwPersistOptions
        );

    HRESULT GetPreferredVendorGUID(
        [out] GUID *pguidPreferredVendor
        );

    HRESULT RefreshStream(
        );
};
```

<span data-ttu-id="80a76-191">O método **GetStream** recupera uma referência para o fluxo de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-191">The **GetStream** method retrieves a reference to your metadata stream.</span></span> <span data-ttu-id="80a76-192">O fluxo retornado deve ter o ponteiro de fluxo redefinido para a posição inicial.</span><span class="sxs-lookup"><span data-stu-id="80a76-192">The stream you return should have the stream pointer reset to the start position.</span></span> <span data-ttu-id="80a76-193">Se o formato de metadados exigir acesso total ao fluxo, a posição inicial deverá ser o início do seu bloco de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-193">If your metadata format requires full stream access, the start position should be the start of your metadata block.</span></span>

<span data-ttu-id="80a76-194">O método **persisteoptions** retorna as opções atuais do fluxo da enumeração [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .</span><span class="sxs-lookup"><span data-stu-id="80a76-194">The **GetPersistOptions** method returns the stream's current options from the [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) enumeration.</span></span>

<span data-ttu-id="80a76-195">O método **GetPreferredVendorGUID** retorna o GUID do fornecedor do leitor de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-195">The **GetPreferredVendorGUID** method returns the GUID of the vendor of the metadata reader.</span></span>

<span data-ttu-id="80a76-196">O método **RefreshStream** atualiza o fluxo de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-196">The **RefreshStream** method refreshes the metadata stream.</span></span> <span data-ttu-id="80a76-197">Esse método deve chamar **LoadEx** com um fluxo **nulo** para todos os blocos de metadados aninhados.</span><span class="sxs-lookup"><span data-stu-id="80a76-197">This method must call **LoadEx** with a **NULL** stream for any nested metadata blocks.</span></span> <span data-ttu-id="80a76-198">Isso é necessário porque os blocos de metadados aninhados e seus itens podem não existir mais, devido à edição in-loco.</span><span class="sxs-lookup"><span data-stu-id="80a76-198">This is necessary because nested metadata blocks and their items may no longer exist, due to in-place editing.</span></span>

## <a name="creating-a-metadata-writer"></a><span data-ttu-id="80a76-199">Criando um gravador de metadados</span><span class="sxs-lookup"><span data-stu-id="80a76-199">Creating a Metadata Writer</span></span>

<span data-ttu-id="80a76-200">Um gravador de metadados é um tipo de manipulador de metadados que fornece uma maneira de serializar um bloco de metadados para um quadro de imagem ou fora de um quadro individual se o formato de imagem der suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="80a76-200">A metadata writer is a type of metadata handler that provides a way to serialize a metadata block to an image frame, or outside an individual frame if the image format supports it.</span></span> <span data-ttu-id="80a76-201">O principal acesso aos gravadores de metadados dentro de um codec é por meio da interface [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) que cada codificador de WIC implementa.</span><span class="sxs-lookup"><span data-stu-id="80a76-201">The main access to the metadata writers within a codec is through the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) interface that each WIC encoder implements.</span></span> <span data-ttu-id="80a76-202">Essa interface permite que os aplicativos enumerem cada um dos blocos de metadados inseridos em uma imagem para que o gravador de metadados apropriado possa ser descoberto e instanciado para cada bloco de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-202">This interface enables applications to enumerate each of the metadata blocks embedded in an image so that the appropriate metadata writer can be discovered and instantiated for each metadata block.</span></span> <span data-ttu-id="80a76-203">Os blocos de metadados que não têm um gravador de metadados correspondente são considerados desconhecidos e são definidos como o CLSID WICUnknownMetadataReader do GUID \_ .</span><span class="sxs-lookup"><span data-stu-id="80a76-203">Metadata blocks that do not have a corresponding metadata writer are considered unknown, and are defined as the GUID CLSID\_WICUnknownMetadataReader.</span></span> <span data-ttu-id="80a76-204">Para permitir que os aplicativos habilitados para WIC serializem e gravem seu formato de metadados, você deve criar uma classe que implemente as seguintes interfaces: [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter), [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)e [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span><span class="sxs-lookup"><span data-stu-id="80a76-204">To enable WIC enabled applications to serialize and write your metadata format, you must create a class that implements the following interfaces: [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter), [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream), and [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span></span>

> [!Note]  
> <span data-ttu-id="80a76-205">Se o formato de metadados tiver restrições que processem alguns métodos das interfaces necessárias inadequadas, esses métodos devem retornar WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.</span><span class="sxs-lookup"><span data-stu-id="80a76-205">If your metadata format has restrictions that render some methods of the required interfaces inappropriate, such methods should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

 

### <a name="iwicmetadatawriter-interface"></a><span data-ttu-id="80a76-206">Interface IWICMetadataWriter</span><span class="sxs-lookup"><span data-stu-id="80a76-206">IWICMetadataWriter Interface</span></span>

<span data-ttu-id="80a76-207">A interface [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) deve ser implementada pelo seu gravador de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-207">The [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) interface must be implemented by your metadata writer.</span></span> <span data-ttu-id="80a76-208">Além disso, como **IWICMetadataWriter** é herdado de [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), você também deve implementar todos os métodos de **IWICMetadataReader**.</span><span class="sxs-lookup"><span data-stu-id="80a76-208">Additionally, because **IWICMetadataWriter** inherits from [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), you must also implement all the methods of **IWICMetadataReader**.</span></span> <span data-ttu-id="80a76-209">Como ambos os tipos de manipulador exigem a mesma herança de interface, talvez você queira criar uma única classe que forneça a funcionalidade de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="80a76-209">Because both handler types require the same interface inheritance, you might want to create a single class that provides both reading and writing functionality.</span></span>

<span data-ttu-id="80a76-210">O código a seguir mostra a definição da interface do gravador de metadados, conforme definido no arquivo wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="80a76-210">The following code shows the definition of the metadata writer interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICMetadataWriter : IWICMetadataReader
{
    HRESULT SetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT SetValueByIndex(
        [in] UINT nIndex,
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT RemoveValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId
        );

    HRESULT RemoveValueByIndex(
        [in] UINT nIndex
        );
};
```

<span data-ttu-id="80a76-211">O método **SetValue** grava o item de metadados especificado para o fluxo de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-211">The **SetValue** method writes the specified metadata item to the metadata stream.</span></span>

<span data-ttu-id="80a76-212">O método **SetValueByIndex** grava o item de metadados especificado no índice especificado no fluxo de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-212">The **SetValueByIndex** method writes the specified metadata item to the specified index in the metadata stream.</span></span> <span data-ttu-id="80a76-213">O índice não se refere à ID, mas à posição do item dentro do bloco de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-213">The index does not refer to the ID but to the position of the item within the metadata block.</span></span>

<span data-ttu-id="80a76-214">O método **removervalue** remove o item de metadados especificado do fluxo de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-214">The **RemoveValue** method removes the specified metadata item from the metadata stream.</span></span>

<span data-ttu-id="80a76-215">O método **RemoveValueByIndex** remove o item de metadados no índice especificado do fluxo de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-215">The **RemoveValueByIndex** method removes the metadata item at the specified index from the metadata stream.</span></span> <span data-ttu-id="80a76-216">Depois de remover um item, espera-se que os itens de metadados restantes ocupem o índice vagado se o índice não for o último índice.</span><span class="sxs-lookup"><span data-stu-id="80a76-216">After removing an item, it is expected that the remaining metadata items will occupy the vacated index if the index is not the last index.</span></span> <span data-ttu-id="80a76-217">Também é esperado que a contagem seja alterada depois que o item for removido.</span><span class="sxs-lookup"><span data-stu-id="80a76-217">It is also expected that the count will change after the item is removed.</span></span>

<span data-ttu-id="80a76-218">É responsabilidade do gravador de metadados converter os itens [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) na estrutura subjacente exigida pelo seu formato.</span><span class="sxs-lookup"><span data-stu-id="80a76-218">It is the metadata writer's responsibility to convert the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) items to the underlying structure required by your format.</span></span> <span data-ttu-id="80a76-219">No entanto, diferentemente do leitor de metadados, os tipos VARIAntes não devem ser normalmente impostos para tipos diferentes, pois o chamador está especificamente indicando qual tipo de dados usar.</span><span class="sxs-lookup"><span data-stu-id="80a76-219">However, unlike the metadata reader, VARIANT types should not normally be coerced to different types as the caller is specifically indicating what data type to use.</span></span>

<span data-ttu-id="80a76-220">O gravador de metadados deve confirmar todos os itens de metadados para o fluxo de imagem, incluindo valores ocultos ou não reconhecidos.</span><span class="sxs-lookup"><span data-stu-id="80a76-220">Your metadata writer must commit all metadata items to the image stream, including hidden or unrecognized values.</span></span> <span data-ttu-id="80a76-221">Isso inclui blocos de metadados aninhados desconhecidos.</span><span class="sxs-lookup"><span data-stu-id="80a76-221">This includes unknown nested metadata blocks.</span></span> <span data-ttu-id="80a76-222">No entanto, é responsabilidade do codificador definir quaisquer itens de metadados críticos antes de iniciar a operação de salvamento.</span><span class="sxs-lookup"><span data-stu-id="80a76-222">However, it is the encoder's responsibility to set any critical metadata items prior to initiating the save operation.</span></span>

<span data-ttu-id="80a76-223">Se o fluxo de metadados contiver conteúdo big endian, o gravador de metadados será responsável por trocar os valores de dados que ele processa.</span><span class="sxs-lookup"><span data-stu-id="80a76-223">If the metadata stream contains big-endian content, the metadata writer is responsible for swapping any data values it processes.</span></span> <span data-ttu-id="80a76-224">Também é responsável por informar quaisquer gravadores de metadados aninhados que estejam trabalhando com um fluxo de dados big endian quando eles salvarem.</span><span class="sxs-lookup"><span data-stu-id="80a76-224">It is also responsible for informing any nested metadata writers that they are working with a big-endian data stream when they save.</span></span>

<span data-ttu-id="80a76-225">Implemente o suporte para a criação e remoção de namespace ao dar suporte a operações set e remove em itens de metadados com um tipo de `VT_CLSID` (um GUID) correspondente a um formato de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-225">Implement support for namespace creation and removal by supporting set and remove operations on metadata items with a type of `VT_CLSID` (a GUID) corresponding to a metadata format.</span></span> <span data-ttu-id="80a76-226">O gravador de metadados chama a função [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) para inserir corretamente o conteúdo do gravador de metadados aninhado no gravador de metadados pai.</span><span class="sxs-lookup"><span data-stu-id="80a76-226">The metadata writer calls the [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) function to properly embed the nested metadata writer content into the parent metadata writer.</span></span>

<span data-ttu-id="80a76-227">Se o formato de metadados oferecer suporte à codificação in-loco, você será responsável por gerenciar o preenchimento necessário.</span><span class="sxs-lookup"><span data-stu-id="80a76-227">If your metadata format supports in-place encoding, you are responsible for managing the required padding.</span></span> <span data-ttu-id="80a76-228">Para obter mais informações sobre codificação in-loco, consulte [visão geral dos metadados do WIC](-wic-about-metadata.md) e [visão geral da leitura e gravação de metadados de imagem](-wic-codec-readingwritingmetadata.md).</span><span class="sxs-lookup"><span data-stu-id="80a76-228">For more information on in-place encoding, see [WIC Metadata Overview](-wic-about-metadata.md) and [Overview of Reading and Writing Image Metadata](-wic-codec-readingwritingmetadata.md).</span></span>

### <a name="iwicpersiststream-interface"></a><span data-ttu-id="80a76-229">Interface IWICPersistStream</span><span class="sxs-lookup"><span data-stu-id="80a76-229">IWICPersistStream Interface</span></span>

<span data-ttu-id="80a76-230">A interface [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) herda de **IPersistStream** e fornece métodos adicionais para salvar e carregar objetos usando a enumeração [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .</span><span class="sxs-lookup"><span data-stu-id="80a76-230">The [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface inherits from **IPersistStream** and provides additional methods for saving and loading objects by using the [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) enumeration.</span></span>

<span data-ttu-id="80a76-231">O código a seguir mostra a definição da interface [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) , conforme definido no arquivo wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="80a76-231">The following code shows the definition of the [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

<span data-ttu-id="80a76-232">O método **LoadEx** fornece o manipulador de metadados com um fluxo de dados que contém o bloco de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-232">The **LoadEx** method provides your metadata handler with a data stream containing your metadata block.</span></span>

<span data-ttu-id="80a76-233">O método **SaveEx** serializa os metadados em um fluxo.</span><span class="sxs-lookup"><span data-stu-id="80a76-233">The **SaveEx** method serializes the metadata into a stream.</span></span> <span data-ttu-id="80a76-234">Se o fluxo fornecido for o mesmo que o fluxo de inicialização, você deverá executar a codificação in-loco.</span><span class="sxs-lookup"><span data-stu-id="80a76-234">If the provided stream is the same as initialization stream, you should perform in-place encoding.</span></span> <span data-ttu-id="80a76-235">Se houver suporte para codificação in-loco, esse método deverá retornar WINCODEC \_ Err \_ TOOMUCHMETADATA quando não houver preenchimento suficiente para executar a codificação in-loco.</span><span class="sxs-lookup"><span data-stu-id="80a76-235">If in-place encoding is supported, this method should return WINCODEC\_ERR\_TOOMUCHMETADATA when there is insufficient padding to perform in-place encoding.</span></span> <span data-ttu-id="80a76-236">Se não houver suporte para codificação in-loco, esse método deverá retornar WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.</span><span class="sxs-lookup"><span data-stu-id="80a76-236">If in-place encoding is not supported, this method should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

<span data-ttu-id="80a76-237">O método **IPersistStream:: GetSizeMax** deve ser implementado e deve retornar o tamanho exato do conteúdo de metadados que seria gravado na gravação subsequente.</span><span class="sxs-lookup"><span data-stu-id="80a76-237">The **IPersistStream::GetSizeMax** method must be implemented and must return the exact size of the metadata content that would be written in subsequent save.</span></span>

<span data-ttu-id="80a76-238">O método **IPersistStream:: IsDirty** deve ser implementado se o gravador de metadados for inicializado por meio de um fluxo, para que uma imagem possa determinar de forma confiável se seu conteúdo foi alterado.</span><span class="sxs-lookup"><span data-stu-id="80a76-238">The **IPersistStream::IsDirty** method should be implemented if the metadata writer is initialized through a stream, so that an image can reliably determine whether its content has changed.</span></span>

<span data-ttu-id="80a76-239">Se o formato de metadados oferecer suporte a blocos de metadados aninhados, o gravador de metadados deverá delegar aos gravadores de metadados aninhados a serialização de seu conteúdo ao salvar em um fluxo.</span><span class="sxs-lookup"><span data-stu-id="80a76-239">If your metadata format supports nested metadata blocks, your metadata writer should delegate to the nested metadata writers the serializing of its content when saving to a stream.</span></span>

### <a name="iwicstreamprovider-interface"></a><span data-ttu-id="80a76-240">Interface IWICStreamProvider</span><span class="sxs-lookup"><span data-stu-id="80a76-240">IWICStreamProvider Interface</span></span>

<span data-ttu-id="80a76-241">A implementação da interface [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) para um gravador de metadados é a mesma que a de um leitor de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-241">The implementation of the [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) interface for a metadata writer is the same as that of a metadata reader.</span></span> <span data-ttu-id="80a76-242">Para obter mais informações, consulte a seção criando um leitor de metadados neste documento.</span><span class="sxs-lookup"><span data-stu-id="80a76-242">For more information, see Creating a Metadata Reader section in this document.</span></span>

## <a name="installing-and-registering-a-metadata-handler"></a><span data-ttu-id="80a76-243">Instalando e registrando um manipulador de metadados</span><span class="sxs-lookup"><span data-stu-id="80a76-243">Installing and Registering a Metadata Handler</span></span>

<span data-ttu-id="80a76-244">Para instalar um manipulador de metadados, você deve fornecer o assembly do manipulador e registrá-lo no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="80a76-244">To install a metadata handler, you must provide the handler assembly and register it in the system registry.</span></span> <span data-ttu-id="80a76-245">Você pode decidir como e quando as chaves do registro são populadas.</span><span class="sxs-lookup"><span data-stu-id="80a76-245">You can decide how and when the registry keys are populated.</span></span>

> [!Note]  
> <span data-ttu-id="80a76-246">Para facilitar a leitura, os GUIDs hexadecimais reais não são mostrados nas chaves do registro mostradas nas seções a seguir deste documento.</span><span class="sxs-lookup"><span data-stu-id="80a76-246">For readability, the actual hexadecimal GUIDs are not shown in the registry keys shown in the following sections of this document.</span></span> <span data-ttu-id="80a76-247">Para localizar o valor hexadecimal para um nome amigável especificado, consulte os arquivos wincodec. idl e wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="80a76-247">To find the hexadecimal value for a specified friendly name, see the wincodec.idl and wincodecsdk.idl files.</span></span>

 

### <a name="metadata-handler-registry-keys"></a><span data-ttu-id="80a76-248">Chaves do registro do manipulador de metadados</span><span class="sxs-lookup"><span data-stu-id="80a76-248">Metadata Handler Registry Keys</span></span>

<span data-ttu-id="80a76-249">Cada manipulador de metadados é identificado por um CLSID exclusivo, e cada manipulador é necessário para registrar seu CLSID sob o GUID de ID de categoria do manipulador de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-249">Each metadata handler is identified by a unique CLSID, and each handler is required to register its CLSID under the metadata handler's category ID GUID.</span></span> <span data-ttu-id="80a76-250">A ID de categoria do tipo de manipulador é definida em wincodec. idl; o nome da ID da categoria para leitores é CATID \_ WICMetadataReader e o nome da ID de categoria para gravadores é CATID \_ WICMetadataWriter.</span><span class="sxs-lookup"><span data-stu-id="80a76-250">Each handler type's category ID is defined in the wincodec.idl; the category ID name for readers is CATID\_WICMetadataReader, and the category ID name for writers is CATID\_WICMetadataWriter.</span></span>

<span data-ttu-id="80a76-251">Cada manipulador de metadados é identificado por um CLSID exclusivo, e cada manipulador é necessário para registrar seu CLSID sob o GUID de ID de categoria do manipulador de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-251">Each metadata handler is identified by a unique CLSID, and each handler is required to register its CLSID under the metadata handler's category ID GUID.</span></span> <span data-ttu-id="80a76-252">A ID de categoria do tipo de manipulador é definida em wincodec. idl; o nome da ID da categoria para leitores é CATID \_ WICMetadataReader e o nome da ID de categoria para gravadores é CATID \_ WICMetadataWriter.</span><span class="sxs-lookup"><span data-stu-id="80a76-252">Each handler type's category ID is defined in the wincodec.idl; the category ID name for readers is CATID\_WICMetadataReader, and the category ID name for writers is CATID\_WICMetadataWriter.</span></span>

> [!Note]  
> <span data-ttu-id="80a76-253">Nas listagens de chave do registro a seguir, {Reader CLSID} refere-se ao CLSID exclusivo que você fornece para o leitor de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-253">In the following registry key listings, {Reader CLSID} refers to the unique CLSID that you provide for your metadata reader.</span></span> <span data-ttu-id="80a76-254">{Writer CLSID} refere-se ao CLSID exclusivo que você fornece para o seu gravador de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-254">{Writer CLSID} refers to the unique CLSID that you provide for your metadata writer.</span></span> <span data-ttu-id="80a76-255">{Handler CLSID} refere-se ao CLSID do leitor, ao CLSID do gravador ou a ambos, dependendo de quais manipuladores você está fornecendo.</span><span class="sxs-lookup"><span data-stu-id="80a76-255">{Handler CLSID} refers to the reader's CLSID, the writer's CLSID, or both, depending on which handlers you are providing.</span></span> <span data-ttu-id="80a76-256">{GUID de contêiner} refere-se ao objeto de contêiner (formato de imagem ou formato de metadados) que pode conter o bloco de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-256">{Container GUID} refers to the container object (image format or metadata format) that can contain the metadata block.</span></span>

 

<span data-ttu-id="80a76-257">As chaves do registro a seguir registram seu manipulador de metadados com os outros manipuladores de metadados disponíveis:</span><span class="sxs-lookup"><span data-stu-id="80a76-257">The following registry keys register your metadata handler with the other metadata handlers available:</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CATID_WICMetadataReaders}\Instance\{Reader CLSID}]
CLSID={Reader CLSID}
Friendly Name="Reader Name"

[HKEY_CLASSES_ROOT\CLSID\{CATID_ WICMetadataWriters}\Instance\{Writer CLSID}]
CLSID={Writer CLSID}
Friendly Name="Writer Name"
```

<span data-ttu-id="80a76-258">Além de registrar seus manipuladores em suas respectivas categorias, você também deve registrar chaves adicionais que fornecem informações específicas para o manipulador.</span><span class="sxs-lookup"><span data-stu-id="80a76-258">In addition to registering your handlers in their respective categories, you must also register additional keys that provide information specific to the handler.</span></span> <span data-ttu-id="80a76-259">Leitores e gravadores compartilham requisitos de chave de registro semelhantes.</span><span class="sxs-lookup"><span data-stu-id="80a76-259">Readers and writers share similar registry key requirements.</span></span> <span data-ttu-id="80a76-260">A sintaxe a seguir mostra como registrar um manipulador.</span><span class="sxs-lookup"><span data-stu-id="80a76-260">The following syntax shows how to register a handler.</span></span> <span data-ttu-id="80a76-261">O manipulador de leitor e o manipulador de gravador devem ser registrados dessa forma, usando seus respectivos CLSIDs:</span><span class="sxs-lookup"><span data-stu-id="80a76-261">Both the reader handler and writer handler must be registered in this way, using their respective CLSIDs:</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CLSID}]
"Vendor"={VendorGUID}
"Date"="yyyy-mm-dd"
"Version"="Major.Minor.Build.Number"
"SpecVersion"="Major.Minor.Build.Number"
"MetadataFormat"={MetadataFormatGUID}
"RequiresFullStream"=dword:1|0
"SupportsPadding"= dword:1|0
"FixedSize"=0

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\InProcServer32]
@="drive:\path\yourdll.dll"
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\{LCID}]
Author="Author's Name"
Description = " Metadata Description"
DeviceManufacturer ="Manufacturer Name"
DeviceModels="Device,Device"
FriendlyName="Friendly Name"
```

### <a name="metadata-readers"></a><span data-ttu-id="80a76-262">Leitores de metadados</span><span class="sxs-lookup"><span data-stu-id="80a76-262">Metadata Readers</span></span>

<span data-ttu-id="80a76-263">O registro do leitor de metadados também inclui chaves que descrevem como o leitor pode ser inserido em um formato de contêiner.</span><span class="sxs-lookup"><span data-stu-id="80a76-263">The metadata reader registration also includes keys that describe how the reader can be embedded in a container format.</span></span> <span data-ttu-id="80a76-264">Um formato de contêiner pode ser um formato de imagem como TIFF ou JPEG; Ele também pode ser outro formato de metadados, como um bloco de metadados IFD.</span><span class="sxs-lookup"><span data-stu-id="80a76-264">A container format can be an image format such as TIFF or JPEG; it can also be another metadata format such as an IFD metadata block.</span></span> <span data-ttu-id="80a76-265">Os formatos de contêiner de imagem com suporte nativo são listados em wincodec. idl; cada formato de contêiner de imagem é definido como um GUID com um nome que começa com GUID \_ containerFormat.</span><span class="sxs-lookup"><span data-stu-id="80a76-265">Natively supported image container formats are listed in wincodec.idl; each image container format is defined as a GUID with a name that begins with GUID\_ContainerFormat.</span></span> <span data-ttu-id="80a76-266">Os formatos de contêiner de metadados com suporte nativo são listados em wincodecsdk. idl; cada formato de contêiner de metadados é definido como um GUID com um nome que começa com GUID \_ MetadataFormat.</span><span class="sxs-lookup"><span data-stu-id="80a76-266">Natively supported metadata container formats are listed in wincodecsdk.idl; each metadata container format is defined as a GUID with a name that begins with GUID\_MetadataFormat.</span></span>

<span data-ttu-id="80a76-267">As chaves a seguir registram um contêiner ao qual o leitor de metadados dá suporte e os dados necessários para a leitura desse contêiner.</span><span class="sxs-lookup"><span data-stu-id="80a76-267">The following keys register a container that the metadata reader supports, and the data needed to read from that container.</span></span> <span data-ttu-id="80a76-268">Cada contêiner com suporte do leitor deve ser registrado dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="80a76-268">Each container supported by the reader must be registered in this way.</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Reader CLSID}\Containers\{Container GUID}\0]
"Position"=dword:00000000
"Pattern"=hex:ff,ff,ff,...
"Mask"=hex:ff,ff,ff,...
"DataOffset"=dword:00000006
```

<span data-ttu-id="80a76-269">A chave de padrão descreve o padrão binário que é usado para corresponder o bloco de metadados ao leitor.</span><span class="sxs-lookup"><span data-stu-id="80a76-269">The Pattern key describes the binary pattern that is used to match the metadata block to the reader.</span></span> <span data-ttu-id="80a76-270">Ao definir um padrão para o leitor de metadados, ele deve ser confiável o suficiente para que uma correspondência positiva signifique que o leitor de metadados possa entender os metadados no bloco de metadados que está sendo processado.</span><span class="sxs-lookup"><span data-stu-id="80a76-270">When defining a pattern for your metadata reader, it should be reliable enough that a positive match means the metadata reader can understand the metadata in the metadata block being processed.</span></span>

<span data-ttu-id="80a76-271">A chave dataOffset descreve o deslocamento fixo dos metadados do cabeçalho de bloco.</span><span class="sxs-lookup"><span data-stu-id="80a76-271">The DataOffset key describes the fixed offset of the metadata from the block header.</span></span> <span data-ttu-id="80a76-272">Essa chave é opcional e, se não for especificada, significa que os metadados reais não podem ser localizados usando um deslocamento fixo do cabeçalho de bloco.</span><span class="sxs-lookup"><span data-stu-id="80a76-272">This key is optional and, if not specified, means that the actual metadata cannot be located using a fixed offset from the block header.</span></span>

### <a name="metadata-writers"></a><span data-ttu-id="80a76-273">Gravadores de metadados</span><span class="sxs-lookup"><span data-stu-id="80a76-273">Metadata Writers</span></span>

<span data-ttu-id="80a76-274">O registro do gravador de metadados também inclui chaves que descrevem como gravar o cabeçalho que precede o conteúdo de metadados inserido em um formato de contêiner.</span><span class="sxs-lookup"><span data-stu-id="80a76-274">The metadata writer registration also includes keys that describe how to write out the header preceding the metadata content embedded in a container format.</span></span> <span data-ttu-id="80a76-275">Assim como no leitor, um formato de contêiner pode ser um formato de imagem ou outro bloco de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-275">As with the reader, a container format can be an image format or another metadata block.</span></span>

<span data-ttu-id="80a76-276">As chaves a seguir registram um contêiner ao qual o gravador de metadados dá suporte e os dados necessários para gravar o cabeçalho e os metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-276">The following keys register a container that the metadata writer supports, and the data needed to write the header and metadata.</span></span> <span data-ttu-id="80a76-277">Cada contêiner com suporte do gravador deve ser registrado dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="80a76-277">Each container supported by the writer must be registered in this way.</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Writer CLSID}\Containers\{Container GUID}]
"WritePosition"=dword:00000000
"WriteHeader"=hex:ff,ff,ff,...
"WriteOffset"=dword:00000000
```

<span data-ttu-id="80a76-278">A chave WriteHeader descreve o padrão binário do cabeçalho do bloco de metadados a ser gravado.</span><span class="sxs-lookup"><span data-stu-id="80a76-278">The WriteHeader key describes the binary pattern of the metadata block header to be written.</span></span> <span data-ttu-id="80a76-279">Esse padrão binário coincide com a chave de padrão de leitor do formato de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-279">This binary pattern coincides with the metadata format's reader Pattern key.</span></span>

<span data-ttu-id="80a76-280">A chave WriteOffset descreve o deslocamento fixo do cabeçalho de bloco no qual os metadados devem ser gravados.</span><span class="sxs-lookup"><span data-stu-id="80a76-280">The WriteOffset key describes the fixed offset from the block header at which the metadata should be written.</span></span> <span data-ttu-id="80a76-281">Essa chave é opcional e, se não for especificada, significa que os metadados reais não devem ser gravados com o cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="80a76-281">This key is optional and, if not specified, means that the actual metadata should not be written out with the header.</span></span>

### <a name="signing-a-metadata-handler"></a><span data-ttu-id="80a76-282">Assinando um manipulador de metadados</span><span class="sxs-lookup"><span data-stu-id="80a76-282">Signing a Metadata Handler</span></span>

<span data-ttu-id="80a76-283">Todos os manipuladores de metadados devem ser assinados digitalmente para participar do processo de descoberta do WIC.</span><span class="sxs-lookup"><span data-stu-id="80a76-283">All metadata handlers must be digitally signed to participate in the WIC discovery process.</span></span> <span data-ttu-id="80a76-284">O WIC não carregará nenhum manipulador que não esteja assinado por uma autoridade de certificação confiável.</span><span class="sxs-lookup"><span data-stu-id="80a76-284">WIC will not load any handler that is not signed by a trusted certificate authority.</span></span> <span data-ttu-id="80a76-285">Para obter mais informações sobre a assinatura digital, consulte [introdução à assinatura de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="80a76-285">For more information on digital signing, see [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span></span>

## <a name="special-considerations"></a><span data-ttu-id="80a76-286">Considerações especiais</span><span class="sxs-lookup"><span data-stu-id="80a76-286">Special Considerations</span></span>

<span data-ttu-id="80a76-287">As seções a seguir incluem informações adicionais que você deve considerar ao criar seus próprios manipuladores de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-287">The following sections include additional information you must consider when creating your own metadata handlers.</span></span>

### <a name="propvariants"></a><span data-ttu-id="80a76-288">PROPVARIANTS</span><span class="sxs-lookup"><span data-stu-id="80a76-288">PROPVARIANTS</span></span>

<span data-ttu-id="80a76-289">O WIC usa um [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) para representar um item de metadados para leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="80a76-289">WIC uses a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) to represent a metadata item for both reading and writing.</span></span> <span data-ttu-id="80a76-290">Um PROPVARIANT fornece um tipo de dados e um valor de dados para um item de metadados usado em um formato de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-290">A PROPVARIANT provides a data type and data value for a metadata item used within a metadata format.</span></span> <span data-ttu-id="80a76-291">Como o gravador de um manipulador de metadados, você tem muita flexibilidade em como os dados são armazenados no formato de metadados e como os dados são representados em um bloco de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-291">As the writer of a metadata handler, you have a lot of flexibility on how data is stored in the metadata format and how data is represented within a metadata block.</span></span> <span data-ttu-id="80a76-292">A tabela a seguir fornece diretrizes para ajudá-lo a decidir sobre o tipo de PROPVARIANT apropriado a ser usado em situações diferentes.</span><span class="sxs-lookup"><span data-stu-id="80a76-292">The following table provides guidelines to help you decide on the appropriate PROPVARIANT type to use in different situations.</span></span>



| <span data-ttu-id="80a76-293">O tipo de metadados é...</span><span class="sxs-lookup"><span data-stu-id="80a76-293">Metadata type is...</span></span>          | <span data-ttu-id="80a76-294">Usar tipo PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="80a76-294">Use PROPVARIANT type</span></span>      | <span data-ttu-id="80a76-295">Propriedade PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="80a76-295">PROPVARIANT Property</span></span>                                                                                                                                                                                                                                                           |
|------------------------------|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80a76-296">Vazio ou não existente.</span><span class="sxs-lookup"><span data-stu-id="80a76-296">Empty or non-existent.</span></span>       | <span data-ttu-id="80a76-297">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="80a76-297">VT\_EMPTY</span></span>                 | <span data-ttu-id="80a76-298">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="80a76-298">Not applicable.</span></span>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="80a76-299">Indefinido.</span><span class="sxs-lookup"><span data-stu-id="80a76-299">Undefined.</span></span>                   | <span data-ttu-id="80a76-300">\_blob VT</span><span class="sxs-lookup"><span data-stu-id="80a76-300">VT\_BLOB</span></span>                  | <span data-ttu-id="80a76-301">Use a propriedade blob para definir o tamanho e o ponteiro para o objeto de BLOB alocado usando CoTaskMemAlloc.</span><span class="sxs-lookup"><span data-stu-id="80a76-301">Use the blob property to set the size and pointer to the BLOB object allocated using CoTaskMemAlloc.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="80a76-302">Um bloco de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-302">A metadata block.</span></span>            | <span data-ttu-id="80a76-303">VT \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="80a76-303">VT\_UNKNOWN</span></span>               | <span data-ttu-id="80a76-304">Esse tipo usa a propriedade punkVal.</span><span class="sxs-lookup"><span data-stu-id="80a76-304">This type uses the punkVal property.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="80a76-305">Uma matriz de tipos.</span><span class="sxs-lookup"><span data-stu-id="80a76-305">An array of types.</span></span>           | <span data-ttu-id="80a76-306">\_Vetor VT \| VT \_ {Type}</span><span class="sxs-lookup"><span data-stu-id="80a76-306">VT\_VECTOR \| VT\_{type}</span></span>  | <span data-ttu-id="80a76-307">Use a propriedade CA {Type} para definir a contagem e o ponteiro para a matriz alocada usando CoTaskMemAlloc.</span><span class="sxs-lookup"><span data-stu-id="80a76-307">Use the ca{type} property to set the count and pointer to the array allocated using CoTaskMemAlloc.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="80a76-308">Uma matriz de blocos de metadados.</span><span class="sxs-lookup"><span data-stu-id="80a76-308">An array of metadata blocks.</span></span> | <span data-ttu-id="80a76-309">\_variante de vetor \| VT \_ VT</span><span class="sxs-lookup"><span data-stu-id="80a76-309">VT\_VECTOR \| VT\_VARIANT</span></span> | <span data-ttu-id="80a76-310">Use a propriedade capropvar para definir a matriz de variantes.</span><span class="sxs-lookup"><span data-stu-id="80a76-310">Use the capropvar property to set the array of variants.</span></span>                                                                                                                                                                                                                       |
| <span data-ttu-id="80a76-311">Um valor racional assinado.</span><span class="sxs-lookup"><span data-stu-id="80a76-311">A signed rational value.</span></span>     | <span data-ttu-id="80a76-312">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="80a76-312">VT\_I8</span></span>                    | <span data-ttu-id="80a76-313">Use a propriedade hVal para definir o valor.</span><span class="sxs-lookup"><span data-stu-id="80a76-313">Use the hVal property to set the value.</span></span> <span data-ttu-id="80a76-314">Defina a palavra alta para o denominador e a palavra inferior para o numerador.</span><span class="sxs-lookup"><span data-stu-id="80a76-314">Set the high word to the denominator and the low word to the numerator.</span></span>                                                                                                                                                                |
| <span data-ttu-id="80a76-315">Um valor racional.</span><span class="sxs-lookup"><span data-stu-id="80a76-315">A rational value.</span></span>            | <span data-ttu-id="80a76-316">\_UI8 VT</span><span class="sxs-lookup"><span data-stu-id="80a76-316">VT\_UI8</span></span>                   | <span data-ttu-id="80a76-317">Use a propriedade uhVal para definir o valor.</span><span class="sxs-lookup"><span data-stu-id="80a76-317">Use the uhVal property to set the value.</span></span> <span data-ttu-id="80a76-318">Defina HighPart para o denominador e o LowPart para o numerador.</span><span class="sxs-lookup"><span data-stu-id="80a76-318">Set the HighPart to the denominator and the LowPart to the numerator.</span></span> <span data-ttu-id="80a76-319">Observe que o LowPart é um int não assinado. O numerador deve ser convertido de um int não assinado para um int para garantir que o bit de sinal seja preservado, se presente.</span><span class="sxs-lookup"><span data-stu-id="80a76-319">Note that the LowPart is an unsigned int. The numerator should be converted from an unsigned int to an int to ensure that the sign bit is preserved if present.</span></span> |



 

<span data-ttu-id="80a76-320">Para evitar redundância na representação de itens de matriz, não use matrizes seguras; Use apenas matrizes simples.</span><span class="sxs-lookup"><span data-stu-id="80a76-320">To avoid redundancy in representing array items, do not use safe arrays; use only simple arrays.</span></span> <span data-ttu-id="80a76-321">Isso reduz o trabalho que um aplicativo precisa executar ao interpretar os tipos de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="80a76-321">This reduces the work an application needs to perform when interpreting [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) types.</span></span>

<span data-ttu-id="80a76-322">Evite usar `VT_BYREF` e armazenar valores embutidos sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="80a76-322">Avoid using `VT_BYREF` and store values inline whenever possible.</span></span> <span data-ttu-id="80a76-323">`VT_BYREF` é ineficiente para tipos pequenos (comuns para itens de metadados) e não fornece informações de tamanho.</span><span class="sxs-lookup"><span data-stu-id="80a76-323">`VT_BYREF` is inefficient for small types (common for metadata items) and does not provide size information.</span></span>

<span data-ttu-id="80a76-324">Antes de usar um [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), sempre chame **PropVariantInit** para inicializar o valor.</span><span class="sxs-lookup"><span data-stu-id="80a76-324">Before using a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), always call **PropVariantInit** to initialize the value.</span></span> <span data-ttu-id="80a76-325">Quando tiver terminado com o PROPVARIANT, sempre chame **PropVariantClear** para liberar qualquer memória alocada para a variável.</span><span class="sxs-lookup"><span data-stu-id="80a76-325">When you are finished with the PROPVARIANT, always call **PropVariantClear** to release any memory allocated for the variable.</span></span>

### <a name="8bim-handlers"></a><span data-ttu-id="80a76-326">Manipuladores 8BIM</span><span class="sxs-lookup"><span data-stu-id="80a76-326">8BIM Handlers</span></span>

<span data-ttu-id="80a76-327">Ao gravar um manipulador de metadados para um bloco de metadados 8BIM, você deve usar uma assinatura que encapsula a assinatura 8BIM e a ID.</span><span class="sxs-lookup"><span data-stu-id="80a76-327">When writing a metadata handler for an 8BIM metadata block, you must use a signature that encapsulates both the 8BIM signature and the ID.</span></span> <span data-ttu-id="80a76-328">Por exemplo, o leitor de metadados 8BIMIPTC nativo fornece as seguintes informações de registro para descoberta de leitor:</span><span class="sxs-lookup"><span data-stu-id="80a76-328">For example, the native 8BIMIPTC metadata reader provides the following registry information for reader discovery:</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{0010668C-0801-4DA6-A4A4-826522B6D28F}\Containers\{16100D66-8570-4BB9-B92D-FDA4B23ECE67}\0]
"Position"=dword:00000000
"Pattern"=hex:38,42,49,4d,04,04
"Mask"=hex:ff,ff,ff,ff,ff,ff
"DataOffset"=dword:00000006
```

<span data-ttu-id="80a76-329">O leitor do 8BIMIPTC tem um padrão registrado de 0x38, 0x42, 0x49, 0x4D, 0x04, 0x04.</span><span class="sxs-lookup"><span data-stu-id="80a76-329">The 8BIMIPTC reader has a registered pattern of 0x38, 0x42, 0x49, 0x4D, 0x04, 0x04.</span></span> <span data-ttu-id="80a76-330">Os primeiros quatro bytes (0x38, 0x42, 0x49, 0x4D) são a assinatura 8BIM e os últimos dois bytes (0x04, 0x04) são a ID do registro IPTC.</span><span class="sxs-lookup"><span data-stu-id="80a76-330">The first four bytes (0x38, 0x42, 0x49, 0x4D) are the 8BIM signature, and the last two bytes (0x04, 0x04) are the ID for the IPTC record.</span></span>

<span data-ttu-id="80a76-331">Portanto, para escrever um leitor de metadados 8BIM para obter informações de resolução, você precisaria de um padrão registrado de 0x38, 0x42, 0x49, 0x4D, 0x03, 0xED.</span><span class="sxs-lookup"><span data-stu-id="80a76-331">So, to write an 8BIM metadata reader for resolution information, you would need a registered pattern of 0x38, 0x42, 0x49, 0x4D, 0x03, 0xED.</span></span> <span data-ttu-id="80a76-332">Novamente, os primeiros quatro bytes (0x38, 0x42, 0x49, 0x4D) são a assinatura 8BIM.</span><span class="sxs-lookup"><span data-stu-id="80a76-332">Again, the first four bytes (0x38, 0x42, 0x49, 0x4D) are the 8BIM signature.</span></span> <span data-ttu-id="80a76-333">Os últimos dois bytes (0x03, 0xED), no entanto, são a ID de informações de resolução, conforme definido pelo formato PSD.</span><span class="sxs-lookup"><span data-stu-id="80a76-333">The last two bytes (0x03, 0xED), however, are the resolution information ID as defined by the PSD format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80a76-334">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="80a76-334">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="80a76-335">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="80a76-335">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="80a76-336">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="80a76-336">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="80a76-337">Visão geral dos metadados do WIC</span><span class="sxs-lookup"><span data-stu-id="80a76-337">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="80a76-338">Visão geral da linguagem de consulta de metadados</span><span class="sxs-lookup"><span data-stu-id="80a76-338">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="80a76-339">Visão geral da leitura e gravação de metadados de imagem</span><span class="sxs-lookup"><span data-stu-id="80a76-339">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="80a76-340">Como: codificar novamente uma imagem JPEG com metadados</span><span class="sxs-lookup"><span data-stu-id="80a76-340">How-to: Re-encode a JPEG Image with Metadata</span></span>](-wic-codec-jpegmetadataencoding.md)
</dt> <dt>

<span data-ttu-id="80a76-341">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="80a76-341">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="80a76-342">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="80a76-342">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
