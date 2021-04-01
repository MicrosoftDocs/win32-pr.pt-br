---
description: As seções a seguir descrevem o uso de ações personalizadas.
ms.assetid: dd2a0681-f50d-4232-bdcc-8aee6bb121a1
title: Usando ações personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be1937adbf64b94667fc3e7c44d82843b561dfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164825"
---
# <a name="using-custom-actions"></a><span data-ttu-id="f1065-103">Usando ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="f1065-103">Using Custom Actions</span></span>

<span data-ttu-id="f1065-104">As seções a seguir descrevem o uso de ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="f1065-104">The following sections describe using custom actions.</span></span>

-   [<span data-ttu-id="f1065-105">Invocando ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="f1065-105">Invoking Custom Actions</span></span>](invoking-custom-actions.md)
-   [<span data-ttu-id="f1065-106">Sequência de ações personalizadas de sequenciamento</span><span class="sxs-lookup"><span data-stu-id="f1065-106">Sequencing Custom Actions</span></span>](sequencing-custom-actions.md)
-   [<span data-ttu-id="f1065-107">Obtendo informações de contexto para ações personalizadas de execução adiada</span><span class="sxs-lookup"><span data-stu-id="f1065-107">Obtaining Context Information for Deferred Execution Custom Actions</span></span>](obtaining-context-information-for-deferred-execution-custom-actions.md)
-   [<span data-ttu-id="f1065-108">Adicionando ações personalizadas ao ProgressBar</span><span class="sxs-lookup"><span data-stu-id="f1065-108">Adding Custom Actions to the ProgressBar</span></span>](adding-custom-actions-to-the-progressbar.md)
-   [<span data-ttu-id="f1065-109">Depurando ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="f1065-109">Debugging Custom Actions</span></span>](debugging-custom-actions.md)
-   [<span data-ttu-id="f1065-110">Determinando o nível da interface do usuário de uma ação personalizada</span><span class="sxs-lookup"><span data-stu-id="f1065-110">Determining UI Level from a Custom Action</span></span>](determining-ui-level-from-a-custom-action.md)
-   [<span data-ttu-id="f1065-111">Desinstalando ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="f1065-111">Uninstalling Custom Actions</span></span>](uninstalling-custom-actions.md)
-   [<span data-ttu-id="f1065-112">Retornando mensagens de erro de ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="f1065-112">Returning Error Messages from Custom Actions</span></span>](returning-error-messages-from-custom-actions.md)
-   [<span data-ttu-id="f1065-113">Definindo um ponto de restauração de uma ação personalizada</span><span class="sxs-lookup"><span data-stu-id="f1065-113">Setting a restore point from a Custom Action</span></span>](setting-a-restore-point-from-a-custom-action.md)
-   [<span data-ttu-id="f1065-114">Funções não para uso em ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="f1065-114">Functions Not for Use in Custom Actions</span></span>](functions-not-for-use-in-custom-actions.md)
-   [<span data-ttu-id="f1065-115">Alterando o estado do sistema usando uma ação personalizada</span><span class="sxs-lookup"><span data-stu-id="f1065-115">Changing the System State Using a Custom Action</span></span>](changing-the-system-state-using-a-custom-action.md)
-   [<span data-ttu-id="f1065-116">Acessando a sessão do instalador atual de dentro de uma ação personalizada</span><span class="sxs-lookup"><span data-stu-id="f1065-116">Accessing the Current Installer Session from Inside a Custom Action</span></span>](accessing-the-current-installer-session-from-inside-a-custom-action.md)
-   [<span data-ttu-id="f1065-117">Acessando um banco de dados ou sessão de dentro de uma ação personalizada</span><span class="sxs-lookup"><span data-stu-id="f1065-117">Accessing a Database or Session from Inside a Custom Action</span></span>](accessing-a-database-or-session-from-inside-a-custom-action.md)
-   [<span data-ttu-id="f1065-118">Usando uma ação personalizada para iniciar um arquivo instalado no final da instalação</span><span class="sxs-lookup"><span data-stu-id="f1065-118">Using a Custom Action to Launch an Installed File at the End of the Installation</span></span>](using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation.md)
-   [<span data-ttu-id="f1065-119">Usando uma ação personalizada para criar contas de usuário em um computador local</span><span class="sxs-lookup"><span data-stu-id="f1065-119">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
-   [<span data-ttu-id="f1065-120">Usando ações personalizadas de 64 bits</span><span class="sxs-lookup"><span data-stu-id="f1065-120">Using 64-bit Custom Actions</span></span>](using-64-bit-custom-actions.md)

<span data-ttu-id="f1065-121">Para obter uma visão geral das ações personalizadas, consulte [sobre ações personalizadas](about-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="f1065-121">For an overview of custom actions, see [About Custom Actions](about-custom-actions.md).</span></span>

<span data-ttu-id="f1065-122">Para obter mais informações sobre como codificar ações personalizadas na [tabela CustomAction](customaction-table.md), consulte [referência de ação personalizada](custom-action-reference.md).</span><span class="sxs-lookup"><span data-stu-id="f1065-122">For more information about encoding custom actions into the [CustomAction table](customaction-table.md), see [Custom Action Reference](custom-action-reference.md).</span></span>

<span data-ttu-id="f1065-123">Para obter um resumo das ações personalizadas e como elas são codificadas na tabela CustomAction, consulte [Resumo da lista de todos os tipos de ação personalizadas](summary-list-of-all-custom-action-types.md).</span><span class="sxs-lookup"><span data-stu-id="f1065-123">For a summary of custom actions and how they are encoded into the CustomAction table, see [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md).</span></span>

 

 



