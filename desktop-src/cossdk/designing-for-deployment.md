---
description: Projetando para implantação
ms.assetid: 31244998-34f5-4fd8-95f6-adcc134bcaf3
title: Projetando para implantação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e60ac561bd05d08253433e52c7f00c2def54df3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456956"
---
# <a name="designing-for-deployment"></a><span data-ttu-id="9afb6-103">Projetando para implantação</span><span class="sxs-lookup"><span data-stu-id="9afb6-103">Designing for Deployment</span></span>

<span data-ttu-id="9afb6-104">Planejar o escopo de aplicativos COM+ é uma tarefa de design importante que você deve considerar no início.</span><span class="sxs-lookup"><span data-stu-id="9afb6-104">Planning the scope of COM+ applications is an important design task you should consider early on.</span></span> <span data-ttu-id="9afb6-105">Os sistemas distribuídos que se destinam a serem executados usando COM+ devem ser projetados para implantação com a menor quantidade de configuração individual e para usar com mais eficiência cada processo.</span><span class="sxs-lookup"><span data-stu-id="9afb6-105">Distributed systems that are intended to run using COM+ should be designed for deployment with the least amount of individual configuration and to most efficiently use each process.</span></span> <span data-ttu-id="9afb6-106">Também há técnicas que você pode usar que permitirão obter um desempenho ideal ao implantar um aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="9afb6-106">There are also techniques you can use that will enable you to achieve optimal performance when deploying a COM+ application.</span></span> <span data-ttu-id="9afb6-107">(Para obter mais informações, consulte [implantando para comunicação mais rápida](deploying-for-faster-communication.md).)</span><span class="sxs-lookup"><span data-stu-id="9afb6-107">(For more information, see [Deploying for Faster Communication](deploying-for-faster-communication.md).)</span></span>

<span data-ttu-id="9afb6-108">Quando exibido com a ferramenta administrativa serviços de componentes, cada aplicativo COM+ aparece como uma pasta dentro da qual os conjuntos de componentes são agrupados logicamente.</span><span class="sxs-lookup"><span data-stu-id="9afb6-108">When viewed with the Component Services administrative tool, each COM+ application appears as a folder within which sets of components are logically grouped.</span></span> <span data-ttu-id="9afb6-109">Embora você possa mover componentes individuais entre pastas de **componentes** de aplicativos do com+ (em outras palavras, de um aplicativo para outro), vários serviços definidos no nível de aplicativo do com+, como segurança, podem ser diferentes.</span><span class="sxs-lookup"><span data-stu-id="9afb6-109">While you can move individual components between COM+ application **Components** folders (in other words, from one application to another), several services set at the COM+ application level, such as security, may differ.</span></span> <span data-ttu-id="9afb6-110">Essas configurações de serviço podem afetar a portabilidade.</span><span class="sxs-lookup"><span data-stu-id="9afb6-110">These service settings can affect portability.</span></span>

## <a name="a-com-server-application-defines-a-process-boundary"></a><span data-ttu-id="9afb6-111">Um aplicativo de servidor COM+ define um limite de processo</span><span class="sxs-lookup"><span data-stu-id="9afb6-111">A COM+ Server Application Defines a Process Boundary</span></span>

<span data-ttu-id="9afb6-112">Ao criar um novo aplicativo de servidor do COM+, você está realmente definindo um novo limite de processo.</span><span class="sxs-lookup"><span data-stu-id="9afb6-112">When you create a new COM+ server application, you are really defining a new process boundary.</span></span> <span data-ttu-id="9afb6-113">(Observe a exceção para aplicativos de biblioteca explicados abaixo.) Esse processo torna-se a instância do aplicativo de controle para os componentes contidos no aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="9afb6-113">(Note the exception for library applications explained below.) This process becomes the controlling application instance for the components that are contained in the COM+ application.</span></span> <span data-ttu-id="9afb6-114">Todos esses componentes são executados em processo em uma nova instância do programa executável COM+ sempre que um programa chama um aplicativo COM+ pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="9afb6-114">These components all run in-process in a new instance of the COM+ executable program whenever a program calls into a COM+ application for the first time.</span></span> <span data-ttu-id="9afb6-115">Isso significa que todos os componentes dentro de uma determinada pasta **componentes** do aplicativo com+ são executados em um único espaço de processo que serve como o servidor DCOM.</span><span class="sxs-lookup"><span data-stu-id="9afb6-115">This means that all of the components within a given COM+ application's **Components** folder run in a single process space that serves as the DCOM server.</span></span> <span data-ttu-id="9afb6-116">No aplicativo COM+, o COM+ gerencia a memória, coordenação com o Coordenador de Transações Distribuídas (DTC), ativação da instância de componente just-in-time, detecção de falhas e recuperação e segurança baseada em função.</span><span class="sxs-lookup"><span data-stu-id="9afb6-116">Within the COM+ application, COM+ manages memory, coordination with the Distributed Transaction Coordinator (DTC), just-in-time component instance activation, crash detection and recovery, and role-based security.</span></span>

## <a name="calling-across-com-application-boundaries"></a><span data-ttu-id="9afb6-117">Chamando entre limites de aplicativos COM+</span><span class="sxs-lookup"><span data-stu-id="9afb6-117">Calling Across COM+ Application Boundaries</span></span>

<span data-ttu-id="9afb6-118">Como cada aplicativo COM+ normalmente é implementado como um executável separado, o efeito de dividir um aplicativo distribuído em vários aplicativos COM+ apresenta chamadas COM fora do processo quando os componentes em um aplicativo COM+ chamam os componentes em outro aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="9afb6-118">Because each COM+ application normally is implemented as a separate executable, the effect of splitting a distributed application across multiple COM+ applications introduces out-of-process COM calls when components in one COM+ application call the components in another COM+ application.</span></span> <span data-ttu-id="9afb6-119">Isso apresenta degradação de desempenho devido à sobrecarga extra que o empacotamento de parâmetros COM em processos impõe.</span><span class="sxs-lookup"><span data-stu-id="9afb6-119">This introduces performance degradation due to the extra burden that marshaling COM parameters across processes imposes.</span></span>

> [!Note]  
> <span data-ttu-id="9afb6-120">Não há nada inerentemente errado com a incorrência desta penalidade de desempenho; Você só precisa estar ciente de que vai ocorrer.</span><span class="sxs-lookup"><span data-stu-id="9afb6-120">There is nothing inherently wrong with incurring this performance penalty; you just need to be aware that it is going to occur.</span></span> <span data-ttu-id="9afb6-121">Dependendo do tempo de resposta necessário, o número de usuários que solicitarão serviços de negócios simultaneamente e o ônus de inicialização adicionado que cada componente adiciona a cada aplicativo COM+, você pode descobrir que o impacto no desempenho atribuído a chamadas entre aplicativos é aceitável.</span><span class="sxs-lookup"><span data-stu-id="9afb6-121">Depending on the required response time, the number of users that will simultaneously request business services, and the added start-up burden that each component adds to each COM+ application, you may find that the performance hit attributable to cross-application calls is acceptable.</span></span>

 

<span data-ttu-id="9afb6-122">Uma possibilidade que elimina a penalidade de desempenho de chamar entre limites de aplicativos COM+ é marcar um determinado aplicativo COM+ como um aplicativo de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="9afb6-122">One possibility that eliminates the performance penalty of calling across COM+ application boundaries is to mark a given COM+ application as a library application.</span></span> <span data-ttu-id="9afb6-123">Um aplicativo de biblioteca COM+ é executado no processo do cliente que o cria.</span><span class="sxs-lookup"><span data-stu-id="9afb6-123">A COM+ library application runs in the process of the client that creates it.</span></span> <span data-ttu-id="9afb6-124">Obviamente, nenhum lucro de desempenho tem nenhum custo.</span><span class="sxs-lookup"><span data-stu-id="9afb6-124">Of course, no performance gain has zero cost.</span></span> <span data-ttu-id="9afb6-125">Nesse caso, a compensação envolve as limitações dos aplicativos de biblioteca COM+.</span><span class="sxs-lookup"><span data-stu-id="9afb6-125">In this case, the trade-off involves the limitations of COM+ library applications.</span></span> <span data-ttu-id="9afb6-126">Embora um aplicativo de biblioteca possa usar a segurança baseada em função, ele não pode dar suporte a componentes enfileirados ou acesso remoto.</span><span class="sxs-lookup"><span data-stu-id="9afb6-126">While a library application can use role-based security, it cannot support queued components or remote access.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9afb6-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9afb6-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9afb6-128">Implantando para comunicação mais rápida</span><span class="sxs-lookup"><span data-stu-id="9afb6-128">Deploying for Faster Communication</span></span>](deploying-for-faster-communication.md)
</dt> <dt>

[<span data-ttu-id="9afb6-129">Projetando para disponibilidade</span><span class="sxs-lookup"><span data-stu-id="9afb6-129">Designing for Availability</span></span>](designing-for-availability.md)
</dt> <dt>

[<span data-ttu-id="9afb6-130">Projetando para escalabilidade</span><span class="sxs-lookup"><span data-stu-id="9afb6-130">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> <dt>

[<span data-ttu-id="9afb6-131">Projetando para segurança</span><span class="sxs-lookup"><span data-stu-id="9afb6-131">Designing for Security</span></span>](designing-for-security.md)
</dt> </dl>

 

 



