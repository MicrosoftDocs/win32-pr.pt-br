---
title: Inicializando a página
description: Inicializando a página
ms.assetid: 66bd3810-01a3-4413-9dad-12cf71e72ed1
keywords:
- Lojas online do Windows Media Player, Gerenciador de download
- lojas online, Gerenciador de download
- tipo 2 lojas online, Gerenciador de download
- Lojas online do Windows Media Player, inicializando páginas
- lojas online, inicializando páginas
- tipo 2 lojas online, inicializando páginas
- Windows Media Player, Gerenciador de download
- Gerenciador de download do Windows Media Player
- Gerenciador de download
- Inicializando páginas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1570d1b77abdc99ba2aee613ed8ddb88fc8097c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160115"
---
# <a name="initializing-the-page"></a><span data-ttu-id="7ce2b-113">Inicializando a página</span><span class="sxs-lookup"><span data-stu-id="7ce2b-113">Initializing the Page</span></span>

<span data-ttu-id="7ce2b-114">Quando a página da Web é carregada, a função **init** é executada.</span><span class="sxs-lookup"><span data-stu-id="7ce2b-114">When the webpage loads, the **Init** function runs.</span></span> <span data-ttu-id="7ce2b-115">Esse código primeiro recupera os dados armazenados em uma sessão anterior.</span><span class="sxs-lookup"><span data-stu-id="7ce2b-115">This code first retrieves any data stored in a previous session.</span></span> <span data-ttu-id="7ce2b-116">Para obter detalhes, consulte [mantendo as informações da sessão](maintaining-session-information.md).</span><span class="sxs-lookup"><span data-stu-id="7ce2b-116">For details, see [Maintaining Session Information](maintaining-session-information.md).</span></span> <span data-ttu-id="7ce2b-117">Em seguida, ele cria o objeto **DownloadManager** e o armazena na variável global chamada g \_ oManager.</span><span class="sxs-lookup"><span data-stu-id="7ce2b-117">It then creates the **DownloadManager** object and stores it in the global variable named g\_oManager.</span></span>


```C++
g_oManager = external.DownloadManager;

```



<span data-ttu-id="7ce2b-118">Em seguida, a função conecta o evento **OnColorChange** à função chamada **OnAppColor** e, em seguida, chama a função diretamente para inicializar a cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="7ce2b-118">Next, the function connects the **OnColorChange** event to the function named **OnAppColor** and then calls the function directly to initialize the background color.</span></span> <span data-ttu-id="7ce2b-119">Consulte [correspondência das cores do Windows Media Player](matching-the-windows-media-player-colors.md).</span><span class="sxs-lookup"><span data-stu-id="7ce2b-119">See [Matching the Windows Media Player Colors](matching-the-windows-media-player-colors.md).</span></span>

<span data-ttu-id="7ce2b-120">Por fim, a função inicia um temporizador com um intervalo de um segundo e inicializa as caixas de listagem que exibem as coleções de download pendentes e os itens de download.</span><span class="sxs-lookup"><span data-stu-id="7ce2b-120">Finally, the function starts a timer with a one-second interval and initializes the list boxes that display the pending download collections and download items.</span></span> <span data-ttu-id="7ce2b-121">Isso é importante porque pode haver sessões em andamento na última vez em que a loja online foi fechada e essas informações precisam ser exibidas novamente.</span><span class="sxs-lookup"><span data-stu-id="7ce2b-121">This is important because there may have been sessions in progress the last time the online store closed and this information needs to be displayed again.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ce2b-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ce2b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ce2b-123">**Usando o Gerenciador de download**</span><span class="sxs-lookup"><span data-stu-id="7ce2b-123">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 




