---
title: Visão geral do desenvolvimento de interface do usuário
description: Esta seção descreve as três fases do design da interface do usuário e apresenta as tarefas que normalmente são associadas a cada fase.
ms.assetid: ab544cb9-eed3-4575-a8dd-2f5d7b5c575f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b531fb07a1805c14441c81777bbdddad0739e7cb
ms.sourcegitcommit: e5c43274e96cb8fd1b60fc187ef16723e9258367
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2020
ms.locfileid: "104007027"
---
# <a name="overview-of-the-user-interface-development-process"></a><span data-ttu-id="2c64f-103">Visão geral do processo de desenvolvimento da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="2c64f-103">Overview of the User Interface Development Process</span></span>

<span data-ttu-id="2c64f-104">Esta seção descreve as três fases do design da interface do usuário e apresenta as tarefas que normalmente são associadas a cada fase.</span><span class="sxs-lookup"><span data-stu-id="2c64f-104">This section outlines the three phases of user interface design and introduces the tasks that are typically associated with each phase.</span></span>

## <a name="the-application-user-interface-and-the-user-experience"></a><span data-ttu-id="2c64f-105">A interface do usuário do aplicativo e a experiência do usuário</span><span class="sxs-lookup"><span data-stu-id="2c64f-105">The Application User Interface and the User Experience</span></span>

<span data-ttu-id="2c64f-106">Para começar, os termos "interface do usuário" e "experiência do usuário" devem ser esclarecidos.</span><span class="sxs-lookup"><span data-stu-id="2c64f-106">To begin, the terms "user interface" and "user experience" must be clarified.</span></span>

<span data-ttu-id="2c64f-107">A interface do usuário de um aplicativo normalmente envolve os objetos que um usuário vê e interage diretamente em sua tela.</span><span class="sxs-lookup"><span data-stu-id="2c64f-107">The user interface of an application typically involves those objects that a user sees and interacts with directly on their screen.</span></span> <span data-ttu-id="2c64f-108">Por exemplo, esses objetos incluem o espaço do documento, os menus, as caixas de diálogo, os ícones, as imagens e as animações.</span><span class="sxs-lookup"><span data-stu-id="2c64f-108">For example, such objects include the document space, menus, dialog boxes, icons, images, and animations.</span></span>

<span data-ttu-id="2c64f-109">No entanto, a interface do usuário de um aplicativo é apenas um aspecto da experiência geral do usuário.</span><span class="sxs-lookup"><span data-stu-id="2c64f-109">However, the user interface of an application is only one aspect of the overall user experience.</span></span> <span data-ttu-id="2c64f-110">Outros aspectos da experiência do usuário que não são visíveis para o usuário, mas são integrantes a um aplicativo e são críticos para sua usabilidade, incluem tempo de inicialização, latência, tratamento de erros e tarefas automatizadas que são concluídas sem interação direta do usuário.</span><span class="sxs-lookup"><span data-stu-id="2c64f-110">Other aspects of the user experience that are not visible to the user, but are integral to an application and critical to its usability, include start up time, latency, error handling, and automated tasks that are completed without direct user interaction.</span></span>

<span data-ttu-id="2c64f-111">Em geral, uma interface do usuário requer ação de um usuário para realizar uma tarefa, enquanto uma ótima experiência do usuário pode ser obtida sem nenhuma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="2c64f-111">In general, a user interface requires action by a user to accomplish a task, while a great user experience can be achieved with no user interface at all.</span></span>

## <a name="user-interface-development"></a><span data-ttu-id="2c64f-112">Desenvolvimento de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="2c64f-112">User Interface Development</span></span>

<span data-ttu-id="2c64f-113">Fornecer uma experiência de usuário bem-sucedida requer uma abordagem equilibrada em todo o ciclo de vida de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="2c64f-113">Providing a successful user experience requires a balanced approach throughout the development life cycle.</span></span> <span data-ttu-id="2c64f-114">Para garantir esse equilíbrio, você não deve apenas se concentrar em implementar a funcionalidade necessária para concluir uma tarefa, mas também sobre como a tarefa é exposta por meio da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="2c64f-114">To ensure this balance, you must not only focus on implementing the functionality required to complete a task but also on how the task is exposed through the user interface.</span></span> <span data-ttu-id="2c64f-115">Lembre-se de que a interface do usuário não deve ser funcional, ela também deve ser utilizável.</span><span class="sxs-lookup"><span data-stu-id="2c64f-115">Remember, the user interface must not only be functional, it must also be usable.</span></span>

<span data-ttu-id="2c64f-116">O seguinte descreve as fases típicas do processo de dvelopment da interface do usuário:</span><span class="sxs-lookup"><span data-stu-id="2c64f-116">The following outlines the typical phases of the user interface dvelopment process:</span></span>

### <a name="designing"></a><span data-ttu-id="2c64f-117">Criando</span><span class="sxs-lookup"><span data-stu-id="2c64f-117">Designing</span></span>

-   <span data-ttu-id="2c64f-118">Requisitos funcionais – determine os requisitos e as metas iniciais para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2c64f-118">Functional requirements – Determine the initial requirements and goals for the application.</span></span>
-   <span data-ttu-id="2c64f-119">Análise de usuário – identifique os cenários de usuário e entenda as necessidades e expectativas dos usuários para cada cenário.</span><span class="sxs-lookup"><span data-stu-id="2c64f-119">User analysis – Identify the user scenarios and understand the needs and expectations of users for each scenario.</span></span>
-   <span data-ttu-id="2c64f-120">Design conceitual – modele a empresa subjacente à qual o aplicativo deve dar suporte.</span><span class="sxs-lookup"><span data-stu-id="2c64f-120">Conceptual design – Model the underlying business that the application must support.</span></span>
-   <span data-ttu-id="2c64f-121">Design lógico – projete o processo e o fluxo de informações do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2c64f-121">Logical design – Design the process and information flow of the application.</span></span>
-   <span data-ttu-id="2c64f-122">Design físico – decida como o design lógico será implementado em plataformas físicas específicas.</span><span class="sxs-lookup"><span data-stu-id="2c64f-122">Physical design – Decide how the logical design will be implemented on specific physical platforms.</span></span>

### <a name="implementing"></a><span data-ttu-id="2c64f-123">Implementado</span><span class="sxs-lookup"><span data-stu-id="2c64f-123">Implementing</span></span>

-   <span data-ttu-id="2c64f-124">Protótipo – desenvolva papel ou tela interativa telas que se concentrem na interface e não inclua elementos de Design Visual confusos.</span><span class="sxs-lookup"><span data-stu-id="2c64f-124">Prototype – Develop paper or interactive screen mockups that focus on the interface and don't include distracting visual design elements.</span></span>
-   <span data-ttu-id="2c64f-125">Construção – compile o aplicativo e prepare-se para solicitações de alteração de design.</span><span class="sxs-lookup"><span data-stu-id="2c64f-125">Construct – Build the application and prepare for design change requests.</span></span>

### <a name="testing"></a><span data-ttu-id="2c64f-126">Teste</span><span class="sxs-lookup"><span data-stu-id="2c64f-126">Testing</span></span>

-   <span data-ttu-id="2c64f-127">Teste de usabilidade – teste o aplicativo com vários usuários e cenários.</span><span class="sxs-lookup"><span data-stu-id="2c64f-127">Usability testing – Test the application with various users and scenarios.</span></span>
-   <span data-ttu-id="2c64f-128">Teste de acessibilidade – teste o aplicativo com tecnologias acessíveis e ferramentas de teste automatizadas.</span><span class="sxs-lookup"><span data-stu-id="2c64f-128">Accessibility testing – Test the application with accessible technologies and automated test tools.</span></span>

 

 




