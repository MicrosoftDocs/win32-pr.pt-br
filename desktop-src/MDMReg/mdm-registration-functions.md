---
title: Funções de registro do MDM
description: As funções a seguir são usadas pelo registro do MDM.
ms.assetid: 1b063a56-f59f-4b02-949f-c8b6bbf45a13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821e08d9c6631bbb300a86ab6b9c480a3af0c25b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104294551"
---
# <a name="mdm-registration-functions"></a><span data-ttu-id="526ed-103">Funções de registro do MDM</span><span class="sxs-lookup"><span data-stu-id="526ed-103">MDM Registration Functions</span></span>

<span data-ttu-id="526ed-104">As funções a seguir são usadas pelo registro do MDM.</span><span class="sxs-lookup"><span data-stu-id="526ed-104">The following functions are used by MDM Registration.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="526ed-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="526ed-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="526ed-106">**DiscoverManagementService**</span><span class="sxs-lookup"><span data-stu-id="526ed-106">**DiscoverManagementService**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-discovermanagementservice)
</dt> <dd>

<span data-ttu-id="526ed-107">Descobre o serviço MDM.</span><span class="sxs-lookup"><span data-stu-id="526ed-107">Discovers the MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="526ed-108">**DiscoverManagementServiceEx**</span><span class="sxs-lookup"><span data-stu-id="526ed-108">**DiscoverManagementServiceEx**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-discovermanagementserviceex)
</dt> <dd>

<span data-ttu-id="526ed-109">Descobre o serviço MDM usando um servidor candidato.</span><span class="sxs-lookup"><span data-stu-id="526ed-109">Discovers the MDM service using a candidate server.</span></span>

</dd> <dt>

[<span data-ttu-id="526ed-110">**GetDeviceRegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="526ed-110">**GetDeviceRegistrationInfo**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-getdeviceregistrationinfo)
</dt> <dd>

<span data-ttu-id="526ed-111">Recupera as informações de registro do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="526ed-111">Retrieves the device registration information.</span></span>

</dd> <dt>

[<span data-ttu-id="526ed-112">**GetManagementAppHyperlink**</span><span class="sxs-lookup"><span data-stu-id="526ed-112">**GetManagementAppHyperlink**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-getmanagementapphyperlink)
</dt> <dd>

<span data-ttu-id="526ed-113">Recupera o hiperlink do aplicativo de gerenciamento associado ao serviço MDM.</span><span class="sxs-lookup"><span data-stu-id="526ed-113">Retrieves the management app hyperlink associated with the MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="526ed-114">**IsDeviceRegisteredWithManagement**</span><span class="sxs-lookup"><span data-stu-id="526ed-114">**IsDeviceRegisteredWithManagement**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-isdeviceregisteredwithmanagement)
</dt> <dd>

<span data-ttu-id="526ed-115">Verifica se o dispositivo está registrado com um serviço MDM.</span><span class="sxs-lookup"><span data-stu-id="526ed-115">Checks whether the device is registered with an MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="526ed-116">**IsManagementRegistrationAllowed**</span><span class="sxs-lookup"><span data-stu-id="526ed-116">**IsManagementRegistrationAllowed**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-ismanagementregistrationallowed)
</dt> <dd>

<span data-ttu-id="526ed-117">Verifica se o registro de MDM é permitido pela política local.</span><span class="sxs-lookup"><span data-stu-id="526ed-117">Checks whether MDM registration is allowed by local policy.</span></span>

</dd> <dt>

[<span data-ttu-id="526ed-118">**RegisterDeviceWithManagement**</span><span class="sxs-lookup"><span data-stu-id="526ed-118">**RegisterDeviceWithManagement**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagement)
</dt> <dd>

<span data-ttu-id="526ed-119">Registra um dispositivo com um serviço MDM, usando o [ \[ \] protocolo de registro de dispositivo móvel MS-MDE:](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267).</span><span class="sxs-lookup"><span data-stu-id="526ed-119">Registers a device with a MDM service, using the [\[MS-MDE\]: Mobile Device Enrollment Protocol](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267).</span></span>

</dd> <dt>

[<span data-ttu-id="526ed-120">**RegisterDeviceWithManagementUsingAADCredentials**</span><span class="sxs-lookup"><span data-stu-id="526ed-120">**RegisterDeviceWithManagementUsingAADCredentials**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagementusingaadcredentials)
</dt> <dd>

<span data-ttu-id="526ed-121">Registra um dispositivo com um serviço MDM, usando as credenciais do Azure Active Directory (AAD).</span><span class="sxs-lookup"><span data-stu-id="526ed-121">Registers a device with a MDM service, using Azure Active Directory (AAD) credentials.</span></span>

</dd> <dt>

[<span data-ttu-id="526ed-122">**SetManagedExternally**</span><span class="sxs-lookup"><span data-stu-id="526ed-122">**SetManagedExternally**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally)
</dt> <dd>

<span data-ttu-id="526ed-123">Indica ao agente MDM que o dispositivo é gerenciado externamente e não deve ser registrado com um serviço MDM.</span><span class="sxs-lookup"><span data-stu-id="526ed-123">Indicates to the MDM agent that the device is managed externally and is not to be registered with an MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="526ed-124">**UnregisterDeviceWithManagement**</span><span class="sxs-lookup"><span data-stu-id="526ed-124">**UnregisterDeviceWithManagement**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-unregisterdevicewithmanagement)
</dt> <dd>

<span data-ttu-id="526ed-125">Cancela o registro de um dispositivo com o serviço MDM</span><span class="sxs-lookup"><span data-stu-id="526ed-125">Unregisters a device with the MDM service</span></span>

</dd> </dl>

 

 