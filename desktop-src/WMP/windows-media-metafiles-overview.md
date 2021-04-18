---
title: Visão geral dos metaarquivos do Windows Media
description: Visão geral dos metaarquivos do Windows Media
ms.assetid: 5b7742c0-f416-4bf4-ae03-9554b51fe620
keywords:
- Metaarquivos do Windows Media, sobre
- Windows Media Player, metaarquivos
- Windows Media Player, metaarquivos do Windows Media
- metaarquivos, sobre
- Windows Media, metaarquivos
- Listas de reprodução do metarquivo do Windows Media, sobre
- listas de reprodução, sobre
- Metaarquivos de mídia do Windows, sintaxe
- metaarquivos, sintaxe
- listas de reprodução de metarquivo, sobre
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e7ed86cca023103c044f28141e0212542d83d200
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105771396"
---
# <a name="windows-media-metafiles-overview"></a><span data-ttu-id="1c16a-113">Visão geral dos metaarquivos do Windows Media</span><span class="sxs-lookup"><span data-stu-id="1c16a-113">Windows Media Metafiles Overview</span></span>

<span data-ttu-id="1c16a-114">A parte mais importante do uso bem-sucedido dos metarquivos de mídia do Windows é usar a sintaxe correta para os elementos Metafile.</span><span class="sxs-lookup"><span data-stu-id="1c16a-114">The most important part of successfully using Windows Media metafiles is using the correct syntax for the metafile elements.</span></span> <span data-ttu-id="1c16a-115">Os erros de sintaxe em um metarquivo do Windows Media podem fazer com que algo de um único atributo seja ignorado, para que o metarquivo não seja reconhecido como válido e não funcione.</span><span class="sxs-lookup"><span data-stu-id="1c16a-115">Syntax errors in a Windows Media metafile can cause anything from a single attribute being overlooked, to the metafile not being recognized as valid and failing to work.</span></span>

<span data-ttu-id="1c16a-116">Quase tão importante é a ordem na qual os elementos aparecem em um metarquivo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1c16a-116">Almost as important is the order in which the elements appear in a Windows Media metafile.</span></span> <span data-ttu-id="1c16a-117">Os atributos de alguns elementos substituem temporariamente os atributos de elementos semelhantes em seções diferentes do metarquivo.</span><span class="sxs-lookup"><span data-stu-id="1c16a-117">The attributes of some elements temporarily override the attributes of similar elements in different sections of the metafile.</span></span> <span data-ttu-id="1c16a-118">Há uma [ordem de precedência](order-of-precedence.md)definida.</span><span class="sxs-lookup"><span data-stu-id="1c16a-118">There is a defined [Order of Precedence](order-of-precedence.md).</span></span>

<span data-ttu-id="1c16a-119">As listas de reprodução do Windows Media Metafile são metarquivos do Windows Media que fornecem informações que o Windows Media Player usa para receber fluxos unicast, fluxos multicast e outras mídias com suporte de uma intranet ou da Internet.</span><span class="sxs-lookup"><span data-stu-id="1c16a-119">Windows Media metafile playlists are Windows Media metafiles that provide information that Windows Media Player uses to receive unicast streams, multicast streams, and other supported media from an intranet or the Internet.</span></span> <span data-ttu-id="1c16a-120">Uma lista de reprodução de metarquivo é basicamente um atalho para conteúdo de mídia.</span><span class="sxs-lookup"><span data-stu-id="1c16a-120">A metafile playlist is basically a shortcut to media content.</span></span> <span data-ttu-id="1c16a-121">Uma lista de reprodução de metarquivo pode ser enviada como email, usada como uma referência de link em uma página da Web, criada dinamicamente usando páginas de Active Server (ASP) ou existir como um arquivo autônomo em uma unidade de disco local.</span><span class="sxs-lookup"><span data-stu-id="1c16a-121">A metafile playlist can be sent as email, used as a link reference on a webpage, created dynamically using Active Server Pages (ASP), or exist as a stand-alone file on a local disk drive.</span></span> <span data-ttu-id="1c16a-122">Uma lista de reprodução de metarquivo pode fazer referência a outra lista de reprodução de metarquivo, uma página ASP ou um arquivo de estação de mídia do Windows (com uma extensão de nome de arquivo. NSC).</span><span class="sxs-lookup"><span data-stu-id="1c16a-122">A metafile playlist can reference another metafile playlist, an ASP page, or a Windows Media station file (with an .nsc file name extension).</span></span> <span data-ttu-id="1c16a-123">Um arquivo. NSC é usado para definir uma estação de mídia do Windows para o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="1c16a-123">An .nsc file is used to define a Windows Media station to Windows Media Player.</span></span> <span data-ttu-id="1c16a-124">O processo básico de manipulação é o mesmo para cada caso.</span><span class="sxs-lookup"><span data-stu-id="1c16a-124">The basic handling process is the same for each case.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c16a-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1c16a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c16a-126">**Sobre os metaarquivos de mídia do Windows**</span><span class="sxs-lookup"><span data-stu-id="1c16a-126">**About Windows Media Metafiles**</span></span>](about-windows-media-metafiles.md)
</dt> </dl>

 

 




