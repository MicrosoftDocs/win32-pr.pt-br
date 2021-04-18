---
description: O desenvolvimento de um aplicativo COM+ bem-sucedido requer o design de arquitetura de aplicativo inicial.
ms.assetid: 6a7cc610-e09a-4097-bc31-4e53db0ee152
title: Criando o aplicativo COM+ usando UML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48526623df5bc929daa4d8ce9cbe4d7592d6b30c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370415"
---
# <a name="designing-the-com-application-using-uml"></a><span data-ttu-id="b7319-103">Criando o aplicativo COM+ usando UML</span><span class="sxs-lookup"><span data-stu-id="b7319-103">Designing the COM+ Application Using UML</span></span>

<span data-ttu-id="b7319-104">O desenvolvimento de um aplicativo COM+ bem-sucedido requer o design de arquitetura de aplicativo inicial.</span><span class="sxs-lookup"><span data-stu-id="b7319-104">Developing a successful COM+ application requires up-front application architectural design.</span></span> <span data-ttu-id="b7319-105">O Unified Modeling Language (UML) é fundamental para esse desenvolvimento de design.</span><span class="sxs-lookup"><span data-stu-id="b7319-105">The Unified Modeling Language (UML) is key to this design development.</span></span> <span data-ttu-id="b7319-106">O UML é uma notação de modelagem para dados e processos de aplicativos que combina as práticas recomendadas do setor de software.</span><span class="sxs-lookup"><span data-stu-id="b7319-106">The UML is a modeling notation for application data and processes that combines the best practices of the software industry.</span></span> <span data-ttu-id="b7319-107">Como o UML divide o aplicativo em três exibições que refletem o aplicativo, bem como seu empacotamento e implementação, a notação de modelagem se estende bem para dar suporte à modelagem empresarial.</span><span class="sxs-lookup"><span data-stu-id="b7319-107">Because the UML breaks the application into three views that reflect the application as well as its packaging and implementation, the modeling notation extends well to support enterprise modeling.</span></span>

<span data-ttu-id="b7319-108">O UML aborda três exibições do aplicativo, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b7319-108">The UML addresses three views of the application, as follows:</span></span>

-   <span data-ttu-id="b7319-109">A exibição estática, que é modelada por informações obtidas de cenários de usuário e diagramas de classe.</span><span class="sxs-lookup"><span data-stu-id="b7319-109">The static view, which is modeled by information taken from user scenarios and class diagrams.</span></span>
-   <span data-ttu-id="b7319-110">A exibição dinâmica, que é modelada usando diagramas de sequência, colaboração e transição de estado.</span><span class="sxs-lookup"><span data-stu-id="b7319-110">The dynamic view, which is modeled using sequence, collaboration, and state transition diagrams.</span></span>
-   <span data-ttu-id="b7319-111">A exibição funcional, que é a narrativa descritiva mais tradicional usando o pseudocódigo e as especificações.</span><span class="sxs-lookup"><span data-stu-id="b7319-111">The functional view, which is the more traditional descriptive narrative using pseudocode and specifications.</span></span>

<span data-ttu-id="b7319-112">As informações para essas exibições podem ser coletadas seguindo três etapas de design que funcionam bem com o UML.</span><span class="sxs-lookup"><span data-stu-id="b7319-112">The information for these views can be gathered by following three design steps that work well with the UML.</span></span> <span data-ttu-id="b7319-113">Antes de escrever uma única linha de código, você precisa criar os seguintes modelos:</span><span class="sxs-lookup"><span data-stu-id="b7319-113">Before writing a single line of code, you need to create the following models:</span></span>

<dl> <dt>

<span data-ttu-id="b7319-114"><span id="Conceptual_model"></span><span id="conceptual_model"></span><span id="CONCEPTUAL_MODEL"></span>Modelo conceitual</span><span class="sxs-lookup"><span data-stu-id="b7319-114"><span id="Conceptual_model"></span><span id="conceptual_model"></span><span id="CONCEPTUAL_MODEL"></span>Conceptual model</span></span>
</dt> <dd>

<span data-ttu-id="b7319-115">Decida quais componentes e serviços são necessários.</span><span class="sxs-lookup"><span data-stu-id="b7319-115">Decide what components and services are required.</span></span>

</dd> <dt>

<span data-ttu-id="b7319-116"><span id="Logical_model"></span><span id="logical_model"></span><span id="LOGICAL_MODEL"></span>Modelo lógico</span><span class="sxs-lookup"><span data-stu-id="b7319-116"><span id="Logical_model"></span><span id="logical_model"></span><span id="LOGICAL_MODEL"></span>Logical model</span></span>
</dt> <dd>

<span data-ttu-id="b7319-117">Determine em qual camada de design lógico ele pertence.</span><span class="sxs-lookup"><span data-stu-id="b7319-117">Determine which logical design tier they belong in.</span></span>

</dd> <dt>

<span data-ttu-id="b7319-118"><span id="Physical_model"></span><span id="physical_model"></span><span id="PHYSICAL_MODEL"></span>Modelo físico</span><span class="sxs-lookup"><span data-stu-id="b7319-118"><span id="Physical_model"></span><span id="physical_model"></span><span id="PHYSICAL_MODEL"></span>Physical model</span></span>
</dt> <dd>

<span data-ttu-id="b7319-119">Determine onde os componentes residem fisicamente e como eles devem ser codificados.</span><span class="sxs-lookup"><span data-stu-id="b7319-119">Determine where the components reside physically and how they are to be coded.</span></span>

</dd> </dl>

<span data-ttu-id="b7319-120">Esses modelos podem ser usados com ferramentas de caso baseado em UML.</span><span class="sxs-lookup"><span data-stu-id="b7319-120">These models can then be used with UML-based CASE tools.</span></span> <span data-ttu-id="b7319-121">Para obter mais informações sobre esses três modelos de design, consulte os seguintes tópicos nesta seção:</span><span class="sxs-lookup"><span data-stu-id="b7319-121">For more information on these three design models, see the following topics in this section:</span></span>

-   [<span data-ttu-id="b7319-122">O modelo conceitual: requisitos de aplicativo</span><span class="sxs-lookup"><span data-stu-id="b7319-122">The Conceptual Model: Application Requirements</span></span>](the-conceptual-model--application-requirements.md)
-   [<span data-ttu-id="b7319-123">O modelo lógico: definição e planejamento de aplicativos</span><span class="sxs-lookup"><span data-stu-id="b7319-123">The Logical Model: Application Definition and Planning</span></span>](the-logical-model--application-definition-and-planning.md)
-   [<span data-ttu-id="b7319-124">O modelo físico: arquitetura de aplicativo</span><span class="sxs-lookup"><span data-stu-id="b7319-124">The Physical Model: Application Architecture</span></span>](the-physical-model--application-architecture.md)

## <a name="related-topics"></a><span data-ttu-id="b7319-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b7319-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7319-126">Princípios e pressuposições de design de COM+</span><span class="sxs-lookup"><span data-stu-id="b7319-126">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="b7319-127">Dicas de design gerais para usar o COM+</span><span class="sxs-lookup"><span data-stu-id="b7319-127">General Design Tips for Using COM+</span></span>](general-design-tips-for-using-com-.md)
</dt> <dt>

[<span data-ttu-id="b7319-128">Otimizando interações com a camada de lógica de negócios do COM+</span><span class="sxs-lookup"><span data-stu-id="b7319-128">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[<span data-ttu-id="b7319-129">Outras ferramentas da Microsoft para a criação de aplicativos distribuídos</span><span class="sxs-lookup"><span data-stu-id="b7319-129">Other Microsoft Tools for Building Distributed Applications</span></span>](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



