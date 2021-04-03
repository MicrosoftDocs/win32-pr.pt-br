---
title: Por que Active Directory Domain Services usa esse modelo de replicação
description: Este tópico explica os motivos para o sistema de forma livre usado pelo Active Directory Domain Services para um modelo de replicação.
ms.assetid: 202df900-6d03-4aa8-9099-016238059ef4
ms.tgt_platform: multiple
keywords:
- Modelo de replicação Active Directory, vantagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538fe291a04953d373ff3cd45cbd4693d3dafab4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822246"
---
# <a name="why-active-directory-domain-services-uses-this-replication-model"></a><span data-ttu-id="9363a-104">Por que Active Directory Domain Services usa esse modelo de replicação</span><span class="sxs-lookup"><span data-stu-id="9363a-104">Why Active Directory Domain Services Uses This Replication Model</span></span>

<span data-ttu-id="9363a-105">Este tópico explica os motivos para o sistema de forma livre usado pelo Active Directory Domain Services para um modelo de replicação.</span><span class="sxs-lookup"><span data-stu-id="9363a-105">This topic explains the reasons for the free-form system used by Active Directory Domain Services for a replication model.</span></span>

<span data-ttu-id="9363a-106">Active Directory Domain Services são um sistema de forma livre pelos seguintes motivos:</span><span class="sxs-lookup"><span data-stu-id="9363a-106">Active Directory Domain Services are a free-form system for the following reasons:</span></span>

-   <span data-ttu-id="9363a-107">Os clientes exigem uma solução altamente distribuída na qual partes do diretório podem ser distribuídas em suas redes e administradas localmente.</span><span class="sxs-lookup"><span data-stu-id="9363a-107">Customers require a highly distributed solution in which parts of the directory can be spread across their networks and administered locally.</span></span>
-   <span data-ttu-id="9363a-108">Clientes grandes geralmente crescem para milhões de objetos, centenas ou milhares de réplicas ou ambos.</span><span class="sxs-lookup"><span data-stu-id="9363a-108">Large customers often grow to millions of objects, hundreds or thousands of replicas, or both.</span></span>
-   <span data-ttu-id="9363a-109">Muitas redes de clientes fornecem apenas conectividade intermitente a alguns locais; por exemplo, plataformas de análise de petróleo remotas e são fornecidos em Sea, portanto, o sistema deve ser tolerante a operações parcialmente conectadas ou desconectadas.</span><span class="sxs-lookup"><span data-stu-id="9363a-109">Many customer networks provide only intermittent connectivity to some locations; for example, remote oil drilling platforms and ships at sea, so the system must be tolerant of partly connected or disconnected operations.</span></span>

<span data-ttu-id="9363a-110">Não há como garantir a conscientização total do estado atual ou futuro de um sistema distribuído, pois o conhecimento das alterações de Estado deve ser propagado e a propagação leva tempo, durante o qual podem ocorrer mais alterações de estado.</span><span class="sxs-lookup"><span data-stu-id="9363a-110">There is no way to guarantee complete awareness of the current or future state of a distributed system because knowledge of state changes must be propagated and propagation takes time, during which more state changes may occur.</span></span>

<span data-ttu-id="9363a-111">Sistemas rigidamente acoplados tratam incertezas ao tentar eliminá-lo.</span><span class="sxs-lookup"><span data-stu-id="9363a-111">Tightly coupled systems handle uncertainty by attempting to eliminate it.</span></span> <span data-ttu-id="9363a-112">Isso é feito por meio de restrições em atualizações, exigindo que todos os nós ou uma maioria dos nós estejam disponíveis antes que as atualizações possam ser executadas, usando esquemas de bloqueio distribuídos ou um mestre único para recursos críticos, restringindo todos os nós a serem bem conectados ou alguma combinação dessas técnicas.</span><span class="sxs-lookup"><span data-stu-id="9363a-112">This is accomplished through constraints on updates, requiring all nodes or some majority of nodes to be available before updates can be performed, using distributed locking schemes or single-mastering for critical resources, constraining all nodes to be well-connected, or some combination of these techniques.</span></span> <span data-ttu-id="9363a-113">Quanto mais rigidamente os nós de computação em um sistema distribuído estiverem, menor será o limite de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="9363a-113">The more tightly coupled the computing nodes in a distributed system are, the lower the scaling limit.</span></span>

<span data-ttu-id="9363a-114">Os sistemas de forma livre manipulam incertezas por tolerar-lo.</span><span class="sxs-lookup"><span data-stu-id="9363a-114">Free-form systems handle uncertainty by tolerating it.</span></span> <span data-ttu-id="9363a-115">Um sistema de forma livre permite que os nós tenham exibições diferentes do estado geral do sistema e fornece algoritmos para resolver conflitos.</span><span class="sxs-lookup"><span data-stu-id="9363a-115">A free-form system enables the nodes to have differing views of the overall system state and provides algorithms for resolving conflicts.</span></span>

<span data-ttu-id="9363a-116">Soluções rigidamente acopladas foram rejeitadas como inadequadas para Active Directory Domain Services devido aos requisitos de administração local, operação desconectada e escalabilidade para números muito grandes de nós.</span><span class="sxs-lookup"><span data-stu-id="9363a-116">Tightly coupled solutions were rejected as unsuitable for Active Directory Domain Services because of the requirements for local administration, disconnected operation, and scalability to very large numbers of nodes.</span></span> <span data-ttu-id="9363a-117">O modelo levemente acoplado escolhido, a consistência de vários mestres com convergência, atende a todos os requisitos.</span><span class="sxs-lookup"><span data-stu-id="9363a-117">The loosely coupled model chosen, multi-master loose consistency with convergence, satisfies all requirements.</span></span>

 

 




