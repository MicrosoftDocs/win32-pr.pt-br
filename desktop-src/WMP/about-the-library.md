---
title: Sobre a biblioteca
description: Sobre a biblioteca
ms.assetid: a43c57ac-deb4-4c86-a8a2-bcfd214b9d0a
keywords:
- Windows Media Player, biblioteca
- Modelo de objeto do Windows Media Player, biblioteca
- modelo de objeto, biblioteca
- Controle ActiveX do Windows Media Player, biblioteca para modelo de objeto
- Controle ActiveX, biblioteca para modelo de objeto
- Controle ActiveX móvel do Windows Media Player, biblioteca para modelo de objeto
- Windows Media Player Mobile, biblioteca para modelo de objeto
- Biblioteca do Windows Media Player, sobre
- biblioteca, sobre
- metadados, biblioteca do Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1781329a78bcb2e9cb25c45135e03465b9d63df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105813394"
---
# <a name="about-the-library"></a><span data-ttu-id="388db-113">Sobre a biblioteca</span><span class="sxs-lookup"><span data-stu-id="388db-113">About the Library</span></span>

<span data-ttu-id="388db-114">A biblioteca é um banco de dados de informações, ou *metadados*, sobre o conteúdo de mídia digital disponível para o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="388db-114">The library is a database of information, or *metadata*, about the digital media content that is available to Windows Media Player.</span></span> <span data-ttu-id="388db-115">Algumas das informações são exibidas no painel **biblioteca** no Player; mais informações estão disponíveis por meio de código.</span><span class="sxs-lookup"><span data-stu-id="388db-115">Some of the information is displayed in the **Library** pane in the Player; more of it is available through code.</span></span>

<span data-ttu-id="388db-116">(No Windows Media Player 9 Series e versões anteriores, esse recurso é chamado de **biblioteca de mídia**.)</span><span class="sxs-lookup"><span data-stu-id="388db-116">(In Windows Media Player 9 Series and earlier, this feature is called **Media Library**.)</span></span>

<span data-ttu-id="388db-117">A biblioteca oferece aos usuários uma maneira fácil de organizar e acessar o conteúdo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="388db-117">The library gives users an easy way to organize and access digital media content.</span></span> <span data-ttu-id="388db-118">Por exemplo, os usuários podem exibir músicas organizadas por álbum, por artista, por gênero ou simplesmente como uma lista de todas as músicas.</span><span class="sxs-lookup"><span data-stu-id="388db-118">For example, users can view music organized by album, by artist, by genre, or simply as a list of all music.</span></span> <span data-ttu-id="388db-119">Você pode usar o modelo de objeto do SDK do Windows Media Player para acessar a biblioteca para reproduzir conteúdo, recuperar listas de reprodução, adicionar conteúdo, remover conteúdo e alterar os metadados associados.</span><span class="sxs-lookup"><span data-stu-id="388db-119">You can use the Windows Media Player SDK object model to access the library to play content, retrieve playlists, add content, remove content, and change the associated metadata.</span></span> <span data-ttu-id="388db-120">O Windows Media Player protege a privacidade dos usuários restringindo sua capacidade de acessar a biblioteca a partir do código sob determinadas condições.</span><span class="sxs-lookup"><span data-stu-id="388db-120">Windows Media Player protects users' privacy by restricting your ability to access the library from code under certain conditions.</span></span> <span data-ttu-id="388db-121">Para obter mais informações sobre direitos de acesso, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="388db-121">For more information about access rights, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="388db-122">A biblioteca armazena metadados sobre dois tipos básicos de conteúdo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="388db-122">The library stores metadata about two basic types of digital media content.</span></span> <span data-ttu-id="388db-123">O primeiro tipo, itens de mídia digital, são arquivos de conteúdo individuais, como uma faixa de música ou uma foto.</span><span class="sxs-lookup"><span data-stu-id="388db-123">The first type, digital media items, are individual content files, such as a music track or a photo.</span></span> <span data-ttu-id="388db-124">O segundo tipo, listas de reprodução, são arquivos que representam um grupo de itens de mídia digital, normalmente destinados a serem reproduzidos em uma ordem especificada.</span><span class="sxs-lookup"><span data-stu-id="388db-124">The second type, playlists, are files that represent a group of digital media items, typically intended to be played in a specified order.</span></span> <span data-ttu-id="388db-125">Os metadados associados ao conteúdo de mídia digital são armazenados como pares de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="388db-125">The metadata associated with digital media content is stored as name-value pairs.</span></span> <span data-ttu-id="388db-126">Por exemplo, os metadados que descrevem a pessoa que realizou uma música se chamaram de "artista" e o valor associado a ele normalmente é uma cadeia de caracteres de texto que contém o nome do executor.</span><span class="sxs-lookup"><span data-stu-id="388db-126">For example, the metadata that describes the person who performed a song is named "Artist" and the value associated with it typically is a text string containing the performer's name.</span></span> <span data-ttu-id="388db-127">Cada nome de metadados exclusivo é chamado de *atributo*.</span><span class="sxs-lookup"><span data-stu-id="388db-127">Each unique metadata name is called an *attribute*.</span></span> <span data-ttu-id="388db-128">Para obter uma lista de atributos com suporte, consulte a [referência de atributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="388db-128">For a listing of supported attributes, see the [Attribute Reference](attribute-reference.md).</span></span> <span data-ttu-id="388db-129">Para obter informações sobre como usar atributos no código, consulte [atributos de item de mídia](media-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="388db-129">For information about using attributes in code, see [Media Item Attributes](media-item-attributes.md).</span></span>

<span data-ttu-id="388db-130">As seções a seguir fornecem mais informações sobre como trabalhar com a biblioteca:</span><span class="sxs-lookup"><span data-stu-id="388db-130">The following sections provide more information about working with the library:</span></span>

-   [<span data-ttu-id="388db-131">Acessando a biblioteca programaticamente</span><span class="sxs-lookup"><span data-stu-id="388db-131">Accessing the Library Programmatically</span></span>](accessing-the-library-programmatically.md)
-   [<span data-ttu-id="388db-132">Sobre os serviços de biblioteca</span><span class="sxs-lookup"><span data-stu-id="388db-132">About Library Services</span></span>](about-library-services.md)

## <a name="related-topics"></a><span data-ttu-id="388db-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="388db-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="388db-134">**Sobre o modelo de objeto do Player**</span><span class="sxs-lookup"><span data-stu-id="388db-134">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> </dl>

 

 




