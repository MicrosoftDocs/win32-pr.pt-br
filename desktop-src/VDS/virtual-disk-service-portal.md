---
description: O VDS (serviço de disco virtual) gerencia uma ampla gama de configurações de armazenamento, desde desktops de disco único até matrizes de armazenamento externo. O serviço expõe uma API (interface de programação de aplicativo).
ms.assetid: 536aafd2-cc04-48cc-8ee7-920efbba2a5f
title: Serviço de Disco Virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcfef0c5a73fcb2e6911395c829380c4bdfe56ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789998"
---
# <a name="virtual-disk-service"></a><span data-ttu-id="d0589-104">Serviço de Disco Virtual</span><span class="sxs-lookup"><span data-stu-id="d0589-104">Virtual Disk Service</span></span>

<span data-ttu-id="d0589-105">\[A partir do Windows 8 e do Windows Server 2012, a interface COM do serviço de disco virtual é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d0589-105">\[Beginning with Windows 8 and Windows Server 2012, the Virtual Disk Service COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

## <a name="purpose"></a><span data-ttu-id="d0589-106">Finalidade</span><span class="sxs-lookup"><span data-stu-id="d0589-106">Purpose</span></span>

<span data-ttu-id="d0589-107">O VDS (serviço de disco virtual) gerencia uma ampla gama de configurações de armazenamento, desde desktops de disco único até matrizes de armazenamento externo.</span><span class="sxs-lookup"><span data-stu-id="d0589-107">The Virtual Disk Service (VDS) manages a wide range of storage configurations, from single-disk desktops to external storage arrays.</span></span> <span data-ttu-id="d0589-108">O serviço expõe uma API (interface de programação de aplicativo).</span><span class="sxs-lookup"><span data-stu-id="d0589-108">The service exposes an application programming interface (API).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="d0589-109">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="d0589-109">Where applicable</span></span>

<span data-ttu-id="d0589-110">A partir do Windows 8 e do Windows Server 8, a interface COM do serviço de disco virtual é substituída pela API de gerenciamento de armazenamento, uma interface de programação baseada em WMI.</span><span class="sxs-lookup"><span data-stu-id="d0589-110">Beginning with Windows 8 and Windows Server 8, the Virtual Disk Service COM interface is superseded by the Storage Management API, a WMI-based programming interface.</span></span> <span data-ttu-id="d0589-111">Para gerenciar subsistemas de armazenamento, discos, partições e volumes do (Windows), é altamente recomendável usar a API de gerenciamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d0589-111">For managing storage subsystems, (Windows) disks, partitions, and volumes, we strongly recommend using the Storage Management API.</span></span> <span data-ttu-id="d0589-112">Para obter mais informações, consulte a [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).</span><span class="sxs-lookup"><span data-stu-id="d0589-112">For more information, see the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).</span></span>

<span data-ttu-id="d0589-113">Para todos os usos, exceto volumes de inicialização espelho (usando um volume espelhado para hospedar o sistema operacional), discos dinâmicos são preteridos.</span><span class="sxs-lookup"><span data-stu-id="d0589-113">For all usages except mirror boot volumes (using a mirror volume to host the operating system ), dynamic disks are deprecated.</span></span> <span data-ttu-id="d0589-114">Para dados que exigem resiliência contra falha de unidade, use espaços de armazenamento, uma solução de virtualização de armazenamento resiliente.</span><span class="sxs-lookup"><span data-stu-id="d0589-114">For data that requires resiliency against drive failure, use Storage Spaces, a resilient storage virtualization solution.</span></span> <span data-ttu-id="d0589-115">Para obter mais informações, consulte [Visualização técnica de espaços de armazenamento](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="d0589-115">For more information, see [Storage Spaces Technical Preview](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).</span></span>

<span data-ttu-id="d0589-116">Os desenvolvedores de aplicativos que usam as interfaces descritas neste guia podem consultar e configurar um conjunto heterogêneo de armazenamento gerenciado internamente e fornecido pelo fornecedor.</span><span class="sxs-lookup"><span data-stu-id="d0589-116">Application developers who use the interfaces described in this guide can query and configure a heterogeneous set of vendor-supplied and internally managed storage.</span></span> <span data-ttu-id="d0589-117">O VDS oculta de aplicativos as complexidades associadas ao armazenamento, tornando o serviço diferente do fornecedor e da tecnologia neutro.</span><span class="sxs-lookup"><span data-stu-id="d0589-117">VDS hides from applications the complexities associated with storage, making the service both vendor and technology neutral.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="d0589-118">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="d0589-118">Developer audience</span></span>

<span data-ttu-id="d0589-119">Esta documentação é destinada a desenvolvedores de aplicativos que estão familiarizados com os recursos de armazenamento das plataformas Microsoft Windows e que são mais experientes em relação ao desenvolvimento COM.</span><span class="sxs-lookup"><span data-stu-id="d0589-119">This documentation is intended for application developers who are familiar with the storage capabilities of Microsoft Windows platforms and who are knowledgeable about COM development.</span></span>

<span data-ttu-id="d0589-120">O guia também destina-se a fabricantes de subsistema de hardware que desenvolvem e dão suporte a programas de provedor de hardware VDS.</span><span class="sxs-lookup"><span data-stu-id="d0589-120">The guide is also intended for hardware subsystem manufacturers who develop and support VDS hardware provider programs.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="d0589-121">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="d0589-121">Run-time requirements</span></span>

<span data-ttu-id="d0589-122">O VDS tem suporte no Windows Server 2003, Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="d0589-122">VDS is supported on Windows Server 2003, Windows Vista, and later.</span></span> <span data-ttu-id="d0589-123">Para obter informações sobre os requisitos de tempo de execução para um determinado elemento de programação, consulte a seção requisitos da documentação para esse elemento.</span><span class="sxs-lookup"><span data-stu-id="d0589-123">For information about run-time requirements for a particular programming element, see the Requirements section of the documentation for that element.</span></span>

<span data-ttu-id="d0589-124">Há suporte para a execução de aplicativos VDS de 32 bits no WOW64, mas os provedores VDS de 64 bits devem ser executados como aplicativos nativos em versões do Windows de bits 64.</span><span class="sxs-lookup"><span data-stu-id="d0589-124">Running 32-bit VDS applications under WOW64 is supported, but 64-bit VDS providers must run as native applications on 64-bit Windows versions.</span></span>

<span data-ttu-id="d0589-125">O VDS está disponível no SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d0589-125">VDS is available in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d0589-126">Você pode instalar o SDK para Windows 7 e Windows Server 2008 R2 no [centro de download do Windows](https://www.microsoft.com/download/details.aspx?id=8279).</span><span class="sxs-lookup"><span data-stu-id="d0589-126">You can install the SDK for Windows 7 and Windows Server 2008 R2 from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).</span></span> <span data-ttu-id="d0589-127">Esta versão do SDK do Windows pode ser usada para desenvolver aplicativos VDS para o Windows Server 2003, o Windows Vista e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="d0589-127">This version of the Windows SDK can be used to develop VDS applications for Windows Server 2003, Windows Vista, and later.</span></span> <span data-ttu-id="d0589-128">Você também pode baixar a [versão ISO](https://www.microsoft.com/download/details.aspx?id=8442) do SDK no centro de download do Windows.</span><span class="sxs-lookup"><span data-stu-id="d0589-128">You can also download the [ISO version](https://www.microsoft.com/download/details.aspx?id=8442) of the SDK from the Windows Download Center.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d0589-129">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="d0589-129">In this section</span></span>



| <span data-ttu-id="d0589-130">Tópico</span><span class="sxs-lookup"><span data-stu-id="d0589-130">Topic</span></span>                                         | <span data-ttu-id="d0589-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0589-131">Description</span></span>                                                                                            |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d0589-132">Sobre o VDS</span><span class="sxs-lookup"><span data-stu-id="d0589-132">About VDS</span></span>](about-vds.md)<br/>         | <span data-ttu-id="d0589-133">Descreve o modelo de objeto VDS, estratégias de configuração de armazenamento e notificações de VDS.</span><span class="sxs-lookup"><span data-stu-id="d0589-133">Describes the VDS object model, storage-configuration strategies, and VDS notifications.</span></span><br/>    |
| [<span data-ttu-id="d0589-134">Usando VDS</span><span class="sxs-lookup"><span data-stu-id="d0589-134">Using VDS</span></span>](using-vds.md)<br/>         | <span data-ttu-id="d0589-135">Descreve como usar o VDS para consultar e configurar dispositivos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d0589-135">Describes how to use VDS to query and configure storage devices.</span></span><br/>                            |
| [<span data-ttu-id="d0589-136">Referência do VDS</span><span class="sxs-lookup"><span data-stu-id="d0589-136">VDS Reference</span></span>](vds-reference.md)<br/> | <span data-ttu-id="d0589-137">Descreve constantes do VDS, tipos de dados, enumerações, interfaces, estruturas e códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="d0589-137">Describes VDS constants, data types, enumerations, interfaces, structures, and error codes.</span></span><br/> |



 

 

