---
title: Obtendo informações do sistema MCI
description: Obtendo informações do sistema MCI
ms.assetid: 06175d6e-6d09-4c95-93e9-03af870a2d3f
keywords:
- MCI_SYSINFO comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b5f5d2bf8cc8edd3edf65a9c559b6ec47b0631
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916174"
---
# <a name="obtaining-mci-system-information"></a><span data-ttu-id="a0269-104">Obtendo informações do sistema MCI</span><span class="sxs-lookup"><span data-stu-id="a0269-104">Obtaining MCI System Information</span></span>

<span data-ttu-id="a0269-105">O comando [sysinfo](sysinfo.md) (do [**MCI do \_ sysinfo**](mci-sysinfo.md)) obtém informações do sistema sobre dispositivos MCI.</span><span class="sxs-lookup"><span data-stu-id="a0269-105">The [sysinfo](sysinfo.md) ([**MCI\_SYSINFO**](mci-sysinfo.md)) command obtains system information about MCI devices.</span></span> <span data-ttu-id="a0269-106">O MCI manipula esse comando sem retransmiti-lo para qualquer dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="a0269-106">MCI handles this command without relaying it to any MCI device.</span></span> <span data-ttu-id="a0269-107">Para a interface de mensagem de comando, o MCI retorna as informações do sistema na estrutura de [**\_ \_ parâmetros do sysinfo do MCI**](mci-sysinfo-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a0269-107">For the command-message interface, MCI returns the system information in the [**MCI\_SYSINFO\_PARMS**](mci-sysinfo-parms.md) structure.</span></span>

<span data-ttu-id="a0269-108">Você pode usar o comando **sysinfo** (do MCI do \_ sysinfo) para recuperar informações como o número de dispositivos MCI em um sistema, o número de dispositivos MCI de um tipo específico, o número de dispositivos MCI abertos e os nomes dos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a0269-108">You can use the **sysinfo** (MCI\_SYSINFO) command to retrieve information such as the number of MCI devices on a system, the number of MCI devices of a particular type, the number of open MCI devices, and the names of the devices.</span></span> <span data-ttu-id="a0269-109">Esse comando geralmente é chamado mais de uma vez para recuperar uma determinada informação.</span><span class="sxs-lookup"><span data-stu-id="a0269-109">This command is often called more than once to retrieve a particular piece of information.</span></span> <span data-ttu-id="a0269-110">Por exemplo, você pode recuperar o número de dispositivos de um tipo específico na primeira chamada e, em seguida, enumerar os nomes dos dispositivos no próximo.</span><span class="sxs-lookup"><span data-stu-id="a0269-110">For example, you might retrieve the number of devices of a particular type in the first call and then enumerate the names of the devices in the next.</span></span>

 

 




