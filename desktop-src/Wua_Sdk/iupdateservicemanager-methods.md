---
description: A interface IUpdateServiceManager define os métodos a seguir.
ms.assetid: b2ae49bc-3fb6-4cb9-82ce-387409096159
title: Métodos IUpdateServiceManager
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 464b0b6e48d074dbc43f370f267fe7a526e8269b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501333"
---
# <a name="iupdateservicemanager-methods"></a><span data-ttu-id="0036c-103">Métodos IUpdateServiceManager</span><span class="sxs-lookup"><span data-stu-id="0036c-103">IUpdateServiceManager Methods</span></span>

<span data-ttu-id="0036c-104">A interface [**IUpdateServiceManager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager) define os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="0036c-104">The [**IUpdateServiceManager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager) interface defines the following methods.</span></span>



| <span data-ttu-id="0036c-105">Método</span><span class="sxs-lookup"><span data-stu-id="0036c-105">Method</span></span>                                                                           | <span data-ttu-id="0036c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="0036c-106">Description</span></span>                                                                                                                                      |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0036c-107">**AddScanPackageService**</span><span class="sxs-lookup"><span data-stu-id="0036c-107">**AddScanPackageService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice)     | <span data-ttu-id="0036c-108">Registra um pacote de verificação como um serviço com o Windows Update Agent (WUA) e, em seguida, retorna uma interface [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) .</span><span class="sxs-lookup"><span data-stu-id="0036c-108">Registers a scan package as a service with Windows Update Agent (WUA) and then returns an [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) interface.</span></span>    |
| [<span data-ttu-id="0036c-109">**AddService**</span><span class="sxs-lookup"><span data-stu-id="0036c-109">**AddService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)                           | <span data-ttu-id="0036c-110">Registra um serviço com WUA.</span><span class="sxs-lookup"><span data-stu-id="0036c-110">Registers a service with WUA.</span></span>                                                                                                                    |
| [<span data-ttu-id="0036c-111">**RegisterServiceWithAU**</span><span class="sxs-lookup"><span data-stu-id="0036c-111">**RegisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)     | <span data-ttu-id="0036c-112">Registra um serviço com Atualizações Automáticas.</span><span class="sxs-lookup"><span data-stu-id="0036c-112">Registers a service with Automatic Updates.</span></span>                                                                                                      |
| [<span data-ttu-id="0036c-113">**RemoveService**</span><span class="sxs-lookup"><span data-stu-id="0036c-113">**RemoveService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-removeservice)                     | <span data-ttu-id="0036c-114">Remove um registro de serviço do WUA.</span><span class="sxs-lookup"><span data-stu-id="0036c-114">Removes a service registration from WUA.</span></span>                                                                                                         |
| [<span data-ttu-id="0036c-115">**SetOption**</span><span class="sxs-lookup"><span data-stu-id="0036c-115">**SetOption**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-setoption)                             | <span data-ttu-id="0036c-116">Define opções para o objeto que especifica a ID de serviço e se é para exibir um aviso ao alterar o registro de Atualizações Automáticas.</span><span class="sxs-lookup"><span data-stu-id="0036c-116">Sets options for the object that specifies the service ID, and whether to display a warning when changing the registration of Automatic Updates.</span></span> |
| [<span data-ttu-id="0036c-117">**UnregisterServiceWithAU**</span><span class="sxs-lookup"><span data-stu-id="0036c-117">**UnregisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau) | <span data-ttu-id="0036c-118">Cancela o registro de um serviço com Atualizações Automáticas.</span><span class="sxs-lookup"><span data-stu-id="0036c-118">Unregisters a service with Automatic Updates.</span></span>                                                                                                    |



 

 

 



