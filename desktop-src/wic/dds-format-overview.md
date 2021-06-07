---
description: Fornece informações sobre o codec DDS nativo disponível por meio do WIC (Windows Imaging Component).
ms.assetid: 6CFDD674-C8AE-4F29-B2E5-C9C9431CB85A
title: Visão geral do formato DDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f860a5759218575acb53be5f2142e71aa34e9554
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444947"
---
# <a name="dds-format-overview"></a><span data-ttu-id="d119b-103">Visão geral do formato DDS</span><span class="sxs-lookup"><span data-stu-id="d119b-103">DDS Format Overview</span></span>

<span data-ttu-id="d119b-104">Este tópico fornece informações sobre o codec DDS nativo disponível por meio do WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="d119b-104">This topic provides information about the native DDS codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="d119b-105">Identidade do Codec</span><span class="sxs-lookup"><span data-stu-id="d119b-105">Codec Identity</span></span>

<span data-ttu-id="d119b-106">A tabela a seguir fornece informações de identificação de codec.</span><span class="sxs-lookup"><span data-stu-id="d119b-106">The following table provides codec identification information.</span></span>



| <span data-ttu-id="d119b-107">Componente</span><span class="sxs-lookup"><span data-stu-id="d119b-107">Component</span></span>              | <span data-ttu-id="d119b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d119b-108">Description</span></span>        |
|------------------------|--------------------|
| <span data-ttu-id="d119b-109">Nomes formais</span><span class="sxs-lookup"><span data-stu-id="d119b-109">Formal Name(s)</span></span>         | <span data-ttu-id="d119b-110">DirectDraw Surface</span><span class="sxs-lookup"><span data-stu-id="d119b-110">DirectDraw Surface</span></span> |
| <span data-ttu-id="d119b-111">Extensões de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="d119b-111">File Name Extension(s)</span></span> | <span data-ttu-id="d119b-112">Dds</span><span class="sxs-lookup"><span data-stu-id="d119b-112">dds</span></span>                |
| <span data-ttu-id="d119b-113">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="d119b-113">MIME type</span></span>              | <span data-ttu-id="d119b-114">image/vnd-ms.dds</span><span class="sxs-lookup"><span data-stu-id="d119b-114">image/vnd-ms.dds</span></span>   |



 

<span data-ttu-id="d119b-115">A tabela a seguir lista os GUIDs usados para identificar os componentes nativos do codec do DDS.</span><span class="sxs-lookup"><span data-stu-id="d119b-115">The following table lists the GUIDs used to identify the native DDS codec components.</span></span>



| <span data-ttu-id="d119b-116">Componente</span><span class="sxs-lookup"><span data-stu-id="d119b-116">Component</span></span>        | <span data-ttu-id="d119b-117">Nome amigável</span><span class="sxs-lookup"><span data-stu-id="d119b-117">Friendly Name</span></span>            | <span data-ttu-id="d119b-118">GUID</span><span class="sxs-lookup"><span data-stu-id="d119b-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="d119b-119">Formato do contêiner</span><span class="sxs-lookup"><span data-stu-id="d119b-119">Container Format</span></span> | <span data-ttu-id="d119b-120">Contêiner \_ GUIDFormatDds</span><span class="sxs-lookup"><span data-stu-id="d119b-120">GUID\_ContainerFormatDds</span></span> | <span data-ttu-id="d119b-121">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span><span class="sxs-lookup"><span data-stu-id="d119b-121">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span></span> |
| <span data-ttu-id="d119b-122">Decodificador</span><span class="sxs-lookup"><span data-stu-id="d119b-122">Decoder</span></span>          | <span data-ttu-id="d119b-123">CLSID \_ WICDdsDecoder</span><span class="sxs-lookup"><span data-stu-id="d119b-123">CLSID\_WICDdsDecoder</span></span>     | <span data-ttu-id="d119b-124">9053699f-a341-429d-9e90ee437cf80c73</span><span class="sxs-lookup"><span data-stu-id="d119b-124">9053699f-a341-429d-9e90ee437cf80c73</span></span> |
| <span data-ttu-id="d119b-125">Codificador</span><span class="sxs-lookup"><span data-stu-id="d119b-125">Encoder</span></span>          | <span data-ttu-id="d119b-126">CLSID \_ WICDdsEncoder</span><span class="sxs-lookup"><span data-stu-id="d119b-126">CLSID\_WICDdsEncoder</span></span>     | <span data-ttu-id="d119b-127">a61dde94-66ce-4ac1-881b71680588895e</span><span class="sxs-lookup"><span data-stu-id="d119b-127">a61dde94-66ce-4ac1-881b71680588895e</span></span> |



 

## <a name="pixel-format-support"></a><span data-ttu-id="d119b-128">Suporte ao formato de pixel</span><span class="sxs-lookup"><span data-stu-id="d119b-128">Pixel Format Support</span></span>

<span data-ttu-id="d119b-129">Observe que o formato DDS dá suporte a qualquer [**valor DXGI \_ FORMAT válido.**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="d119b-129">Note that the DDS format supports any valid [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) value.</span></span> <span data-ttu-id="d119b-130">No entanto, o codec DDS do WIC dá suporte apenas a arquivos de decodificação e codificação que contêm os seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="d119b-130">However, the WIC DDS codec only supports decoding and encoding files containing the following formats:</span></span>

-   <span data-ttu-id="d119b-131">FORMATO DXGI \_ \_ BC1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="d119b-131">DXGI\_FORMAT\_BC1\_UNORM</span></span>
-   <span data-ttu-id="d119b-132">FORMATO DXGI \_ \_ BC2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="d119b-132">DXGI\_FORMAT\_BC2\_UNORM</span></span>
-   <span data-ttu-id="d119b-133">FORMATO DXGI \_ \_ BC3 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="d119b-133">DXGI\_FORMAT\_BC3\_UNORM</span></span>

## <a name="encoding"></a><span data-ttu-id="d119b-134">Codificação</span><span class="sxs-lookup"><span data-stu-id="d119b-134">Encoding</span></span>

<span data-ttu-id="d119b-135">As APIs de codificação WIC são projetadas para serem independentes de codec e, portanto, a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="d119b-135">The WIC encoding APIs are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="d119b-136">Para obter mais informações sobre a codificação de imagem usando a API WIC, consulte a [Visão geral de codificação](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="d119b-136">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="d119b-137">O formato de arquivo DDS tem requisitos exclusivos que surgem de seu suporte para conceitos como mipmaps e matrizes de textura.</span><span class="sxs-lookup"><span data-stu-id="d119b-137">The DDS file format has unique requirements that arise from its support for concepts such as mipmaps and texture arrays.</span></span> <span data-ttu-id="d119b-138">Para controlar totalmente a codificação de imagem DDS, você deve usar a interface [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) para definir parâmetros de codificação específicos do DDS.</span><span class="sxs-lookup"><span data-stu-id="d119b-138">To fully exercise control over DDS image encoding, you should use the [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) interface to set DDS-specific encoding parameters.</span></span>

## <a name="decoding"></a><span data-ttu-id="d119b-139">Decodificação</span><span class="sxs-lookup"><span data-stu-id="d119b-139">Decoding</span></span>

<span data-ttu-id="d119b-140">As APIs de decodificação do WIC foram projetadas para serem independentes de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="d119b-140">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="d119b-141">Para obter mais informações sobre decodificação de imagem, consulte Visão [geral de decodificação.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="d119b-141">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="d119b-142">Para obter mais informações sobre como usar dados de imagem decodificados, consulte Visão geral das [fontes de bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="d119b-142">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="block-compressed-data-access"></a><span data-ttu-id="d119b-143">Bloquear o acesso a dados compactados</span><span class="sxs-lookup"><span data-stu-id="d119b-143">Block compressed data access</span></span>

<span data-ttu-id="d119b-144">Além de dar suporte às interfaces de codec padrão do WIC, o decodificador DDS fornece acesso direto aos dados compactados de bloco nativo usando as interfaces específicas de DDS, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) e [**IWICDdsFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode)</span><span class="sxs-lookup"><span data-stu-id="d119b-144">In addition to supporting the standard WIC codec interfaces, the DDS decoder provides direct access to the native block compressed data using the DDS-specific interfaces, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) and [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode).</span></span> <span data-ttu-id="d119b-145">Para usar essas interfaces, chame QueryInterface de [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e [**IWICBitmapFrameDecode,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d119b-145">To use these interfaces, call QueryInterface off of [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), respectively.</span></span>

 

 
