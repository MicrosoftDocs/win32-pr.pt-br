---
description: Um aplicativo em execução como um usuário padrão executa operações que exigem privilégios de administrador, iniciando uma tarefa agendada.
ms.assetid: cd7485b3-6be5-4163-9a86-7892dbc59181
title: Modelo de tarefa elevada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27006e32210cfea05de5c2b3b9adf36613dc4f5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297435"
---
# <a name="elevated-task-model"></a><span data-ttu-id="f36d5-103">Modelo de tarefa elevada</span><span class="sxs-lookup"><span data-stu-id="f36d5-103">Elevated Task Model</span></span>

<span data-ttu-id="f36d5-104">No modelo de tarefa com privilégios elevados, um aplicativo em execução como usuário padrão executa operações que exigem privilégios de administrador, iniciando uma tarefa agendada.</span><span class="sxs-lookup"><span data-stu-id="f36d5-104">In the elevated task model, an application running as a standard user performs operations that require administrator privilege by starting a scheduled task.</span></span>

<span data-ttu-id="f36d5-105">**Windows Server 2003 e Windows XP:** Não há suporte para o modelo de tarefa privilegiada.</span><span class="sxs-lookup"><span data-stu-id="f36d5-105">**Windows Server 2003 and Windows XP:** The elevated task model is not supported.</span></span>

<span data-ttu-id="f36d5-106">As tarefas não consomem tantos recursos do sistema como serviços, e as tarefas são fechadas automaticamente quando terminarem.</span><span class="sxs-lookup"><span data-stu-id="f36d5-106">Tasks do not consume as many system resources as services, and tasks automatically close when finished.</span></span> <span data-ttu-id="f36d5-107">Considere o uso desse modelo em vez do [modelo de serviço do sistema operacional](operating-system-service-model.md) , a menos que a compatibilidade com versões anteriores dos sistemas operacionais sejam necessárias.</span><span class="sxs-lookup"><span data-stu-id="f36d5-107">Consider using this model instead of the [Operating System Service Model](operating-system-service-model.md) unless backward compatibility with earlier operating systems is necessary.</span></span>

<span data-ttu-id="f36d5-108">Para usar uma tarefa para executar operações privilegiadas para um aplicativo de usuário padrão, as seguintes condições devem ser atendidas:</span><span class="sxs-lookup"><span data-stu-id="f36d5-108">To use a task to perform privileged operations for a standard user application, the following conditions must be met:</span></span>

-   <span data-ttu-id="f36d5-109">A tarefa deve ser definida para executar como **sistema**.</span><span class="sxs-lookup"><span data-stu-id="f36d5-109">The task must be set to run as **SYSTEM**.</span></span>
-   <span data-ttu-id="f36d5-110">O [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) associado à tarefa deve ser configurado para permitir que usuários padrão iniciem a tarefa.</span><span class="sxs-lookup"><span data-stu-id="f36d5-110">The [*security descriptor*](/windows/desktop/SecGloss/s-gly) associated with the task must be configured to allow standard users to start the task.</span></span>
-   <span data-ttu-id="f36d5-111">O serviço Agendador de tarefas deve estar em execução.</span><span class="sxs-lookup"><span data-stu-id="f36d5-111">The task scheduler service must be running.</span></span>

<span data-ttu-id="f36d5-112">Para obter informações sobre como criar e iniciar tarefas, consulte [Agendador de tarefas](/windows/desktop/TaskSchd/task-scheduler-start-page).</span><span class="sxs-lookup"><span data-stu-id="f36d5-112">For information about how to create and start tasks, see [Task Scheduler](/windows/desktop/TaskSchd/task-scheduler-start-page).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f36d5-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f36d5-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f36d5-114">Desenvolvendo aplicativos que exigem privilégios de administrador</span><span class="sxs-lookup"><span data-stu-id="f36d5-114">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="f36d5-115">Modelo de agente do administrador</span><span class="sxs-lookup"><span data-stu-id="f36d5-115">Administrator Broker Model</span></span>](administrator-broker-model.md)
</dt> <dt>

[<span data-ttu-id="f36d5-116">Modelo de objeto COM do administrador</span><span class="sxs-lookup"><span data-stu-id="f36d5-116">Administrator COM Object Model</span></span>](administrator-com-object-model.md)
</dt> <dt>

[<span data-ttu-id="f36d5-117">Modelo de serviço do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="f36d5-117">Operating System Service Model</span></span>](operating-system-service-model.md)
</dt> </dl>

 

 
