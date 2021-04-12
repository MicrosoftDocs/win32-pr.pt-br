---
description: Interfaces usadas no gerenciamento de disco.
ms.assetid: c1f79e2e-834b-41dc-a15f-6dd1034d021b
title: Interfaces de gerenciamento de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c86881ff3bf6232da68c4cf1539dbbedf87c50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171144"
---
# <a name="disk-management-interfaces"></a><span data-ttu-id="573fb-103">Interfaces de gerenciamento de disco</span><span class="sxs-lookup"><span data-stu-id="573fb-103">Disk Management Interfaces</span></span>

<span data-ttu-id="573fb-104">As interfaces a seguir são usadas no gerenciamento de disco.</span><span class="sxs-lookup"><span data-stu-id="573fb-104">The following interfaces are used in disk management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="573fb-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="573fb-105">In this section</span></span>



| <span data-ttu-id="573fb-106">Interface</span><span class="sxs-lookup"><span data-stu-id="573fb-106">Interface</span></span>                                                     | <span data-ttu-id="573fb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="573fb-107">Description</span></span>                                                                                                    |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="573fb-108">**IDiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="573fb-108">**IDiskQuotaControl**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)<br/>     | <span data-ttu-id="573fb-109">Controla os recursos de cota de disco de um único volume do sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="573fb-109">Controls the disk quota facilities of a single NTFS file system volume.</span></span><br/>                             |
| [<span data-ttu-id="573fb-110">**IDiskQuotaEvents**</span><span class="sxs-lookup"><span data-stu-id="573fb-110">**IDiskQuotaEvents**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)<br/>       | <span data-ttu-id="573fb-111">Recebe notificações de eventos relacionadas à cota.</span><span class="sxs-lookup"><span data-stu-id="573fb-111">Receives quota-related event notifications.</span></span><br/>                                                         |
| [<span data-ttu-id="573fb-112">**IDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="573fb-112">**IDiskQuotaUser**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)<br/>           | <span data-ttu-id="573fb-113">Representa uma entrada de cota de usuário único no arquivo de informações de cota de volume.</span><span class="sxs-lookup"><span data-stu-id="573fb-113">Represents a single user quota entry in the volume quota information file.</span></span><br/>                          |
| [<span data-ttu-id="573fb-114">**IDiskQuotaUserBatch**</span><span class="sxs-lookup"><span data-stu-id="573fb-114">**IDiskQuotaUserBatch**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch)<br/> | <span data-ttu-id="573fb-115">Adiciona vários objetos de usuário de cota a um contêiner que é enviado para atualização em uma única chamada.</span><span class="sxs-lookup"><span data-stu-id="573fb-115">Adds multiple quota user objects to a container that is then submitted for update in a single call.</span></span><br/> |
| [<span data-ttu-id="573fb-116">**IEnumDiskQuotaUsers**</span><span class="sxs-lookup"><span data-stu-id="573fb-116">**IEnumDiskQuotaUsers**</span></span>](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers)<br/> | <span data-ttu-id="573fb-117">Enumera as entradas de cota do usuário no volume.</span><span class="sxs-lookup"><span data-stu-id="573fb-117">Enumerates user quota entries on the volume.</span></span><br/>                                                        |



 

 

