---
description: O Windows Imaging Component (WIC) fornece uma API baseada em Component Object Model (COM) para uso em C e C++.
ms.assetid: 74b14b5e-70e9-410f-a6e6-d8873a5f4fa4
title: Visão geral da API do WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86e5a876010e52489adac9baa7ce57fdfdf80f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105802135"
---
# <a name="wic-api-overview"></a><span data-ttu-id="ba807-103">Visão geral da API do WIC</span><span class="sxs-lookup"><span data-stu-id="ba807-103">WIC API Overview</span></span>

<span data-ttu-id="ba807-104">O Windows Imaging Component (WIC) fornece uma API baseada em Component Object Model (COM) para uso em C e C++.</span><span class="sxs-lookup"><span data-stu-id="ba807-104">The Windows Imaging Component (WIC) provides a Component Object Model (COM) based API for use in C and C++.</span></span> <span data-ttu-id="ba807-105">A API do WIC expõe uma variedade de funcionalidades relacionadas a imagens, incluindo:</span><span class="sxs-lookup"><span data-stu-id="ba807-105">The WIC API exposes a variety of image-related functionality, including:</span></span>

-   <span data-ttu-id="ba807-106">Codecs internos para os formatos de imagem da Web padrão.</span><span class="sxs-lookup"><span data-stu-id="ba807-106">Built-in codecs for the standard web image formats.</span></span>
-   <span data-ttu-id="ba807-107">Suporte interno para formatos de metadados padrão.</span><span class="sxs-lookup"><span data-stu-id="ba807-107">Built-in support for standard metadata formats.</span></span>
-   <span data-ttu-id="ba807-108">Ampla gama de suporte a formato de pixel.</span><span class="sxs-lookup"><span data-stu-id="ba807-108">Wide range of pixel format support.</span></span>
-   <span data-ttu-id="ba807-109">Suporte de alta cor; incluindo um intervalo estendido de 30 bits, alta precisão de 30 bits e formatos de pixel de grande precisão de 48 bits e de gama ampla.</span><span class="sxs-lookup"><span data-stu-id="ba807-109">High-color support; including 30-bit extended range, 30-bit high precision, and 48-bit high precision and wide gamut pixel formats.</span></span>
-   <span data-ttu-id="ba807-110">Estrutura extensível para codecs de imagem, formatos de pixel e formatos de metadados.</span><span class="sxs-lookup"><span data-stu-id="ba807-110">Extensible framework for image codecs, pixel formats, and metadata formats.</span></span>

<span data-ttu-id="ba807-111">Este tópico contém os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ba807-111">This topic contains the following topics.</span></span>

-   [<span data-ttu-id="ba807-112">Arquivos de cabeçalho do WIC</span><span class="sxs-lookup"><span data-stu-id="ba807-112">WIC Header Files</span></span>](#wic-header-files)
-   [<span data-ttu-id="ba807-113">Arquivos de biblioteca</span><span class="sxs-lookup"><span data-stu-id="ba807-113">Library Files</span></span>](#library-files)
-   [<span data-ttu-id="ba807-114">Fábricas de classe</span><span class="sxs-lookup"><span data-stu-id="ba807-114">Class Factories</span></span>](#class-factories)
-   [<span data-ttu-id="ba807-115">Componentes de geração de imagens</span><span class="sxs-lookup"><span data-stu-id="ba807-115">Imaging Components</span></span>](#imaging-components)
-   [<span data-ttu-id="ba807-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ba807-116">See Also</span></span>](#see-also)

## <a name="wic-header-files"></a><span data-ttu-id="ba807-117">Arquivos de cabeçalho do WIC</span><span class="sxs-lookup"><span data-stu-id="ba807-117">WIC Header Files</span></span>

<span data-ttu-id="ba807-118">As APIs do WIC são definidas nos seguintes arquivos de cabeçalho e IDL (linguagem de definição de interface):</span><span class="sxs-lookup"><span data-stu-id="ba807-118">The WIC APIs are defined in the following header and Interface Definition Language (IDL) files:</span></span>



| <span data-ttu-id="ba807-119">Arquivo</span><span class="sxs-lookup"><span data-stu-id="ba807-119">File</span></span>              | <span data-ttu-id="ba807-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba807-120">Description</span></span>                                          |
|-------------------|------------------------------------------------------|
| <span data-ttu-id="ba807-121">wincodec. h</span><span class="sxs-lookup"><span data-stu-id="ba807-121">wincodec.h</span></span>        | <span data-ttu-id="ba807-122">Define as versões C e C++ das APIs primárias do WIC.</span><span class="sxs-lookup"><span data-stu-id="ba807-122">Defines C and C++ versions of the primary WIC APIs.</span></span>  |
| <span data-ttu-id="ba807-123">wincodec. idl</span><span class="sxs-lookup"><span data-stu-id="ba807-123">wincodec.idl</span></span>      | <span data-ttu-id="ba807-124">Define as interfaces WIC primárias.</span><span class="sxs-lookup"><span data-stu-id="ba807-124">Defines the primary WIC interfaces.</span></span>                  |
| <span data-ttu-id="ba807-125">wincodecsdk. h</span><span class="sxs-lookup"><span data-stu-id="ba807-125">wincodecsdk.h</span></span>     | <span data-ttu-id="ba807-126">Define as versões C e C++ das APIs de WIC de metadados.</span><span class="sxs-lookup"><span data-stu-id="ba807-126">Defines C and C++ versions of the metadata WIC APIs.</span></span> |
| <span data-ttu-id="ba807-127">wincodecsdk. idl</span><span class="sxs-lookup"><span data-stu-id="ba807-127">wincodecsdk.idl</span></span>   | <span data-ttu-id="ba807-128">Define as interfaces de metadados do WIC.</span><span class="sxs-lookup"><span data-stu-id="ba807-128">Defines the WIC metadata interfaces.</span></span>                 |
| <span data-ttu-id="ba807-129">wincodec \_ proxy. h</span><span class="sxs-lookup"><span data-stu-id="ba807-129">wincodec\_proxy.h</span></span> | <span data-ttu-id="ba807-130">Define as exportações de proxy do WIC.</span><span class="sxs-lookup"><span data-stu-id="ba807-130">Defines the WIC proxy exports.</span></span>                       |



 

<span data-ttu-id="ba807-131">Para usar o WIC, seus aplicativos devem incluir wincodec. h e/ou wincodecsdk. h, dependendo da API de que seu aplicativo precisa.</span><span class="sxs-lookup"><span data-stu-id="ba807-131">To use WIC, your applications must include wincodec.h and/or wincodecsdk.h, depending on the API your application needs.</span></span>

## <a name="library-files"></a><span data-ttu-id="ba807-132">Arquivos de biblioteca</span><span class="sxs-lookup"><span data-stu-id="ba807-132">Library Files</span></span>

<span data-ttu-id="ba807-133">Os arquivos de biblioteca do WIC:</span><span class="sxs-lookup"><span data-stu-id="ba807-133">The WIC library files:</span></span>



| <span data-ttu-id="ba807-134">Arquivo</span><span class="sxs-lookup"><span data-stu-id="ba807-134">File</span></span>              | <span data-ttu-id="ba807-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba807-135">Description</span></span>                                                            |
|-------------------|------------------------------------------------------------------------|
| <span data-ttu-id="ba807-136">WindowsCodecs. lib</span><span class="sxs-lookup"><span data-stu-id="ba807-136">windowscodecs.lib</span></span> | <span data-ttu-id="ba807-137">Biblioteca de importação fornecida pelo SDK (Software Development Kit) do Windows.</span><span class="sxs-lookup"><span data-stu-id="ba807-137">Import library provided by the Windows Software Development Kit (SDK).</span></span> |
| <span data-ttu-id="ba807-138">windowscodecs.dll</span><span class="sxs-lookup"><span data-stu-id="ba807-138">windowscodecs.dll</span></span> | <span data-ttu-id="ba807-139">Biblioteca de implementação de estoque fornecida pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ba807-139">Stock implementation library provided by the operating system.</span></span>         |



 

<span data-ttu-id="ba807-140">Para vincular as APIs do WIC, seu aplicativo deve incluir windowscodec. lib como uma dependência de vinculador adicional.</span><span class="sxs-lookup"><span data-stu-id="ba807-140">To link to WIC APIs, your application must include windowscodec.lib as an additional linker dependency.</span></span>

## <a name="class-factories"></a><span data-ttu-id="ba807-141">Fábricas de classe</span><span class="sxs-lookup"><span data-stu-id="ba807-141">Class Factories</span></span>

<span data-ttu-id="ba807-142">A tabela a seguir descreve as duas fábricas de classes COM que as APIs do WIC fornecem para a criação de componentes do WIC.</span><span class="sxs-lookup"><span data-stu-id="ba807-142">The following table describes the two COM class factories the WIC APIs provide for creating WIC components.</span></span>



| <span data-ttu-id="ba807-143">Interface de fábrica</span><span class="sxs-lookup"><span data-stu-id="ba807-143">Factory Interface</span></span>                                               | <span data-ttu-id="ba807-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba807-144">Description</span></span>                                                                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba807-145">**IWICImagingFactory**</span><span class="sxs-lookup"><span data-stu-id="ba807-145">**IWICImagingFactory**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)     | <span data-ttu-id="ba807-146">Fábrica de classes primária para desenvolvimento de aplicativos usando componentes de WIC.</span><span class="sxs-lookup"><span data-stu-id="ba807-146">Primary class factory for application development using WIC components.</span></span> <span data-ttu-id="ba807-147">Essa fábrica cria componentes como decodificadores de imagem, codificadores e fluxos.</span><span class="sxs-lookup"><span data-stu-id="ba807-147">This factory creates components such as image decoders, encoders and streams.</span></span>   |
| [<span data-ttu-id="ba807-148">**IWICComponentFactory**</span><span class="sxs-lookup"><span data-stu-id="ba807-148">**IWICComponentFactory**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) | <span data-ttu-id="ba807-149">Fábrica de classes direcionada para desenvolvedores de componentes do WIC.</span><span class="sxs-lookup"><span data-stu-id="ba807-149">Class factory targeted for WIC component developers.</span></span> <span data-ttu-id="ba807-150">Os componentes criados a partir dessa fábrica são usados principalmente no desenvolvimento de manipulador de metadados e de codec.</span><span class="sxs-lookup"><span data-stu-id="ba807-150">Components created from this factory are primarily used in codec and metadata handler development.</span></span> |



 

<span data-ttu-id="ba807-151">Para criar uma fábrica de classes, use a função com [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="ba807-151">To create either class factory, use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) COM function.</span></span> <span data-ttu-id="ba807-152">O exemplo a seguir demonstra a criação da fábrica de imagens do WIC.</span><span class="sxs-lookup"><span data-stu-id="ba807-152">The following example demonstrates the creation of the WIC imaging factory.</span></span>


```C++
// Initialize COM
CoInitialize(NULL);

// The factory pointer
IWICImagingFactory *pFactory = NULL;

// Create the COM imaging factory
HRESULT hr = CoCreateInstance(
    CLSID_WICImagingFactory,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_PPV_ARGS(&pFactory)
);
```



## <a name="imaging-components"></a><span data-ttu-id="ba807-153">Componentes de geração de imagens</span><span class="sxs-lookup"><span data-stu-id="ba807-153">Imaging Components</span></span>

<span data-ttu-id="ba807-154">As APIs do WIC fornecem vários tipos de componentes de geração de imagens.</span><span class="sxs-lookup"><span data-stu-id="ba807-154">The WIC APIs provide several types of imaging components.</span></span> <span data-ttu-id="ba807-155">A tabela a seguir descreve alguns dos componentes do WIC comuns.</span><span class="sxs-lookup"><span data-stu-id="ba807-155">The following table describes some of the common WIC components.</span></span> <span data-ttu-id="ba807-156">Para obter uma lista completa dos componentes disponíveis, consulte [interfaces WIC](-wic-codec-ifaces.md).</span><span class="sxs-lookup"><span data-stu-id="ba807-156">For a full list of available components, see [WIC interfaces](-wic-codec-ifaces.md).</span></span>



| <span data-ttu-id="ba807-157">Tipo de componente</span><span class="sxs-lookup"><span data-stu-id="ba807-157">Component Type</span></span>                                                      | <span data-ttu-id="ba807-158">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba807-158">Description</span></span>                                                                                                   |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba807-159">**Bitmap**</span><span class="sxs-lookup"><span data-stu-id="ba807-159">**Bitmap**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)                             | <span data-ttu-id="ba807-160">Representa uma representação na memória gravável de um [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource).</span><span class="sxs-lookup"><span data-stu-id="ba807-160">Represents a writable in-memory representation of an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource).</span></span> |
| [<span data-ttu-id="ba807-161">**Decodificador**</span><span class="sxs-lookup"><span data-stu-id="ba807-161">**Decoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)                     | <span data-ttu-id="ba807-162">Usado para decodificar dados de imagem de um fluxo em um formato útil para processamento de imagem.</span><span class="sxs-lookup"><span data-stu-id="ba807-162">Used to decode image data from a stream into a format that is useful for image processing.</span></span>                    |
| [<span data-ttu-id="ba807-163">**Fita**</span><span class="sxs-lookup"><span data-stu-id="ba807-163">**Encoder**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)                     | <span data-ttu-id="ba807-164">Grava dados de imagem em um fluxo.</span><span class="sxs-lookup"><span data-stu-id="ba807-164">Writes image data to a stream.</span></span>                                                                                |
| [<span data-ttu-id="ba807-165">**Stream**</span><span class="sxs-lookup"><span data-stu-id="ba807-165">**Stream**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)                             | <span data-ttu-id="ba807-166">Usado para ler e gravar dados de um arquivo, recurso de rede, um bloco de memória e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="ba807-166">Used to read and write data from a file, network resource, a block of memory, and so on.</span></span>                      |
| [<span data-ttu-id="ba807-167">**Conversor de formato**</span><span class="sxs-lookup"><span data-stu-id="ba807-167">**Format Converter**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)          | <span data-ttu-id="ba807-168">Usado para converter de um formato de pixel para outro.</span><span class="sxs-lookup"><span data-stu-id="ba807-168">Used to convert from one pixel format to another.</span></span>                                                             |
| [<span data-ttu-id="ba807-169">**Leitor de consulta de metadados**</span><span class="sxs-lookup"><span data-stu-id="ba807-169">**Metadata Query Reader**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) | <span data-ttu-id="ba807-170">Usado para ler metadados de uma imagem ou quadro de imagem.</span><span class="sxs-lookup"><span data-stu-id="ba807-170">Used to read metadata of an image or image frame.</span></span>                                                             |
| [<span data-ttu-id="ba807-171">**Gravador de consulta de metadados**</span><span class="sxs-lookup"><span data-stu-id="ba807-171">**Metadata Query Writer**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) | <span data-ttu-id="ba807-172">Usado para gravar metadados em um quadro de imagem ou imagem.</span><span class="sxs-lookup"><span data-stu-id="ba807-172">Used to write metadata to an image or image frame.</span></span>                                                            |



 

## <a name="see-also"></a><span data-ttu-id="ba807-173">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ba807-173">See Also</span></span>

[<span data-ttu-id="ba807-174">Referências</span><span class="sxs-lookup"><span data-stu-id="ba807-174">References</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="ba807-175">Amostras e exemplos de código</span><span class="sxs-lookup"><span data-stu-id="ba807-175">Samples and Code Examples</span></span>](-wic-samples.md)


 

 
