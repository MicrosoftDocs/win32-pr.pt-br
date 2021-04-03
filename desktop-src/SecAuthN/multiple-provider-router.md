---
description: O roteador de vários provedores (MPR) lida com a comunicação entre o sistema operacional Windows e os provedores de rede instalados. Ele permite que o Windows apresente uma rede integrada ao usuário.
ms.assetid: 3f473273-f696-45f7-afbf-fd55f974ba48
title: Roteador de vários provedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa7c4e76901c31e3b5dc7f329a23838aba4f7be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829453"
---
# <a name="multiple-provider-router"></a><span data-ttu-id="fefc9-104">Roteador de vários provedores</span><span class="sxs-lookup"><span data-stu-id="fefc9-104">Multiple Provider Router</span></span>

<span data-ttu-id="fefc9-105">O [*roteador de vários provedores*](../secgloss/m-gly.md) (MPR) lida com a comunicação entre o sistema operacional Windows e os provedores de rede instalados.</span><span class="sxs-lookup"><span data-stu-id="fefc9-105">The [*Multiple Provider Router*](../secgloss/m-gly.md) (MPR) handles communication between the Windows operating system and the installed network providers.</span></span> <span data-ttu-id="fefc9-106">Ele permite que o Windows apresente uma rede integrada ao usuário.</span><span class="sxs-lookup"><span data-stu-id="fefc9-106">It enables Windows to present an integrated network to the user.</span></span>

<span data-ttu-id="fefc9-107">Quando o MPR é iniciado, ele verifica o registro para determinar quais provedores de rede estão instalados no sistema e a ordem em que eles devem ser alternados.</span><span class="sxs-lookup"><span data-stu-id="fefc9-107">When the MPR starts, it checks the registry to determine which network providers are installed on the system and the order they should be cycled through.</span></span> <span data-ttu-id="fefc9-108">Ele carrega todas as DLLs de provedor de rede registradas e as usa para processar chamadas WNet subsequentes feitas pela interface do usuário ou por outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="fefc9-108">It loads all registered network provider DLLs and uses them to process subsequent WNet calls made by the user interface or other applications.</span></span>

<span data-ttu-id="fefc9-109">Para obter mais informações sobre as funções do WNet, consulte [sistema de rede do Windows](../wnet/windows-networking-wnet-.md).</span><span class="sxs-lookup"><span data-stu-id="fefc9-109">For more information about WNet functions, see [Windows Networking](../wnet/windows-networking-wnet-.md).</span></span>

 

 
