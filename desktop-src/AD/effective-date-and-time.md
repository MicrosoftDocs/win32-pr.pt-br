---
title: Data e hora de efetivação
description: Data e hora de efetivação é uma estratégia de prevenção que impede a distorção de versão e atualizações parciais, adiando os dados efetivos de informações para algum momento no futuro, quando a alteração tem uma alta probabilidade de ser totalmente replicada.
ms.assetid: 5e24f90a-dd53-4720-815e-9a1db51847a3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448941b7ab0d85d50123985a120beb04f256d877
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004934"
---
# <a name="effective-date-and-time"></a><span data-ttu-id="d675a-103">Data e hora de efetivação</span><span class="sxs-lookup"><span data-stu-id="d675a-103">Effective Date and Time</span></span>

<span data-ttu-id="d675a-104">*Data e hora de efetivação* é uma estratégia de prevenção que impede a distorção de versão e atualizações parciais, adiando os dados efetivos de informações para algum momento no futuro, quando a alteração tem uma alta probabilidade de ser totalmente replicada.</span><span class="sxs-lookup"><span data-stu-id="d675a-104">*Effective date and time* is an avoidance strategy that prevents version skew and partial updates by deferring the effective data of information to some point in the future when the change has a high probability of being fully replicated.</span></span> <span data-ttu-id="d675a-105">Para implementar datas efetivas, os objetos de aplicativo devem incluir um carimbo de data/hora de efetivação, que é preenchido quando o objeto é criado ou alterado.</span><span class="sxs-lookup"><span data-stu-id="d675a-105">To implement effective dates, the application objects must include an effective date timestamp, which is filled in when the object is created or changed.</span></span> <span data-ttu-id="d675a-106">Os consumidores dos objetos verificam o carimbo de data/hora e adiam o uso dos objetos até que essa data e hora sejam atingidas.</span><span class="sxs-lookup"><span data-stu-id="d675a-106">Consumers of the objects verify the timestamp and defer use of the objects until that date and time are reached.</span></span>

<span data-ttu-id="d675a-107">Algumas considerações importantes:</span><span class="sxs-lookup"><span data-stu-id="d675a-107">Some important considerations:</span></span>

-   <span data-ttu-id="d675a-108">Os aplicativos que escolhem essa abordagem devem garantir que haja um conjunto de dados aplicáveis a serem usados até que os objetos atualizados se tornem efetivos.</span><span class="sxs-lookup"><span data-stu-id="d675a-108">Applications that choose this approach must ensure that there is a set of applicable data to use until the updated objects become effective.</span></span>
-   <span data-ttu-id="d675a-109">O serviço de tempo distribuído no Windows NT 4,0 mantém os relógios da sincronização do Windows 2000 conectada.</span><span class="sxs-lookup"><span data-stu-id="d675a-109">Distributed time service in Windows NT 4.0 keeps the clocks of the connected Windows 2000 synchronized.</span></span> <span data-ttu-id="d675a-110">No entanto, nenhum serviço de tempo é perfeito; portanto, há uma pequena janela para distorção de versão.</span><span class="sxs-lookup"><span data-stu-id="d675a-110">No time service is perfect, however, so there is a small window for version skew.</span></span>
-   <span data-ttu-id="d675a-111">Definir uma boa data de efetivação pressupõe o conhecimento da latência geral de replicação para o sistema distribuído em questão.</span><span class="sxs-lookup"><span data-stu-id="d675a-111">Setting a good effective date presumes knowledge of the overall replication latency for the distributed system in question.</span></span> <span data-ttu-id="d675a-112">Em uma rede estável, uma boa regra prática para datas efetivas é a (hora da atualização) + (2 \* (latência geral média)).</span><span class="sxs-lookup"><span data-stu-id="d675a-112">In a stable network a good rule of thumb for effective dates is the (time of the update) + (2\*(average overall latency)).</span></span> <span data-ttu-id="d675a-113">Portanto, para um sistema cuja média de latência geral é de 4 horas, um atraso de 8 horas é razoável.</span><span class="sxs-lookup"><span data-stu-id="d675a-113">So, for a system whose overall latency averages 4 hours, a delay of 8 hours is reasonable.</span></span>
-   <span data-ttu-id="d675a-114">Em uma rede instável, a determinação de um valor "bom" para datas efetivas é muito mais difícil, pois a latência pode ser altamente variável.</span><span class="sxs-lookup"><span data-stu-id="d675a-114">In an unstable network, determining a "good" value for effective dates is much more difficult, since the latency may be highly variable.</span></span> <span data-ttu-id="d675a-115">A data de efetivação é a mais "eficaz" em uma rede instável quando combinada com outras estratégias de prevenção ou detecção, como somas de verificação ou GUIDs de consistência.</span><span class="sxs-lookup"><span data-stu-id="d675a-115">Effective date is most "effective" in an unstable network when combined with other avoidance or detection strategies such as checksums or consistency GUIDs.</span></span> <span data-ttu-id="d675a-116">Para obter mais informações, consulte [somas de verificação e contagens de objetos](checksums-and-object-counts.md).</span><span class="sxs-lookup"><span data-stu-id="d675a-116">For more information, see [Checksums and Object Counts](checksums-and-object-counts.md).</span></span>

 

 




