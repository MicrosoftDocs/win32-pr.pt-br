---
title: Diretrizes para tarefas em segundo plano no Serviços de Área de Trabalho Remota
description: Para maximizar a disponibilidade da CPU para todos os usuários, desabilite as tarefas em segundo plano ao executar em um ambiente de Serviços de Área de Trabalho Remota ou crie tarefas em segundo plano eficientes que não usam muitos recursos.
ms.assetid: c3688319-dbe7-4be5-8895-622a8f8797d2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b93169b248fb086b7ccad88aa57c0feae171f91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105784067"
---
# <a name="guidelines-for-background-tasks-in-remote-desktop-services"></a><span data-ttu-id="ab6a3-103">Diretrizes para tarefas em segundo plano no Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="ab6a3-103">Guidelines for background tasks in Remote Desktop Services</span></span>

<span data-ttu-id="ab6a3-104">Tarefas em segundo plano – tarefas executadas quando o loop de mensagem de um aplicativo está ocioso — fornecem um mecanismo para lidar com tarefas de baixa prioridade em um ambiente de usuário único.</span><span class="sxs-lookup"><span data-stu-id="ab6a3-104">Background tasks—tasks performed when an application's message loop is idle—provide a mechanism for handling low-priority tasks in a single-user environment.</span></span> <span data-ttu-id="ab6a3-105">No entanto, em um ambiente de Serviços de Área de Trabalho Remota, a tarefa em segundo plano de um usuário compete em ciclos de CPU com as tarefas de primeiro plano de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="ab6a3-105">In a Remote Desktop Services environment, however, one user's background task competes for CPU cycles with another user's foreground tasks.</span></span> <span data-ttu-id="ab6a3-106">Quando vários usuários estão executando tarefas em primeiro plano e em segundo plano, as demandas de CPU são muito maiores do que quando todos os usuários estão executando apenas tarefas em primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="ab6a3-106">When multiple users are running both foreground and background tasks, the CPU demands are much higher than when all users are running only foreground tasks.</span></span> <span data-ttu-id="ab6a3-107">Para maximizar a disponibilidade da CPU para todos os usuários, desabilite as tarefas em segundo plano ao executar em um ambiente de Serviços de Área de Trabalho Remota ou crie tarefas em segundo plano eficientes que não usam muitos recursos.</span><span class="sxs-lookup"><span data-stu-id="ab6a3-107">To maximize CPU availability for all users, either disable background tasks when running in a Remote Desktop Services environment or create efficient background tasks that are not resource-intensive.</span></span>

<span data-ttu-id="ab6a3-108">Para obter mais informações, consulte [detectando o ambiente de serviços de área de trabalho remota](detecting-the-terminal-services-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ab6a3-108">For more information, see [Detecting the Remote Desktop Services environment](detecting-the-terminal-services-environment.md).</span></span> <span data-ttu-id="ab6a3-109">Depois de detectar o ambiente de Serviços de Área de Trabalho Remota, você pode desabilitar ou reconfigurar tarefas em segundo plano para o aplicativo usando o mesmo conjunto de APIs que você usou para gerenciar as tarefas.</span><span class="sxs-lookup"><span data-stu-id="ab6a3-109">After you detect the Remote Desktop Services environment, you can disable or reconfigure background tasks for the application using the same set of APIs that you used to manage the tasks.</span></span>

 

 




