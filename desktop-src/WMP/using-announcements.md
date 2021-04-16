---
title: Usando anúncios
description: Usando anúncios
ms.assetid: c372a4f8-2355-4c69-bba2-72b224879c4d
keywords:
- Listas de reprodução do metarquivo do Windows Media, anúncios
- listas de reprodução, anúncios
- listas de reprodução de metarquivo, anúncios
- Windows Media Player, anúncios
- comunicados
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c16fafee1984d08992b96c39d7c3893ea54f682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105765627"
---
# <a name="using-announcements"></a><span data-ttu-id="54267-108">Usando anúncios</span><span class="sxs-lookup"><span data-stu-id="54267-108">Using Announcements</span></span>

<span data-ttu-id="54267-109">Um comunicado é um arquivo que contém informações sobre a URL para um fluxo de mídia, incluindo o endereço IP de multicast, a porta, o formato de fluxo e outras configurações de estação.</span><span class="sxs-lookup"><span data-stu-id="54267-109">An announcement is a file that contains information about the URL for a media stream, including the multicast IP address, port, stream format, and other station settings.</span></span> <span data-ttu-id="54267-110">Os anúncios são criados pelo administrador do Windows Media quando um fluxo de publicação unicast ou multicast é criado.</span><span class="sxs-lookup"><span data-stu-id="54267-110">Announcements are created by Windows Media Administrator when a unicast or multicast publishing stream is created.</span></span> <span data-ttu-id="54267-111">O cliente pode carregar rapidamente o arquivo de anúncio e, em seguida, continuar a acessar o arquivo de mídia de streaming.</span><span class="sxs-lookup"><span data-stu-id="54267-111">The client can quickly load the announcement file, then proceed to access the streaming media file.</span></span>

<span data-ttu-id="54267-112">Para um ponto de publicação unicast, o fluxo de mídia do ponto de publicação é aberto.</span><span class="sxs-lookup"><span data-stu-id="54267-112">For a unicast publishing point, the publishing point media stream is opened.</span></span> <span data-ttu-id="54267-113">Para um ponto de publicação multicast, a URL é extraída de um arquivo de estação de difusão com uma extensão. NSC e a mídia de streaming é acessada.</span><span class="sxs-lookup"><span data-stu-id="54267-113">For a multicast publishing point, the URL is extracted from a broadcast station file with an .nsc extension, and the streaming media is accessed.</span></span> <span data-ttu-id="54267-114">Ao contrário de um fluxo unicast, nenhuma informação de cabeçalho está contida em um fluxo de multicast.</span><span class="sxs-lookup"><span data-stu-id="54267-114">Unlike a unicast stream, no header information is contained in a multicast stream.</span></span> <span data-ttu-id="54267-115">Essas informações são provenientes do arquivo de estação de difusão com uma extensão. NSC.</span><span class="sxs-lookup"><span data-stu-id="54267-115">That information comes from the broadcast station file with an .nsc extension.</span></span> <span data-ttu-id="54267-116">O Windows Media Player geralmente abre primeiro um arquivo de anúncio, que é usado para listas de reprodução de metarquivo, que aponta para o local do arquivo de estação de difusão.</span><span class="sxs-lookup"><span data-stu-id="54267-116">Windows Media Player usually first opens an announcement file, which is one use for metafile playlists, that points to the location of the broadcast station file.</span></span>

<span data-ttu-id="54267-117">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="54267-117">Example Code</span></span>


```XML
<ASX VERSION="3.0">
    <TITLE>title</TITLE>
    <ENTRY>
        <REF HREF="mms://proseware.com/pubpoint"/>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="54267-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="54267-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54267-119">**Criando listas de reprodução de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="54267-119">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="54267-120">**Usando listas de reprodução de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="54267-120">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> </dl>

 

 




