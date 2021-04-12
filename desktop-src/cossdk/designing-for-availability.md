---
description: A disponibilidade é a capacidade de um aplicativo tolerar falhas em recursos do servidor.
ms.assetid: 5d9a8216-a568-4443-b94f-1b2f2827a4be
title: Projetando para disponibilidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222583c9f53a1ccc88f2a4f984f445de02a2c976
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500924"
---
# <a name="designing-for-availability"></a><span data-ttu-id="b54f0-103">Projetando para disponibilidade</span><span class="sxs-lookup"><span data-stu-id="b54f0-103">Designing for Availability</span></span>

<span data-ttu-id="b54f0-104">A disponibilidade é a capacidade de um aplicativo tolerar falhas em recursos do servidor.</span><span class="sxs-lookup"><span data-stu-id="b54f0-104">Availability is the ability of an application to tolerate failures in server resources.</span></span> <span data-ttu-id="b54f0-105">Isso significa que o cliente continua a ser servido por meio da falha e isso, idealmente, a falha é transparente para o cliente.</span><span class="sxs-lookup"><span data-stu-id="b54f0-105">This means that the client continues to be served through the failure and that, ideally, the failure is transparent to the client.</span></span> <span data-ttu-id="b54f0-106">Obviamente, a falha pode vir de fontes de hardware ou software, portanto, você deve desenvolver para ambos os casos.</span><span class="sxs-lookup"><span data-stu-id="b54f0-106">Obviously, the failure can come from either hardware or software sources, so you must develop for both cases.</span></span>

<span data-ttu-id="b54f0-107">A disponibilidade pode ser afetada pelos seguintes fatores:</span><span class="sxs-lookup"><span data-stu-id="b54f0-107">Availability can be affected by the following factors:</span></span>

-   <span data-ttu-id="b54f0-108">Modelo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b54f0-108">Application model.</span></span> <span data-ttu-id="b54f0-109">Para maior disponibilidade, verifique se a lógica de aplicativo crítica é conduzida usando o serviço de [Transações com+](com--transactions.md) .</span><span class="sxs-lookup"><span data-stu-id="b54f0-109">For highest availability, ensure that the critical application logic is conducted using the [COM+ transactions](com--transactions.md) service.</span></span> <span data-ttu-id="b54f0-110">Além disso, o uso de um mecanismo de compensação pode ser eficaz para garantir que os recursos permaneçam em um estado íntegro após falhas.</span><span class="sxs-lookup"><span data-stu-id="b54f0-110">In addition, using a compensation mechanism can be effective in ensuring that resources remain in a healthy state after failures.</span></span>
-   <span data-ttu-id="b54f0-111">Modelo de cliente.</span><span class="sxs-lookup"><span data-stu-id="b54f0-111">Client model.</span></span> <span data-ttu-id="b54f0-112">Integre a lógica de "repetição em caso de falha" no aplicativo cliente e procure uma degradação normal no aplicativo se os recursos ou serviços estiverem indisponíveis.</span><span class="sxs-lookup"><span data-stu-id="b54f0-112">Integrate "retry on failure" logic into the client application, and strive for a graceful degradation in the application if resources or services are unavailable.</span></span> <span data-ttu-id="b54f0-113">Entenda o que o cliente está esperando do aplicativo e crie um design que permita alternativas quando ocorrer uma falha.</span><span class="sxs-lookup"><span data-stu-id="b54f0-113">Understand what the client is expecting from the application, and create a design that allows for alternatives when a failure occurs.</span></span>
-   <span data-ttu-id="b54f0-114">Disponibilidade de dados/estado.</span><span class="sxs-lookup"><span data-stu-id="b54f0-114">Data/state availability.</span></span> <span data-ttu-id="b54f0-115">Para ter acesso consistente a dados persistentes, use o clustering do Windows para fornecer suporte a failover.</span><span class="sxs-lookup"><span data-stu-id="b54f0-115">For consistent access to persistent data, use Windows Clustering to provide failover support.</span></span>
-   <span data-ttu-id="b54f0-116">Disponibilidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="b54f0-116">Service availability.</span></span> <span data-ttu-id="b54f0-117">Você pode usar o balanceamento de carga de rede para balancear a carga de solicitações de entrada de IP em um cluster de servidores.</span><span class="sxs-lookup"><span data-stu-id="b54f0-117">You can use Network Load Balancing to load balance incoming IP requests across a cluster of servers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b54f0-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b54f0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b54f0-119">Projetando para implantação</span><span class="sxs-lookup"><span data-stu-id="b54f0-119">Designing for Deployment</span></span>](designing-for-deployment.md)
</dt> <dt>

[<span data-ttu-id="b54f0-120">Projetando para escalabilidade</span><span class="sxs-lookup"><span data-stu-id="b54f0-120">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> <dt>

[<span data-ttu-id="b54f0-121">Projetando para segurança</span><span class="sxs-lookup"><span data-stu-id="b54f0-121">Designing for Security</span></span>](designing-for-security.md)
</dt> </dl>

 

 



