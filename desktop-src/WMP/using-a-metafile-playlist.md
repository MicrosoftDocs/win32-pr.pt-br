---
title: Usando uma lista de reprodução de metarquivo
description: Usando uma lista de reprodução de metarquivo
ms.assetid: e6cbdb76-4405-409e-93c3-38a3baa7c231
keywords:
- Playlists do metarquivo do Windows Media, usando
- listas de reprodução de metarquivo, usando
- listas de reprodução, usando
- Listas de reprodução do metarquivo do Windows Media, sobre
- listas de reprodução de metarquivo, sobre
- listas de reprodução, sobre
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a5f1832c0c739874fbbd4db219f2c622fc2debfa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635685"
---
# <a name="using-a-metafile-playlist"></a><span data-ttu-id="78e2c-109">Usando uma lista de reprodução de metarquivo</span><span class="sxs-lookup"><span data-stu-id="78e2c-109">Using a Metafile Playlist</span></span>

<span data-ttu-id="78e2c-110">Como não é possível vincular diretamente de uma página da Web a um servidor de mídia de streaming, você usa listas de reprodução de metarquivo.</span><span class="sxs-lookup"><span data-stu-id="78e2c-110">Because you cannot link directly from a webpage to a streaming media server, you use metafile playlists.</span></span> <span data-ttu-id="78e2c-111">As listas de reprodução do metarquivo contêm as informações necessárias para o Windows Media Player e são armazenadas em um servidor Web.</span><span class="sxs-lookup"><span data-stu-id="78e2c-111">The metafile playlists contain the information needed by Windows Media Player and are stored on a web server.</span></span> <span data-ttu-id="78e2c-112">Em seguida, você pode vincular do documento da Web a uma lista de reprodução de metarquivo.</span><span class="sxs-lookup"><span data-stu-id="78e2c-112">You can then link from the Web document to a metafile playlist.</span></span> <span data-ttu-id="78e2c-113">Quando uma lista de reprodução de metarquivo é aberta, o controla as transferências para o Windows Media Player, que processa o arquivo, conecta-se ao servidor de streaming de mídia e reproduz o conteúdo especificado.</span><span class="sxs-lookup"><span data-stu-id="78e2c-113">When a metafile playlist is opened, control transfers to Windows Media Player, which processes the file, connects to the streaming media server, and plays the specified content.</span></span>

<span data-ttu-id="78e2c-114">O navegador primeiro baixa a lista de reprodução do metarquivo para o diretório de cache do usuário.</span><span class="sxs-lookup"><span data-stu-id="78e2c-114">The browser first downloads the metafile playlist to the user's cache directory.</span></span> <span data-ttu-id="78e2c-115">Como a lista de reprodução do metarquivo é pequena, essa é uma etapa muito rápida.</span><span class="sxs-lookup"><span data-stu-id="78e2c-115">Because the metafile playlist is small, this is a very quick step.</span></span> <span data-ttu-id="78e2c-116">Em seguida, o computador do usuário encontra em sua tabela associações de arquivo a associação da lista de reprodução do metarquivo ao Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="78e2c-116">The user's computer then finds in its file associations table the association of the metafile playlist with Windows Media Player.</span></span> <span data-ttu-id="78e2c-117">O Windows Media Player abre e interpreta os scripts na lista de reprodução do metarquivo, que contém, entre outras coisas, a URL do conteúdo de streaming.</span><span class="sxs-lookup"><span data-stu-id="78e2c-117">Windows Media Player opens and interprets the scripting in the metafile playlist, which contains, among other things, the URL of the streaming content.</span></span> <span data-ttu-id="78e2c-118">O Windows Media Player usa a URL para localizar o conteúdo e iniciar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="78e2c-118">Windows Media Player uses the URL to locate the content and initiate the stream.</span></span> <span data-ttu-id="78e2c-119">A lista de reprodução de metarquivos controla a experiência de streaming.</span><span class="sxs-lookup"><span data-stu-id="78e2c-119">The metafile playlist scripting then controls the streaming experience.</span></span>

<span data-ttu-id="78e2c-120">Como as listas de reprodução de metarquivo funcionam por meio de um aplicativo auxiliar associado ao tipo ASXMIME (Application/mplayer2 ou video/x-ms-asf), elas são compatíveis com qualquer navegador que dê suporte a aplicativos auxiliares.</span><span class="sxs-lookup"><span data-stu-id="78e2c-120">Because metafile playlists work through a helper application associated with the ASXMIME type (application/mplayer2 or video/x-ms-asf), they are compatible with any browser that supports helper applications.</span></span> <span data-ttu-id="78e2c-121">Os exemplos mostrados neste documento funcionarão com o Microsoft Internet Explorer 4,0 e posterior e com o Netscape Navigator 4,0 e posterior nas plataformas Microsoft Win32® e Apple Macintosh.</span><span class="sxs-lookup"><span data-stu-id="78e2c-121">The examples shown in this document will work with Microsoft Internet Explorer 4.0 and later, and with Netscape Navigator 4.0 and later on Microsoft Win32® and Apple Macintosh platforms.</span></span> <span data-ttu-id="78e2c-122">Em todos os exemplos, você precisará ter certeza de que todos os arquivos de mídia digital referenciados têm caminhos e nomes de arquivos válidos para o seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="78e2c-122">In all examples, you will have to be sure that any digital media files referenced have valid paths and file names for your environment.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78e2c-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="78e2c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78e2c-124">**Guia de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="78e2c-124">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> <dt>

[<span data-ttu-id="78e2c-125">**Referência do metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="78e2c-125">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> <dt>

[<span data-ttu-id="78e2c-126">**Visão geral dos metaarquivos do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="78e2c-126">**Windows Media Metafiles Overview**</span></span>](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




