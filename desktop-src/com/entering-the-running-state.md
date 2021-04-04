---
title: Entrando no estado de execução
description: Entrando no estado de execução
ms.assetid: 2173eaa9-0e60-4411-81e4-dbabc5fe89b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 959038c8f64fe8750ab1bcf0f06b753371f04136
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916211"
---
# <a name="entering-the-running-state"></a><span data-ttu-id="c03b5-103">Entrando no estado de execução</span><span class="sxs-lookup"><span data-stu-id="c03b5-103">Entering the Running State</span></span>

<span data-ttu-id="c03b5-104">Quando um objeto incorporado faz a transição para o estado de execução, o manipulador de objetos deve localizar e executar o aplicativo de servidor para utilizar os serviços que apenas o servidor fornece.</span><span class="sxs-lookup"><span data-stu-id="c03b5-104">When an embedded object makes the transition to the running state, the object handler must locate and run the server application in order to utilize the services that only the server provides.</span></span> <span data-ttu-id="c03b5-105">Os objetos inseridos são colocados no estado de execução explicitamente por meio de uma solicitação pelo contêiner, como uma necessidade de desenhar um formato não armazenado em cache no momento ou implicitamente pelo OLE em resposta à invocação de alguma operação, como quando um usuário do contêiner clica duas vezes no objeto.</span><span class="sxs-lookup"><span data-stu-id="c03b5-105">Embedded objects are placed in the running state either explicitly through a request by the container, such as a need to draw a format not currently cached, or implicitly by OLE in response to invoking some operation, such as when a user of the container double-clicks the object.</span></span>

<span data-ttu-id="c03b5-106">Quando um objeto vinculado faz a transição para o estado de execução, o processo é conhecido como *Associação*.</span><span class="sxs-lookup"><span data-stu-id="c03b5-106">When a linked object makes the transition into the running state, the process is known as *binding*.</span></span> <span data-ttu-id="c03b5-107">No processo de associação, o manipulador de objeto solicita que seu moniker armazenado Localize os dados do link e, em seguida, executa o aplicativo do servidor.</span><span class="sxs-lookup"><span data-stu-id="c03b5-107">In the process of binding, the object handler asks its stored moniker to locate the link's data, then runs the server application.</span></span>

<span data-ttu-id="c03b5-108">À primeira vista, a associação de um objeto vinculado parece não ser mais complicada do que a execução de um objeto inserido.</span><span class="sxs-lookup"><span data-stu-id="c03b5-108">At first glance, binding a linked object appears to be no more complicated than running an embedded object.</span></span> <span data-ttu-id="c03b5-109">No entanto, os seguintes pontos complicam o processo:</span><span class="sxs-lookup"><span data-stu-id="c03b5-109">However, the following points complicate the process:</span></span>

-   <span data-ttu-id="c03b5-110">Um link pode se referir a um objeto ou a uma parte dele, que é inserida em outro contêiner.</span><span class="sxs-lookup"><span data-stu-id="c03b5-110">A link can refer to an object, or a portion thereof, that is embedded in another container.</span></span> <span data-ttu-id="c03b5-111">Esse recurso implica um potencial para incorporações aninhadas.</span><span class="sxs-lookup"><span data-stu-id="c03b5-111">This capability implies a potential for nested embeddings.</span></span> <span data-ttu-id="c03b5-112">A resolução de referências a tal hierarquia requer a passagem recursiva de um *moniker composto*, começando com o membro mais à direita.</span><span class="sxs-lookup"><span data-stu-id="c03b5-112">Resolving references to such a hierarchy requires recursively traversing a *composite moniker*, beginning with the rightmost member.</span></span>
-   <span data-ttu-id="c03b5-113">Quando a origem do link está em execução, o OLE é associado à instância em execução do objeto em vez de executar outra instância.</span><span class="sxs-lookup"><span data-stu-id="c03b5-113">When the link source is running, OLE binds to the running instance of the object rather than running another instance.</span></span> <span data-ttu-id="c03b5-114">No caso de objetos incorporados aninhados, um dos quais é a origem do link, o OLE deve ser capaz de se associar a um objeto já em execução em qualquer ponto.</span><span class="sxs-lookup"><span data-stu-id="c03b5-114">In the case of nested embedded objects, one of which is the link source, OLE must be able to bind to an already running object at any point.</span></span>
-   <span data-ttu-id="c03b5-115">A execução de um objeto requer o acesso à área de armazenamento para o objeto.</span><span class="sxs-lookup"><span data-stu-id="c03b5-115">Running an object requires accessing the storage area for the object.</span></span> <span data-ttu-id="c03b5-116">Quando um objeto inserido é executado, o OLE recebe um ponteiro para o armazenamento durante o processo de carregamento, que passa para o aplicativo do servidor OLE.</span><span class="sxs-lookup"><span data-stu-id="c03b5-116">When an embedded object is run, OLE receives a pointer to the storage during the load process, which it passes on to the OLE server application.</span></span> <span data-ttu-id="c03b5-117">Para objetos vinculados, no entanto, não há nenhuma interface padrão para acessar o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c03b5-117">For linked objects, however, there is no standard interface for accessing storage.</span></span> <span data-ttu-id="c03b5-118">O aplicativo do servidor OLE pode usar a interface do sistema de arquivos ou algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="c03b5-118">The OLE server application may use the file system interface or some other mechanism.</span></span>

 

 




