---
title: Usando listas de reprodução em pacotes de download do Windows Media (preterido)
description: Usando listas de reprodução em pacotes de download do Windows Media (preterido)
ms.assetid: c40efe24-aaed-47fc-8a8a-f412dfc36af7
keywords:
- Metaarquivos do Windows Media, pacotes de download do Windows Media
- Windows Media Player, pacotes de download do Windows Media
- metaarquivos, pacotes de download do Windows Media
- Windows Media, pacotes de download do Windows Media
- listas de reprodução, pacotes de download do Windows Media
- listas de reprodução de metarquivo, pacotes de download do Windows Media
- Listas de reprodução do metarquivo do Windows Media, pacotes de download do Windows Media
- Pacotes de download do Windows Media, playlists
- Pacotes de download do Windows Media, listas de reprodução do metarquivo
- Pacotes de download do Windows Media, playlists do metarquivo do Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00c4daa26d18294c00aad7b4926a017d2f3f6343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364258"
---
# <a name="using-playlists-in-windows-media-download-packages-deprecated"></a><span data-ttu-id="15356-113">Usando listas de reprodução em pacotes de download do Windows Media (preterido)</span><span class="sxs-lookup"><span data-stu-id="15356-113">Using Playlists in Windows Media Download Packages (deprecated)</span></span>

<span data-ttu-id="15356-114">Esta página documenta um recurso que pode não estar disponível em versões futuras do Windows Media Player e no SDK do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="15356-114">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="15356-115">As listas de reprodução são arquivos de mídia do Windows com uma extensão de nome de arquivo. asx que fornece informações que dizem ao Windows Media Player como reproduzir o conteúdo empacotado.</span><span class="sxs-lookup"><span data-stu-id="15356-115">Playlists are Windows Media metafiles with an .asx file name extension that provide information that tells Windows Media Player how to play the packaged content.</span></span> <span data-ttu-id="15356-116">Ao combinar vários arquivos de conteúdo em um único pacote de download do Windows Media, você pode controlar e personalizar o pacote de download do Windows Media usando a lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="15356-116">By combining multiple content files into a single Windows Media Download package, you can control and customize your Windows Media Download package by using the playlist.</span></span>

> [!Note]  
> <span data-ttu-id="15356-117">Em geral, as listas de reprodução de metarquivo são usadas pelos pacotes de download de mídia do Windows para fazer referência ao conteúdo de multimídia no pacote, em vez de um fluxo de um servidor em uma intranet ou na Internet.</span><span class="sxs-lookup"><span data-stu-id="15356-117">In general, metafile playlists are used by Windows Media Download packages to reference the multimedia content in the package rather than a stream from a server on an intranet or the Internet.</span></span> <span data-ttu-id="15356-118">No entanto, há suporte para referências de URL dentro do arquivo. asx.</span><span class="sxs-lookup"><span data-stu-id="15356-118">However, URL references within the .asx file are supported.</span></span>

 

<span data-ttu-id="15356-119">Usando XML, o metarquivo fornece as informações que o Windows Media Player usa para reproduzir e exibir conteúdo.</span><span class="sxs-lookup"><span data-stu-id="15356-119">Using XML, the metafile provides the information Windows Media Player uses to play and display content.</span></span> <span data-ttu-id="15356-120">As listas de reprodução são constituídas de vários elementos de código XML com suas marcas e atributos associados.</span><span class="sxs-lookup"><span data-stu-id="15356-120">Playlists are made up of various XML code elements with their associated tags and attributes.</span></span> <span data-ttu-id="15356-121">Cada elemento em uma lista de reprodução do metarquivo do Windows Media define uma configuração ou ação específica no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="15356-121">Each element in a Windows Media metafile playlist defines a particular setting or action in Windows Media Player.</span></span>

<span data-ttu-id="15356-122">O computador do usuário associa um metarquivo do Windows Media que tem uma extensão de nome de arquivo. asx com o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="15356-122">The user's computer associates a Windows Media metafile that has an .asx file name extension with Windows Media Player.</span></span> <span data-ttu-id="15356-123">O Windows Media Player abre e analisa o código XML no metarquivo, que contém o caminho para localizar os arquivos de áudio ou vídeo empacotados.</span><span class="sxs-lookup"><span data-stu-id="15356-123">Windows Media Player opens and parses the XML code in the metafile, which contains the path for locating the packaged audio or video files.</span></span> <span data-ttu-id="15356-124">Em seguida, o script de metarquivo controla a experiência gráfica, de vídeo e de áudio.</span><span class="sxs-lookup"><span data-stu-id="15356-124">The metafile script then controls the audio, video, and graphical experience.</span></span> <span data-ttu-id="15356-125">O metarquivo também contém informações que o Windows Media Player processa e exibe na caixa suspensa playlist.</span><span class="sxs-lookup"><span data-stu-id="15356-125">The metafile also contains information that Windows Media Player processes and displays in the playlist drop-down box.</span></span> <span data-ttu-id="15356-126">Imediatamente após a lista ser exibida, o primeiro item da lista é reproduzido.</span><span class="sxs-lookup"><span data-stu-id="15356-126">Immediately after the list is displayed, the first item in the list is played.</span></span>

<span data-ttu-id="15356-127">Uma playlist de metarquivo é um atalho para os arquivos que contêm o conteúdo do pacote.</span><span class="sxs-lookup"><span data-stu-id="15356-127">A metafile playlist is a shortcut to the files that contain your packaged content.</span></span> <span data-ttu-id="15356-128">O código a seguir é um exemplo de um metarquivo que especifica a borda a ser exibida usando o elemento **Skin** , duas músicas a serem reproduzidas e as informações da playlist para cada música.</span><span class="sxs-lookup"><span data-stu-id="15356-128">The following code is an example of a metafile that specifies the border to display by using the **SKIN** element, two songs to be played, and the playlist information for each song.</span></span>


```XML
<ASX Version="3.0">
<AUTHOR>Name of content creator goes here</AUTHOR>
<TITLE>Album Title goes here</TITLE>
<PARAM name="Album" value="Album Title "/>
<PARAM name="Artist" value="Artist Name"/>
<PARAM name="Genre" value="Genre"/>
<SKIN HREF="myborder.wmz"/>
    <ENTRY>
        <REF HREF="song1.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #1 title</TITLE>
    </ENTRY>
    <ENTRY>
        <REF HREF="song2.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #2 name</TITLE>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="15356-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="15356-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15356-130">**Bordas do Windows Media Player (preterido)**</span><span class="sxs-lookup"><span data-stu-id="15356-130">**Borders for Windows Media Player (deprecated)**</span></span>](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[<span data-ttu-id="15356-131">**Pacotes de download do Windows Media (preterido)**</span><span class="sxs-lookup"><span data-stu-id="15356-131">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> <dt>

[<span data-ttu-id="15356-132">**Metaarquivos do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="15356-132">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 




