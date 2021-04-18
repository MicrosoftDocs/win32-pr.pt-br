---
description: Os codecs de áudio e vídeo do Windows Media são uma coleção de objetos que você pode usar para compactar e descompactar dados de mídia digital.
ms.assetid: 74de2e75-b1ee-436d-8d78-efe366ab7aa6
title: Codificações de mídia do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec98f98fbd0561b291dfc4cc18e4270bf363baf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105781375"
---
# <a name="windows-media-codecs"></a><span data-ttu-id="a94bf-103">Codificações de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="a94bf-103">Windows Media Codecs</span></span>

<span data-ttu-id="a94bf-104">Os codecs de áudio e vídeo do Windows Media são uma coleção de objetos que você pode usar para compactar e descompactar dados de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="a94bf-104">The Windows Media Audio and Video codecs are a collection of objects that you can use to compress and decompress digital media data.</span></span> <span data-ttu-id="a94bf-105">Cada codec consiste em dois objetos, um codificador e um decodificador.</span><span class="sxs-lookup"><span data-stu-id="a94bf-105">Each codec consists of two objects, an encoder and a decoder.</span></span> <span data-ttu-id="a94bf-106">Esta parte da documentação descreve como usar os recursos dos codecs de áudio e vídeo do Windows Media para produzir e consumir fluxos de dados compactados.</span><span class="sxs-lookup"><span data-stu-id="a94bf-106">This part of the documentation describes how to use the features of the Windows Media Audio and Video codecs to produce and consume compressed data streams.</span></span>

> [!Note]  
> <span data-ttu-id="a94bf-107">Esta documentação destina-se principalmente aos desenvolvedores que desejam usar os codecs de mídia do Windows em seus aplicativos de mídia baseados em C++.</span><span class="sxs-lookup"><span data-stu-id="a94bf-107">This documentation is primarily for developers who want to use Windows Media codecs in their C++-based media applications.</span></span> <span data-ttu-id="a94bf-108">Para obter uma visão geral técnica dos recursos dos codecs de mídia do Windows, consulte [sobre os codecs de mídia do Windows](about-the-windows-media-codecs.md).</span><span class="sxs-lookup"><span data-stu-id="a94bf-108">For a technical overview of the features of the Windows Media codecs, see [About the Windows Media Codecs](about-the-windows-media-codecs.md).</span></span>

 

<span data-ttu-id="a94bf-109">O termo *codec* é uma ajuntamento do compressor de termos e do descompactador.</span><span class="sxs-lookup"><span data-stu-id="a94bf-109">The term *codec* is an amalgamation of the terms compressor and decompressor.</span></span> <span data-ttu-id="a94bf-110">Um codec geralmente é implementado como um par de objetos COM: um para codificar conteúdo e outro para decodificar conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a94bf-110">A codec is usually implemented as a pair of COM objects: one for encoding content, and another for decoding content.</span></span> <span data-ttu-id="a94bf-111">Em alguns casos, os objetos COM ocupam a mesma biblioteca de vínculos dinâmicos (DLL).</span><span class="sxs-lookup"><span data-stu-id="a94bf-111">In some cases the COM objects occupy the same dynamically linked library (DLL).</span></span>

<span data-ttu-id="a94bf-112">Cada objeto de codec implementa duas interfaces separadas, mas semelhantes:</span><span class="sxs-lookup"><span data-stu-id="a94bf-112">Every codec object implements two separate but similar interfaces:</span></span>



| <span data-ttu-id="a94bf-113">Interface</span><span class="sxs-lookup"><span data-stu-id="a94bf-113">Interface</span></span>                              | <span data-ttu-id="a94bf-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="a94bf-114">Description</span></span>                                 |
|----------------------------------------|---------------------------------------------|
| [<span data-ttu-id="a94bf-115">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="a94bf-115">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | <span data-ttu-id="a94bf-116">Compatível com Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a94bf-116">Compatible with Microsoft Media Foundation.</span></span> |
| [<span data-ttu-id="a94bf-117">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="a94bf-117">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | <span data-ttu-id="a94bf-118">Compatível com o DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a94bf-118">Compatible with DirectShow.</span></span>                 |



 

<span data-ttu-id="a94bf-119">Não só há codecs diferentes para áudio e vídeo, mas também codecs diferentes para tipos diferentes de conteúdo que você pode querer colocar em um arquivo de áudio ou de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a94bf-119">Not only are there different codecs for audio and for video, but also different codecs for different kinds of content that you might want to put into an audio or video file.</span></span> <span data-ttu-id="a94bf-120">Os algoritmos usados para compactar e descompactar dados de palavras faladas diferem dos algoritmos usados para compactar e descompactar dados de música.</span><span class="sxs-lookup"><span data-stu-id="a94bf-120">The algorithms used to compress and decompress data for spoken words differ from the algorithms used to compress and decompress music data.</span></span>

## <a name="codec-descriptions"></a><span data-ttu-id="a94bf-121">Descrições de codec</span><span class="sxs-lookup"><span data-stu-id="a94bf-121">Codec Descriptions</span></span>

<span data-ttu-id="a94bf-122">A tabela a seguir descreve os usos pretendidos dos codecs de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="a94bf-122">The following table describes the intended uses of the Windows Media codecs.</span></span>



| <span data-ttu-id="a94bf-123">Codec</span><span class="sxs-lookup"><span data-stu-id="a94bf-123">Codec</span></span>                                                                     | <span data-ttu-id="a94bf-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="a94bf-124">Description</span></span>                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a94bf-125">Áudio do Windows Media</span><span class="sxs-lookup"><span data-stu-id="a94bf-125">Windows Media Audio</span></span>](windowsmediaaudioencoder.md)                       | <span data-ttu-id="a94bf-126">Um codec de áudio que dá suporte a três categorias de conteúdo codificado: Standard, Professional e Lossless.</span><span class="sxs-lookup"><span data-stu-id="a94bf-126">An audio codec that supports three categories of encoded content: Standard, Professional, and Lossless.</span></span>                                                                                                                                                                                      |
| [<span data-ttu-id="a94bf-127">Voz de áudio do Windows Media</span><span class="sxs-lookup"><span data-stu-id="a94bf-127">Windows Media Audio Voice</span></span>](windowsmediaaudiovoiceencoder.md)            | <span data-ttu-id="a94bf-128">Codec de áudio otimizado para codificar a voz humana em altas taxas de compactação.</span><span class="sxs-lookup"><span data-stu-id="a94bf-128">Audio codec optimized for encoding the human voice at high compression ratios.</span></span> <span data-ttu-id="a94bf-129">Esse é o codec preferencial para fluxos que consistem principalmente em palavras faladas.</span><span class="sxs-lookup"><span data-stu-id="a94bf-129">This is the preferred codec for streams consisting mostly of spoken words.</span></span> <span data-ttu-id="a94bf-130">Para o conteúdo que é música e fala mista, esse codec pode alterar dinamicamente o algoritmo de codificação usado para obter a qualidade ideal.</span><span class="sxs-lookup"><span data-stu-id="a94bf-130">For content that is mixed music and speech, this codec can dynamically change the encoding algorithm used, to get optimal quality.</span></span> |
| [<span data-ttu-id="a94bf-131">Vídeo do Windows Media 9</span><span class="sxs-lookup"><span data-stu-id="a94bf-131">Windows Media Video 9</span></span>](windowsmediavideo9encoder.md)                    | <span data-ttu-id="a94bf-132">Um codec de vídeo que dá suporte a quatro categorias de conteúdo codificado: perfil simples, perfil principal, perfil avançado e imagem..</span><span class="sxs-lookup"><span data-stu-id="a94bf-132">A video codec that supports four categories of encoded content: Simple Profile, Main Profile, Advanced Profile, and Image..</span></span>                                                                                                                                                                  |
| [<span data-ttu-id="a94bf-133">Tela do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="a94bf-133">Windows Media Video 9 Screen</span></span>](usingthewindowsmediavideo9screencodec.md) | <span data-ttu-id="a94bf-134">Codec de vídeo otimizado para codificação de capturas de tela sequenciais de monitores de computador.</span><span class="sxs-lookup"><span data-stu-id="a94bf-134">Video codec optimized for encoding sequential screen shots from computer monitors.</span></span> <span data-ttu-id="a94bf-135">Esse codec é geralmente usado para treinamento de software ou suporte ao gravar imagens de monitor enquanto os aplicativos de computador estão sendo usados.</span><span class="sxs-lookup"><span data-stu-id="a94bf-135">This codec is often used for software training or support by recording monitor images while computer applications are being used.</span></span>                                                                         |



 

<span data-ttu-id="a94bf-136">As versões mais recentes dos objetos de codec também habilitam o acesso a alguns codecs herdados, incluindo o Windows Media Video 7 e 8, Windows Media tela 7, os codecs mais antigos do Microsoft MPEG-4 e os codecs ISO MPEG-4 da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a94bf-136">The most recent versions of the codec objects also enable access to some legacy codecs, including Windows Media Video 7 and 8, Windows Media Screen 7, the older Microsoft MPEG-4 codecs, and the Microsoft ISO MPEG-4 codecs.</span></span>

> [!Note]  
> <span data-ttu-id="a94bf-137">Esta documentação não aborda esses codecs herdados; Ele abrange apenas as versões atuais dos codecs.</span><span class="sxs-lookup"><span data-stu-id="a94bf-137">This documentation does not cover these legacy codecs; it covers only the current versions of codecs.</span></span>

 

<span data-ttu-id="a94bf-138">Para codecs mais antigos, use os mesmos procedimentos que ao usar os codecs atuais; no entanto, lembre-se de que nem todos os recursos têm suporte em todos os codecs.</span><span class="sxs-lookup"><span data-stu-id="a94bf-138">For older codecs, use the same procedures as when using the current codecs; however, remember that not all features are supported in all codecs.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a94bf-139">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="a94bf-139">In this section</span></span>

-   [<span data-ttu-id="a94bf-140">Sobre os codecs de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="a94bf-140">About the Windows Media Codecs</span></span>](about-the-windows-media-codecs.md)
-   [<span data-ttu-id="a94bf-141">Usando os objetos codec e DSP</span><span class="sxs-lookup"><span data-stu-id="a94bf-141">Using the Codec and DSP Objects</span></span>](decidinghowtousethewindowsmediaaudioandvideocodecs.md)
-   [<span data-ttu-id="a94bf-142">Métodos de codificação</span><span class="sxs-lookup"><span data-stu-id="a94bf-142">Encoding Methods</span></span>](encodingmethods.md)
-   [<span data-ttu-id="a94bf-143">Implementação de codec</span><span class="sxs-lookup"><span data-stu-id="a94bf-143">Codec Implementation</span></span>](codecimplementation.md)
-   [<span data-ttu-id="a94bf-144">O modelo de buffer de buckets vazados</span><span class="sxs-lookup"><span data-stu-id="a94bf-144">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
-   [<span data-ttu-id="a94bf-145">Trabalhando com codec DMOs</span><span class="sxs-lookup"><span data-stu-id="a94bf-145">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
-   [<span data-ttu-id="a94bf-146">Trabalhando com codec MFTs</span><span class="sxs-lookup"><span data-stu-id="a94bf-146">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
-   [<span data-ttu-id="a94bf-147">Trabalhando com áudio</span><span class="sxs-lookup"><span data-stu-id="a94bf-147">Working with Audio</span></span>](workingwithaudio.md)
-   [<span data-ttu-id="a94bf-148">Trabalhando com vídeo</span><span class="sxs-lookup"><span data-stu-id="a94bf-148">Working with Video</span></span>](workingwithvideo.md)
-   [<span data-ttu-id="a94bf-149">Armazenando mídia compactada em arquivos AVI</span><span class="sxs-lookup"><span data-stu-id="a94bf-149">Storing Compressed Media in AVI Files</span></span>](storingcompressedmediainavifiles.md)
-   [<span data-ttu-id="a94bf-150">Usando a codificação de VBR</span><span class="sxs-lookup"><span data-stu-id="a94bf-150">Using VBR Encoding</span></span>](usingvbrencoding.md)
-   [<span data-ttu-id="a94bf-151">Usando a codificação Two-Pass</span><span class="sxs-lookup"><span data-stu-id="a94bf-151">Using Two-Pass Encoding</span></span>](usingtwoencodingpasses.md)
-   [<span data-ttu-id="a94bf-152">Obtendo estatísticas de codificação</span><span class="sxs-lookup"><span data-stu-id="a94bf-152">Getting Encoding Statistics</span></span>](gettingencodingstatistics.md)
-   [<span data-ttu-id="a94bf-153">Usando extensões de unidade de dados</span><span class="sxs-lookup"><span data-stu-id="a94bf-153">Using Data Unit Extensions</span></span>](usingdataunitextensions.md)
-   [<span data-ttu-id="a94bf-154">Constantes IPropertyBag de codec e DSP</span><span class="sxs-lookup"><span data-stu-id="a94bf-154">Codec and DSP IPropertyBag Constants</span></span>](codecanddspproperties.md)
-   [<span data-ttu-id="a94bf-155">Analisador de Sumário</span><span class="sxs-lookup"><span data-stu-id="a94bf-155">Table of Contents Parser</span></span>](toc-parser.md)
-   [<span data-ttu-id="a94bf-156">Perguntas frequentes sobre o Windows Media Codec</span><span class="sxs-lookup"><span data-stu-id="a94bf-156">Windows Media Codec FAQ</span></span>](frequentlyaskedquestions.md)

## <a name="related-topics"></a><span data-ttu-id="a94bf-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a94bf-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a94bf-158">Guia de programação Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a94bf-158">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

<span data-ttu-id="a94bf-159">[Tecnologias de mídia para Windows](/previous-versions/bg125389(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="a94bf-159">[Media Technologies for Windows](/previous-versions/bg125389(v=msdn.10))</span></span>
</dt> </dl>

 

 
