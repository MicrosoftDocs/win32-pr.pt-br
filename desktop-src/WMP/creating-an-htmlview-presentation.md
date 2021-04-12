---
title: Criando uma apresentação do HTMLView
description: Criando uma apresentação do HTMLView
ms.assetid: 70203160-2dd9-4096-be6a-c704db757f7f
keywords:
- Playlists do metarquivo do Windows Media, apresentações do HTMLView
- listas de reprodução, apresentações HTMLViews
- listas de reprodução de metarquivo, apresentações HTMLView
- Playlists do metarquivo do Windows Media, criando apresentações do HTMLView
- listas de reprodução, criando apresentações do HTMLView
- listas de reprodução de metarquivo, criando apresentações do HTMLView
- Criando apresentações do HTMLView
- Windows Media Player, criando apresentações do HTMLView
- Windows Media Player, apresentações do HTMLView
- HTMLView, criando apresentações
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1094ce787e55fbeb98e628389b5fd51ab94ab415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364155"
---
# <a name="creating-an-htmlview-presentation"></a><span data-ttu-id="09186-113">Criando uma apresentação do HTMLView</span><span class="sxs-lookup"><span data-stu-id="09186-113">Creating an HTMLView Presentation</span></span>

<span data-ttu-id="09186-114">Para criar uma apresentação HTMLView básica, você precisa de pelo menos três elementos:</span><span class="sxs-lookup"><span data-stu-id="09186-114">To create a basic HTMLView presentation, you need at least three elements:</span></span>

-   <span data-ttu-id="09186-115">**Conteúdo de mídia digital.**</span><span class="sxs-lookup"><span data-stu-id="09186-115">**Digital media content.**</span></span> <span data-ttu-id="09186-116">Este é um ou mais arquivos de áudio ou vídeo que o Windows Media Player reproduz.</span><span class="sxs-lookup"><span data-stu-id="09186-116">This is one or more audio or video files that Windows Media Player plays.</span></span>
-   <span data-ttu-id="09186-117">**Uma página da Web.**</span><span class="sxs-lookup"><span data-stu-id="09186-117">**A webpage.**</span></span> <span data-ttu-id="09186-118">Esse é o conteúdo baseado na Web que é exibido no recurso de **agora em execução** da interface do usuário do Player.</span><span class="sxs-lookup"><span data-stu-id="09186-118">This is the Web-based content that displays in the **Now Playing** feature of the Player UI.</span></span>
-   <span data-ttu-id="09186-119">**Um metarquivo do Windows Media.**</span><span class="sxs-lookup"><span data-stu-id="09186-119">**A Windows Media metafile.**</span></span> <span data-ttu-id="09186-120">Esta é a lista de reprodução de metarquivo que direciona o Windows Media Player para combinar o conteúdo de mídia digital com a página da Web.</span><span class="sxs-lookup"><span data-stu-id="09186-120">This is the metafile playlist that directs Windows Media Player to combine the digital media content with the webpage.</span></span>

<span data-ttu-id="09186-121">Um arquivo. asx é um arquivo de texto que fornece informações sobre um fluxo de arquivos e sua apresentação.</span><span class="sxs-lookup"><span data-stu-id="09186-121">An .asx file is a text file that provides information about a file stream and its presentation.</span></span> <span data-ttu-id="09186-122">Com base na sintaxe de linguagem XML (XML), os arquivos. asx podem conter uma variedade de elementos, cada um identificado por uma marca com atributos associados.</span><span class="sxs-lookup"><span data-stu-id="09186-122">Based on Extensible Markup Language (XML) syntax, .asx files can contain a variety of elements, each identified by a tag with associated attributes.</span></span> <span data-ttu-id="09186-123">O elemento **param** fornece uma maneira de associar um parâmetro personalizado a uma entrada específica em uma lista de reprodução de metarquivo ou a todo o metarquivo.</span><span class="sxs-lookup"><span data-stu-id="09186-123">The **PARAM** element provides a way to associate a custom parameter with either a particular entry in a metafile playlist or the entire metafile.</span></span> <span data-ttu-id="09186-124">Um dos nomes de parâmetro predefinidos disponíveis para seu uso é "HTMLView".</span><span class="sxs-lookup"><span data-stu-id="09186-124">One of the predefined parameter names available for your use is "HTMLView".</span></span> <span data-ttu-id="09186-125">Esse é o parâmetro que faz com que a página da Web especificada pelo valor da URL seja exibida no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="09186-125">This is the parameter that causes the webpage specified by the URL value to be displayed in Windows Media Player.</span></span>

<span data-ttu-id="09186-126">O código de exemplo a seguir mostra um arquivo. asx que combina um único arquivo de mídia digital com uma única página da Web:</span><span class="sxs-lookup"><span data-stu-id="09186-126">The following example code shows an .asx file that combines a single digital media file with a single webpage:</span></span>


```XML
<ASX version="3.0">
<PARAM name="HTMLView" value="https://www.proseware.com/htmlview.htm"/>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



<span data-ttu-id="09186-127">Quando o Windows Media Player abre o arquivo. ASX no exemplo anterior, ele reproduz o áudio do arquivo chamado content1. WMA e abre a página da Web chamada htmlview.htm no recurso de **agora em execução** do player de modo completo.</span><span class="sxs-lookup"><span data-stu-id="09186-127">When Windows Media Player opens the .asx file in the preceding example, it plays the audio from the file named content1.wma and opens the webpage named htmlview.htm in the **Now Playing** feature of the full-mode Player.</span></span> <span data-ttu-id="09186-128">O usuário pode pausar, buscar e parar o conteúdo de áudio usando os controles do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="09186-128">The user can pause, seek, and stop the audio content using the Windows Media Player controls.</span></span>

<span data-ttu-id="09186-129">Você pode alterar facilmente a página da Web que é exibida para cada parte do conteúdo associando um elemento **param** a cada entrada, como mostra o exemplo de código a seguir:</span><span class="sxs-lookup"><span data-stu-id="09186-129">You can easily change the webpage that is displayed for each piece of content by associating a **PARAM** element with each entry, as the following code example shows:</span></span>


```XML
<ASX version="3.0">

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview2.htm"/>
   <REF href="rtsp://www.proseware.com/content2.wma"/>
</ENTRY>

</ASX>

```



<span data-ttu-id="09186-130">No exemplo anterior, o Windows Media Player primeiro exibe a página da Web htmlview1.htm ao reproduzir o arquivo de áudio digital content1. WMA.</span><span class="sxs-lookup"><span data-stu-id="09186-130">In the preceding example, Windows Media Player first displays the webpage htmlview1.htm while playing the digital audio file content1.wma.</span></span> <span data-ttu-id="09186-131">Quando o Player abre a próxima entrada na lista de reprodução, content2. WMA, a página da Web exibida em **agora executa** alterações no htmlview2.htm.</span><span class="sxs-lookup"><span data-stu-id="09186-131">When the Player opens the next entry in the playlist, content2.wma, the webpage displayed in **Now Playing** changes to htmlview2.htm.</span></span> <span data-ttu-id="09186-132">Dessa forma, você pode especificar qual página da Web o usuário vê para cada parte do conteúdo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="09186-132">In this way, you can specify which webpage the user sees for each piece of digital media content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09186-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="09186-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09186-134">**Exibindo páginas da Web no Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="09186-134">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="09186-135">**Elemento PARAM**</span><span class="sxs-lookup"><span data-stu-id="09186-135">**PARAM Element**</span></span>](param-element.md)
</dt> </dl>

 

 




