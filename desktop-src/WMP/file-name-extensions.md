---
title: Extensões de nome de arquivo
description: Extensões de nome de arquivo
ms.assetid: c17bf4e5-b469-45b6-bc22-2b451723d85e
keywords:
- Metaarquivos do Windows Media, extensões
- Metaarquivos do Windows Media, extensões de nome de arquivo
- metaarquivos, extensões
- metaarquivos, extensões de nome de arquivo
- Windows Media, metaarquivos
- extensões de nome de arquivo para os metaarquivos do Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d95d5bcba9bbad5f04b0d085ba712d5b9306c8b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105811100"
---
# <a name="file-name-extensions"></a><span data-ttu-id="13316-109">Extensões de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="13316-109">File Name Extensions</span></span>

<span data-ttu-id="13316-110">Há diretrizes específicas para o uso de extensões de nome de arquivo para os metaarquivos do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="13316-110">There are specific guidelines for the use of file name extensions for Windows Media metafiles.</span></span> <span data-ttu-id="13316-111">As extensões de nome de metarquivo do Windows Media são usadas para identificar os diferentes tipos de arquivos de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="13316-111">Windows Media metafile name extensions are used to identify the different types of Windows Media files.</span></span> <span data-ttu-id="13316-112">Uma extensão de nome de arquivo fornece um fornecedor de software independente (ISV) com informações sobre os requisitos de renderização de um aplicativo que usa uma extensão específica e permite que os autores de conteúdo direcionem tipos gerais de players de mídia.</span><span class="sxs-lookup"><span data-stu-id="13316-112">A file name extension provides an Independent Software Vendor (ISV) with information about the rendering requirements of an application that uses a particular extension, and enables content authors to target general types of media players.</span></span>

<span data-ttu-id="13316-113">As diretrizes de extensão de nome de arquivo são listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="13316-113">The file name extension guidelines are listed in the following table.</span></span> <span data-ttu-id="13316-114">É recomendável que o tipo MIME de um arquivo, localizado no cabeçalho do arquivo, seja usado para a identificação do tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="13316-114">It is recommended that a file's MIME type, located in the file header, be used for file-type identification.</span></span>



| <span data-ttu-id="13316-115">Extensão de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="13316-115">File name extension</span></span> | <span data-ttu-id="13316-116">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="13316-116">MIME type</span></span>      | <span data-ttu-id="13316-117">Conteúdo do arquivo</span><span class="sxs-lookup"><span data-stu-id="13316-117">File content</span></span>                                                                                                                                                                            |
|---------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13316-118">.wma</span><span class="sxs-lookup"><span data-stu-id="13316-118">.wma</span></span>                | <span data-ttu-id="13316-119">áudio/x-MS-WMA</span><span class="sxs-lookup"><span data-stu-id="13316-119">audio/x-ms-wma</span></span> | <span data-ttu-id="13316-120">Arquivo de mídia do Windows com conteúdo de áudio apenas.</span><span class="sxs-lookup"><span data-stu-id="13316-120">Windows Media file with audio content only.</span></span> <span data-ttu-id="13316-121">Normalmente usado para baixar e reproduzir arquivos ou transmitir conteúdo.</span><span class="sxs-lookup"><span data-stu-id="13316-121">Typically used to download and play files or to stream content.</span></span>                                                                             |
| <span data-ttu-id="13316-122">.wmv</span><span class="sxs-lookup"><span data-stu-id="13316-122">.wmv</span></span>                | <span data-ttu-id="13316-123">vídeo/x-MS-WMV</span><span class="sxs-lookup"><span data-stu-id="13316-123">video/x-ms-wmv</span></span> | <span data-ttu-id="13316-124">Arquivo de mídia do Windows com conteúdo de áudio e/ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="13316-124">Windows Media file with audio and/or video content.</span></span> <span data-ttu-id="13316-125">Normalmente usado para baixar e reproduzir arquivos ou transmitir conteúdo.</span><span class="sxs-lookup"><span data-stu-id="13316-125">Typically used to download and play files or to stream content.</span></span>                                                                     |
| <span data-ttu-id="13316-126">.asf</span><span class="sxs-lookup"><span data-stu-id="13316-126">.asf</span></span>                | <span data-ttu-id="13316-127">vídeo/x-ms-asf</span><span class="sxs-lookup"><span data-stu-id="13316-127">video/x-ms-asf</span></span> | <span data-ttu-id="13316-128">Conteúdo herdado.</span><span class="sxs-lookup"><span data-stu-id="13316-128">Legacy content.</span></span> <span data-ttu-id="13316-129">Normalmente usado para baixar e reproduzir arquivos ou transmitir conteúdo.</span><span class="sxs-lookup"><span data-stu-id="13316-129">Typically used to download and play files or to stream content.</span></span> <span data-ttu-id="13316-130">Pode conter conteúdo de áudio e/ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="13316-130">May contain audio and/or video content.</span></span> <span data-ttu-id="13316-131">Normalmente usado para baixar e reproduzir arquivos ou transmitir conteúdo.</span><span class="sxs-lookup"><span data-stu-id="13316-131">Typically used to download and play files or to stream content.</span></span> |
| <span data-ttu-id="13316-132">.wm</span><span class="sxs-lookup"><span data-stu-id="13316-132">.wm</span></span>                 | <span data-ttu-id="13316-133">vídeo/x-MS-WM</span><span class="sxs-lookup"><span data-stu-id="13316-133">video/x-ms-wm</span></span>  | <span data-ttu-id="13316-134">Reservado</span><span class="sxs-lookup"><span data-stu-id="13316-134">Reserved</span></span>                                                                                                                                                                                |
| <span data-ttu-id="13316-135">. Wax</span><span class="sxs-lookup"><span data-stu-id="13316-135">.wax</span></span>                | <span data-ttu-id="13316-136">áudio/x-MS-Wax</span><span class="sxs-lookup"><span data-stu-id="13316-136">audio/x-ms-wax</span></span> | <span data-ttu-id="13316-137">Os metaarquivos que fazem referência a arquivos de mídia do Windows com extensões de nome de arquivo. ASF,. WMA ou. Wax.</span><span class="sxs-lookup"><span data-stu-id="13316-137">Metafiles that reference Windows Media files with .asf, .wma, or .wax file name extensions.</span></span>                                                                                             |
| <span data-ttu-id="13316-138">.wvx</span><span class="sxs-lookup"><span data-stu-id="13316-138">.wvx</span></span>                | <span data-ttu-id="13316-139">vídeo/x-MS-wvx</span><span class="sxs-lookup"><span data-stu-id="13316-139">video/x-ms-wvx</span></span> | <span data-ttu-id="13316-140">Os metaarquivos que fazem referência a arquivos de mídia do Windows com extensões de nome de arquivo. WMA,. wmv,. wvx ou. Wax.</span><span class="sxs-lookup"><span data-stu-id="13316-140">Metafiles that reference Windows Media files with .wma, .wmv, .wvx, or .wax file name extensions.</span></span>                                                                                       |
| <span data-ttu-id="13316-141">.asx</span><span class="sxs-lookup"><span data-stu-id="13316-141">.asx</span></span>                | <span data-ttu-id="13316-142">vídeo/x-ms-asf</span><span class="sxs-lookup"><span data-stu-id="13316-142">video/x-ms-asf</span></span> | <span data-ttu-id="13316-143">Os metaarquivos que fazem referência a arquivos de mídia do Windows com extensões de nome de arquivo. WMA,. Wax,. wmv,. WVX,. ASF ou. asx.</span><span class="sxs-lookup"><span data-stu-id="13316-143">Metafiles that reference Windows Media files with .wma, .wax, .wmv, .wvx, .asf, or .asx file name extensions.</span></span>                                                                           |
| <span data-ttu-id="13316-144">. WMX</span><span class="sxs-lookup"><span data-stu-id="13316-144">.wmx</span></span>                | <span data-ttu-id="13316-145">vídeo/x-MS-wvx</span><span class="sxs-lookup"><span data-stu-id="13316-145">video/x-ms-wvx</span></span> | <span data-ttu-id="13316-146">Reservado.</span><span class="sxs-lookup"><span data-stu-id="13316-146">Reserved.</span></span>                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="13316-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="13316-147">Remarks</span></span>

<span data-ttu-id="13316-148">O script e o DRM (gerenciamento de direitos digitais) devem ser suportados por qualquer aplicativo que processe arquivos de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="13316-148">Scripting and digital rights management (DRM) must be supported by any application that renders Windows Media files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13316-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="13316-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13316-150">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="13316-150">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="13316-151">**Guia de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="13316-151">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> <dt>

[<span data-ttu-id="13316-152">**Referência do metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="13316-152">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 




