---
title: Recuperando informações sobre um dispositivo
description: Recuperando informações sobre um dispositivo
ms.assetid: d038d3fb-43d0-4d9d-836c-205f6d8c98e3
keywords:
- MCI_GETDEVCAPS comando
- MCI_STATUS comando
- MCI_INFO comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10acb53fa1a961fe7a70042350f8d889d9fdf572
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916594"
---
# <a name="retrieving-information-about-a-device"></a><span data-ttu-id="8799b-106">Recuperando informações sobre um dispositivo</span><span class="sxs-lookup"><span data-stu-id="8799b-106">Retrieving Information About a Device</span></span>

<span data-ttu-id="8799b-107">Cada dispositivo responde aos comandos [**de recurso**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)), [**status**](status.md) ([**\_ status do MCI**](mci-status.md)) e [**informações**](info.md) ([**MCI \_ info**](mci-info.md)).</span><span class="sxs-lookup"><span data-stu-id="8799b-107">Every device responds to the [**capability**](capability.md) ([**MCI\_GETDEVCAPS**](mci-getdevcaps.md)), [**status**](status.md) ([**MCI\_STATUS**](mci-status.md)), and [**info**](info.md) ([**MCI\_INFO**](mci-info.md)) commands.</span></span> <span data-ttu-id="8799b-108">Esses comandos obtêm informações sobre o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8799b-108">These commands obtain information about the device.</span></span> <span data-ttu-id="8799b-109">Por exemplo, o comando a seguir retornará "true" se um dispositivo **cdaudio** puder ejetar o disco:</span><span class="sxs-lookup"><span data-stu-id="8799b-109">For example, the following command returns "true" if a **cdaudio** device can eject the disc:</span></span>


```C++
mciSendString(
    "capability cdaudio can eject", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="8799b-110">Os sinalizadores listados para os comandos obrigatórios e básicos fornecem uma quantidade mínima de informações sobre um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8799b-110">The flags listed for the required and basic commands provide a minimum amount of information about a device.</span></span> <span data-ttu-id="8799b-111">Muitos dispositivos complementam os comandos obrigatórios e básicos com sinalizadores estendidos para fornecer informações adicionais sobre o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8799b-111">Many devices supplement the required and basic commands with extended flags to provide additional information about the device.</span></span>

 

 




