---
description: 'O Windows fornece funções que executam as seguintes tarefas:'
ms.assetid: 437419c7-d6c5-4cae-b5d0-d552c75d4448
title: Interface de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adc85eafdcfe4bb573d3e156b20f9b74dbf0652
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461191"
---
# <a name="object-interface"></a><span data-ttu-id="356a7-103">Interface de objeto</span><span class="sxs-lookup"><span data-stu-id="356a7-103">Object Interface</span></span>

<span data-ttu-id="356a7-104">O Windows fornece funções que executam as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="356a7-104">Windows provides functions that perform the following tasks:</span></span>

-   <span data-ttu-id="356a7-105">Criar um objeto</span><span class="sxs-lookup"><span data-stu-id="356a7-105">Create an object</span></span>
-   <span data-ttu-id="356a7-106">Obter um identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="356a7-106">Get an object handle</span></span>
-   <span data-ttu-id="356a7-107">Obter informações sobre o objeto</span><span class="sxs-lookup"><span data-stu-id="356a7-107">Get information about the object</span></span>
-   <span data-ttu-id="356a7-108">Definir informações sobre o objeto</span><span class="sxs-lookup"><span data-stu-id="356a7-108">Set information about the object</span></span>
-   <span data-ttu-id="356a7-109">Fechar o identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="356a7-109">Close the object handle</span></span>
-   <span data-ttu-id="356a7-110">Destruir o objeto</span><span class="sxs-lookup"><span data-stu-id="356a7-110">Destroy the object</span></span>

<span data-ttu-id="356a7-111">Algumas dessas tarefas não são necessárias para cada objeto.</span><span class="sxs-lookup"><span data-stu-id="356a7-111">Some of these tasks are not necessary for each object.</span></span> <span data-ttu-id="356a7-112">Algumas dessas tarefas são combinadas para determinados objetos.</span><span class="sxs-lookup"><span data-stu-id="356a7-112">Some of these tasks are combined for certain objects.</span></span> <span data-ttu-id="356a7-113">Por exemplo, um aplicativo pode criar um objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="356a7-113">For example, an application can create an event object.</span></span> <span data-ttu-id="356a7-114">Outros aplicativos podem abrir o evento para obter um identificador exclusivo para esse objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="356a7-114">Other applications can open the event to obtain a unique handle to this event object.</span></span> <span data-ttu-id="356a7-115">À medida que cada aplicativo termina de usar o evento, ele fecha seu identificador para o objeto.</span><span class="sxs-lookup"><span data-stu-id="356a7-115">As each application finishes using the event, it closes its handle to the object.</span></span> <span data-ttu-id="356a7-116">Quando não há identificadores abertos restantes para o objeto de evento, o sistema destrói o objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="356a7-116">When there are no remaining open handles to the event object, the system destroys the event object.</span></span> <span data-ttu-id="356a7-117">Por outro lado, um aplicativo pode obter um identificador para um objeto de janela existente.</span><span class="sxs-lookup"><span data-stu-id="356a7-117">In contrast, an application can obtain a handle to an existing window object.</span></span> <span data-ttu-id="356a7-118">Quando o objeto Window não é mais necessário, o aplicativo deve destruir o objeto, o que invalida o identificador de janela.</span><span class="sxs-lookup"><span data-stu-id="356a7-118">When the window object is no longer needed, the application must destroy the object, which invalidates the window handle.</span></span>

<span data-ttu-id="356a7-119">Ocasionalmente, um objeto permanece na memória depois que todos os identificadores de objeto foram fechados.</span><span class="sxs-lookup"><span data-stu-id="356a7-119">Occasionally, an object remains in memory after all object handles have been closed.</span></span> <span data-ttu-id="356a7-120">Por exemplo, um thread pode criar um objeto de evento e aguardar o identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="356a7-120">For example, a thread could create an event object and wait on the event handle.</span></span> <span data-ttu-id="356a7-121">Enquanto o thread está aguardando, outro thread pode fechar o mesmo identificador de objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="356a7-121">While the thread is waiting, another thread could close the same event object handle.</span></span> <span data-ttu-id="356a7-122">O objeto de evento permanece na memória, sem identificadores de objeto de evento, até que o objeto de evento seja definido como o estado sinalizado e a operação de espera seja concluída.</span><span class="sxs-lookup"><span data-stu-id="356a7-122">The event object remains in memory, without any event object handles, until the event object is set to the signaled state and the wait operation is completed.</span></span> <span data-ttu-id="356a7-123">Neste momento, o sistema remove o objeto da memória.</span><span class="sxs-lookup"><span data-stu-id="356a7-123">At this time, the system removes the object from memory.</span></span>

<span data-ttu-id="356a7-124">Identificadores e objetos consomem memória.</span><span class="sxs-lookup"><span data-stu-id="356a7-124">Handles and objects consume memory.</span></span> <span data-ttu-id="356a7-125">Portanto, para preservar o desempenho do sistema, você deve fechar identificadores e excluir objetos assim que eles não forem mais necessários.</span><span class="sxs-lookup"><span data-stu-id="356a7-125">Therefore, to preserve system performance, you should close handles and delete objects as soon as they are no longer needed.</span></span> <span data-ttu-id="356a7-126">Se você não fizer isso, seu aplicativo poderá prejudicar o desempenho do sistema, devido ao uso excessivo do arquivo de paginação.</span><span class="sxs-lookup"><span data-stu-id="356a7-126">If you do not do this, your application can hurt system performance, due to excessive use of the paging file.</span></span>

<span data-ttu-id="356a7-127">Quando um processo é encerrado, o sistema fecha automaticamente os identificadores e exclui os objetos criados pelo processo.</span><span class="sxs-lookup"><span data-stu-id="356a7-127">When a process terminates, the system automatically closes handles and deletes objects created by the process.</span></span> <span data-ttu-id="356a7-128">No entanto, quando um thread é encerrado, o sistema geralmente não fecha identificadores ou exclui objetos.</span><span class="sxs-lookup"><span data-stu-id="356a7-128">However, when a thread terminates, the system usually does not close handles or delete objects.</span></span> <span data-ttu-id="356a7-129">As únicas exceções são janela, gancho, posição da janela e objetos de conversa DDE (troca de dados dinâmicos); esses objetos são destruídos quando o thread de criação é encerrado.</span><span class="sxs-lookup"><span data-stu-id="356a7-129">The only exceptions are window, hook, window position, and dynamic data exchange (DDE) conversation objects; these objects are destroyed when the creating thread terminates.</span></span>

 

 



