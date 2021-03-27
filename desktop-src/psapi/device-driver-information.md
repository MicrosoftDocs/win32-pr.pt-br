---
title: Informações de driver de dispositivo
description: Drivers de dispositivo e módulos são semelhantes porque ambos são baseados em arquivos PE.
ms.assetid: 4f4ec15b-5592-4fe3-b754-fda25ab24159
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0735e791b8c6e1fc7434decc7ac71ccb5c1c469e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005142"
---
# <a name="device-driver-information"></a><span data-ttu-id="5609c-103">Informações de driver de dispositivo</span><span class="sxs-lookup"><span data-stu-id="5609c-103">Device Driver Information</span></span>

<span data-ttu-id="5609c-104">Drivers de dispositivo e módulos são semelhantes porque ambos são baseados em arquivos PE.</span><span class="sxs-lookup"><span data-stu-id="5609c-104">Device drivers and modules are similar in that they are both based on PE files.</span></span> <span data-ttu-id="5609c-105">No entanto, embora cada processo tenha sua própria lista privada de módulos carregados, os drivers de dispositivo têm módulos que são globais para o sistema.</span><span class="sxs-lookup"><span data-stu-id="5609c-105">However, while each process has its own private list of loaded modules, device drivers have modules that are global to the system.</span></span> <span data-ttu-id="5609c-106">Portanto, o PSAPI tem funções específicas para obter a lista de drivers de dispositivo e seus nomes.</span><span class="sxs-lookup"><span data-stu-id="5609c-106">Therefore, PSAPI has specific functions for obtaining the list of device drivers and their names.</span></span>

<span data-ttu-id="5609c-107">Você pode recuperar o endereço de carregamento para cada driver de dispositivo chamando a função [**EnumDeviceDrivers**](/windows/desktop/api/Psapi/nf-psapi-enumdevicedrivers) .</span><span class="sxs-lookup"><span data-stu-id="5609c-107">You can retrieve the load address for each device driver by calling the [**EnumDeviceDrivers**](/windows/desktop/api/Psapi/nf-psapi-enumdevicedrivers) function.</span></span> <span data-ttu-id="5609c-108">Essa função preenche uma matriz de valores **LPVOID** com os endereços de carga de todos os drivers de dispositivo no sistema.</span><span class="sxs-lookup"><span data-stu-id="5609c-108">This function fills an array of **LPVOID** values with the load addresses of all device drivers in the system.</span></span>

<span data-ttu-id="5609c-109">A função [**GetDeviceDriverBaseName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverbasenamea) usa um endereço de carregamento de driver como entrada e preenche um buffer com o nome base do driver (por exemplo, Win32k.sys).</span><span class="sxs-lookup"><span data-stu-id="5609c-109">The [**GetDeviceDriverBaseName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverbasenamea) function takes a driver load address as input and fills in a buffer with the base name of the driver (for example, Win32k.sys).</span></span> <span data-ttu-id="5609c-110">Uma função relacionada, [**GetDeviceDriverFileName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverfilenamea), usa os mesmos parâmetros e retorna o caminho para o driver de dispositivo (por exemplo, C: \\ Windows \\ System32 \\Win32k.sys).</span><span class="sxs-lookup"><span data-stu-id="5609c-110">A related function, [**GetDeviceDriverFileName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverfilenamea), takes the same parameters and returns the path to the device driver (for example, C:\\Windows\\System32\\Win32k.sys).</span></span>

 

 




