---
title: Funções do Gerenciador de reinicialização
description: A API do Gerenciador de reinicialização usa as funções identificadas na tabela a seguir.
ms.assetid: ed39695a-1eb6-42fe-87a0-bd690bbce028
keywords:
- Gerente de reinicialização do Gerenciador de reinicialização, referência, funções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33187bff8522bfa347dc852f2cac157c2c3966a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822543"
---
# <a name="restart-manager-functions"></a><span data-ttu-id="1e22f-104">Funções do Gerenciador de reinicialização</span><span class="sxs-lookup"><span data-stu-id="1e22f-104">Restart Manager Functions</span></span>

<span data-ttu-id="1e22f-105">A API do Gerenciador de reinicialização usa as funções identificadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1e22f-105">The Restart Manager API uses the functions identified in the following table.</span></span>



| <span data-ttu-id="1e22f-106">Função</span><span class="sxs-lookup"><span data-stu-id="1e22f-106">Function</span></span>                                           | <span data-ttu-id="1e22f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e22f-107">Description</span></span>                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e22f-108">**RmAddFilter**</span><span class="sxs-lookup"><span data-stu-id="1e22f-108">**RmAddFilter**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter)                 | <span data-ttu-id="1e22f-109">Modifica ações de desligamento ou reinicialização.</span><span class="sxs-lookup"><span data-stu-id="1e22f-109">Modifies shutdown or restart actions.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="1e22f-110">**RmStartSession**</span><span class="sxs-lookup"><span data-stu-id="1e22f-110">**RmStartSession**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession)           | <span data-ttu-id="1e22f-111">Inicia uma nova sessão do Gerenciador de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="1e22f-111">Starts a new Restart Manager session.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="1e22f-112">**RmJoinSession**</span><span class="sxs-lookup"><span data-stu-id="1e22f-112">**RmJoinSession**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession)             | <span data-ttu-id="1e22f-113">Une o processo de um aplicativo a uma sessão do Gerenciador de reinicialização existente.</span><span class="sxs-lookup"><span data-stu-id="1e22f-113">Joins the process of an application to an existing Restart Manager session.</span></span>                                                                                                                  |
| [<span data-ttu-id="1e22f-114">**RmEndSession**</span><span class="sxs-lookup"><span data-stu-id="1e22f-114">**RmEndSession**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession)               | <span data-ttu-id="1e22f-115">Encerra a sessão do Gerenciador de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="1e22f-115">Ends the Restart Manager session.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="1e22f-116">**RmRegisterResources**</span><span class="sxs-lookup"><span data-stu-id="1e22f-116">**RmRegisterResources**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) | <span data-ttu-id="1e22f-117">Registra os recursos, como nomes de filenames, nomes curtos de serviço ou estruturas de [**\_ \_ processo exclusivo do RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) , em uma sessão do Gerenciador de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="1e22f-117">Registers resources, such as filenames, service short names, or [**RM\_UNIQUE\_PROCESS**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) structures, to a Restart Manager session.</span></span>                                   |
| [<span data-ttu-id="1e22f-118">**RmGetList**</span><span class="sxs-lookup"><span data-stu-id="1e22f-118">**RmGetList**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist)                     | <span data-ttu-id="1e22f-119">Usado por instaladores para obter uma lista de todos os aplicativos afetados por recursos registrados e seu status atual.</span><span class="sxs-lookup"><span data-stu-id="1e22f-119">Used by installers to get a list of all applications affected by registered resources and their current status.</span></span>                                                                              |
| [<span data-ttu-id="1e22f-120">**RmGetFilterList**</span><span class="sxs-lookup"><span data-stu-id="1e22f-120">**RmGetFilterList**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist)         | <span data-ttu-id="1e22f-121">Consulta o status de desligamento e reinicialização de modificações que já foram aplicadas.</span><span class="sxs-lookup"><span data-stu-id="1e22f-121">Queries the status of shutdown and restart modifications that have already been applied.</span></span>                                                                                                     |
| [<span data-ttu-id="1e22f-122">**RmShutdown**</span><span class="sxs-lookup"><span data-stu-id="1e22f-122">**RmShutdown**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)                   | <span data-ttu-id="1e22f-123">Inicia o desligamento de aplicativos e serviços.</span><span class="sxs-lookup"><span data-stu-id="1e22f-123">Initiates the shut down of applications and services.</span></span>                                                                                                                                        |
| [<span data-ttu-id="1e22f-124">**RmRemoveFilter**</span><span class="sxs-lookup"><span data-stu-id="1e22f-124">**RmRemoveFilter**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter)           | <span data-ttu-id="1e22f-125">Remove as modificações de desligamento e reinicialização que já foram aplicadas.</span><span class="sxs-lookup"><span data-stu-id="1e22f-125">Removes shutdown and restart modifications that have already been applied.</span></span>                                                                                                                   |
| [<span data-ttu-id="1e22f-126">**RmRestart**</span><span class="sxs-lookup"><span data-stu-id="1e22f-126">**RmRestart**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart)                     | <span data-ttu-id="1e22f-127">Reinicia os aplicativos e serviços que foram desligados pela função [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) e que foram registrados para reinicializar usando **RegisterApplicationRestart**.</span><span class="sxs-lookup"><span data-stu-id="1e22f-127">Restarts applications and services that have been shut down by the [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) function and that have been registered for restart using **RegisterApplicationRestart**.</span></span> |
| [<span data-ttu-id="1e22f-128">**RmCancelCurrentTask**</span><span class="sxs-lookup"><span data-stu-id="1e22f-128">**RmCancelCurrentTask**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) | <span data-ttu-id="1e22f-129">Cancela a função atual [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist), [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)ou [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) .</span><span class="sxs-lookup"><span data-stu-id="1e22f-129">Cancels the current [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist), [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown), or [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) function.</span></span>                                                            |



 

 

 




