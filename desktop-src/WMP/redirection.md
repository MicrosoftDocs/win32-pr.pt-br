---
title: Redirecionamento
description: Redirecionamento
ms.assetid: c8e3b43f-c11a-4ca7-b85c-038f0bfc3eb3
keywords:
- Listas de reprodução do metarquivo do Windows Media, redirecionamento
- listas de reprodução, redirecionamento
- listas de reprodução de metarquivo, redirecionamento
- Windows Media Player, redirecionamento
- redirecionamento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf1bb4d690c8aa6808e009a45a7bff1d6efada72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291832"
---
# <a name="redirection"></a><span data-ttu-id="6c3d2-108">Redirecionamento</span><span class="sxs-lookup"><span data-stu-id="6c3d2-108">Redirection</span></span>

<span data-ttu-id="6c3d2-109">A lista de reprodução redirecionará o navegador para o Windows Media Player para reproduzir o fluxo de mídia designado ou o arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="6c3d2-109">The playlist will redirect the browser to Windows Media Player to play the designated media stream or media file.</span></span> <span data-ttu-id="6c3d2-110">A lista de reprodução de metarquivo mais básica contém apenas o Uniform Resource Locator (URL) de um arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="6c3d2-110">The most basic metafile playlist contains only the Uniform Resource Locator (URL) of a media file.</span></span>

<span data-ttu-id="6c3d2-111">Para criar uma lista de reprodução de metarquivo básico, abra seu editor de texto favorito, como o bloco de notas da Microsoft e digite o código de exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="6c3d2-111">To create a basic metafile playlist, open your favorite text editor, such as Microsoft Notepad, and type the following example code.</span></span>


```XML
<ASX version="3.0">
   <ENTRY>
      <REF HREF="PathToYourFile"/>
   </ENTRY>
</ASX>

```



<span data-ttu-id="6c3d2-112">Substitua um caminho válido para o arquivo de mídia do Windows usando a sintaxe na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6c3d2-112">Substitute a valid path to your Windows Media file using the syntax in the following table.</span></span>



| <span data-ttu-id="6c3d2-113">Fonte de conteúdo</span><span class="sxs-lookup"><span data-stu-id="6c3d2-113">Source of content</span></span>                                                                                 | <span data-ttu-id="6c3d2-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c3d2-114">Syntax</span></span>                                    |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="6c3d2-115">O conteúdo é um arquivo em um servidor do Windows Media</span><span class="sxs-lookup"><span data-stu-id="6c3d2-115">Content is a file on a Windows Media server</span></span>                                                       | <span data-ttu-id="6c3d2-116">mms://ServerName/Path/FileName.wma</span><span class="sxs-lookup"><span data-stu-id="6c3d2-116">mms://ServerName/Path/FileName.wma</span></span>        |
| <span data-ttu-id="6c3d2-117">O conteúdo é um multicast de difusão que é acessado de uma estação de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="6c3d2-117">Content is a broadcast multicast that is accessed from a Windows Media station</span></span>                    | https://WebServerName/Stations/kxyz.nsc    |
| <span data-ttu-id="6c3d2-118">O conteúdo é uma difusão unicast que é acessada de um ponto de publicação em um Windows Media Server</span><span class="sxs-lookup"><span data-stu-id="6c3d2-118">Content is a broadcast unicast that is accessed from a publishing point on a Windows Media server</span></span> | <span data-ttu-id="6c3d2-119">mms://ServerName/PublishingPointAlias</span><span class="sxs-lookup"><span data-stu-id="6c3d2-119">mms://ServerName/PublishingPointAlias</span></span>     |
| <span data-ttu-id="6c3d2-120">O conteúdo é um arquivo em um servidor Web</span><span class="sxs-lookup"><span data-stu-id="6c3d2-120">Content is a file on a web server</span></span>                                                                 | https://WebServerName/Path/Filename.wma    |
| <span data-ttu-id="6c3d2-121">O conteúdo é um arquivo em um disco rígido local</span><span class="sxs-lookup"><span data-stu-id="6c3d2-121">Content is a file on a local hard disk</span></span>                                                            | <span data-ttu-id="6c3d2-122">file://c: \\ caminho \\ filename. WMA</span><span class="sxs-lookup"><span data-stu-id="6c3d2-122">file://c:\\Path\\Filename.wma</span></span>             |
| <span data-ttu-id="6c3d2-123">O conteúdo é um arquivo em um compartilhamento de rede</span><span class="sxs-lookup"><span data-stu-id="6c3d2-123">Content is a file on a network share</span></span>                                                              | <span data-ttu-id="6c3d2-124">file:// \\ \\ ServerName \\ caminho \\ nome_do_arquivo. WMA</span><span class="sxs-lookup"><span data-stu-id="6c3d2-124">file://\\\\ServerName\\Path\\Filename.wma</span></span> |
| <span data-ttu-id="6c3d2-125">O conteúdo é um arquivo em um servidor do Windows Media</span><span class="sxs-lookup"><span data-stu-id="6c3d2-125">Content is a file on a Windows Media server</span></span>                                                       | <span data-ttu-id="6c3d2-126">mms://ServerName/Path/FileName.wmv</span><span class="sxs-lookup"><span data-stu-id="6c3d2-126">mms://ServerName/Path/FileName.wmv</span></span>        |



 

<span data-ttu-id="6c3d2-127">Salve o arquivo que você criou com um nome de arquivo e extensão, conforme descrito em [extensões de nome de arquivo](file-name-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="6c3d2-127">Save the file you have created with a file name and extension as described in [File Name Extensions](file-name-extensions.md).</span></span> <span data-ttu-id="6c3d2-128">Clique duas vezes no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="6c3d2-128">Double-click it in Windows Explorer.</span></span> <span data-ttu-id="6c3d2-129">O Windows Media Player deve abrir e começar a transmitir o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="6c3d2-129">Windows Media Player should open and start streaming the content.</span></span> <span data-ttu-id="6c3d2-130">Você pode salvar o arquivo em seu servidor Web, juntamente com suas páginas da Web, e vinculá-lo a um elemento **href** ou inseri-lo em uma página da Web usando a marca de **objeto** do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6c3d2-130">You can save the file to your web server, along with your webpages, and link to it with an **HREF** element, or embed it in a webpage using the Windows Media Player **OBJECT** tag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c3d2-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6c3d2-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c3d2-132">**Playlists de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="6c3d2-132">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="6c3d2-133">**Usando listas de reprodução de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="6c3d2-133">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="6c3d2-134">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="6c3d2-134">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="6c3d2-135">**Guia de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="6c3d2-135">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




