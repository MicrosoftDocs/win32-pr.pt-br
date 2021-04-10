---
title: Servidores In-Process
description: Servidores In-Process
ms.assetid: cc0c4350-fa75-4321-834f-711158776cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4886932b9669aa2d3cdd49979324f9ccc6e03d44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159773"
---
# <a name="in-process-servers"></a><span data-ttu-id="6d123-103">Servidores In-Process</span><span class="sxs-lookup"><span data-stu-id="6d123-103">In-Process Servers</span></span>

<span data-ttu-id="6d123-104">Se você implementar um aplicativo de servidor OLE como um servidor em processo — uma DLL em execução no espaço de processo do aplicativo de contêiner — e não como um servidor local — um EXE em execução em seu próprio espaço de processo — a comunicação entre o contêiner e o servidor é simplificada porque a comunicação entre os dois pode assumir a forma de chamadas de função normais.</span><span class="sxs-lookup"><span data-stu-id="6d123-104">If you implement an OLE server application as an in-process server — a DLL running in the process space of the container application — rather than as a local server — an EXE running in its own process space — communication between container and server is simplified because communication between the two can take the form of normal function calls.</span></span> <span data-ttu-id="6d123-105">As chamadas de procedimento remoto não são necessárias porque os dois aplicativos são executados no mesmo espaço de processo.</span><span class="sxs-lookup"><span data-stu-id="6d123-105">Remote procedure calls are not required because the two applications run in the same process space.</span></span> <span data-ttu-id="6d123-106">Como esperado, os objetos que gerenciam o marshaling de parâmetros também são desnecessários, embora possam ser agregados dentro da DLL sem interferir na comunicação entre o contêiner e o servidor.</span><span class="sxs-lookup"><span data-stu-id="6d123-106">As you would expect, the objects that manage the marshaling of parameters are also unnecessary, although they may be aggregated within the DLL without interfering with the communication between container and server.</span></span>

<span data-ttu-id="6d123-107">Quando um aplicativo de servidor OLE é implementado como um servidor em processo, um manipulador de objeto separado não é necessário porque o próprio servidor reside no espaço de processo do cliente.</span><span class="sxs-lookup"><span data-stu-id="6d123-107">When an OLE server application is implemented as an in-process server, a separate object handler is not required because the server itself lives in the client's process space.</span></span> <span data-ttu-id="6d123-108">A principal diferença entre um servidor em processo e o manipulador de objetos é que o servidor é capaz de gerenciar o objeto em um estado de execução enquanto o manipulador não pode.</span><span class="sxs-lookup"><span data-stu-id="6d123-108">The main difference between an in-process server and object handler is that the server is able to manage the object in a running state while the handler cannot.</span></span> <span data-ttu-id="6d123-109">Uma consequência dessa diferença é que um servidor deve fornecer uma interface do usuário para manipular o objeto em execução, enquanto um manipulador Delega esse requisito ao servidor do objeto.</span><span class="sxs-lookup"><span data-stu-id="6d123-109">One consequence of this difference is that a server must provide a user interface for manipulating the running object, while a handler delegates this requirement to the object's server.</span></span> <span data-ttu-id="6d123-110">Ao criar um servidor em processo, você pode agregar no manipulador padrão OLE, permitindo que ele lide com tarefas básicas, como exibição, armazenamento e notificações enquanto você implementa apenas os serviços que o manipulador não fornece ou não implementa da maneira que você precisa.</span><span class="sxs-lookup"><span data-stu-id="6d123-110">In creating an in-process server, you can aggregate on the OLE default handler, letting it handle basic chores, such as display, storage, and notifications while you implement only those services that the handler either does not provide or does not implement in the way you require.</span></span>

<span data-ttu-id="6d123-111">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="6d123-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="6d123-112">Vantagens</span><span class="sxs-lookup"><span data-stu-id="6d123-112">Advantages</span></span>](advantages.md)
-   [<span data-ttu-id="6d123-113">Desvantagens</span><span class="sxs-lookup"><span data-stu-id="6d123-113">Disadvantages</span></span>](disadvantages.md)

## <a name="related-topics"></a><span data-ttu-id="6d123-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6d123-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d123-115">Documentos compostos</span><span class="sxs-lookup"><span data-stu-id="6d123-115">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 




