---
description: Um aplicativo COM+ é a principal unidade de administração e segurança para serviços de componentes e consiste em um grupo de componentes COM que geralmente executam funções relacionadas.
ms.assetid: 82e94acb-e7ce-4423-a720-26ee65d0d7b4
title: Visão geral do aplicativo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3365e0c0e7598d8f1eb2f466e8a2cea2d93edf4
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "105768420"
---
# <a name="com-application-overview"></a><span data-ttu-id="f4327-103">Visão geral do aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="f4327-103">COM+ Application Overview</span></span>

<span data-ttu-id="f4327-104">Um aplicativo COM+ é a principal unidade de administração e segurança para serviços de componentes e consiste em um grupo de componentes COM que geralmente executam funções relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f4327-104">A COM+ application is the primary unit of administration and security for Component Services and consists of a group of COM components that generally perform related functions.</span></span> <span data-ttu-id="f4327-105">Esses componentes consistem mais em interfaces e métodos, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="f4327-105">These components further consist of interfaces and methods, as shown in the following illustration.</span></span>

![Diagrama que mostra interfaces e métodos dentro de caixas, em ordem de método dentro da interface dentro do componente dentro do aplicativo COM+.](images/487518b4-0460-4b2d-a834-c4ea57755ffd.png)

<span data-ttu-id="f4327-107">Você pode usar a ferramenta administrativa serviços de componentes para criar novos aplicativos COM+, adicionar componentes a aplicativos e definir os atributos para um aplicativo e seus componentes.</span><span class="sxs-lookup"><span data-stu-id="f4327-107">You can use the Component Services administrative tool to create new COM+ applications, add components to applications, and set the attributes for an application and its components.</span></span>

<span data-ttu-id="f4327-108">Criando grupos lógicos de componentes COM como aplicativos COM+, você pode aproveitar os seguintes benefícios do COM+:</span><span class="sxs-lookup"><span data-stu-id="f4327-108">By creating logical groups of COM components as COM+ applications, you can take advantage of the following benefits of COM+:</span></span>

-   <span data-ttu-id="f4327-109">Um escopo de implantação para componentes COM.</span><span class="sxs-lookup"><span data-stu-id="f4327-109">A deployment scope for COM components.</span></span>
-   <span data-ttu-id="f4327-110">Um escopo de configuração comum para componentes COM, incluindo limites de segurança e enfileiramento.</span><span class="sxs-lookup"><span data-stu-id="f4327-110">A common configuration scope for COM components, including security boundaries and queuing.</span></span>
-   <span data-ttu-id="f4327-111">Armazenamento de atributos de componente não fornecidos pelo desenvolvedor de componentes (por exemplo, transações e sincronização).</span><span class="sxs-lookup"><span data-stu-id="f4327-111">Storage of component attributes not provided by the component developer (for example, transactions and synchronization).</span></span>
-   <span data-ttu-id="f4327-112">Bibliotecas de vínculo dinâmico (DLLs) do componente carregadas em processos (DLLHost.exe) sob demanda.</span><span class="sxs-lookup"><span data-stu-id="f4327-112">Component dynamic-link libraries (DLLs) loaded into processes (DLLHost.exe) on demand.</span></span>
-   <span data-ttu-id="f4327-113">Processos de servidor gerenciado para hospedar componentes.</span><span class="sxs-lookup"><span data-stu-id="f4327-113">Managed server processes to host components.</span></span>
-   <span data-ttu-id="f4327-114">Criação e gerenciamento de threads usados por componentes.</span><span class="sxs-lookup"><span data-stu-id="f4327-114">Creation and management of threads used by components.</span></span>
-   <span data-ttu-id="f4327-115">Acesso ao objeto de contexto para dispensadores de recursos, permitindo que os recursos adquiridos sejam associados automaticamente ao contexto.</span><span class="sxs-lookup"><span data-stu-id="f4327-115">Access to the context object for resource dispensers, allowing acquired resources to be automatically associated with the context.</span></span> <span data-ttu-id="f4327-116">(Para obter mais informações sobre componentes COM e contextos, consulte [contextos do com+](com--contexts.md).)</span><span class="sxs-lookup"><span data-stu-id="f4327-116">(For more information on COM components and contexts, see [COM+ Contexts](com--contexts.md).)</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4327-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f4327-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4327-118">Desenvolvendo aplicativos COM+</span><span class="sxs-lookup"><span data-stu-id="f4327-118">Developing COM+ Applications</span></span>](developing-com--applications.md)
</dt> <dt>

[<span data-ttu-id="f4327-119">Partes de um aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="f4327-119">Parts of a COM+ Application</span></span>](parts-of-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="f4327-120">Tipos de aplicativos COM+</span><span class="sxs-lookup"><span data-stu-id="f4327-120">Types of COM+ Applications</span></span>](types-of-com--applications.md)
</dt> </dl>

 

 



