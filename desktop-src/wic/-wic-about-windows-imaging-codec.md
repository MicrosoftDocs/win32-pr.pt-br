---
description: O Windows Imaging Component (WIC) fornece uma estrutura extensível para trabalhar com imagens e metadados de imagem.
ms.assetid: a05b496a-bd4c-4065-8060-df0f8930cde7
title: Visão geral do Windows Imaging Component
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764260dd9375f1372c1936c7dbd776295eb34433
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169884"
---
# <a name="windows-imaging-component-overview"></a><span data-ttu-id="2a116-103">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="2a116-103">Windows Imaging Component Overview</span></span>

<span data-ttu-id="2a116-104">O Windows Imaging Component (WIC) fornece uma estrutura extensível para trabalhar com imagens e metadados de imagem.</span><span class="sxs-lookup"><span data-stu-id="2a116-104">The Windows Imaging Component (WIC) provides an extensible framework for working with images and image metadata.</span></span> <span data-ttu-id="2a116-105">O WIC possibilita que ISVs (fornecedores independentes de software) e IHVs (fornecedores independentes de hardware) desenvolvam seus próprios codecs de imagem e obtenham o mesmo suporte de plataforma como formatos de imagem padrão (por exemplo, TIFF, JPEG, PNG, GIF, BMP e HDPhoto).</span><span class="sxs-lookup"><span data-stu-id="2a116-105">WIC makes it possible for independent software vendors (ISVs) and independent hardware vendors (IHVs) to develop their own image codecs and get the same platform support as standard image formats (for example, TIFF, JPEG, PNG, GIF, BMP, and HDPhoto).</span></span> <span data-ttu-id="2a116-106">Um único conjunto consistente de interfaces é usado para todo o processamento de imagem, independentemente do formato da imagem, de modo que qualquer aplicativo que use o WIC Obtenha suporte automático para novos formatos de imagem assim que o codec for instalado.</span><span class="sxs-lookup"><span data-stu-id="2a116-106">A single, consistent set of interfaces is used for all image processing, regardless of image format, so any application using the WIC gets automatic support for new image formats as soon as the codec is installed.</span></span> <span data-ttu-id="2a116-107">A estrutura de metadados extensíveis possibilita que os aplicativos leiam e gravem seus próprios metadados proprietários diretamente nos arquivos de imagem, para que os metadados nunca sejam perdidos ou separados da imagem.</span><span class="sxs-lookup"><span data-stu-id="2a116-107">The extensible metadata framework makes it possible for applications to read and write their own proprietary metadata directly to image files, so the metadata never gets lost or separated from the image.</span></span>

<span data-ttu-id="2a116-108">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="2a116-108">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="2a116-109">Recursos do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="2a116-109">Windows Imaging Component Features</span></span>](#windows-imaging-component-features)
-   [<span data-ttu-id="2a116-110">Codecs nativos</span><span class="sxs-lookup"><span data-stu-id="2a116-110">Native Codecs</span></span>](#native-codecs)
-   [<span data-ttu-id="2a116-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2a116-111">Related topics</span></span>](#related-topics)

## <a name="windows-imaging-component-features"></a><span data-ttu-id="2a116-112">Recursos do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="2a116-112">Windows Imaging Component Features</span></span>

<span data-ttu-id="2a116-113">Os principais recursos do WIC são:</span><span class="sxs-lookup"><span data-stu-id="2a116-113">The primary features of WIC are:</span></span>

-   <span data-ttu-id="2a116-114">Permite que os desenvolvedores de aplicativos executem operações de processamento de imagens em qualquer formato de imagem por meio de um único conjunto consistente de interfaces comuns, sem a necessidade de conhecimento prévio de formatos de imagem específicos.</span><span class="sxs-lookup"><span data-stu-id="2a116-114">Enables application developers to perform image processing operations on any image format through a single, consistent set of common interfaces, without requiring prior knowledge of specific image formats.</span></span>
-   <span data-ttu-id="2a116-115">Fornece uma arquitetura "plug and Play" extensível para codecs de imagem, formatos de pixel e metadados, com a descoberta automática de tempo de execução de novos formatos.</span><span class="sxs-lookup"><span data-stu-id="2a116-115">Provides an extensible "plug and play" architecture for image codecs, pixel formats, and metadata, with automatic run-time discovery of new formats.</span></span>
-   <span data-ttu-id="2a116-116">Dá suporte à leitura e gravação de metadados arbitrários em arquivos de imagem, com a capacidade de preservar metadados não reconhecidos durante a edição.</span><span class="sxs-lookup"><span data-stu-id="2a116-116">Supports reading and writing of arbitrary metadata in image files, with the ability to preserve unrecognized metadata during editing.</span></span>
-   <span data-ttu-id="2a116-117">Preserva dados de imagem de alta profundidade de bits, até 32 bits por canal, em todo o pipeline de processamento de imagens.</span><span class="sxs-lookup"><span data-stu-id="2a116-117">Preserves high bit depth image data, up to 32 bits per channel, throughout the image processing pipeline.</span></span>
-   <span data-ttu-id="2a116-118">Fornece suporte interno para os formatos de imagem mais populares, formatos de pixel e esquemas de metadados.</span><span class="sxs-lookup"><span data-stu-id="2a116-118">Provides built-in support for most popular image formats, pixel formats, and metadata schemas.</span></span>

## <a name="native-codecs"></a><span data-ttu-id="2a116-119">Codecs nativos</span><span class="sxs-lookup"><span data-stu-id="2a116-119">Native Codecs</span></span>

<span data-ttu-id="2a116-120">O WIC inclui vários codecs internos.</span><span class="sxs-lookup"><span data-stu-id="2a116-120">WIC includes several built-in codecs.</span></span> <span data-ttu-id="2a116-121">Os codecs padrão a seguir são fornecidos com a plataforma.</span><span class="sxs-lookup"><span data-stu-id="2a116-121">The following standard codecs are provided with the platform.</span></span> 

| <span data-ttu-id="2a116-122">Codec</span><span class="sxs-lookup"><span data-stu-id="2a116-122">Codec</span></span>                                                                                             | <span data-ttu-id="2a116-123">Tipos de MIME</span><span class="sxs-lookup"><span data-stu-id="2a116-123">Mime Types</span></span>                       | <span data-ttu-id="2a116-124">Decodificadores</span><span class="sxs-lookup"><span data-stu-id="2a116-124">Decoders</span></span> | <span data-ttu-id="2a116-125">Codificadores</span><span class="sxs-lookup"><span data-stu-id="2a116-125">Encoders</span></span> |
|---------------------------------------------------------------------------------------------------|----------------------------------|----------|----------|
| <span data-ttu-id="2a116-126">BMP (formato de bitmap do Windows), especificação BMP v5.</span><span class="sxs-lookup"><span data-stu-id="2a116-126">BMP (Windows Bitmap Format), BMP Specification v5.</span></span>                                                | <span data-ttu-id="2a116-127">image/bmp</span><span class="sxs-lookup"><span data-stu-id="2a116-127">image/bmp</span></span>                        | <span data-ttu-id="2a116-128">Sim</span><span class="sxs-lookup"><span data-stu-id="2a116-128">Yes</span></span>      | <span data-ttu-id="2a116-129">Sim</span><span class="sxs-lookup"><span data-stu-id="2a116-129">Yes</span></span>      |
| <span data-ttu-id="2a116-130">GIF (Graphics Interchange Format 89A), especificação GIF 89A/89m</span><span class="sxs-lookup"><span data-stu-id="2a116-130">GIF (Graphics Interchange Format 89a), GIF Specification 89a/89m</span></span>                                  | <span data-ttu-id="2a116-131">image/gif</span><span class="sxs-lookup"><span data-stu-id="2a116-131">image/gif</span></span>                        | <span data-ttu-id="2a116-132">Sim</span><span class="sxs-lookup"><span data-stu-id="2a116-132">Yes</span></span>      | <span data-ttu-id="2a116-133">Sim</span><span class="sxs-lookup"><span data-stu-id="2a116-133">Yes</span></span>      |
| <span data-ttu-id="2a116-134">ICO (formato de ícone)</span><span class="sxs-lookup"><span data-stu-id="2a116-134">ICO (Icon Format)</span></span>                                                                                 | <span data-ttu-id="2a116-135">imagem/ico</span><span class="sxs-lookup"><span data-stu-id="2a116-135">image/ico</span></span>                        | <span data-ttu-id="2a116-136">Sim</span><span class="sxs-lookup"><span data-stu-id="2a116-136">Yes</span></span>      | <span data-ttu-id="2a116-137">Não</span><span class="sxs-lookup"><span data-stu-id="2a116-137">No</span></span>       |
| <span data-ttu-id="2a116-138">JPEG (Joint multigraphic Experts Group), JFIF Specification 1, 2</span><span class="sxs-lookup"><span data-stu-id="2a116-138">JPEG (Joint Photographic Experts Group), JFIF Specification 1.02</span></span>                                  | <span data-ttu-id="2a116-139">imagem/JPEG, imagem/JPE, imagem/jpg</span><span class="sxs-lookup"><span data-stu-id="2a116-139">image/jpeg, image/jpe, image/jpg</span></span> | <span data-ttu-id="2a116-140">Sim</span><span class="sxs-lookup"><span data-stu-id="2a116-140">Yes</span></span>      | <span data-ttu-id="2a116-141">Sim</span><span class="sxs-lookup"><span data-stu-id="2a116-141">Yes</span></span>      |
| <span data-ttu-id="2a116-142">PNG (Portable Network Graphics), especificação de PNG 1,2</span><span class="sxs-lookup"><span data-stu-id="2a116-142">PNG (Portable Network Graphics), PNG Specification 1.2</span></span>                                            | <span data-ttu-id="2a116-143">image/png</span><span class="sxs-lookup"><span data-stu-id="2a116-143">image/png</span></span>                        | <span data-ttu-id="2a116-144">Sim</span><span class="sxs-lookup"><span data-stu-id="2a116-144">Yes</span></span>      | <span data-ttu-id="2a116-145">Sim</span><span class="sxs-lookup"><span data-stu-id="2a116-145">Yes</span></span>      |
| <span data-ttu-id="2a116-146">TIFF (formato de arquivo de imagem marcada), especificação TIFF 6,0</span><span class="sxs-lookup"><span data-stu-id="2a116-146">TIFF (Tagged Image File Format), TIFF Specification 6.0</span></span>                                           | <span data-ttu-id="2a116-147">imagem/TIFF, imagem/TIF</span><span class="sxs-lookup"><span data-stu-id="2a116-147">image/tiff, image/tif</span></span>            | <span data-ttu-id="2a116-148">Sim</span><span class="sxs-lookup"><span data-stu-id="2a116-148">Yes</span></span>      | <span data-ttu-id="2a116-149">Sim</span><span class="sxs-lookup"><span data-stu-id="2a116-149">Yes</span></span>      |
| <span data-ttu-id="2a116-150">Foto do Windows Media, [especificação de foto de HD 1,0](https://www.microsoft.com/whdc/xps/wmphoto.mspx)</span><span class="sxs-lookup"><span data-stu-id="2a116-150">Windows Media Photo, [HD Photo Specification 1.0](https://www.microsoft.com/whdc/xps/wmphoto.mspx)</span></span> | <span data-ttu-id="2a116-151">Image/vnd. ms-phot</span><span class="sxs-lookup"><span data-stu-id="2a116-151">image/vnd.ms-phot</span></span>                | <span data-ttu-id="2a116-152">Sim</span><span class="sxs-lookup"><span data-stu-id="2a116-152">Yes</span></span>      | <span data-ttu-id="2a116-153">Sim</span><span class="sxs-lookup"><span data-stu-id="2a116-153">Yes</span></span>      |
| <span data-ttu-id="2a116-154">DDS (superfície do DirectDraw)</span><span class="sxs-lookup"><span data-stu-id="2a116-154">DDS (DirectDraw Surface)</span></span>                                                                          | <span data-ttu-id="2a116-155">Image/vnd. ms-DDS</span><span class="sxs-lookup"><span data-stu-id="2a116-155">image/vnd.ms-dds</span></span>                 | <span data-ttu-id="2a116-156">Sim</span><span class="sxs-lookup"><span data-stu-id="2a116-156">Yes</span></span>      | <span data-ttu-id="2a116-157">Sim</span><span class="sxs-lookup"><span data-stu-id="2a116-157">Yes</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="2a116-158">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2a116-158">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2a116-159">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="2a116-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2a116-160">Visão geral dos metadados do WIC</span><span class="sxs-lookup"><span data-stu-id="2a116-160">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

<span data-ttu-id="2a116-161">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="2a116-161">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="2a116-162">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="2a116-162">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

<span data-ttu-id="2a116-163">[CODEC de exemplo AITCodec](/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2a116-163">[AITCodec Sample CODEC](/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85))</span></span>
</dt> </dl>

 

 
