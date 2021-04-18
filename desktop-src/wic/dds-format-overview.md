---
description: Fornece informações sobre o codec do DDS nativo disponível por meio do Windows Imaging Component (WIC).
ms.assetid: 6CFDD674-C8AE-4F29-B2E5-C9C9431CB85A
title: Visão geral do formato DDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c45222a66d5a250caaf46db465d2359e09b3e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810657"
---
# <a name="dds-format-overview"></a><span data-ttu-id="41e33-103">Visão geral do formato DDS</span><span class="sxs-lookup"><span data-stu-id="41e33-103">DDS Format Overview</span></span>

<span data-ttu-id="41e33-104">Este tópico fornece informações sobre o codec do DDS nativo disponível por meio do Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="41e33-104">This topic provides information about the native DDS codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="41e33-105">Identidade do codec</span><span class="sxs-lookup"><span data-stu-id="41e33-105">Codec Identity</span></span>

<span data-ttu-id="41e33-106">A tabela a seguir fornece informações de identificação do codec.</span><span class="sxs-lookup"><span data-stu-id="41e33-106">The following table provides codec identification information.</span></span>



|                        |                    |
|------------------------|--------------------|
| <span data-ttu-id="41e33-107">Nome (s) formal (es)</span><span class="sxs-lookup"><span data-stu-id="41e33-107">Formal Name(s)</span></span>         | <span data-ttu-id="41e33-108">Superfície do DirectDraw</span><span class="sxs-lookup"><span data-stu-id="41e33-108">DirectDraw Surface</span></span> |
| <span data-ttu-id="41e33-109">Extensão (s) de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="41e33-109">File Name Extension(s)</span></span> | <span data-ttu-id="41e33-110">DDS</span><span class="sxs-lookup"><span data-stu-id="41e33-110">dds</span></span>                |
| <span data-ttu-id="41e33-111">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="41e33-111">MIME type</span></span>              | <span data-ttu-id="41e33-112">Image/VND-MS. DDS</span><span class="sxs-lookup"><span data-stu-id="41e33-112">image/vnd-ms.dds</span></span>   |



 

<span data-ttu-id="41e33-113">A tabela a seguir lista os GUIDs usados para identificar os componentes do codec DDS nativo.</span><span class="sxs-lookup"><span data-stu-id="41e33-113">The following table lists the GUIDs used to identify the native DDS codec components.</span></span>



| <span data-ttu-id="41e33-114">Componente</span><span class="sxs-lookup"><span data-stu-id="41e33-114">Component</span></span>        | <span data-ttu-id="41e33-115">Nome amigável</span><span class="sxs-lookup"><span data-stu-id="41e33-115">Friendly Name</span></span>            | <span data-ttu-id="41e33-116">GUID</span><span class="sxs-lookup"><span data-stu-id="41e33-116">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="41e33-117">Formato do contêiner</span><span class="sxs-lookup"><span data-stu-id="41e33-117">Container Format</span></span> | <span data-ttu-id="41e33-118">\_CONTAINERFORMATDDS GUID</span><span class="sxs-lookup"><span data-stu-id="41e33-118">GUID\_ContainerFormatDds</span></span> | <span data-ttu-id="41e33-119">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span><span class="sxs-lookup"><span data-stu-id="41e33-119">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span></span> |
| <span data-ttu-id="41e33-120">Decodificador</span><span class="sxs-lookup"><span data-stu-id="41e33-120">Decoder</span></span>          | <span data-ttu-id="41e33-121">\_WICDDSDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="41e33-121">CLSID\_WICDdsDecoder</span></span>     | <span data-ttu-id="41e33-122">9053699f-a341-429d-9e90ee437cf80c73</span><span class="sxs-lookup"><span data-stu-id="41e33-122">9053699f-a341-429d-9e90ee437cf80c73</span></span> |
| <span data-ttu-id="41e33-123">Codificador</span><span class="sxs-lookup"><span data-stu-id="41e33-123">Encoder</span></span>          | <span data-ttu-id="41e33-124">\_WICDDSENCODER CLSID</span><span class="sxs-lookup"><span data-stu-id="41e33-124">CLSID\_WICDdsEncoder</span></span>     | <span data-ttu-id="41e33-125">a61dde94-66ce-4ac1-881b71680588895e</span><span class="sxs-lookup"><span data-stu-id="41e33-125">a61dde94-66ce-4ac1-881b71680588895e</span></span> |



 

## <a name="pixel-format-support"></a><span data-ttu-id="41e33-126">Suporte a formato de pixel</span><span class="sxs-lookup"><span data-stu-id="41e33-126">Pixel Format Support</span></span>

<span data-ttu-id="41e33-127">Observe que o formato DDS dá suporte a qualquer valor de [**\_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) válido.</span><span class="sxs-lookup"><span data-stu-id="41e33-127">Note that the DDS format supports any valid [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) value.</span></span> <span data-ttu-id="41e33-128">No entanto, o codec DDS do WIC dá suporte apenas à decodificação e à codificação de arquivos que contêm os seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="41e33-128">However, the WIC DDS codec only supports decoding and encoding files containing the following formats:</span></span>

-   <span data-ttu-id="41e33-129">\_Formato dxgi \_ BC1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="41e33-129">DXGI\_FORMAT\_BC1\_UNORM</span></span>
-   <span data-ttu-id="41e33-130">\_Formato dxgi \_ BC2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="41e33-130">DXGI\_FORMAT\_BC2\_UNORM</span></span>
-   <span data-ttu-id="41e33-131">\_Formato dxgi \_ BC3 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="41e33-131">DXGI\_FORMAT\_BC3\_UNORM</span></span>

## <a name="encoding"></a><span data-ttu-id="41e33-132">Codificação</span><span class="sxs-lookup"><span data-stu-id="41e33-132">Encoding</span></span>

<span data-ttu-id="41e33-133">As APIs de codificação do WIC são projetadas para serem independentes de codec e, portanto, a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="41e33-133">The WIC encoding APIs are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="41e33-134">Para obter mais informações sobre codificação de imagem usando a API do WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="41e33-134">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="41e33-135">O formato de arquivo DDS tem requisitos exclusivos que surgem de seu suporte para conceitos como mipmaps e matrizes de textura.</span><span class="sxs-lookup"><span data-stu-id="41e33-135">The DDS file format has unique requirements that arise from its support for concepts such as mipmaps and texture arrays.</span></span> <span data-ttu-id="41e33-136">Para exercer total controle sobre a codificação de imagem DDS, você deve usar a interface [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) para definir parâmetros de codificação específicos do DDS.</span><span class="sxs-lookup"><span data-stu-id="41e33-136">To fully exercise control over DDS image encoding, you should use the [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) interface to set DDS-specific encoding parameters.</span></span>

## <a name="decoding"></a><span data-ttu-id="41e33-137">Decodificação</span><span class="sxs-lookup"><span data-stu-id="41e33-137">Decoding</span></span>

<span data-ttu-id="41e33-138">As APIs de decodificação de WIC são projetadas para serem independentes de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="41e33-138">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="41e33-139">Para obter mais informações sobre a decodificação de imagem, consulte a [visão geral da decodificação](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="41e33-139">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="41e33-140">Para obter mais informações sobre como usar dados de imagem decodificados, consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="41e33-140">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="block-compressed-data-access"></a><span data-ttu-id="41e33-141">Bloquear acesso a dados compactados</span><span class="sxs-lookup"><span data-stu-id="41e33-141">Block compressed data access</span></span>

<span data-ttu-id="41e33-142">Além de dar suporte às interfaces de codec padrão do WIC, o decodificador DDS fornece acesso direto aos dados compactados do bloco nativo usando as interfaces específicas do DDS, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) e [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode).</span><span class="sxs-lookup"><span data-stu-id="41e33-142">In addition to supporting the standard WIC codec interfaces, the DDS decoder provides direct access to the native block compressed data using the DDS-specific interfaces, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) and [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode).</span></span> <span data-ttu-id="41e33-143">Para usar essas interfaces, chame QueryInterface fora de [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="41e33-143">To use these interfaces, call QueryInterface off of [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), respectively.</span></span>

 

 
