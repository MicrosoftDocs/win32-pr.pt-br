---
title: Diretrizes de extensão de metarquivo
description: Diretrizes de extensão de metarquivo
ms.assetid: 079fac31-7a6f-4775-a337-870ad25a56a0
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
ms.openlocfilehash: 31d2793b19576e26096bc30c834666828cf9ed29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006092"
---
# <a name="metafile-extension-guidelines"></a><span data-ttu-id="273a2-109">Diretrizes de extensão de metarquivo</span><span class="sxs-lookup"><span data-stu-id="273a2-109">Metafile Extension Guidelines</span></span>

<span data-ttu-id="273a2-110">Uma extensão de nome de arquivo fornece um fornecedor de software independente (ISV) com informações sobre os requisitos de renderização de um aplicativo que usa a extensão e permite que os autores de conteúdo direcionem tipos gerais de players.</span><span class="sxs-lookup"><span data-stu-id="273a2-110">A file name extension provides an independent software vendor (ISV) with information about the rendering requirements of an application that uses the extension, and enables content authors to target general types of players.</span></span>

<span data-ttu-id="273a2-111">Extensões de nome de metarquivo do Windows Media são usadas para identificar o formato dos arquivos de mídia do Windows que um metarquivo faz referência.</span><span class="sxs-lookup"><span data-stu-id="273a2-111">Windows Media metafile name extensions are used to identify the format of the Windows Media files that a metafile references.</span></span> <span data-ttu-id="273a2-112">Os metaarquivos do Windows Media com extensões. Wax,. wvx ou. asx fazem referência a arquivos com as extensões. WMA,. wmv e. ASF, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="273a2-112">Windows Media metafiles with .wax, .wvx, or .asx extensions reference files with .wma, .wmv, and .asf extensions, respectively.</span></span> <span data-ttu-id="273a2-113">Todos os metaarquivos, independentemente da extensão de nome de arquivo usada, têm a marca de elemento **ASX** no início do arquivo com o atributo **version** especificado.</span><span class="sxs-lookup"><span data-stu-id="273a2-113">All metafiles, regardless of the file name extension used, have the **ASX** element tag at the beginning of the file with the **version** attribute specified.</span></span>

<span data-ttu-id="273a2-114">A tabela a seguir mostra os tipos de arquivo de mídia referenciados por cada tipo de extensão de nome de arquivo de metarquivo.</span><span class="sxs-lookup"><span data-stu-id="273a2-114">The following table shows the media file types referenced by each type of metafile file name extension.</span></span> <span data-ttu-id="273a2-115">As colunas listam extensões de nome de arquivo de mídia, as linhas listam extensões de nome de metarquivo.</span><span class="sxs-lookup"><span data-stu-id="273a2-115">The columns list media file name extensions, the rows list metafile name extensions.</span></span> <span data-ttu-id="273a2-116">Um X em uma coluna indica um tipo de arquivo de mídia que pode ser referenciado por uma extensão de nome de arquivo de metarquivo específica.</span><span class="sxs-lookup"><span data-stu-id="273a2-116">An X in a column indicates a media file type that can be referenced by a particular metafile file name extension.</span></span>



| <span data-ttu-id="273a2-117">Extensão</span><span class="sxs-lookup"><span data-stu-id="273a2-117">Extension</span></span> | <span data-ttu-id="273a2-118">.asf</span><span class="sxs-lookup"><span data-stu-id="273a2-118">.asf</span></span> | <span data-ttu-id="273a2-119">.wma</span><span class="sxs-lookup"><span data-stu-id="273a2-119">.wma</span></span> | <span data-ttu-id="273a2-120">.wmv</span><span class="sxs-lookup"><span data-stu-id="273a2-120">.wmv</span></span> |
|-----------|------|------|------|
| <span data-ttu-id="273a2-121">.wvx</span><span class="sxs-lookup"><span data-stu-id="273a2-121">.wvx</span></span>      | <span data-ttu-id="273a2-122">X</span><span class="sxs-lookup"><span data-stu-id="273a2-122">X</span></span>    | <span data-ttu-id="273a2-123">X</span><span class="sxs-lookup"><span data-stu-id="273a2-123">X</span></span>    | <span data-ttu-id="273a2-124">X</span><span class="sxs-lookup"><span data-stu-id="273a2-124">X</span></span>    |
| <span data-ttu-id="273a2-125">. Wax</span><span class="sxs-lookup"><span data-stu-id="273a2-125">.wax</span></span>      | <span data-ttu-id="273a2-126">X</span><span class="sxs-lookup"><span data-stu-id="273a2-126">X</span></span>    | <span data-ttu-id="273a2-127">X</span><span class="sxs-lookup"><span data-stu-id="273a2-127">X</span></span>    |      |
| <span data-ttu-id="273a2-128">.asx</span><span class="sxs-lookup"><span data-stu-id="273a2-128">.asx</span></span>      | <span data-ttu-id="273a2-129">X</span><span class="sxs-lookup"><span data-stu-id="273a2-129">X</span></span>    |      |      |



 

## <a name="related-topics"></a><span data-ttu-id="273a2-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="273a2-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="273a2-131">**Extensões de nome de arquivo**</span><span class="sxs-lookup"><span data-stu-id="273a2-131">**File Name Extensions**</span></span>](file-name-extensions.md)
</dt> <dt>

[<span data-ttu-id="273a2-132">**Playlists de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="273a2-132">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="273a2-133">**Guia de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="273a2-133">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




