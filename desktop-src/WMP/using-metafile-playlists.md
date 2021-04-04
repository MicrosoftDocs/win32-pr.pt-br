---
title: Usando listas de reprodução de metarquivo
description: Usando listas de reprodução de metarquivo
ms.assetid: f5711a7f-7674-4b92-8262-cee8bac4aa77
keywords:
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
ms.openlocfilehash: 71f245d1fc1610174f842347a15dfcfaa13286e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822397"
---
# <a name="using-metafile-playlists"></a><span data-ttu-id="8050f-106">Usando listas de reprodução de metarquivo</span><span class="sxs-lookup"><span data-stu-id="8050f-106">Using Metafile Playlists</span></span>

<span data-ttu-id="8050f-107">As listas de reprodução especificam como a mídia de streaming ou os arquivos de mídia serão reproduzidos e quais metadados serão exibidos no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8050f-107">Playlists specify how the streaming media or media files will be played and what metadata Windows Media Player will display.</span></span>

<span data-ttu-id="8050f-108">Esta seção explica várias maneiras pelas quais você pode usar as listas de reprodução.</span><span class="sxs-lookup"><span data-stu-id="8050f-108">This section explains several ways you can use playlists.</span></span> <span data-ttu-id="8050f-109">A seção é dividida nos tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="8050f-109">The section is divided into the following topics.</span></span>



| <span data-ttu-id="8050f-110">Tópico</span><span class="sxs-lookup"><span data-stu-id="8050f-110">Topic</span></span>                                                                                              | <span data-ttu-id="8050f-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="8050f-111">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8050f-112">Modificando a exibição</span><span class="sxs-lookup"><span data-stu-id="8050f-112">Modifying the Display</span></span>](modifying-the-display.md)                                                 | <span data-ttu-id="8050f-113">Adicionar texto, links e imagens.</span><span class="sxs-lookup"><span data-stu-id="8050f-113">Adding text, links, and images.</span></span>                                                                                                                                |
| [<span data-ttu-id="8050f-114">Redirecionamento</span><span class="sxs-lookup"><span data-stu-id="8050f-114">Redirection</span></span>](redirection.md)                                                                     | <span data-ttu-id="8050f-115">Usar listas de reprodução para redirecionar o navegador para o Windows Media Player e especificar a URL de um fluxo ou arquivo de mídia a ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="8050f-115">Using playlists to redirect the browser to Windows Media Player and specifying the URL of a stream or media file to play.</span></span>                                      |
| [<span data-ttu-id="8050f-116">Acessando mídia</span><span class="sxs-lookup"><span data-stu-id="8050f-116">Accessing Media</span></span>](accessing-media.md)                                                             | <span data-ttu-id="8050f-117">Usar elementos de metarquivo e seus elementos filho para especificar o conteúdo a ser acessado e a ordem e a duração de sua reprodução.</span><span class="sxs-lookup"><span data-stu-id="8050f-117">Using metafile elements and their child elements to specify the content to access, and the order and duration of their playback.</span></span>                               |
| [<span data-ttu-id="8050f-118">Usando a alternância de fluxo de eventos ao vivo</span><span class="sxs-lookup"><span data-stu-id="8050f-118">Using Live Event Stream Switching</span></span>](using-live-event-stream-switching.md)                         | <span data-ttu-id="8050f-119">Usando o elemento **Event** para especificar um fluxo de mídia para acessar e retomar a reprodução do fluxo original.</span><span class="sxs-lookup"><span data-stu-id="8050f-119">Using the **EVENT** element to specify a media stream to access and then resume playing the original stream.</span></span> <span data-ttu-id="8050f-120">Usado para inserção de anúncio.</span><span class="sxs-lookup"><span data-stu-id="8050f-120">Used for ad insertion.</span></span>                            |
| [<span data-ttu-id="8050f-121">Usando os metaarquivos para alternância de fluxo contínuo</span><span class="sxs-lookup"><span data-stu-id="8050f-121">Using Metafiles for Seamless Stream Switching</span></span>](using-metafiles-for-seamless-stream-switching.md) | <span data-ttu-id="8050f-122">Usando o elemento **Event** para pré-carregar o próximo fluxo de mídia a ser acessado para evitar lacunas na apresentação.</span><span class="sxs-lookup"><span data-stu-id="8050f-122">Using the **EVENT** element to preload the next media stream to access to avoid gaps in the presentation.</span></span>                                                      |
| [<span data-ttu-id="8050f-123">Usando anúncios</span><span class="sxs-lookup"><span data-stu-id="8050f-123">Using Announcements</span></span>](using-announcements.md)                                                     | <span data-ttu-id="8050f-124">Usar um metarquivo para fornecer informações sobre a URL para um fluxo de mídia, incluindo o endereço IP de multicast, a porta, o formato de fluxo e outras configurações de estação.</span><span class="sxs-lookup"><span data-stu-id="8050f-124">Using a metafile to provide information about the URL for a media stream, including the multicast IP address, port, stream format, and other station settings.</span></span> |
| [<span data-ttu-id="8050f-125">Usando a substituição de URL e de servidor</span><span class="sxs-lookup"><span data-stu-id="8050f-125">Using URL and Server Rollover</span></span>](using-url-and-server-rollover.md)                                 | <span data-ttu-id="8050f-126">Usar listas de reprodução de metarquivo para fornecer um meio de reverter automaticamente para fontes de conteúdo alternativas quando um fluxo não pode ser acessado ou reproduzido.</span><span class="sxs-lookup"><span data-stu-id="8050f-126">Using metafile playlists to provide a means of automatically rolling over to alternate content sources when a stream cannot be accessed or played.</span></span>             |
| [<span data-ttu-id="8050f-127">Usando parâmetros e comandos personalizados</span><span class="sxs-lookup"><span data-stu-id="8050f-127">Using Custom Parameters and Commands</span></span>](using-custom-parameters-and-commands.md)                   | <span data-ttu-id="8050f-128">Usando o elemento **param** para definir elementos personalizados para fornecer metadados adicionais.</span><span class="sxs-lookup"><span data-stu-id="8050f-128">Using the **PARAM** element to define custom elements to provide additional metadata.</span></span>                                                                          |
| [<span data-ttu-id="8050f-129">Personalizando a entrega de mídia</span><span class="sxs-lookup"><span data-stu-id="8050f-129">Personalizing Media Delivery</span></span>](personalizing-media-delivery.md)                                   | <span data-ttu-id="8050f-130">Usando as preferências do usuário para determinar o conteúdo da transmissão.</span><span class="sxs-lookup"><span data-stu-id="8050f-130">Using user preferences to determine broadcast content.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="8050f-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8050f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8050f-132">**Playlists de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="8050f-132">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="8050f-133">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="8050f-133">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="8050f-134">**Guia de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="8050f-134">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




