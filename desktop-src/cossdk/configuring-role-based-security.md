---
description: Se seu aplicativo COM+ usar a segurança baseada em função, haverá várias tarefas que precisam ser concluídas.
ms.assetid: f53b9945-cd34-4afc-a03a-dd72b0af160d
title: Configurando a segurança do Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eafa71430dfa13f497b0e4f7f7cea45229a422e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296077"
---
# <a name="configuring-role-based-security"></a><span data-ttu-id="85b78-103">Configurando a segurança do Role-Based</span><span class="sxs-lookup"><span data-stu-id="85b78-103">Configuring Role-Based Security</span></span>

<span data-ttu-id="85b78-104">Se seu aplicativo COM+ usar a segurança baseada em função, haverá várias tarefas que precisam ser concluídas.</span><span class="sxs-lookup"><span data-stu-id="85b78-104">If your COM+ application uses role-based security, there are several tasks that need to be completed.</span></span> <span data-ttu-id="85b78-105">Ao criar os componentes em seu aplicativo, você define as funções que são necessárias para ajudar a proteger o acesso a esses componentes.</span><span class="sxs-lookup"><span data-stu-id="85b78-105">When designing the components in your application, you define the roles that are necessary to help protect access to those components.</span></span> <span data-ttu-id="85b78-106">Você também decide quais funções atribuir aos componentes, interfaces e métodos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="85b78-106">You also decide which roles to assign to the application's components, interfaces, and methods.</span></span> <span data-ttu-id="85b78-107">Durante a integração de aplicativos, você usa a ferramenta administrativa serviços de componentes para adicionar as funções definidas ao aplicativo e atribuir cada função aos componentes, interfaces e métodos apropriados.</span><span class="sxs-lookup"><span data-stu-id="85b78-107">During application integration, you use the Component Services administrative tool to add the defined roles to the application and assign each role to the appropriate components, interfaces, and methods.</span></span>

<span data-ttu-id="85b78-108">Em Configurando a segurança baseada em função, você executa as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="85b78-108">In configuring role-based security, you perform the following steps:</span></span>

1.  <span data-ttu-id="85b78-109">Habilitar verificações de acesso no nível do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="85b78-109">Enable access checks at the application level.</span></span> <span data-ttu-id="85b78-110">Para ativar a verificação de segurança para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="85b78-110">To turn on security checking for an application.</span></span> <span data-ttu-id="85b78-111">Consulte [habilitando verificações de acesso para um aplicativo](enabling-access-checks-for-an-application.md) para obter detalhes sobre como executar essa etapa.</span><span class="sxs-lookup"><span data-stu-id="85b78-111">See [Enabling Access Checks for an Application](enabling-access-checks-for-an-application.md) for details on how to perform this step.</span></span>
2.  <span data-ttu-id="85b78-112">Definir nível de segurança para verificações de acesso.</span><span class="sxs-lookup"><span data-stu-id="85b78-112">Set security level for access checks.</span></span> <span data-ttu-id="85b78-113">Para definir a segurança em processo ou em nível de processo e componente.</span><span class="sxs-lookup"><span data-stu-id="85b78-113">To set security either at process or at process and component level.</span></span> <span data-ttu-id="85b78-114">Consulte [definindo um nível de segurança para verificações de acesso](setting-a-security-level-for-access-checks.md) para obter detalhes sobre como executar essa etapa.</span><span class="sxs-lookup"><span data-stu-id="85b78-114">See [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md) for details on how to perform this step.</span></span>
3.  <span data-ttu-id="85b78-115">Habilitar verificações de acesso no nível do componente.</span><span class="sxs-lookup"><span data-stu-id="85b78-115">Enable access checks at the component level.</span></span> <span data-ttu-id="85b78-116">Para ativar a verificação de segurança nos níveis de componente, interface e método.</span><span class="sxs-lookup"><span data-stu-id="85b78-116">To turn on security checking at the component, interface, and method levels.</span></span> <span data-ttu-id="85b78-117">Consulte [habilitando verificações de acesso no nível do componente](enabling-access-checks-at-the-component-level.md) para obter detalhes sobre como executar essa etapa.</span><span class="sxs-lookup"><span data-stu-id="85b78-117">See [Enabling Access Checks at the Component Level](enabling-access-checks-at-the-component-level.md) for details on how to perform this step.</span></span>
4.  <span data-ttu-id="85b78-118">Definir funções para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="85b78-118">Define roles for an application.</span></span> <span data-ttu-id="85b78-119">Para criar funções para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="85b78-119">To create roles for an application.</span></span> <span data-ttu-id="85b78-120">Consulte [definindo funções para um aplicativo](defining-roles-for-an-application.md) para obter detalhes sobre como executar essa etapa.</span><span class="sxs-lookup"><span data-stu-id="85b78-120">See [Defining Roles for an Application](defining-roles-for-an-application.md) for details on how to perform this step.</span></span>
5.  <span data-ttu-id="85b78-121">Atribua funções a componentes, interfaces ou métodos.</span><span class="sxs-lookup"><span data-stu-id="85b78-121">Assign roles to components, interfaces, or methods.</span></span> <span data-ttu-id="85b78-122">Para atribuir funções a recursos específicos dentro de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="85b78-122">To assign roles to specific resources within an application.</span></span> <span data-ttu-id="85b78-123">Consulte [atribuindo funções a componentes, interfaces ou métodos](assigning-roles-to-components--interfaces--or-methods.md) para obter detalhes sobre como executar essa etapa.</span><span class="sxs-lookup"><span data-stu-id="85b78-123">See [Assigning Roles to Components, Interfaces, or Methods](assigning-roles-to-components--interfaces--or-methods.md) for details on how to perform this step.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85b78-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="85b78-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85b78-125">Configurando a política de restrição de software</span><span class="sxs-lookup"><span data-stu-id="85b78-125">Configuring the Software Restriction Policy</span></span>](configuring-the-software-restriction-policy.md)
</dt> <dt>

[<span data-ttu-id="85b78-126">Definindo um nível de representação</span><span class="sxs-lookup"><span data-stu-id="85b78-126">Setting an Impersonation Level</span></span>](setting-an-impersonation-level.md)
</dt> </dl>

 

 



