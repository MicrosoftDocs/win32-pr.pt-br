---
description: Reenumerando e atualizando
ms.assetid: 67d34946-47df-43e2-8ca7-628d0671b869
title: Reenumerando e atualizando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a6302c817390ea2eb6bda3d5da0302c4bfefbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763184"
---
# <a name="reenumerating-and-refreshing"></a><span data-ttu-id="4dab9-103">Reenumerando e atualizando</span><span class="sxs-lookup"><span data-stu-id="4dab9-103">Reenumerating and Refreshing</span></span>

<span data-ttu-id="4dab9-104">\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4dab9-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="4dab9-105">A operação de reenumeração descobre os dispositivos recentemente conectados e recentemente desconectados.</span><span class="sxs-lookup"><span data-stu-id="4dab9-105">The reenumeration operation discovers newly connected and newly disconnected devices.</span></span> <span data-ttu-id="4dab9-106">A operação de atualização atualiza as informações de configuração dos dispositivos existentes.</span><span class="sxs-lookup"><span data-stu-id="4dab9-106">The refresh operation updates the configuration information of existing devices.</span></span>

<span data-ttu-id="4dab9-107">**Para reenumerar objetos de provedor de software**</span><span class="sxs-lookup"><span data-stu-id="4dab9-107">**To reenumerate software provider objects**</span></span>

-   <span data-ttu-id="4dab9-108">Chame o método [**IVdsService:: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) .</span><span class="sxs-lookup"><span data-stu-id="4dab9-108">Call the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method.</span></span> <span data-ttu-id="4dab9-109">Esse método descobre todos os discos recentemente conectados e desconectados e unidades de CD-ROM e garante que todos os discos tenham o proprietário adequado.</span><span class="sxs-lookup"><span data-stu-id="4dab9-109">This method discovers all newly connected and disconnected disks and CD-ROM drives, and ensures that all disks have the proper owner.</span></span> <span data-ttu-id="4dab9-110">O VDS possui discos brutos ou discos com falhas; o provedor básico possui discos básicos; e o provedor dinâmico possui discos dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="4dab9-110">VDS owns raw disks or disks with failures; the basic provider owns basic disks; and the dynamic provider owns dynamic disks.</span></span> <span data-ttu-id="4dab9-111">Essa operação pode envolver a verificação de barramentos de subsistema internos e a espera de tempos limite.</span><span class="sxs-lookup"><span data-stu-id="4dab9-111">This operation can involve scanning internal subsystem buses and waiting for time-outs.</span></span>

<span data-ttu-id="4dab9-112">**Para reenumerar e atualizar objetos do provedor de software**</span><span class="sxs-lookup"><span data-stu-id="4dab9-112">**To reenumerate and refresh software provider objects**</span></span>

-   <span data-ttu-id="4dab9-113">Chame o método [**IVdsService:: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) e, em seguida, chame o método [**IVdsService:: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) .</span><span class="sxs-lookup"><span data-stu-id="4dab9-113">Call the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method and then call the [**IVdsService::Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) method.</span></span> <span data-ttu-id="4dab9-114">Além de descobrir discos e unidades de CD-ROM recentemente conectados e desconectados, essa combinação de métodos atualiza todas as informações de disco, volume e Plex no cache do VDS para discos que não foram conectados ou desconectados recentemente.</span><span class="sxs-lookup"><span data-stu-id="4dab9-114">In addition to discovering newly connected and disconnected disks and CD-ROM drives, this combination of methods updates all disk, volume, and plex information in the VDS cache for disks that have not been recently connected or disconnected.</span></span> <span data-ttu-id="4dab9-115">Chame somente **Atualizar** para atualizar as informações de propriedade de objetos existentes no cache.</span><span class="sxs-lookup"><span data-stu-id="4dab9-115">Call **Refresh** alone to refresh the property information of existing objects in the cache.</span></span> <span data-ttu-id="4dab9-116">Essa operação pode envolver a verificação de barramentos de subsistema internos e a espera de tempos limite.</span><span class="sxs-lookup"><span data-stu-id="4dab9-116">This operation can involve scanning internal subsystem buses and waiting for time-outs.</span></span> <span data-ttu-id="4dab9-117">Observe que o VDS atualiza o cache automaticamente sempre que ocorre uma alteração que dispara uma notificação.</span><span class="sxs-lookup"><span data-stu-id="4dab9-117">Note that VDS updates the cache automatically whenever a change occurs that triggers a notification.</span></span> <span data-ttu-id="4dab9-118">Além disso, chamar a **atualização** em resposta a uma notificação do VDS pode fazer com que um loop interminável de notificações seja enviado.</span><span class="sxs-lookup"><span data-stu-id="4dab9-118">Also, calling **Refresh** in response to a VDS notification could cause an endless loop of notifications to be sent.</span></span> <span data-ttu-id="4dab9-119">Por esses motivos, a **atualização** deve ser chamada somente quando parece que o cache não está sendo atualizado corretamente.</span><span class="sxs-lookup"><span data-stu-id="4dab9-119">For these reasons, **Refresh** should be called only when it appears that the cache is not being updated properly.</span></span>

<span data-ttu-id="4dab9-120">**Para reenumerar subsistemas de hardware**</span><span class="sxs-lookup"><span data-stu-id="4dab9-120">**To reenumerate hardware subsystems**</span></span>

-   <span data-ttu-id="4dab9-121">Chame o método [**IVdsHwProvider:: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate) .</span><span class="sxs-lookup"><span data-stu-id="4dab9-121">Call the [**IVdsHwProvider::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate) method.</span></span> <span data-ttu-id="4dab9-122">Dependendo do provedor, essa operação pode envolver o envio de pacotes de rede e a espera de tempos limite, a verificação de barramentos SCSI e a espera de tempos limite e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="4dab9-122">Depending on the provider, this operation can involve sending network packets and waiting for time-outs, rescanning SCSI buses and waiting for time-outs, and so on.</span></span>

<span data-ttu-id="4dab9-123">**Para reenumerar objetos de subsistema de hardware**</span><span class="sxs-lookup"><span data-stu-id="4dab9-123">**To reenumerate hardware subsystem objects**</span></span>

-   <span data-ttu-id="4dab9-124">Chame o método [**IVdsSubSystem:: reenumerar**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate) para inventariar os objetos (normalmente unidades) no subsistema.</span><span class="sxs-lookup"><span data-stu-id="4dab9-124">Call the [**IVdsSubSystem::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate) method to inventory the objects (typically drives) in the subsystem.</span></span> <span data-ttu-id="4dab9-125">Dependendo do subsistema, essa operação pode envolver a verificação de barramentos de subsistema internos e a espera de tempos limite.</span><span class="sxs-lookup"><span data-stu-id="4dab9-125">Depending on the subsystem, this operation can involve scanning internal subsystem buses and waiting for time-outs.</span></span>

<span data-ttu-id="4dab9-126">**Para atualizar subsistemas de hardware e objetos de subsistema**</span><span class="sxs-lookup"><span data-stu-id="4dab9-126">**To refresh hardware subsystems and subsystem objects**</span></span>

-   <span data-ttu-id="4dab9-127">Chame o método [**IVdsHwProvider:: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh) para atualizar o cache VDS de informações sobre subsistemas existentes que são gerenciados por provedores de hardware VDS.</span><span class="sxs-lookup"><span data-stu-id="4dab9-127">Call the [**IVdsHwProvider::Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh) method to refresh the VDS cache of information about existing subsystems that are managed by VDS hardware providers.</span></span> <span data-ttu-id="4dab9-128">Observe que o VDS atualiza o cache automaticamente sempre que ocorre uma alteração que dispara uma notificação.</span><span class="sxs-lookup"><span data-stu-id="4dab9-128">Note that VDS updates the cache automatically whenever a change occurs that triggers a notification.</span></span> <span data-ttu-id="4dab9-129">Além disso, chamar a [**atualização**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) em resposta a uma notificação do VDS pode fazer com que um loop interminável de notificações seja enviado.</span><span class="sxs-lookup"><span data-stu-id="4dab9-129">Also, calling [**Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) in response to a VDS notification could cause an endless loop of notifications to be sent.</span></span> <span data-ttu-id="4dab9-130">Por esses motivos, a **atualização** deve ser chamada somente quando parece que o cache não está sendo atualizado corretamente.</span><span class="sxs-lookup"><span data-stu-id="4dab9-130">For these reasons, **Refresh** should be called only when it appears that the cache is not being updated properly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4dab9-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4dab9-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dab9-132">Usando VDS</span><span class="sxs-lookup"><span data-stu-id="4dab9-132">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="4dab9-133">**IVdsService:: reenumerar**</span><span class="sxs-lookup"><span data-stu-id="4dab9-133">**IVdsService::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[<span data-ttu-id="4dab9-134">**IVdsService:: atualizar**</span><span class="sxs-lookup"><span data-stu-id="4dab9-134">**IVdsService::Refresh**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh)
</dt> <dt>

[<span data-ttu-id="4dab9-135">**IVdsHwProvider:: reenumerar**</span><span class="sxs-lookup"><span data-stu-id="4dab9-135">**IVdsHwProvider::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate)
</dt> <dt>

[<span data-ttu-id="4dab9-136">**IVdsSubSystem:: reenumerar**</span><span class="sxs-lookup"><span data-stu-id="4dab9-136">**IVdsSubSystem::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate)
</dt> <dt>

[<span data-ttu-id="4dab9-137">**IVdsHwProvider:: atualizar**</span><span class="sxs-lookup"><span data-stu-id="4dab9-137">**IVdsHwProvider::Refresh**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh)
</dt> </dl>

 

 
