---
title: Arquitetura do Gerenciador de download
description: Arquitetura do Gerenciador de download
ms.assetid: cbd46bf2-613f-40ae-8506-2f3c5eb84ada
keywords:
- Lojas online do Windows Media Player, Gerenciador de download
- lojas online, Gerenciador de download
- tipo 2 lojas online, Gerenciador de download
- Windows Media Player, Gerenciador de download
- Gerenciador de download do Windows Media Player
- Gerenciador de download
- arquitetura do Gerenciador de download
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a0567c32430e0cc15ea589bed43e2e81ffb3a08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635255"
---
# <a name="download-manager-architecture"></a><span data-ttu-id="8e5f6-110">Arquitetura do Gerenciador de download</span><span class="sxs-lookup"><span data-stu-id="8e5f6-110">Download Manager Architecture</span></span>

<span data-ttu-id="8e5f6-111">O Gerenciador de download do Windows Media Player usa a tecnologia COM.</span><span class="sxs-lookup"><span data-stu-id="8e5f6-111">The Windows Media Player Download Manager uses COM technology.</span></span> <span data-ttu-id="8e5f6-112">A funcionalidade é ditáticas em um conjunto de interfaces de programação; Você pode escrever o código de programação que usa essas interfaces usando o Microsoft JScript ou o C++.</span><span class="sxs-lookup"><span data-stu-id="8e5f6-112">The functionality is distilled into a set of programming interfaces; you can write programming code that uses these interfaces by using Microsoft JScript or C++.</span></span>

<span data-ttu-id="8e5f6-113">As linguagens de script usam o conceito de objetos para dividir a funcionalidade de programação.</span><span class="sxs-lookup"><span data-stu-id="8e5f6-113">The scripting languages use the concept of objects to divide programming functionality.</span></span> <span data-ttu-id="8e5f6-114">O modelo de objeto **DownloadManager** usa vários objetos para dividir os métodos e as propriedades em uma organização lógica que agrupa funções semanticamente relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8e5f6-114">The **DownloadManager** object model uses several objects to divide the methods and properties into a logical organization that groups semantically related functions together.</span></span> <span data-ttu-id="8e5f6-115">As seções a seguir contêm informações sobre os objetos do Gerenciador de download.</span><span class="sxs-lookup"><span data-stu-id="8e5f6-115">The following sections contain information about the Download Manager objects.</span></span>



| <span data-ttu-id="8e5f6-116">Seção</span><span class="sxs-lookup"><span data-stu-id="8e5f6-116">Section</span></span>                                                                     | <span data-ttu-id="8e5f6-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e5f6-117">Description</span></span>                                                                                              |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e5f6-118">Sobre o objeto DownloadManager</span><span class="sxs-lookup"><span data-stu-id="8e5f6-118">About the DownloadManager Object</span></span>](#about-the-downloadmanager-object)       | <span data-ttu-id="8e5f6-119">O objeto **DownloadManager** representa o objeto raiz do Gerenciador de download do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8e5f6-119">The **DownloadManager** object represents the root object for the Windows Media Player Download Manager.</span></span> |
| [<span data-ttu-id="8e5f6-120">Sobre o objeto Downloadcollection</span><span class="sxs-lookup"><span data-stu-id="8e5f6-120">About the DownloadCollection Object</span></span>](#about-the-downloadcollection-object) | <span data-ttu-id="8e5f6-121">O objeto **downloadcollection** representa uma coleção de itens de download.</span><span class="sxs-lookup"><span data-stu-id="8e5f6-121">The **DownloadCollection** object represents a collection of download items.</span></span>                             |
| [<span data-ttu-id="8e5f6-122">Sobre o objeto DownloadItem</span><span class="sxs-lookup"><span data-stu-id="8e5f6-122">About the DownloadItem Object</span></span>](#about-the-downloaditem-object)             | <span data-ttu-id="8e5f6-123">O objeto **DownloadItem** representa uma solicitação de download individual.</span><span class="sxs-lookup"><span data-stu-id="8e5f6-123">The **DownloadItem** object represents an individual download request.</span></span>                                   |



 

## <a name="about-the-downloadmanager-object"></a><span data-ttu-id="8e5f6-124">Sobre o objeto DownloadManager</span><span class="sxs-lookup"><span data-stu-id="8e5f6-124">About the DownloadManager Object</span></span>

<span data-ttu-id="8e5f6-125">**DownloadManager** é o objeto raiz do Gerenciador de download do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8e5f6-125">**DownloadManager** is the root object for the Windows Media Player Download Manager.</span></span> <span data-ttu-id="8e5f6-126">Todos os outros objetos são acessados por esse objeto.</span><span class="sxs-lookup"><span data-stu-id="8e5f6-126">All other objects are accessed through this object.</span></span> <span data-ttu-id="8e5f6-127">Para obter acesso ao objeto **DownloadManager** , use a seguinte sintaxe do JScript:</span><span class="sxs-lookup"><span data-stu-id="8e5f6-127">To gain access to the **DownloadManager** object, use the following JScript syntax:</span></span>


```C++
var DownloadManager = external.DownloadManager;
```



<span data-ttu-id="8e5f6-128">Isso cria uma instância do objeto **DownloadManager** , que pode ser usada para recuperar os objetos filho.</span><span class="sxs-lookup"><span data-stu-id="8e5f6-128">This creates an instance of the **DownloadManager** object, which can then be used to retrieve the child objects.</span></span> <span data-ttu-id="8e5f6-129">Por exemplo, a sintaxe a seguir recupera o primeiro item da coleção de download com o número de ID 253675:</span><span class="sxs-lookup"><span data-stu-id="8e5f6-129">For example, the following syntax retrieves the first item from the download collection that has id number 253675:</span></span>


```C++
var firstItem = DownloadManager.getDownloadCollection(253675).item(0);
```



## <a name="about-the-downloadcollection-object"></a><span data-ttu-id="8e5f6-130">Sobre o objeto Downloadcollection</span><span class="sxs-lookup"><span data-stu-id="8e5f6-130">About the DownloadCollection Object</span></span>

<span data-ttu-id="8e5f6-131">O objeto **downloadcollection** representa uma coleção de arquivos a serem baixados.</span><span class="sxs-lookup"><span data-stu-id="8e5f6-131">The **DownloadCollection** object represents a collection of files to be downloaded.</span></span> <span data-ttu-id="8e5f6-132">Você pode usar esse objeto para determinar quantos downloads estão na coleção, remover itens da coleção, recuperar um item de download específico e iniciar um novo download.</span><span class="sxs-lookup"><span data-stu-id="8e5f6-132">You can use this object to determine how many downloads are in the collection, remove items from the collection, retrieve a specific download item, and to start a new download.</span></span> <span data-ttu-id="8e5f6-133">Iniciar um novo download adiciona automaticamente o download à coleção.</span><span class="sxs-lookup"><span data-stu-id="8e5f6-133">Starting a new download automatically adds the download to the collection.</span></span>

## <a name="about-the-downloaditem-object"></a><span data-ttu-id="8e5f6-134">Sobre o objeto DownloadItem</span><span class="sxs-lookup"><span data-stu-id="8e5f6-134">About the DownloadItem Object</span></span>

<span data-ttu-id="8e5f6-135">O objeto **DownloadItem** representa um download individual.</span><span class="sxs-lookup"><span data-stu-id="8e5f6-135">The **DownloadItem** object represents an individual download.</span></span> <span data-ttu-id="8e5f6-136">Os itens de download sempre existem como parte de uma coleção de download.</span><span class="sxs-lookup"><span data-stu-id="8e5f6-136">Download items always exist as part of a download collection.</span></span> <span data-ttu-id="8e5f6-137">Use esse objeto para recuperar informações sobre o item de download e para pausar, retomar ou cancelar o download em andamento.</span><span class="sxs-lookup"><span data-stu-id="8e5f6-137">Use this object to retrieve information about the download item and to pause, resume, or cancel the download in progress.</span></span>

<span data-ttu-id="8e5f6-138">Quando você cancela um download, o item de download permanece em vigor em sua coleção de download.</span><span class="sxs-lookup"><span data-stu-id="8e5f6-138">When you cancel a download, the download item remains in place in its download collection.</span></span> <span data-ttu-id="8e5f6-139">Nesse caso, **downloadcollection**. **downloadstate** recupera um valor de 4, significando cancelado.</span><span class="sxs-lookup"><span data-stu-id="8e5f6-139">In this case, **downloadCollection**.**downloadState** retrieves a value of 4, meaning canceled.</span></span>

<span data-ttu-id="8e5f6-140">Você pode usar **downloadItem**. **progresso** para informar ao usuário sobre quanto do arquivo foi transferido ou quanto resta ser baixado.</span><span class="sxs-lookup"><span data-stu-id="8e5f6-140">You can use **downloadItem**.**progress** to inform the user about how much of the file has been transferred or how much remains to be downloaded.</span></span> <span data-ttu-id="8e5f6-141">Você pode usar esse valor para estimar o tempo restante também.</span><span class="sxs-lookup"><span data-stu-id="8e5f6-141">You might use this value to estimate the time remaining as well.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e5f6-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e5f6-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e5f6-143">**Gerenciador de download**</span><span class="sxs-lookup"><span data-stu-id="8e5f6-143">**Download Manager**</span></span>](download-manager.md)
</dt> </dl>

 

 




