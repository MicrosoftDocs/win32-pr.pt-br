---
title: Iniciando os downloads
description: Iniciando os downloads
ms.assetid: 0a830b11-f7e1-41da-a867-86f9ac361c0b
keywords:
- Lojas online do Windows Media Player, Gerenciador de download
- lojas online, Gerenciador de download
- tipo 2 lojas online, Gerenciador de download
- Armazenamentos online do Windows Media Player, Iniciando downloads
- lojas online, Iniciando downloads
- Digite 2 lojas online, Iniciando downloads
- Windows Media Player, Gerenciador de download
- Gerenciador de download do Windows Media Player
- Gerenciador de download
- Iniciando downloads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec723bd504cc511c3ca43db90f3c613a8acefd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364383"
---
# <a name="starting-the-downloads"></a><span data-ttu-id="ed0b1-113">Iniciando os downloads</span><span class="sxs-lookup"><span data-stu-id="ed0b1-113">Starting the Downloads</span></span>

<span data-ttu-id="ed0b1-114">O download é iniciado quando o usuário clica em **baixar**.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-114">The downloading starts when the user clicks **Download**.</span></span> <span data-ttu-id="ed0b1-115">Esse botão é denominado btnDownload no código e a função do manipulador de eventos para o evento **onclick** é denominada "ondownload".</span><span class="sxs-lookup"><span data-stu-id="ed0b1-115">This button is named btnDownload in the code and the event handler function for the **onClick** event is named "OnDownload".</span></span>

<span data-ttu-id="ed0b1-116">"Ondownload" primeiro cria um novo objeto vazio **downloadcollection** e o atribui a uma variável local.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-116">"OnDownload" first creates a new empty **DownloadCollection** object and assigns it to a local variable.</span></span>


```C++
oDLC = g_oManager.createDownloadCollection();

```



<span data-ttu-id="ed0b1-117">Em seguida, a função inicia cada um dos cinco itens baixando e armazena o objeto **DownloadItem** retornado em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-117">Next, the function starts each of the five items downloading and stores the returned **DownloadItem** object in an array.</span></span>


```C++
g_DLI[0] = oDLC.startDownload(g_sFiles[0], g_sDLType);
g_DLI[1] = oDLC.startDownload(g_sFiles[1], g_sDLType);
g_DLI[2] = oDLC.startDownload(g_sFiles[2], g_sDLType);
g_DLI[3] = oDLC.startDownload(g_sFiles[3], g_sDLType);
g_DLI[4] = oDLC.startDownload(g_sFiles[4], g_sDLType);

```



<span data-ttu-id="ed0b1-118">Em seguida, o código atualiza os elementos da interface do usuário com as informações sobre a coleção de download e seus itens de download.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-118">The code then updates the user interface elements with the information about the download collection and its download items.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed0b1-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ed0b1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed0b1-120">**Usando o Gerenciador de download**</span><span class="sxs-lookup"><span data-stu-id="ed0b1-120">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 




