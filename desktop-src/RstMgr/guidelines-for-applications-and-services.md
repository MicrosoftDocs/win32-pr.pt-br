---
title: Diretrizes para aplicativos e serviços
description: Para reduzir o número de reinicializações do sistema ao instalar e atender aplicativos no Windows Vista ou no Windows Server 2008, você deve observar as diretrizes a seguir para permitir que seu aplicativo ou serviço seja desligado corretamente e reiniciado.
ms.assetid: d0b9344f-05c6-4054-90b9-86942df50b3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaf2963c03432a8b016f01316b79b387754f1459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105750205"
---
# <a name="guidelines-for-applications-and-services"></a><span data-ttu-id="33f6f-103">Diretrizes para aplicativos e serviços</span><span class="sxs-lookup"><span data-stu-id="33f6f-103">Guidelines for Applications and Services</span></span>

<span data-ttu-id="33f6f-104">Para reduzir o número de reinicializações do sistema ao instalar e atender aplicativos no Windows Vista ou no Windows Server 2008, você deve observar as diretrizes a seguir para permitir que seu aplicativo ou serviço seja desligado corretamente e reiniciado.</span><span class="sxs-lookup"><span data-stu-id="33f6f-104">To reduce the number of system restarts when installing and servicing applications on Windows Vista or Windows Server 2008, you should observe the following guidelines to enable your application or service to be shut down cleanly and restarted.</span></span>

-   <span data-ttu-id="33f6f-105">Seus aplicativos e serviços devem estar preparados para serem desligados e reiniciados pelo sistema quando for necessário instalar uma atualização.</span><span class="sxs-lookup"><span data-stu-id="33f6f-105">Your applications and services should be prepared to be shut down and restarted by the system when this is necessary to install an update.</span></span> <span data-ttu-id="33f6f-106">Normalmente, quando uma atualização é instalada, um aplicativo ou serviço precisa ser desligado porque atualmente ele contém um arquivo afetado em uso.</span><span class="sxs-lookup"><span data-stu-id="33f6f-106">Typically, when an update is installed, an application or service needs to be shut down because it currently holds an affected file in use.</span></span> <span data-ttu-id="33f6f-107">Todos os aplicativos ou serviços que podem manter um arquivo em uso durante uma atualização devem estar preparados para desligar corretamente.</span><span class="sxs-lookup"><span data-stu-id="33f6f-107">All applications or services that can hold a file in use during an update should be prepared to shut down cleanly.</span></span>
-   <span data-ttu-id="33f6f-108">Seus aplicativos devem salvar dados do usuário e informações de estado necessárias após uma reinicialização e devem aderir às diretrizes descritas na seção [diretrizes para aplicativos](guidelines-for-applications.md).</span><span class="sxs-lookup"><span data-stu-id="33f6f-108">Your applications should save user data and state information that are needed after a restart and should adhere to the guidelines that are described in the section [Guidelines for Applications](guidelines-for-applications.md).</span></span>
-   <span data-ttu-id="33f6f-109">Seus serviços devem aderir às diretrizes descritas na seção [diretrizes para serviços](guidelines-for-services.md).</span><span class="sxs-lookup"><span data-stu-id="33f6f-109">Your services should adhere to the guidelines that are described in the section [Guidelines for Services](guidelines-for-services.md).</span></span>
-   <span data-ttu-id="33f6f-110">O Gerenciador de reinicialização não encerra os [serviços críticos do sistema](critical-system-services.md); Portanto, esses serviços devem limitar o número de DLLs que dependem.</span><span class="sxs-lookup"><span data-stu-id="33f6f-110">Restart Manager does not shut down [critical system services](critical-system-services.md); therefore, these services should limit the number of DLLs they depend on.</span></span>

 

 




