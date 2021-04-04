---
title: Obtendo o status de uma operação do Gerenciador de reinicialização
description: Quando muitos aplicativos e serviços devem ser desligados ou reiniciados, a operação do Gerenciador de reinicialização pode levar um longo período de tempo. O método a seguir pode ser usado para obter o status da operação atual.
ms.assetid: 0df9de1f-df37-46a5-8010-6c8b34429376
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afa5f329a8f21aa625c5c7b61a3e65b2c907bbf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084811"
---
# <a name="getting-the-status-of-a-restart-manager-operation"></a><span data-ttu-id="92bf9-104">Obtendo o status de uma operação do Gerenciador de reinicialização</span><span class="sxs-lookup"><span data-stu-id="92bf9-104">Getting the Status of a Restart Manager Operation</span></span>

<span data-ttu-id="92bf9-105">Quando muitos aplicativos e serviços devem ser desligados ou reiniciados, a operação do Gerenciador de reinicialização pode levar um longo período de tempo.</span><span class="sxs-lookup"><span data-stu-id="92bf9-105">When many applications and services must be shut down or restarted, the Restart Manager operation can take an extended period of time.</span></span> <span data-ttu-id="92bf9-106">O método a seguir pode ser usado para obter o status da operação atual.</span><span class="sxs-lookup"><span data-stu-id="92bf9-106">The following method can be used to obtain the status of the current operation.</span></span>

<span data-ttu-id="92bf9-107">**Para obter o status da operação atual do Gerenciador de reinicialização**</span><span class="sxs-lookup"><span data-stu-id="92bf9-107">**To get the status of the current Restart Manager operation**</span></span>

1.  <span data-ttu-id="92bf9-108">O instalador deve implementar uma função de retorno de chamada de status de gravação do RM que determina o status dos aplicativos que foram desligados ou reiniciados. [**\_ \_ \_**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback)</span><span class="sxs-lookup"><span data-stu-id="92bf9-108">The installer should implement a [**RM\_WRITE\_STATUS\_CALLBACK**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) function that determines the status of the applications that have been shut down or restarted.</span></span> <span data-ttu-id="92bf9-109">A função pode fornecer as informações para a interface do usuário ou o log.</span><span class="sxs-lookup"><span data-stu-id="92bf9-109">The function can provide the information to the user interface or log.</span></span>
2.  <span data-ttu-id="92bf9-110">O instalador passa o ponteiro para a função de [**retorno de chamada de status de \_ gravação \_ \_ do RM**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) ao chamar a função [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) ou [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) .</span><span class="sxs-lookup"><span data-stu-id="92bf9-110">The installer passes the pointer to the [**RM\_WRITE\_STATUS\_CALLBACK**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) function when calling the [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) or [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) function.</span></span>

 

 