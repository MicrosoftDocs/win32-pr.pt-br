---
description: Adicionando uma letra de unidade a um LUN
ms.assetid: 3f350312-3f1f-4020-90d0-85521ea9c7c8
title: Adicionando uma letra de unidade a um LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426a4f3bf720b21a02462edde4a381012d2084d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759798"
---
# <a name="adding-a-drive-letter-to-a-lun"></a><span data-ttu-id="ed089-103">Adicionando uma letra de unidade a um LUN</span><span class="sxs-lookup"><span data-stu-id="ed089-103">Adding a Drive Letter to a LUN</span></span>

<span data-ttu-id="ed089-104">\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ed089-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="ed089-105">Você pode atribuir letras de unidade a objetos de volume diretamente; no entanto, se o disco for um objeto de LUN, você terá algumas etapas adicionais.</span><span class="sxs-lookup"><span data-stu-id="ed089-105">You can assign drive letters to volume objects directly; however, if your disk is a LUN object, you have a few additional steps.</span></span>

<span data-ttu-id="ed089-106">**Para atribuir uma letra da unidade a um objeto LUN**</span><span class="sxs-lookup"><span data-stu-id="ed089-106">**To assign a drive letter to a LUN object**</span></span>

1.  <span data-ttu-id="ed089-107">Se necessário, desmascarar o LUN para o host local.</span><span class="sxs-lookup"><span data-stu-id="ed089-107">If necessary, unmask the LUN to the local host.</span></span>
    > [!Note]  
    > <span data-ttu-id="ed089-108">Você não pode executar operações administrativas de software em um objeto de LUN que não é mascarado para outro computador na sessão VDS atual.</span><span class="sxs-lookup"><span data-stu-id="ed089-108">You cannot perform software administrative operations on a LUN object that is unmasked to another computer within the current VDS session.</span></span>

     

2.  <span data-ttu-id="ed089-109">Invoque o método [**IVdsService:: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) no computador que está executando o provedor de hardware.</span><span class="sxs-lookup"><span data-stu-id="ed089-109">Invoke the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method on the computer that is running the hardware provider.</span></span>
3.  <span data-ttu-id="ed089-110">Inicialize o LUN como um disco básico da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="ed089-110">Initialize the LUN as a basic disk as follows:</span></span>
    1.  <span data-ttu-id="ed089-111">Invoque o método [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no objeto LUN para consultar a interface [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) .</span><span class="sxs-lookup"><span data-stu-id="ed089-111">Invoke the [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the LUN object to query for the [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) interface.</span></span>
    2.  <span data-ttu-id="ed089-112">Invoque o método [**IVdsSwProvider:: createpack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) para criar um pacote básico.</span><span class="sxs-lookup"><span data-stu-id="ed089-112">Invoke the [**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) method to create a basic pack.</span></span>
    3.  <span data-ttu-id="ed089-113">Invoque o método [**IVdsPack:: adddisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) para adicionar o disco ao novo pacote.</span><span class="sxs-lookup"><span data-stu-id="ed089-113">Invoke the [**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) method to add the disk to the new pack.</span></span>
4.  <span data-ttu-id="ed089-114">Crie uma partição no disco e obtenha o objeto de volume da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="ed089-114">Create a partition on the disk and obtain the volume object as follows:</span></span>
    1.  <span data-ttu-id="ed089-115">Invoque o método [**IVdsCreatePartitionEx:: CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) para criar uma partição.</span><span class="sxs-lookup"><span data-stu-id="ed089-115">Invoke the [**IVdsCreatePartitionEx::CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) method to create a partition.</span></span>
    2.  <span data-ttu-id="ed089-116">Invoque o método [**IVdsAsync:: Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) no objeto Async que é retornado por [**CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) para obter o identificador de volume da estrutura [**de \_ \_ saída do VDS Async**](/windows/desktop/api/Vds/ns-vds-vds_async_output) .</span><span class="sxs-lookup"><span data-stu-id="ed089-116">Invoke the [**IVdsAsync::Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) method on the async object that is returned by [**CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) to get the volume identifier from the [**VDS\_ASYNC\_OUTPUT**](/windows/desktop/api/Vds/ns-vds-vds_async_output) structure.</span></span>
    3.  <span data-ttu-id="ed089-117">Passe o identificador de volume como um parâmetro para o método [**IVdsService:: GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) para obter um ponteiro de objeto de volume.</span><span class="sxs-lookup"><span data-stu-id="ed089-117">Pass the volume identifier as a parameter to the [**IVdsService::GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) method to get a volume object pointer.</span></span>
5.  <span data-ttu-id="ed089-118">Invoque o método [**IVdsVolumeMF:: AddAccessPath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath) para atribuir a letra da unidade.</span><span class="sxs-lookup"><span data-stu-id="ed089-118">Invoke the [**IVdsVolumeMF::AddAccessPath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath) method to assign the drive letter.</span></span>

> [!Note]  
> <span data-ttu-id="ed089-119">O método [**IVdsAdvancedDisk:: AssignDriveLetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter) atribui letras de unidade a partições sem volumes associados, como partições OEM ou ESP.</span><span class="sxs-lookup"><span data-stu-id="ed089-119">The [**IVdsAdvancedDisk::AssignDriveLetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter) method assigns drive letters to partitions without associated volumes, such as OEM or ESP partitions.</span></span> <span data-ttu-id="ed089-120">Você não pode usá-lo para atribuir uma letra de unidade a um objeto LUN.</span><span class="sxs-lookup"><span data-stu-id="ed089-120">You cannot use it to assign a drive letter to a LUN object.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ed089-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ed089-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed089-122">Usando VDS</span><span class="sxs-lookup"><span data-stu-id="ed089-122">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="ed089-123">**IVdsService:: reenumerar**</span><span class="sxs-lookup"><span data-stu-id="ed089-123">**IVdsService::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[<span data-ttu-id="ed089-124">**IVdsDisk**</span><span class="sxs-lookup"><span data-stu-id="ed089-124">**IVdsDisk**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> <dt>

[<span data-ttu-id="ed089-125">**IVdsSwProvider:: createpack**</span><span class="sxs-lookup"><span data-stu-id="ed089-125">**IVdsSwProvider::CreatePack**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[<span data-ttu-id="ed089-126">**IVdsPack:: adddisk**</span><span class="sxs-lookup"><span data-stu-id="ed089-126">**IVdsPack::AddDisk**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> <dt>

[<span data-ttu-id="ed089-127">**IVdsCreatePartitionEx::CreatePartitionEx**</span><span class="sxs-lookup"><span data-stu-id="ed089-127">**IVdsCreatePartitionEx::CreatePartitionEx**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex)
</dt> <dt>

[<span data-ttu-id="ed089-128">**IVdsAsync:: aguardar**</span><span class="sxs-lookup"><span data-stu-id="ed089-128">**IVdsAsync::Wait**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)
</dt> <dt>

[<span data-ttu-id="ed089-129">**saída do VDS \_ assíncrono \_**</span><span class="sxs-lookup"><span data-stu-id="ed089-129">**VDS\_ASYNC\_OUTPUT**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_async_output)
</dt> <dt>

[<span data-ttu-id="ed089-130">**IVdsVolumeMF::AddAccessPath**</span><span class="sxs-lookup"><span data-stu-id="ed089-130">**IVdsVolumeMF::AddAccessPath**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath)
</dt> <dt>

[<span data-ttu-id="ed089-131">**IVdsAdvancedDisk::AssignDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="ed089-131">**IVdsAdvancedDisk::AssignDriveLetter**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter)
</dt> </dl>

 

 
