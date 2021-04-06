---
description: Esta seção de tópicos fornece aos desenvolvedores orientações sobre como implementar codecs de formato de arquivo de imagem que funcionarão dentro da estrutura do Windows Imaging Component (WIC).
ms.assetid: 58f03dc2-cc31-4d76-b75a-f332da1f900f
title: Como escrever um codec de WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee694d9a857781e97a31cb37f5ef18c518dae964
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828605"
---
# <a name="how-to-write-a-wic-enabled-codec"></a><span data-ttu-id="ddcd1-103">Como escrever um codec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="ddcd1-103">How to Write a WIC-Enabled Codec</span></span>

<span data-ttu-id="ddcd1-104">Esta seção de tópicos fornece aos desenvolvedores orientações sobre como implementar codecs de formato de arquivo de imagem que funcionarão dentro da estrutura do Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="ddcd1-104">This section of topics provide developers with guidance on how to implement image file format codecs that will function within the Windows Imaging Component (WIC) framework.</span></span>

<dl>

[<span data-ttu-id="ddcd1-105">Introdução</span><span class="sxs-lookup"><span data-stu-id="ddcd1-105">Introduction</span></span>](-wic-howtowriteacodec-intro.md)  
[<span data-ttu-id="ddcd1-106">Como funciona o Windows Imaging Component (WIC)</span><span class="sxs-lookup"><span data-stu-id="ddcd1-106">How The Windows Imaging Component (WIC) Works</span></span>](-wic-howwicworks.md)  
<dl>

[<span data-ttu-id="ddcd1-107">Descoberta e arbitragem</span><span class="sxs-lookup"><span data-stu-id="ddcd1-107">Discovery and Arbitration</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="ddcd1-108">Decodificação</span><span class="sxs-lookup"><span data-stu-id="ddcd1-108">Decoding</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="ddcd1-109">Codificação</span><span class="sxs-lookup"><span data-stu-id="ddcd1-109">Encoding</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="ddcd1-110">O tempo de vida de um codec</span><span class="sxs-lookup"><span data-stu-id="ddcd1-110">The Lifetime of a Codec</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="ddcd1-111">Como habilitar um codec por WIC</span><span class="sxs-lookup"><span data-stu-id="ddcd1-111">How to WIC-enable a Codec</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="ddcd1-112">Suporte a multi-threaded apartment no WIC</span><span class="sxs-lookup"><span data-stu-id="ddcd1-112">Multi-Threaded Apartment Support in WIC</span></span>](-wic-howwicworks.md)  
<span data-ttu-id="ddcd1-113"></dl> </dd> <a href="-wic-implementingwicdecoder.md">Implementando um decodificador de WIC-Enabled</a></span><span class="sxs-lookup"><span data-stu-id="ddcd1-113"></dl> </dd> <a href="-wic-implementingwicdecoder.md">Implementing a WIC-Enabled Decoder</a></span></span><dl>

[<span data-ttu-id="ddcd1-114">Interfaces do decodificador</span><span class="sxs-lookup"><span data-stu-id="ddcd1-114">Decoder Interfaces</span></span>](-wic-decoderinterfaces.md)<dl>

[<span data-ttu-id="ddcd1-115">IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="ddcd1-115">IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)  
[<span data-ttu-id="ddcd1-116">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="ddcd1-116">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)  
[<span data-ttu-id="ddcd1-117">IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="ddcd1-117">IWICBitmapSource</span></span>](-wic-imp-iwicbitmapsource.md)  
[<span data-ttu-id="ddcd1-118">IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="ddcd1-118">IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)  
[<span data-ttu-id="ddcd1-119">IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="ddcd1-119">IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)  
[<span data-ttu-id="ddcd1-120">IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="ddcd1-120">IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md)  
[<span data-ttu-id="ddcd1-121">IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="ddcd1-121">IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)  
<span data-ttu-id="ddcd1-122"></dl> </dd> </dl> </dd> <a href="-wic-implementingwicencoder.md">Implementando um codificador de WIC-Enabled</a>  
</span><span class="sxs-lookup"><span data-stu-id="ddcd1-122"></dl> </dd> </dl> </dd> <a href="-wic-implementingwicencoder.md">Implementing a WIC-Enabled Encoder</a>  
</span></span><dl>

[<span data-ttu-id="ddcd1-123">Interfaces do codificador</span><span class="sxs-lookup"><span data-stu-id="ddcd1-123">Encoder Interfaces</span></span>](-wic-encoderinterfaces.md)  
<dl>

[<span data-ttu-id="ddcd1-124">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="ddcd1-124">IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)  
[<span data-ttu-id="ddcd1-125">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="ddcd1-125">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)  
[<span data-ttu-id="ddcd1-126">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="ddcd1-126">IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)  
[<span data-ttu-id="ddcd1-127">IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="ddcd1-127">IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)  
<span data-ttu-id="ddcd1-128"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Instalação e registro de codec</a>  
</span><span class="sxs-lookup"><span data-stu-id="ddcd1-128"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Codec Installation and Registration</a>  
</span></span><dl>

[<span data-ttu-id="ddcd1-129">Registrando um codec</span><span class="sxs-lookup"><span data-stu-id="ddcd1-129">Registering a Codec</span></span>](-wic-codecinstallandreg.md)  
<dl>

[<span data-ttu-id="ddcd1-130">Entradas gerais de registro</span><span class="sxs-lookup"><span data-stu-id="ddcd1-130">General Register Entries</span></span>](-wic-generalregentries.md)  
[<span data-ttu-id="ddcd1-131">Entradas de registro específicas do codificador</span><span class="sxs-lookup"><span data-stu-id="ddcd1-131">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)  
<dl>

[<span data-ttu-id="ddcd1-132">Registrando um formato de contêiner com gravadores de metadados</span><span class="sxs-lookup"><span data-stu-id="ddcd1-132">Registering a Container Format with Metadata Writers</span></span>](-wic-encoderregentries.md)  
<span data-ttu-id="ddcd1-133"></dl> </dd> <a href="-wic-decoderregentries.md">Entradas de registro específicas do codificador</a>  
</span><span class="sxs-lookup"><span data-stu-id="ddcd1-133"></dl> </dd> <a href="-wic-decoderregentries.md">Encoder-Specific Registry Entries</a>  
</span></span><dl>

[<span data-ttu-id="ddcd1-134">Registrando um novo formato de contêiner com leitores de metadados</span><span class="sxs-lookup"><span data-stu-id="ddcd1-134">Registering a New Container Format with Metadata Readers</span></span>](-wic-decoderregentries.md)  
<span data-ttu-id="ddcd1-135"></dl> </dd> <a href="-wic-integrationregentries.md">Integração com o Windows Vista galeria e o Explorer</a>  
</span><span class="sxs-lookup"><span data-stu-id="ddcd1-135"></dl> </dd> <a href="-wic-integrationregentries.md">Integration with Windows Vista PhotoGallery and Explorer</a>  
</span></span><dl>

[<span data-ttu-id="ddcd1-136">Armazenamento de propriedades do Windows</span><span class="sxs-lookup"><span data-stu-id="ddcd1-136">Windows Property Store</span></span>](-wic-integrationregentries.md)  
[<span data-ttu-id="ddcd1-137">Galeria de fotos do Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ddcd1-137">Windows Vista Photo Gallery</span></span>](-wic-integrationregentries.md)  
[<span data-ttu-id="ddcd1-138">Cache de miniaturas do Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ddcd1-138">Windows Vista Thumbnail Cache</span></span>](-wic-integrationregentries.md)  
<span data-ttu-id="ddcd1-139"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Atualizando o cache de miniaturas ao instalar um codec que</a> [torna o codec de WIC-Enabled disponível para os usuários](-wic-codecinstallandreg.md) </dl> </dd> <a href="-wic-howtowriteacodec-conclusion.md">concluir</a>  
</span><span class="sxs-lookup"><span data-stu-id="ddcd1-139"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Updating the Thumbnail Cache when Installing a Codec</a> [Making Your WIC-Enabled Codec Available to Users](-wic-codecinstallandreg.md) </dl> </dd> <a href="-wic-howtowriteacodec-conclusion.md">Conclusion</a>  
</span></span></dl>

## <a name="related-topics"></a><span data-ttu-id="ddcd1-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ddcd1-140">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ddcd1-141">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="ddcd1-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ddcd1-142">Introdução (como escrever um CODEC de WIC-Enabled)</span><span class="sxs-lookup"><span data-stu-id="ddcd1-142">Introduction (How to Write a WIC-Enabled CODEC)</span></span>](-wic-howtowriteacodec-intro.md)
</dt> <dt>

[<span data-ttu-id="ddcd1-143">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="ddcd1-143">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



