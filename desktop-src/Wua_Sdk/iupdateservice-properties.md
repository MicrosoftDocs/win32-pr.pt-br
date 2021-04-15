---
description: A interface IUpdateService define as propriedades a seguir.
ms.assetid: 33bc28e8-0b83-4d58-a03e-ccf2a97887e6
title: Propriedades de IUpdateService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ff3cf92c89a5ba02b7d95f1a1c99f33de3202d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461162"
---
# <a name="iupdateservice-properties"></a><span data-ttu-id="46054-103">Propriedades de IUpdateService</span><span class="sxs-lookup"><span data-stu-id="46054-103">IUpdateService Properties</span></span>

<span data-ttu-id="46054-104">A interface [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) define as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="46054-104">The [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) interface defines the following properties.</span></span>



| <span data-ttu-id="46054-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="46054-105">Property</span></span>                                                              | <span data-ttu-id="46054-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="46054-106">Description</span></span>                                                                                     |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46054-107">**CanRegisterWithAU**</span><span class="sxs-lookup"><span data-stu-id="46054-107">**CanRegisterWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_canregisterwithau)         | <span data-ttu-id="46054-108">Obtém um valor booliano que indica se o serviço pode ser registrado com Atualizações Automáticas.</span><span class="sxs-lookup"><span data-stu-id="46054-108">Gets a Boolean value that indicates whether the service can register with Automatic Updates.</span></span>    |
| [<span data-ttu-id="46054-109">**ContentValidationCert**</span><span class="sxs-lookup"><span data-stu-id="46054-109">**ContentValidationCert**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_contentvalidationcert) | <span data-ttu-id="46054-110">Obtém um hash SHA-1 do certificado que é usado para assinar o conteúdo do serviço.</span><span class="sxs-lookup"><span data-stu-id="46054-110">Gets an SHA-1 hash of the certificate that is used to sign the contents of the service.</span></span>         |
| [<span data-ttu-id="46054-111">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="46054-111">**ExpirationDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_expirationdate)               | <span data-ttu-id="46054-112">Obtém a data em que o arquivo de gabinete de autorização expira.</span><span class="sxs-lookup"><span data-stu-id="46054-112">Gets the date on which the authorization cabinet file expires.</span></span>                                  |
| [<span data-ttu-id="46054-113">**IsManaged**</span><span class="sxs-lookup"><span data-stu-id="46054-113">**IsManaged**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_ismanaged)                         | <span data-ttu-id="46054-114">Obtém um valor booliano que indica se um serviço é um serviço gerenciado.</span><span class="sxs-lookup"><span data-stu-id="46054-114">Gets a Boolean value that indicates whether a service is a managed service.</span></span>                     |
| [<span data-ttu-id="46054-115">**IsRegisteredWithAU**</span><span class="sxs-lookup"><span data-stu-id="46054-115">**IsRegisteredWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_isregisteredwithau)       | <span data-ttu-id="46054-116">Obtém um valor booliano que indica se um serviço está registrado com Atualizações Automáticas.</span><span class="sxs-lookup"><span data-stu-id="46054-116">Gets a Boolean value that indicates whether a service is registered with Automatic Updates.</span></span>     |
| [<span data-ttu-id="46054-117">**IsScanPackageService**</span><span class="sxs-lookup"><span data-stu-id="46054-117">**IsScanPackageService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_isscanpackageservice)   | <span data-ttu-id="46054-118">Obtém um valor booliano que indica se um serviço é baseado em um pacote de verificação.</span><span class="sxs-lookup"><span data-stu-id="46054-118">Gets a Boolean value that indicates whether a service is based on a scan package.</span></span>               |
| [<span data-ttu-id="46054-119">**Emitido**</span><span class="sxs-lookup"><span data-stu-id="46054-119">**IssueDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_issuedate)                         | <span data-ttu-id="46054-120">Obtém a data em que o arquivo de gabinete de autorização foi emitido.</span><span class="sxs-lookup"><span data-stu-id="46054-120">Gets the date on which the authorization cabinet file was issued.</span></span>                               |
| [<span data-ttu-id="46054-121">**Nome**</span><span class="sxs-lookup"><span data-stu-id="46054-121">**Name**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_name)                                   | <span data-ttu-id="46054-122">Obtém o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="46054-122">Gets the name of the service.</span></span>                                                                   |
| [<span data-ttu-id="46054-123">**OffersWindowsUpdates**</span><span class="sxs-lookup"><span data-stu-id="46054-123">**OffersWindowsUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_offerswindowsupdates)   | <span data-ttu-id="46054-124">Obtém um valor booliano que indica se o serviço atual oferece atualizações de atualizações do Windows.</span><span class="sxs-lookup"><span data-stu-id="46054-124">Gets a Boolean value indicates whether the current service offers updates from Windows Updates.</span></span> |
| [<span data-ttu-id="46054-125">**RedirectUrls**</span><span class="sxs-lookup"><span data-stu-id="46054-125">**RedirectUrls**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_redirecturls)                   | <span data-ttu-id="46054-126">Obtém a URL para o arquivo de gabinete do redirecionador.</span><span class="sxs-lookup"><span data-stu-id="46054-126">Gets the URL for the redirector cabinet file.</span></span>                                                   |
| [<span data-ttu-id="46054-127">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="46054-127">**ServiceID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_serviceid)                         | <span data-ttu-id="46054-128">Obtém o identificador de um serviço.</span><span class="sxs-lookup"><span data-stu-id="46054-128">Gets the identifier for a service.</span></span>                                                              |
| [<span data-ttu-id="46054-129">**ServiceUrl**</span><span class="sxs-lookup"><span data-stu-id="46054-129">**ServiceUrl**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_serviceurl)                       | <span data-ttu-id="46054-130">Obtém a URL para o serviço.</span><span class="sxs-lookup"><span data-stu-id="46054-130">Gets the URL for the service.</span></span>                                                                   |
| [<span data-ttu-id="46054-131">**SetupPrefix**</span><span class="sxs-lookup"><span data-stu-id="46054-131">**SetupPrefix**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_setupprefix)                     | <span data-ttu-id="46054-132">Obtém o prefixo dos arquivos de instalação.</span><span class="sxs-lookup"><span data-stu-id="46054-132">Gets the prefix for the setup files.</span></span>                                                            |



 

 

 



