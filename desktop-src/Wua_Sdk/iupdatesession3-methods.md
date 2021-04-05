---
description: A interface IUpdateSession3 define os métodos a seguir.
ms.assetid: 8015443a-e232-44ab-b53a-e8cc4acd4dd3
title: Métodos IUpdateSession3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd4126d8bae9e1ba768e574fd9520bdb6cf3d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089934"
---
# <a name="iupdatesession3-methods"></a><span data-ttu-id="3c36d-103">Métodos IUpdateSession3</span><span class="sxs-lookup"><span data-stu-id="3c36d-103">IUpdateSession3 Methods</span></span>

<span data-ttu-id="3c36d-104">A interface [**IUpdateSession3**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession3) define os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="3c36d-104">The [**IUpdateSession3**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession3) interface defines the following methods.</span></span>



| <span data-ttu-id="3c36d-105">Método</span><span class="sxs-lookup"><span data-stu-id="3c36d-105">Method</span></span>                                                                           | <span data-ttu-id="3c36d-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="3c36d-106">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c36d-107">**CreateUpdateServiceManager**</span><span class="sxs-lookup"><span data-stu-id="3c36d-107">**CreateUpdateServiceManager**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-createupdateservicemanager) | <span data-ttu-id="3c36d-108">Retorna um ponteiro para uma interface [**IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) para a sessão.</span><span class="sxs-lookup"><span data-stu-id="3c36d-108">Returns a pointer to an [**IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) interface for the session.</span></span>                                                                                                                                                                                                                |
| [<span data-ttu-id="3c36d-109">**QueryHistory**</span><span class="sxs-lookup"><span data-stu-id="3c36d-109">**QueryHistory**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory)                             | <span data-ttu-id="3c36d-110">Retorna um ponteiro para uma interface [**IUpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) .</span><span class="sxs-lookup"><span data-stu-id="3c36d-110">Returns a pointer to an [**IUpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) interface.</span></span> <span data-ttu-id="3c36d-111">A interface contém registros de eventos correspondentes no computador.</span><span class="sxs-lookup"><span data-stu-id="3c36d-111">The interface contains matching event records on the computer.</span></span> <span data-ttu-id="3c36d-112">Isso faz com que o método [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory) consulte de forma síncrona o computador para o histórico de eventos de atualização.</span><span class="sxs-lookup"><span data-stu-id="3c36d-112">This causes the [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory) method to synchronously query the computer for the history of update events.</span></span> |



 

<span data-ttu-id="3c36d-113">Para obter informações sobre os membros herdados por essa interface, consulte as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="3c36d-113">For information about the members inherited by this interface, see the following interfaces:</span></span>

-   [<span data-ttu-id="3c36d-114">**IUpdateSession2**</span><span class="sxs-lookup"><span data-stu-id="3c36d-114">**IUpdateSession2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [<span data-ttu-id="3c36d-115">**IUpdateSession**</span><span class="sxs-lookup"><span data-stu-id="3c36d-115">**IUpdateSession**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)

 

 



