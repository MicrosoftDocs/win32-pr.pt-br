---
title: Cancelando a operação atual do Gerenciador de reinicialização
description: Quando uma ação do usuário direciona o instalador para executar uma ação diferente, o método a seguir pode ser usado para cancelar a operação atual do Gerenciador de reinicialização.
ms.assetid: 87c8cf27-cd77-46fb-8298-cccbf4b1071a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633882cc723f19823c6b832ee6927c5a3aacaab7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637288"
---
# <a name="canceling-the-current-restart-manager-operation"></a><span data-ttu-id="01e61-103">Cancelando a operação atual do Gerenciador de reinicialização</span><span class="sxs-lookup"><span data-stu-id="01e61-103">Canceling the Current Restart Manager Operation</span></span>

<span data-ttu-id="01e61-104">Quando uma ação do usuário direciona o instalador para executar uma ação diferente, o método a seguir pode ser usado para cancelar a operação atual do Gerenciador de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="01e61-104">When a user action directs the installer to perform a different action, the following method can be used to cancel the current Restart Manager operation.</span></span>

<span data-ttu-id="01e61-105">**Para cancelar a operação atual do Gerenciador de reinicialização**</span><span class="sxs-lookup"><span data-stu-id="01e61-105">**To cancel the current Restart Manager operation**</span></span>

-   <span data-ttu-id="01e61-106">O instalador pode chamar a função [**RMCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) de outro thread para cancelar a operação atual de [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) ou [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) .</span><span class="sxs-lookup"><span data-stu-id="01e61-106">The installer can call the [**RMCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) function from another thread to cancel the current [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) or [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) operation.</span></span> <span data-ttu-id="01e61-107">O Gerenciador de reinicialização pode cancelar a operação dependendo da extensão até a qual a operação foi concluída quando a função **RMCancelCurrentTask** é chamada.</span><span class="sxs-lookup"><span data-stu-id="01e61-107">The Restart Manager may cancel the operation depending on the extent to which the operation has completed when the **RMCancelCurrentTask** function is called.</span></span>

 

 




