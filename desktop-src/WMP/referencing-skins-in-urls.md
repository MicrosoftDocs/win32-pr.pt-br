---
title: Referenciando capas em URLs
description: Referenciando capas em URLs
ms.assetid: 9ae30c12-2dee-46b2-90e2-c101a83856fb
keywords:
- Capas do Windows Media Player, referências de URL
- capas, referências de URL
- Referências de URL em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b33ac9a5f37dce242797ae93dc4e85b973c76b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637084"
---
# <a name="referencing-skins-in-urls"></a><span data-ttu-id="3b2a8-106">Referenciando capas em URLs</span><span class="sxs-lookup"><span data-stu-id="3b2a8-106">Referencing Skins in URLs</span></span>

<span data-ttu-id="3b2a8-107">Se você usar uma URL para carregar um arquivo de mídia que será reproduzido pelo Windows Media Player, você poderá solicitar que uma determinada capa seja usada com esse arquivo.</span><span class="sxs-lookup"><span data-stu-id="3b2a8-107">If you use a URL to load a media file that will be played by Windows Media Player, you can request that a particular skin be used with that file.</span></span> <span data-ttu-id="3b2a8-108">Se a capa já estiver instalada no computador do usuário, ela será usada; caso contrário, a capa anterior será usada.</span><span class="sxs-lookup"><span data-stu-id="3b2a8-108">If the skin is already installed on the user's machine, it will be used; otherwise the previous skin will be used.</span></span>

<span data-ttu-id="3b2a8-109">Para solicitar uma capa, adicione o seguinte ao final da URL:</span><span class="sxs-lookup"><span data-stu-id="3b2a8-109">To request a skin, add the following to the end of the URL:</span></span>


```C++
?WMPSkin=skinname
```



<span data-ttu-id="3b2a8-110">*skinname* é o nome da capa que você deseja solicitar.</span><span class="sxs-lookup"><span data-stu-id="3b2a8-110">*skinname* is the name of the skin you want to request.</span></span> <span data-ttu-id="3b2a8-111">Não use aspas em volta do nome da capa.</span><span class="sxs-lookup"><span data-stu-id="3b2a8-111">Do not use quotes around the name of the skin.</span></span>

<span data-ttu-id="3b2a8-112">Por exemplo, para solicitar que a capa headspace seja usada, digite a seguinte URL http:</span><span class="sxs-lookup"><span data-stu-id="3b2a8-112">For example, to request the headspace skin be used, type the following http URL:</span></span>


```C++
https://www.proseware.com/mymedia.wma?WMPSkin=headspace

```



## <a name="related-topics"></a><span data-ttu-id="3b2a8-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3b2a8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b2a8-114">**Sobre as capas**</span><span class="sxs-lookup"><span data-stu-id="3b2a8-114">**About Skins**</span></span>](about-skins.md)
</dt> </dl>

 

 




