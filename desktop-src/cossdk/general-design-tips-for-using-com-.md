---
description: A chave para o bom design é o planejamento. Se você não estiver familiarizado com a criação de um aplicativo de três camadas, consulte a seção intitulada criando o aplicativo COM+ usando UML.
ms.assetid: 463f4154-92f6-46c3-95ff-8513963dcadd
title: Dicas de design gerais para usar o COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5765259f170b1a98f1abb2d097dfdaec2e09d47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089133"
---
# <a name="general-design-tips-for-using-com"></a><span data-ttu-id="171ae-104">Dicas de design gerais para usar o COM+</span><span class="sxs-lookup"><span data-stu-id="171ae-104">General Design Tips for Using COM+</span></span>

<span data-ttu-id="171ae-105">A chave para o bom design é o planejamento.</span><span class="sxs-lookup"><span data-stu-id="171ae-105">The key to good design is planning.</span></span> <span data-ttu-id="171ae-106">Se você não estiver familiarizado com a criação de um aplicativo de três camadas, consulte a seção intitulada [criando o aplicativo com+ usando UML](designing-the-com--application-using-uml.md).</span><span class="sxs-lookup"><span data-stu-id="171ae-106">If you are unfamiliar with designing a three-tier application, see the section entitled [Designing the COM+ Application Using UML](designing-the-com--application-using-uml.md).</span></span>

<span data-ttu-id="171ae-107">A forma como você constrói os componentes COM que compõem a camada intermediária do seu aplicativo COM+ pode afetar drasticamente o desempenho, a escalabilidade e a facilidade de implantação.</span><span class="sxs-lookup"><span data-stu-id="171ae-107">How you construct the COM components that make up the middle tier of your COM+ application can dramatically affect performance, scalability, and ease of deployment.</span></span> <span data-ttu-id="171ae-108">Os tópicos a seguir fornecem considerações de design e dicas de implementação que você deve saber ao criar componentes COM.</span><span class="sxs-lookup"><span data-stu-id="171ae-108">The following topics provide design considerations and implementation tips you should know about when designing COM components.</span></span>



| <span data-ttu-id="171ae-109">Tópico</span><span class="sxs-lookup"><span data-stu-id="171ae-109">Topic</span></span>                                                                   | <span data-ttu-id="171ae-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="171ae-110">Description</span></span>                                                                                                                |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="171ae-111">Projetando para escalabilidade</span><span class="sxs-lookup"><span data-stu-id="171ae-111">Designing for Scalability</span></span>](designing-for-scalability.md)<br/>   | <span data-ttu-id="171ae-112">Sugere maneiras de aumentar a escalabilidade de seu aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="171ae-112">Suggests ways to increase the scalability of your COM+ application.</span></span><br/>                                             |
| [<span data-ttu-id="171ae-113">Projetando para disponibilidade</span><span class="sxs-lookup"><span data-stu-id="171ae-113">Designing for Availability</span></span>](designing-for-availability.md)<br/> | <span data-ttu-id="171ae-114">Discute os serviços que você pode usar para melhorar a disponibilidade de sua funcionalidade de camada intermediária em aplicativos COM+.</span><span class="sxs-lookup"><span data-stu-id="171ae-114">Discusses services you can use to improve the availability your middle-tier functionality in COM+ applications.</span></span><br/> |
| [<span data-ttu-id="171ae-115">Projetando para segurança</span><span class="sxs-lookup"><span data-stu-id="171ae-115">Designing for Security</span></span>](designing-for-security.md)<br/>         | <span data-ttu-id="171ae-116">Discute maneiras de configurar a segurança de forma mais eficiente para um aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="171ae-116">Discusses ways to most efficiently set up security for a COM+ application.</span></span><br/>                                      |
| [<span data-ttu-id="171ae-117">Projetando para implantação</span><span class="sxs-lookup"><span data-stu-id="171ae-117">Designing for Deployment</span></span>](designing-for-deployment.md)<br/>     | <span data-ttu-id="171ae-118">Discute maneiras de minimizar problemas de implantação ao criar um aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="171ae-118">Discusses ways to minimize deployment headaches when designing a distributed application.</span></span><br/>                       |



 

<span data-ttu-id="171ae-119">Além disso, lembre-se de ver [melhorar o desempenho com o pool de objetos](improving-performance-with-object-pooling.md) para maneiras de usar o pool de objetos com mais eficiência.</span><span class="sxs-lookup"><span data-stu-id="171ae-119">Also, be sure to see [Improving Performance with Object Pooling](improving-performance-with-object-pooling.md) for ways to most effectively use object pooling.</span></span>

## <a name="related-topics"></a><span data-ttu-id="171ae-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="171ae-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="171ae-121">Princípios e pressuposições de design de COM+</span><span class="sxs-lookup"><span data-stu-id="171ae-121">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="171ae-122">Criando o aplicativo COM+ usando UML</span><span class="sxs-lookup"><span data-stu-id="171ae-122">Designing the COM+ Application Using UML</span></span>](designing-the-com--application-using-uml.md)
</dt> <dt>

[<span data-ttu-id="171ae-123">Otimizando interações com a camada de lógica de negócios do COM+</span><span class="sxs-lookup"><span data-stu-id="171ae-123">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[<span data-ttu-id="171ae-124">Outras ferramentas da Microsoft para a criação de aplicativos distribuídos</span><span class="sxs-lookup"><span data-stu-id="171ae-124">Other Microsoft Tools for Building Distributed Applications</span></span>](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 




