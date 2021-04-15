---
description: Interfaces usadas com cotas de disco.
ms.assetid: 422d93d9-f4aa-428d-94c1-fdf2dcf4c974
title: Interfaces de cota de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bbcd4240a6a5910942aad71c7ea080da40918a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461285"
---
# <a name="disk-quota-interfaces"></a><span data-ttu-id="9a7fa-103">Interfaces de cota de disco</span><span class="sxs-lookup"><span data-stu-id="9a7fa-103">Disk Quota Interfaces</span></span>

<span data-ttu-id="9a7fa-104">As interfaces a seguir são usadas com cotas de disco.</span><span class="sxs-lookup"><span data-stu-id="9a7fa-104">The following interfaces are used with disk quotas.</span></span>



| <span data-ttu-id="9a7fa-105">Interface</span><span class="sxs-lookup"><span data-stu-id="9a7fa-105">Interface</span></span>                                          | <span data-ttu-id="9a7fa-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a7fa-106">Description</span></span>                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a7fa-107">**IDiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="9a7fa-107">**IDiskQuotaControl**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)     | <span data-ttu-id="9a7fa-108">Controla os recursos de cota de disco de um único volume do sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="9a7fa-108">Controls the disk quota facilities of a single NTFS file system volume.</span></span><br/>                             |
| [<span data-ttu-id="9a7fa-109">**IDiskQuotaEvents**</span><span class="sxs-lookup"><span data-stu-id="9a7fa-109">**IDiskQuotaEvents**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)       | <span data-ttu-id="9a7fa-110">Recebe notificações de eventos relacionadas à cota.</span><span class="sxs-lookup"><span data-stu-id="9a7fa-110">Receives quota-related event notifications.</span></span><br/>                                                         |
| [<span data-ttu-id="9a7fa-111">**IDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="9a7fa-111">**IDiskQuotaUser**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)           | <span data-ttu-id="9a7fa-112">Representa uma entrada de cota de usuário único no arquivo de informações de cota de volume.</span><span class="sxs-lookup"><span data-stu-id="9a7fa-112">Represents a single user quota entry in the volume quota information file.</span></span><br/>                          |
| [<span data-ttu-id="9a7fa-113">**IDiskQuotaUserBatch**</span><span class="sxs-lookup"><span data-stu-id="9a7fa-113">**IDiskQuotaUserBatch**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch) | <span data-ttu-id="9a7fa-114">Adiciona vários objetos de usuário de cota a um contêiner que é enviado para atualização em uma única chamada.</span><span class="sxs-lookup"><span data-stu-id="9a7fa-114">Adds multiple quota user objects to a container that is then submitted for update in a single call.</span></span><br/> |
| [<span data-ttu-id="9a7fa-115">**IEnumDiskQuotaUsers**</span><span class="sxs-lookup"><span data-stu-id="9a7fa-115">**IEnumDiskQuotaUsers**</span></span>](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers) | <span data-ttu-id="9a7fa-116">Enumera as entradas de cota do usuário no volume.</span><span class="sxs-lookup"><span data-stu-id="9a7fa-116">Enumerates user quota entries on the volume.</span></span><br/>                                                        |



 

 

