---
description: Adicionando discos externos a um pacote
ms.assetid: 4018c742-1d23-47b9-a787-69bf8847b54a
title: Adicionando discos externos a um pacote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fbfa2ff3d00857fd4e1b92e78f1760c25ce516b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297505"
---
# <a name="adding-foreign-disks-to-a-pack"></a><span data-ttu-id="504da-103">Adicionando discos externos a um pacote</span><span class="sxs-lookup"><span data-stu-id="504da-103">Adding Foreign Disks to a Pack</span></span>

<span data-ttu-id="504da-104">\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="504da-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="504da-105">Normalmente, um disco externo é um disco dinâmico que é alocado em um computador e fisicamente movido para outro computador.</span><span class="sxs-lookup"><span data-stu-id="504da-105">Most commonly, a foreign disk is a dynamic disk that is allocated on one computer and physically moved to another computer.</span></span> <span data-ttu-id="504da-106">No entanto, qualquer disco que pertença a um pacote que não seja o pacote online é considerado um disco externo que pertence a um pacote de disco externo.</span><span class="sxs-lookup"><span data-stu-id="504da-106">However, any disk that belongs to a pack other than the online pack is considered to be a foreign disk that belongs to a foreign disk pack.</span></span>

<span data-ttu-id="504da-107">Um pacote estrangeiro tem o **sinalizador \_ \_ estrangeiro PKF Foreign** definido no membro **ulFlags** da estrutura de [**\_ \_ prop do VDS Pack**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) .</span><span class="sxs-lookup"><span data-stu-id="504da-107">A foreign pack has the **VDS\_PKF\_FOREIGN** flag set in the **ulFlags** member of the [**VDS\_PACK\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) structure.</span></span> <span data-ttu-id="504da-108">Os pacotes estrangeiros estão sempre offline.</span><span class="sxs-lookup"><span data-stu-id="504da-108">Foreign packs are always offline.</span></span>

<span data-ttu-id="504da-109">O procedimento a seguir descreve como importar um ou mais discos externos.</span><span class="sxs-lookup"><span data-stu-id="504da-109">The following procedure describes how to import one or more foreign disks.</span></span>

<span data-ttu-id="504da-110">**Para importar um ou mais discos estrangeiros**</span><span class="sxs-lookup"><span data-stu-id="504da-110">**To import one or more foreign disks**</span></span>

1.  <span data-ttu-id="504da-111">Mova os discos para o novo computador.</span><span class="sxs-lookup"><span data-stu-id="504da-111">Move disks to the new computer.</span></span>
2.  <span data-ttu-id="504da-112">No novo computador, use o método [**IVdsService:: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) para instalar os discos externos.</span><span class="sxs-lookup"><span data-stu-id="504da-112">On the new computer, use the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method to install the foreign disks.</span></span>
3.  <span data-ttu-id="504da-113">Selecione o pacote online para ser o pacote de destino que recebe os discos externos.</span><span class="sxs-lookup"><span data-stu-id="504da-113">Select the online pack to be the target pack that receives the foreign disks.</span></span> <span data-ttu-id="504da-114">Se não existir nenhum pacote online, use o método [**IVdsSwProvider:: createpack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) para criar um novo pacote vazio.</span><span class="sxs-lookup"><span data-stu-id="504da-114">If no online pack exists, use the [**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) method to create a new empty pack.</span></span>
4.  <span data-ttu-id="504da-115">Use o método [**IVdsPack:: MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) para importar os discos para o novo pacote dinâmico.</span><span class="sxs-lookup"><span data-stu-id="504da-115">Use the [**IVdsPack::MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) method to import the disks to the new dynamic pack.</span></span>
5.  <span data-ttu-id="504da-116">Use o método [**IVdsSwProvider:: QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) para enumerar os pacotes e [**IVdsPack:: GetProperties**](/windows/desktop/api/Vds/nf-vds-ivdspack-getproperties) para determinar qual pacote agora é o pacote online.</span><span class="sxs-lookup"><span data-stu-id="504da-116">Use the [**IVdsSwProvider::QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) method to enumerate the packs and [**IVdsPack::GetProperties**](/windows/desktop/api/Vds/nf-vds-ivdspack-getproperties) to determine which pack is now the online pack.</span></span>

<span data-ttu-id="504da-117">Se você criar um novo pacote de destino vazio, os discos externos não serão realmente migrados para esse pacote.</span><span class="sxs-lookup"><span data-stu-id="504da-117">If you create a new empty target pack, the foreign disks are not actually migrated to that pack.</span></span> <span data-ttu-id="504da-118">Em vez disso, o pacote estrangeiro é marcado como online, o sinalizador **\_ \_ estrangeiro do VDS PKF** para o pacote é limpo (portanto, o pacote não é mais estrangeiro) e o pacote de destino que você criou é Descartado.</span><span class="sxs-lookup"><span data-stu-id="504da-118">Instead, the foreign pack is marked online, the **VDS\_PKF\_FOREIGN** flag for the pack is cleared (so the pack is no longer foreign), and the target pack that you created is discarded.</span></span>

> [!Note]  
> <span data-ttu-id="504da-119">Use o método [**IVdsPack:: adddisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) para adicionar discos não alocados, discos não reivindicados por um provedor, a um pacote.</span><span class="sxs-lookup"><span data-stu-id="504da-119">Use the [**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) method to add unallocated disks—disks not claimed by a provider—to a pack.</span></span> <span data-ttu-id="504da-120">Um disco não alocado não pode ser estrangeiro.</span><span class="sxs-lookup"><span data-stu-id="504da-120">An unallocated disk cannot be foreign.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="504da-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="504da-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="504da-122">Usando VDS</span><span class="sxs-lookup"><span data-stu-id="504da-122">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="504da-123">**IVdsService:: reenumerar**</span><span class="sxs-lookup"><span data-stu-id="504da-123">**IVdsService::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[<span data-ttu-id="504da-124">**IVdsSwProvider:: createpack**</span><span class="sxs-lookup"><span data-stu-id="504da-124">**IVdsSwProvider::CreatePack**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[<span data-ttu-id="504da-125">**IVdsPack::MigrateDisks**</span><span class="sxs-lookup"><span data-stu-id="504da-125">**IVdsPack::MigrateDisks**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks)
</dt> <dt>

[<span data-ttu-id="504da-126">**IVdsPack:: adddisk**</span><span class="sxs-lookup"><span data-stu-id="504da-126">**IVdsPack::AddDisk**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> </dl>

 

 
