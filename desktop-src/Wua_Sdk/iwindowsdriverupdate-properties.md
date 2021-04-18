---
description: A interface IWindowsDriverUpdate define as propriedades a seguir.
ms.assetid: 2177c5e0-47db-44ae-a0ce-2544ff2d0855
title: Propriedades de IWindowsDriverUpdate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291d7933cf3e73dee6f47edab3240c4ebd14f454
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761842"
---
# <a name="iwindowsdriverupdate-properties"></a><span data-ttu-id="bc3fb-103">Propriedades de IWindowsDriverUpdate</span><span class="sxs-lookup"><span data-stu-id="bc3fb-103">IWindowsDriverUpdate Properties</span></span>

<span data-ttu-id="bc3fb-104">A interface [**IWindowsDriverUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate) define as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-104">The [**IWindowsDriverUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate) interface defines the following properties.</span></span>



| <span data-ttu-id="bc3fb-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="bc3fb-105">Property</span></span>                                                                                                    | <span data-ttu-id="bc3fb-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc3fb-106">Description</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc3fb-107">[](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_deviceproblemnumber)[**Endereço** DeviceProblemNumber](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_address)</span><span class="sxs-lookup"><span data-stu-id="bc3fb-107">[**DeviceProblemNumber**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_deviceproblemnumber)[**Address**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_address)</span></span> | <span data-ttu-id="bc3fb-108">Obtém o número do problema do dispositivo que corresponde à atualização de driver do Windows.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-108">Gets the problem number of the device that matches for the Windows driver update.</span></span>                     |
| [<span data-ttu-id="bc3fb-109">**DeviceStatus**</span><span class="sxs-lookup"><span data-stu-id="bc3fb-109">**DeviceStatus**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_devicestatus)                                                   | <span data-ttu-id="bc3fb-110">Obtém o status do dispositivo que corresponde à atualização de driver do Windows.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-110">Gets the status of the device that matches for the Windows driver update.</span></span>                             |
| [<span data-ttu-id="bc3fb-111">**DriverClass**</span><span class="sxs-lookup"><span data-stu-id="bc3fb-111">**DriverClass**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driverclass)                                                     | <span data-ttu-id="bc3fb-112">Obtém a classe da atualização de driver do Windows.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-112">Gets the class of the Windows driver update.</span></span>                                                          |
| [<span data-ttu-id="bc3fb-113">**DriverHardwareID**</span><span class="sxs-lookup"><span data-stu-id="bc3fb-113">**DriverHardwareID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driverhardwareid)                                           | <span data-ttu-id="bc3fb-114">Obtém a ID de hardware ou a ID compatível à qual a atualização de driver do Windows deve corresponder para ser instalada.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-114">Gets the hardware ID or compatible ID that the Windows driver update must match to be installable.</span></span>    |
| [<span data-ttu-id="bc3fb-115">**DriverManufacturer**</span><span class="sxs-lookup"><span data-stu-id="bc3fb-115">**DriverManufacturer**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_drivermanufacturer)                                       | <span data-ttu-id="bc3fb-116">Obtém o nome invariável de idioma do fabricante da atualização de driver do Windows.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-116">Gets the language-invariant name of the manufacturer of the Windows driver update.</span></span>                    |
| [<span data-ttu-id="bc3fb-117">**DriverModel**</span><span class="sxs-lookup"><span data-stu-id="bc3fb-117">**DriverModel**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_drivermodel)                                                     | <span data-ttu-id="bc3fb-118">Obtém o nome do modelo invariável de idioma do dispositivo para o qual a atualização de driver do Windows se destina.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-118">Gets the language-invariant model name of the device for which the Windows driver update is intended.</span></span> |
| [<span data-ttu-id="bc3fb-119">**Driverprovider**</span><span class="sxs-lookup"><span data-stu-id="bc3fb-119">**DriverProvider**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driverprovider)                                               | <span data-ttu-id="bc3fb-120">Obtém o nome invariável de idioma do provedor da atualização de driver do Windows.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-120">Gets the language-invariant name of the provider of the Windows driver update.</span></span>                        |
| [<span data-ttu-id="bc3fb-121">**DriverVerDate**</span><span class="sxs-lookup"><span data-stu-id="bc3fb-121">**DriverVerDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driververdate)                                                 | <span data-ttu-id="bc3fb-122">Obtém a data da versão do driver da atualização do driver do Windows.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-122">Gets the driver version date of the Windows driver update.</span></span>                                            |



 

 

 



