---
description: O aplicativo é dividido em dois programas. Um dos programas é executado como usuário padrão e o outro é executado com o privilégio de administrador.
ms.assetid: 1e661915-5797-421d-b96f-72949f441aba
title: Modelo de agente do administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299d35c995fb56f969fc5983864cfc93b25b6c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828829"
---
# <a name="administrator-broker-model"></a><span data-ttu-id="3f76f-104">Modelo de agente do administrador</span><span class="sxs-lookup"><span data-stu-id="3f76f-104">Administrator Broker Model</span></span>

<span data-ttu-id="3f76f-105">No modelo de agente do administrador, o aplicativo é dividido em dois programas.</span><span class="sxs-lookup"><span data-stu-id="3f76f-105">In the administrator broker model, the application is divided into two programs.</span></span> <span data-ttu-id="3f76f-106">Um dos programas é executado como usuário padrão e o outro é executado com o privilégio de administrador.</span><span class="sxs-lookup"><span data-stu-id="3f76f-106">One of the programs runs as a standard user, and the other runs with administrator privilege.</span></span>

<span data-ttu-id="3f76f-107">Usando um manifesto de aplicativo, marque o programa de usuário padrão com um **requestedExecutionLevel** de **asInvoker** e marque o programa administrativo com um **requestedExecutionLevel** de **requireAdministrator**.</span><span class="sxs-lookup"><span data-stu-id="3f76f-107">Using an application manifest, mark the standard user program with a **requestedExecutionLevel** of **asInvoker** and mark the administrative program with a **requestedExecutionLevel** of **requireAdministrator**.</span></span> <span data-ttu-id="3f76f-108">Um usuário inicia o programa de usuário padrão primeiro.</span><span class="sxs-lookup"><span data-stu-id="3f76f-108">A user launches the standard user program first.</span></span> <span data-ttu-id="3f76f-109">Quando o usuário tenta executar uma operação que requer um token de acesso de administrador completo, o programa de usuário padrão chama a função [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) para iniciar o programa administrativo.</span><span class="sxs-lookup"><span data-stu-id="3f76f-109">When the user attempts to perform an operation that requires a full administrator access token, the standard user program calls the [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) function to launch the administrative program.</span></span> <span data-ttu-id="3f76f-110">A função **ShellExecute** solicita aprovação do usuário antes de executar o aplicativo com o token de acesso de administrador completo do usuário.</span><span class="sxs-lookup"><span data-stu-id="3f76f-110">The **ShellExecute** function prompts the user for approval before running the application with the user's full administrator access token.</span></span> <span data-ttu-id="3f76f-111">O programa administrativo pode executar tarefas que exigem privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="3f76f-111">The administrative program can then perform tasks that require administrator privilege.</span></span>

<span data-ttu-id="3f76f-112">O programa administrativo não está completamente isolado do programa de usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="3f76f-112">The administrative program is not completely isolated from the standard user program.</span></span> <span data-ttu-id="3f76f-113">O programa administrativo pode habilitar a comunicação entre processos com o programa de usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="3f76f-113">The administrative program can enable interprocess communication with the standard user program.</span></span> <span data-ttu-id="3f76f-114">No entanto, essa comunicação é limitada pela política de integridade obrigatória padrão.</span><span class="sxs-lookup"><span data-stu-id="3f76f-114">However, such communication is limited by the default mandatory integrity policy.</span></span> <span data-ttu-id="3f76f-115">Para obter informações sobre considerações de integridade obrigatórias, consulte [projetando aplicativos para serem executados em um nível de baixa integridade](/previous-versions/dotnet/articles/bb625960(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="3f76f-115">For information about mandatory integrity considerations, see [Designing Applications to Run at a Low Integrity Level](/previous-versions/dotnet/articles/bb625960(v=msdn.10)).</span></span>

<span data-ttu-id="3f76f-116">Os seguintes usos são possíveis para o modelo de agente do administrador:</span><span class="sxs-lookup"><span data-stu-id="3f76f-116">The following are possible uses for the administrator broker model:</span></span>

-   <span data-ttu-id="3f76f-117">Desenvolvendo assistentes.</span><span class="sxs-lookup"><span data-stu-id="3f76f-117">Developing wizards.</span></span> <span data-ttu-id="3f76f-118">Quando um assistente de hardware determina que um driver necessário não está instalado no computador ou localizado no local aprovado da empresa, ele chama um aplicativo elevado com a capacidade de mover um driver para o repositório do computador.</span><span class="sxs-lookup"><span data-stu-id="3f76f-118">When a hardware wizard determines that a required driver is not installed on the computer or located in the enterprise's approved location, it calls an elevated application with the ability to move a driver into the computer store.</span></span>
-   <span data-ttu-id="3f76f-119">Autorun.exe chamando Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="3f76f-119">Autorun.exe calling Setup.exe.</span></span> <span data-ttu-id="3f76f-120">Quando um usuário executa software de um CD, Autorun.exe, que é executado como usuário padrão, inicia Setup.exe, que é executado como administrador, para instalar o software no computador.</span><span class="sxs-lookup"><span data-stu-id="3f76f-120">When a user runs software from a CD, Autorun.exe, which runs as a standard user, starts Setup.exe, which runs as an administrator, to install the software onto the computer.</span></span>

<span data-ttu-id="3f76f-121">A seguir estão as desvantagens de usar o modelo de agente do administrador:</span><span class="sxs-lookup"><span data-stu-id="3f76f-121">The following are drawbacks to using the administrator broker model:</span></span>

-   <span data-ttu-id="3f76f-122">As transições do aplicativo para o aplicativo podem ser confusas para o usuário.</span><span class="sxs-lookup"><span data-stu-id="3f76f-122">The transitions from application to application can be confusing to the user.</span></span> <span data-ttu-id="3f76f-123">Pode ser difícil informar ao usuário por que um novo aplicativo aparece no monitor.</span><span class="sxs-lookup"><span data-stu-id="3f76f-123">It can be difficult to inform the user why a new application appears on the monitor.</span></span>
-   <span data-ttu-id="3f76f-124">Pode ser difícil passar informações de estado entre os dois aplicativos.</span><span class="sxs-lookup"><span data-stu-id="3f76f-124">It can be difficult to pass state information between the two applications.</span></span> <span data-ttu-id="3f76f-125">Por exemplo, você não usaria esse modelo para passar informações de estado entre um CPL (painel de controle de usuário) padrão e sua contraparte de administrador simplesmente para permitir que o mesmo CPL tenha funcionalidade de usuário administrativa e padrão.</span><span class="sxs-lookup"><span data-stu-id="3f76f-125">For example, you would not use this model to pass state information between a standard user control panel (CPL) and its administrator counterpart simply to allow the same CPL to have administrative and standard user functionality.</span></span> <span data-ttu-id="3f76f-126">O CPL de usuário padrão teria que armazenar seu estado em algum lugar.</span><span class="sxs-lookup"><span data-stu-id="3f76f-126">The standard user CPL would have to store its state somewhere.</span></span>
-   <span data-ttu-id="3f76f-127">Pode haver muitos códigos replicados ao dividir a funcionalidade entre dois programas.</span><span class="sxs-lookup"><span data-stu-id="3f76f-127">There can be a lot of replicated code when splitting the functionality between two programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f76f-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3f76f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f76f-129">Desenvolvendo aplicativos que exigem privilégios de administrador</span><span class="sxs-lookup"><span data-stu-id="3f76f-129">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="3f76f-130">Modelo de objeto COM do administrador</span><span class="sxs-lookup"><span data-stu-id="3f76f-130">Administrator COM Object Model</span></span>](administrator-com-object-model.md)
</dt> <dt>

[<span data-ttu-id="3f76f-131">Modelo de serviço do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="3f76f-131">Operating System Service Model</span></span>](operating-system-service-model.md)
</dt> <dt>

[<span data-ttu-id="3f76f-132">Modelo de tarefa elevada</span><span class="sxs-lookup"><span data-stu-id="3f76f-132">Elevated Task Model</span></span>](elevated-task-model.md)
</dt> </dl>

 

 
