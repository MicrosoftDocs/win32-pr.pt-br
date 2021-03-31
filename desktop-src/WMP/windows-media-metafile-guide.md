---
title: Guia de metarquivo do Windows Media
description: Guia de metarquivo do Windows Media
ms.assetid: d2360a63-f073-44b0-8637-1f22b577f51a
keywords:
- Metaarquivos do Windows Media, sobre
- Windows Media Player, metaarquivos
- Windows Media Player, metaarquivos do Windows Media
- metaarquivos, sobre
- Windows Media, metaarquivos
- Listas de reprodução do metarquivo do Windows Media, sobre
- listas de reprodução, sobre
- listas de reprodução de metarquivo, sobre
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fcf0a4c98ae49d1cdf3b7e36e8a278f184cd4632
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916582"
---
# <a name="windows-media-metafile-guide"></a><span data-ttu-id="dd1c0-111">Guia de metarquivo do Windows Media</span><span class="sxs-lookup"><span data-stu-id="dd1c0-111">Windows Media Metafile Guide</span></span>

<span data-ttu-id="dd1c0-112">Um metarquivo do Windows Media pode ser simples ou complexo, pois você precisa que ele seja.</span><span class="sxs-lookup"><span data-stu-id="dd1c0-112">A Windows Media metafile can be as simple or complex as you need it to be.</span></span> <span data-ttu-id="dd1c0-113">O metarquivo do Windows Media mais básico contém apenas o Uniform Resource Locator (URL) de algum conteúdo multimídia em um servidor.</span><span class="sxs-lookup"><span data-stu-id="dd1c0-113">The most basic Windows Media metafile contains only the Uniform Resource Locator (URL) of some multimedia content on a server.</span></span> <span data-ttu-id="dd1c0-114">O cliente do, o Windows Media Player, analisa essas informações e, em seguida, abre o arquivo de mídia ou o fluxo definido no metarquivo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dd1c0-114">The client, Windows Media Player, parses this information and then opens the media file or stream defined in the Windows Media metafile.</span></span> <span data-ttu-id="dd1c0-115">Um metarquivo complexo pode conter vários arquivos ou fluxos organizados em uma lista de reprodução, instruções sobre como reproduzir os arquivos ou fluxos, elementos de texto e gráficos, como título, autor e texto de direitos autorais, inserção personalizada de anúncios em uma transmissão ao vivo, hiperlinks associados a elementos na interface do Windows Media Player e muito mais.</span><span class="sxs-lookup"><span data-stu-id="dd1c0-115">A complex metafile can contain multiple files or streams arranged in a playlist, instructions on how to play the files or streams, text and graphic elements such as title, author, and copyright text, personalized ad insertion into a live stream, hyperlinks associated with elements on the Windows Media Player interface, and more.</span></span>

<span data-ttu-id="dd1c0-116">As seções a seguir fornecem informações detalhadas sobre como criar e usar listas de reprodução do metarquivo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dd1c0-116">The following sections provide detailed information on how to create and use Windows Media metafile playlists.</span></span>



| <span data-ttu-id="dd1c0-117">Seção</span><span class="sxs-lookup"><span data-stu-id="dd1c0-117">Section</span></span>                                                            | <span data-ttu-id="dd1c0-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="dd1c0-118">Description</span></span>                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd1c0-119">Tipos de listas de reprodução</span><span class="sxs-lookup"><span data-stu-id="dd1c0-119">Types of Playlists</span></span>](types-of-playlists.md)                       | <span data-ttu-id="dd1c0-120">Lista as extensões de nome de arquivo disponíveis.</span><span class="sxs-lookup"><span data-stu-id="dd1c0-120">Lists available file name extensions.</span></span>                                               |
| [<span data-ttu-id="dd1c0-121">Criando listas de reprodução de metarquivo</span><span class="sxs-lookup"><span data-stu-id="dd1c0-121">Creating Metafile Playlists</span></span>](creating-metafile-playlists.md)     | <span data-ttu-id="dd1c0-122">Descreve como criar listas de reprodução do metarquivo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dd1c0-122">Describes how to create Windows Media metafile playlists.</span></span>                           |
| [<span data-ttu-id="dd1c0-123">Playlists de metarquivo</span><span class="sxs-lookup"><span data-stu-id="dd1c0-123">Metafile Playlists</span></span>](metafile-playlists.md)                       | <span data-ttu-id="dd1c0-124">Descreve o uso, o script, os metadados e o processamento da lista de reprodução do metarquivo.</span><span class="sxs-lookup"><span data-stu-id="dd1c0-124">Describes metafile playlist usage, scripting, metadata, and processing.</span></span>             |
| [<span data-ttu-id="dd1c0-125">Diretrizes de extensão de metarquivo</span><span class="sxs-lookup"><span data-stu-id="dd1c0-125">Metafile Extension Guidelines</span></span>](metafile-extension-guidelines.md) | <span data-ttu-id="dd1c0-126">Descreve o uso preferencial de extensões de nome de arquivo para streaming de arquivos de mídia.</span><span class="sxs-lookup"><span data-stu-id="dd1c0-126">Describes the preferred use of file name extensions for streaming media files.</span></span>      |
| [<span data-ttu-id="dd1c0-127">Ordem de Precedência</span><span class="sxs-lookup"><span data-stu-id="dd1c0-127">Order of Precedence</span></span>](order-of-precedence.md)                     | <span data-ttu-id="dd1c0-128">Descreve como os elementos de playlist do metarquivo substituem outros elementos da lista de reprodução do metarquivo.</span><span class="sxs-lookup"><span data-stu-id="dd1c0-128">Describes how metafile playlist elements override other metafile playlist elements.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="dd1c0-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dd1c0-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd1c0-130">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="dd1c0-130">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="dd1c0-131">**Metaarquivos do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="dd1c0-131">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 




