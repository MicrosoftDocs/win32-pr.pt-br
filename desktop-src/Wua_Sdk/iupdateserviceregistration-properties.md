---
description: A interface IUpdateServiceRegistration define as propriedades a seguir.
ms.assetid: 2bcde8b4-7bff-4887-8080-89da817afb5f
title: Propriedades de IUpdateServiceRegistration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716c06f2fc8ed9a7ce12542a09440cf0ec0b5c49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811438"
---
# <a name="iupdateserviceregistration-properties"></a><span data-ttu-id="419c8-103">Propriedades de IUpdateServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="419c8-103">IUpdateServiceRegistration Properties</span></span>

<span data-ttu-id="419c8-104">A interface **IUpdateServiceRegistration** define as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="419c8-104">The **IUpdateServiceRegistration** interface defines the following properties.</span></span>



| <span data-ttu-id="419c8-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="419c8-105">Property</span></span>                                                                                      | <span data-ttu-id="419c8-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="419c8-106">Description</span></span>                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="419c8-107">**IsPendingRegistrationWithAU**</span><span class="sxs-lookup"><span data-stu-id="419c8-107">**IsPendingRegistrationWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_ispendingregistrationwithau) | <span data-ttu-id="419c8-108">Obtém um valor booliano que indica se o serviço também será registrado com Atualizações Automáticas, quando adicionado.</span><span class="sxs-lookup"><span data-stu-id="419c8-108">Gets a Boolean value that indicates whether the service will also be registered with Automatic Updates, when added.</span></span>                                  |
| [<span data-ttu-id="419c8-109">**RegistrationState**</span><span class="sxs-lookup"><span data-stu-id="419c8-109">**RegistrationState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_registrationstate)                     | <span data-ttu-id="419c8-110">Obtém um valor de [**UpdateServiceRegistrationState**](/windows/win32/api/wuapi/ne-wuapi-updateserviceregistrationstate) que indica o estado atual do registro de serviço.</span><span class="sxs-lookup"><span data-stu-id="419c8-110">Gets an [**UpdateServiceRegistrationState**](/windows/win32/api/wuapi/ne-wuapi-updateserviceregistrationstate) value that indicates the current state of the service registration.</span></span> |
| [<span data-ttu-id="419c8-111">**Serviço**</span><span class="sxs-lookup"><span data-stu-id="419c8-111">**Service**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_service)                                         | <span data-ttu-id="419c8-112">Obtém um ponteiro para uma interface [**IUpdateService2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice2) .</span><span class="sxs-lookup"><span data-stu-id="419c8-112">Gets a pointer to an [**IUpdateService2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice2) interface.</span></span> <span data-ttu-id="419c8-113">Essa propriedade é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="419c8-113">This property is the default property.</span></span>                                    |



 

 

 



