---
title: Usando a substituição de URL e de servidor
description: Usando a substituição de URL e de servidor
ms.assetid: d0d15b1c-5631-486e-8490-b85ec51bd355
keywords:
- Playlists do metarquivo do Windows Media, substituições de URL
- listas de reprodução, substituições de URL
- listas de reprodução de metarquivo, substituições de URL
- Playlists do metarquivo do Windows Media, substituições do servidor
- listas de reprodução, substituições de servidor
- listas de reprodução de metarquivo, substituições de servidor
- Playlists do metarquivo do Windows Media, substituições de protocolo
- listas de reprodução, sobreposições de protocolo
- listas de reprodução de metarquivo, substituições de protocolo
- Windows Media Player, substituições de URL
- Windows Media Player, substituições de servidor
- Windows Media Player, substituições de protocolo
- Substituições de URL
- substituições do servidor
- sobreposições de protocolo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: eae38e81f8ae23199628e543f65f2766491f1a2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292253"
---
# <a name="using-url-and-server-rollover"></a><span data-ttu-id="80ede-118">Usando a substituição de URL e de servidor</span><span class="sxs-lookup"><span data-stu-id="80ede-118">Using URL and Server Rollover</span></span>

<span data-ttu-id="80ede-119">Você pode usar listas de reprodução de metarquivo para fornecer um meio de reverter automaticamente para fontes de conteúdo alternativas quando um fluxo não pode ser acessado ou reproduzido.</span><span class="sxs-lookup"><span data-stu-id="80ede-119">You can use metafile playlists to provide a means of automatically rolling over to alternate content sources when a stream cannot be accessed or played.</span></span> <span data-ttu-id="80ede-120">Você pode usar esse método de substituição para especificar fontes do mesmo conteúdo em servidores diferentes ou diferentes tipos de servidores.</span><span class="sxs-lookup"><span data-stu-id="80ede-120">You can use this rollover method to specify sources of the same content on different servers or different types of servers.</span></span> <span data-ttu-id="80ede-121">Você pode, por exemplo, especificar uma primeira alternativa em um Windows Media Server diferente.</span><span class="sxs-lookup"><span data-stu-id="80ede-121">You can, for example, specify a first alternate on a different Windows Media server.</span></span> <span data-ttu-id="80ede-122">Se esse conteúdo não for reproduzido, o cliente poderá passar para uma segunda alternativa em um servidor Web.</span><span class="sxs-lookup"><span data-stu-id="80ede-122">If that content fails to play, the client can roll over to a second alternate on a web server.</span></span> <span data-ttu-id="80ede-123">O Windows Media Player tenta automaticamente se sobrepor a protocolos diferentes de acordo com suas configurações de Propriedade do Windows Media antes de tentar as URLs de substituição na playlist.</span><span class="sxs-lookup"><span data-stu-id="80ede-123">Windows Media Player automatically tries to roll over to different protocols according to its Windows Media property settings before trying the rollover URLs in the playlist.</span></span>

<span data-ttu-id="80ede-124">Defina a substituição de servidor e protocolo colocando vários elementos **ref** sucessivamente dentro de um elemento **entry** .</span><span class="sxs-lookup"><span data-stu-id="80ede-124">Set server and protocol rollover by placing multiple **REF** elements in succession within one **ENTRY** element.</span></span> <span data-ttu-id="80ede-125">Cada elemento **ref** especifica um local alternativo ou protocolo para um fluxo ou arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="80ede-125">Each **REF** element specifies an alternate location or protocol for a media file or stream.</span></span>

<span data-ttu-id="80ede-126">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="80ede-126">Example Code</span></span>


```XML
<!--Server and protocol rollover is set for the file Rollover.wma.-->
<ASX version="3.0">
    <TITLE>MyServer Rollover</TITLE>
   <ENTRY>
      <REF HREF="mms://Server1.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server2.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server3.proseware.com/Path/Rollover.wma"/>
      <REF HREF="https://www.proseware.com/Path/Rollover.wma"/>
   </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="80ede-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="80ede-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80ede-128">**Criando listas de reprodução de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="80ede-128">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="80ede-129">**Usando listas de reprodução de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="80ede-129">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> </dl>

 

 




