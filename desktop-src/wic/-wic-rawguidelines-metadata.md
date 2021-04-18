---
description: Suporte a metadados
ms.assetid: f3b4a3d9-a353-4af8-9998-cb7da7a062b7
title: Suporte a metadados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32499a88bd9cc12186629476f4d9f32a6e811858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812163"
---
# <a name="metadata-support"></a><span data-ttu-id="5c4f4-103">Suporte a metadados</span><span class="sxs-lookup"><span data-stu-id="5c4f4-103">Metadata Support</span></span>

<span data-ttu-id="5c4f4-104">Os formatos BRUTOs também devem dar suporte aos cenários comuns de leitura e gravação de metadados para imagens no Windows.</span><span class="sxs-lookup"><span data-stu-id="5c4f4-104">RAW formats should also support the common metadata read and write scenarios for images in Windows.</span></span> <span data-ttu-id="5c4f4-105">A Microsoft desenvolveu um conjunto de provedores de metadados nativos para o arquivo de imagem exchangável (EXIF), o IPTC (International Telecommunications Council) e os metadados da XMP (plataforma de metadados extensível) que são atualmente invocados apenas para contêineres TIFF e JPEG.</span><span class="sxs-lookup"><span data-stu-id="5c4f4-105">Microsoft has developed a set of native metadata providers for exchangeable image file (EXIF), International Press Telecommunications Council (IPTC), and Extensible Metadata Platform (XMP) metadata that are currently invoked only for TIFF and JPEG containers.</span></span> <span data-ttu-id="5c4f4-106">Se a imagem bruta for armazenada em um desses formatos de contêiner, é recomendável usar os provedores de metadados internos do Windows.</span><span class="sxs-lookup"><span data-stu-id="5c4f4-106">If the RAW image is stored in one of these container formats, it is recommended to use the Windows built-in metadata providers.</span></span> <span data-ttu-id="5c4f4-107">No entanto, o autor do codec é responsável por configurar isso corretamente.</span><span class="sxs-lookup"><span data-stu-id="5c4f4-107">However, the codec author is responsible for configuring this properly.</span></span> <span data-ttu-id="5c4f4-108">Para arquivos BRUTOs que não são baseados em um contêiner TIFF, pode ser necessário implementar os gravadores EXIF, IPTC ou XMP porque os leitores e gravadores internos esperam que os dados estejam em conformidade com as especificações de layout de EXIF, IPTC e XMP no disco.</span><span class="sxs-lookup"><span data-stu-id="5c4f4-108">For RAW files that are not based on a TIFF container, it might be necessary to implement EXIF, IPTC, or XMP writers because the built-in readers and writers expect the data to conform to EXIF, IPTC, and XMP on-disk layout specifications.</span></span> <span data-ttu-id="5c4f4-109">Os autores de codec também podem implementar seus próprios provedores para qualquer metadado personalizado.</span><span class="sxs-lookup"><span data-stu-id="5c4f4-109">Codec authors can also implement their own providers for any custom metadata.</span></span>

<span data-ttu-id="5c4f4-110">Devido à arquitetura do Windows Imaging Component (WIC), os gravadores de metadados podem ser invocados somente por meio de uma instância de um codificador de imagem.</span><span class="sxs-lookup"><span data-stu-id="5c4f4-110">Because of the architecture of Windows Imaging Component (WIC), metadata writers can be invoked only through an instance of an image encoder.</span></span> <span data-ttu-id="5c4f4-111">Portanto, os proprietários de formato bruto devem criar pelo menos um codificador "stub" [**WICRawParameterSet. WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) , mesmo que a codificação real de pixels em um formato bruto não seja implementada.</span><span class="sxs-lookup"><span data-stu-id="5c4f4-111">Therefore, RAW format owners should create at least a "stub" [**WICRawParameterSet.WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) encoder, even if the actual encoding of pixels into a RAW format is not implemented.</span></span> <span data-ttu-id="5c4f4-112">O autor do codec deve invocar os manipuladores de metadados apropriados:</span><span class="sxs-lookup"><span data-stu-id="5c4f4-112">The codec author must invoke the proper metadata handlers:</span></span>

-   <span data-ttu-id="5c4f4-113">[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) no decodificador e no decodificador de quadro, conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="5c4f4-113">[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) on both the decoder and frame decoder as appropriate.</span></span>
-   <span data-ttu-id="5c4f4-114">[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) tanto no codificador quanto no codificador de quadros, conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="5c4f4-114">[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) on both the encoder and frame encoder as appropriate.</span></span>

<span data-ttu-id="5c4f4-115">Para dar suporte a todos os cenários previstos em aplicativos de geração de imagens no Windows Vista, é recomendável que os fornecedores de codecs suportam o seguinte no mínimo:</span><span class="sxs-lookup"><span data-stu-id="5c4f4-115">To support all of the anticipated scenarios in imaging applications in Windows Vista, it is recommended that codec vendors support the following at a minimum:</span></span>

-   <span data-ttu-id="5c4f4-116">Leitura de EXIF</span><span class="sxs-lookup"><span data-stu-id="5c4f4-116">EXIF read</span></span>
-   <span data-ttu-id="5c4f4-117">Gravação parcial de EXIF (para permitir que as atualizações capturem data e hora)</span><span class="sxs-lookup"><span data-stu-id="5c4f4-117">Partial EXIF write (to permit updates to capture date and time)</span></span>
-   <span data-ttu-id="5c4f4-118">XMP de leitura e gravação (incluindo opcionalmente IPTC core para XMP)</span><span class="sxs-lookup"><span data-stu-id="5c4f4-118">XMP read and write (including optionally IPTC Core for XMP)</span></span>
-   <span data-ttu-id="5c4f4-119">Leitura e gravação de IPTC IIMv4</span><span class="sxs-lookup"><span data-stu-id="5c4f4-119">IPTC IIMv4 read and write</span></span>

<span data-ttu-id="5c4f4-120">A maior parte do acesso aos metadados (leitura e gravação) no Windows Vista ocorre por meio da interface [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) ou [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="5c4f4-120">Most of the metadata access (both read and write) in Windows Vista occurs through the [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) or [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) interface.</span></span> <span data-ttu-id="5c4f4-121">Portanto, para participar das experiências de metadados do Windows Vista, os autores de codec BRUTOs devem implementar os métodos [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) e [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="5c4f4-121">Therefore, to participate in the Windows Vista metadata experiences, RAW codec authors must implement the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) and [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c4f4-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5c4f4-122">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5c4f4-123">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="5c4f4-123">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5c4f4-124">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="5c4f4-124">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="5c4f4-125">Diretrizes do WIC para formatos de imagem bruta de câmera</span><span class="sxs-lookup"><span data-stu-id="5c4f4-125">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="5c4f4-126">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="5c4f4-126">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



