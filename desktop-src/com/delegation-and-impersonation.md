---
title: Delegação e representação
description: Em cenários de cliente/servidor, é comum que um servidor Chame outro servidor para realizar alguma tarefa em nome de um cliente. A situação em que um servidor recebe a autoridade para agir em nome de um cliente é chamada de delegação.
ms.assetid: 245bff1a-31d3-49ce-847e-c37d0c96f9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356708008274bdeb2aa80631bec777fbd02fd38d
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "104566828"
---
# <a name="delegation-and-impersonation"></a><span data-ttu-id="8378f-104">Delegação e representação</span><span class="sxs-lookup"><span data-stu-id="8378f-104">Delegation and Impersonation</span></span>

<span data-ttu-id="8378f-105">Em cenários de cliente/servidor, é comum que um servidor Chame outro servidor para realizar alguma tarefa em nome de um cliente.</span><span class="sxs-lookup"><span data-stu-id="8378f-105">In client/server scenarios, it is common for one server to call another server to accomplish some task on a client's behalf.</span></span> <span data-ttu-id="8378f-106">A situação em que um servidor recebe a autoridade para agir em nome de um cliente é chamada de *delegação*.</span><span class="sxs-lookup"><span data-stu-id="8378f-106">The situation where a server is given the authority to act on a client's behalf is called *delegation*.</span></span>

<span data-ttu-id="8378f-107">Do ponto de vista da segurança, dois problemas surgem em relação à delegação:</span><span class="sxs-lookup"><span data-stu-id="8378f-107">From a security standpoint, two issues arise regarding delegation:</span></span>

-   <span data-ttu-id="8378f-108">O que o servidor deve ter permissão para fazer ao agir em nome do cliente?</span><span class="sxs-lookup"><span data-stu-id="8378f-108">What should the server be allowed to do when acting on the client's behalf?</span></span>
-   <span data-ttu-id="8378f-109">Qual identidade é apresentada pelo servidor quando ele chama outros servidores em nome de um cliente?</span><span class="sxs-lookup"><span data-stu-id="8378f-109">What identity is presented by the server when it calls other servers on behalf of a client?</span></span>

<span data-ttu-id="8378f-110">Para lidar com esses problemas, o COM fornece a funcionalidade a seguir.</span><span class="sxs-lookup"><span data-stu-id="8378f-110">To deal with these issues, COM provides the following functionality.</span></span> <span data-ttu-id="8378f-111">O cliente pode definir um *nível de representação* que determina até que ponto o servidor será capaz de atuar como o cliente.</span><span class="sxs-lookup"><span data-stu-id="8378f-111">The client can set an *impersonation level* that determines to what extent the server will be able to act as the client.</span></span> <span data-ttu-id="8378f-112">Se o cliente conceder autoridade suficiente ao servidor, o servidor poderá *representar* (fingir ser) o cliente.</span><span class="sxs-lookup"><span data-stu-id="8378f-112">If the client grants enough authority to the server, the server can *impersonate* (pretend to be) the client.</span></span> <span data-ttu-id="8378f-113">Ao representar o cliente, o servidor recebe acesso apenas a esses objetos ou recursos que o cliente tem permissão para usar.</span><span class="sxs-lookup"><span data-stu-id="8378f-113">When impersonating the client, the server is given access to only those objects or resources that the client has permission to use.</span></span> <span data-ttu-id="8378f-114">O servidor, agindo como um cliente, também pode habilitar o *encobrimento* para mascarar sua própria identidade e projetar a identidade do cliente em chamadas para outros componentes com.</span><span class="sxs-lookup"><span data-stu-id="8378f-114">The server, acting as a client, can also enable *cloaking* to mask its own identity and project the client's identity in calls to other COM components.</span></span>

![Diagrama que mostra como o servidor que atua como o cliente pode habilitar o encobrimento.](images/172e04f7-568d-450b-9785-2c1a2b40e549.png)

<span data-ttu-id="8378f-116">Considere o cenário ilustrado pela figura anterior, em que a e B são processos em um computador diferente de C. processar uma chamada B e B chama C. o cliente A define o nível de representação.</span><span class="sxs-lookup"><span data-stu-id="8378f-116">Consider the scenario illustrated by the preceding figure, where A and B are processes on a different machine from C. Process A calls B, and B calls C. Client A sets the impersonation level.</span></span> <span data-ttu-id="8378f-117">B define o recurso de encobrimento.</span><span class="sxs-lookup"><span data-stu-id="8378f-117">B sets the cloaking capability.</span></span> <span data-ttu-id="8378f-118">Se um definir um nível de representação que permita A representação, B poderá representar um ao chamar C em nome.</span><span class="sxs-lookup"><span data-stu-id="8378f-118">If A sets an impersonation level that permits impersonation, B can impersonate A when calling C on A's behalf.</span></span> <span data-ttu-id="8378f-119">A identidade que é apresentada para o processo C será A identidade de uma identidade ou de B, dependendo se o encobrimento foi habilitado por B. Se o encobrimento estiver habilitado, a identidade apresentada ao processo C será a de um. Se o encobrimento não estiver habilitado, a identidade de B será apresentada a C.</span><span class="sxs-lookup"><span data-stu-id="8378f-119">The identity that is presented to process C will be either A's identity or B's identity, depending on whether cloaking was enabled by B. If cloaking is enabled, the identity presented to process C will be that of A. If cloaking is not enabled, B's identity will be presented to C.</span></span>

<span data-ttu-id="8378f-120">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="8378f-120">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="8378f-121">Representação</span><span class="sxs-lookup"><span data-stu-id="8378f-121">Impersonation</span></span>](impersonation.md)
-   [<span data-ttu-id="8378f-122">Níveis de representação</span><span class="sxs-lookup"><span data-stu-id="8378f-122">Impersonation Levels</span></span>](impersonation-levels.md)
-   [<span data-ttu-id="8378f-123">Encobrimento</span><span class="sxs-lookup"><span data-stu-id="8378f-123">Cloaking</span></span>](cloaking.md)

 

 




