---
description: As notificações a seguir são usadas com as funções SetupInstallFile, SetupInstallFileEx e SetupInstallFromInfSection. Para obter mais informações sobre o formato e o uso de notificações, consulte notificações.
ms.assetid: 095cf4c9-3cb9-4b95-a8a2-9312c134e721
title: Notificações de arquivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f58863d48c1af809c0cbbcdc2d625214a6e90a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921840"
---
# <a name="inf-file-notifications"></a><span data-ttu-id="22838-104">Notificações de arquivo INF</span><span class="sxs-lookup"><span data-stu-id="22838-104">INF File Notifications</span></span>

<span data-ttu-id="22838-105">As notificações a seguir são usadas com as funções [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea), [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)e [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) .</span><span class="sxs-lookup"><span data-stu-id="22838-105">The following notifications are used with the [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea), [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa), and [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) functions.</span></span> <span data-ttu-id="22838-106">Para obter mais informações sobre o formato e o uso de notificações, consulte [notificações](notifications.md).</span><span class="sxs-lookup"><span data-stu-id="22838-106">For more information about the format and use of notifications, see [Notifications](notifications.md).</span></span>



| <span data-ttu-id="22838-107">Notificação</span><span class="sxs-lookup"><span data-stu-id="22838-107">Notification</span></span>                                                      | <span data-ttu-id="22838-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="22838-108">Description</span></span>                                                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="22838-109">**SPFILENOTIFY \_ FILEOPDELAYED**</span><span class="sxs-lookup"><span data-stu-id="22838-109">**SPFILENOTIFY\_FILEOPDELAYED**</span></span>](spfilenotify-fileopdelayed.md) | <span data-ttu-id="22838-110">O arquivo está em uso e a operação atual é atrasada até que o sistema seja reinicializado.</span><span class="sxs-lookup"><span data-stu-id="22838-110">The file is in use, and the current operation is delayed until the system is rebooted.</span></span> |
| [<span data-ttu-id="22838-111">**SPFILENOTIFY \_ LANGMISMATCH**</span><span class="sxs-lookup"><span data-stu-id="22838-111">**SPFILENOTIFY\_LANGMISMATCH**</span></span>](spfilenotify-langmismatch.md)   | <span data-ttu-id="22838-112">O idioma do arquivo atual não corresponde ao idioma do sistema.</span><span class="sxs-lookup"><span data-stu-id="22838-112">The language of the current file does not match the system language.</span></span>                   |
| [<span data-ttu-id="22838-113">**SPFILENOTIFY \_ TARGETEXISTS**</span><span class="sxs-lookup"><span data-stu-id="22838-113">**SPFILENOTIFY\_TARGETEXISTS**</span></span>](spfilenotify-targetexists.md)   | <span data-ttu-id="22838-114">Já existe uma cópia do arquivo especificado no destino.</span><span class="sxs-lookup"><span data-stu-id="22838-114">A copy of the specified file already exists on the target.</span></span>                             |
| [<span data-ttu-id="22838-115">**SPFILENOTIFY \_ TARGETNEWER**</span><span class="sxs-lookup"><span data-stu-id="22838-115">**SPFILENOTIFY\_TARGETNEWER**</span></span>](spfilenotify-targetnewer.md)     | <span data-ttu-id="22838-116">Existe uma versão mais recente do arquivo especificado no destino.</span><span class="sxs-lookup"><span data-stu-id="22838-116">A newer version of the specified file exists on the target.</span></span>                            |



 

> [!Note]  
> <span data-ttu-id="22838-117">Como o [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) cria e confirma uma fila de arquivos interna, ele também usa as [notificações de fila de arquivos](file-queue-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="22838-117">Because [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) creates and commits an internal file queue, it also uses the [File Queue Notifications](file-queue-notifications.md).</span></span>

 

 

 



