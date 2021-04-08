---
description: Visão geral da configuração
ms.assetid: 5cdc21a1-ff55-4c36-8106-b045256778ce
title: Visão geral da configuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4db13827bf08ee65ed8015f0c19ba2980a9a71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920841"
---
# <a name="configuration-overview"></a><span data-ttu-id="76413-103">Visão geral da configuração</span><span class="sxs-lookup"><span data-stu-id="76413-103">Configuration Overview</span></span>

<span data-ttu-id="76413-104">\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="76413-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="76413-105">Se você não estiver familiarizado com os objetos definidos pelo VDS, consulte o modelo de [objeto do VDS](vds-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="76413-105">If you are unfamiliar with the objects that are defined by VDS, see the [VDS Object Model](vds-object-model.md).</span></span>

<span data-ttu-id="76413-106">A complexidade da configuração de um disco virtual pode variar de muito simples para ajustado.</span><span class="sxs-lookup"><span data-stu-id="76413-106">The configuration complexity of a virtual disk can range from very simple to finely tuned.</span></span> <span data-ttu-id="76413-107">Os discos virtuais corporativos, gratuitos e sem cuidado definem três perspectivas de configuração típicas.</span><span class="sxs-lookup"><span data-stu-id="76413-107">No-care, free-from-care, and enterprise virtual disks define three typical configuration perspectives.</span></span> <span data-ttu-id="76413-108">Cada perspectiva apresenta requisitos um pouco diferentes:</span><span class="sxs-lookup"><span data-stu-id="76413-108">Each perspective presents somewhat different requirements:</span></span>

-   <span data-ttu-id="76413-109">Discos virtuais sem cuidado são levemente configurados, talvez apenas para automatizar o particionamento e a formatação de novos discos, ou para criar temporariamente um volume espelhado para migrar dados de um disco para outro sem tempo de inatividade.</span><span class="sxs-lookup"><span data-stu-id="76413-109">No-care virtual disks are lightly configured, perhaps only to automate the partitioning and formatting of new disks, or to temporarily create a mirrored volume for migrating data from one disk to another without downtime.</span></span> <span data-ttu-id="76413-110">Esses discos são bons para computadores notebook e outros sistemas com um ou alguns discos.</span><span class="sxs-lookup"><span data-stu-id="76413-110">Such disks are good for notebook computers and other systems with one or a few disks.</span></span>
-   <span data-ttu-id="76413-111">Os discos virtuais livres do próprio atendimento fornecem armazenamento que aparece autoconfigurável, auto-recuperação e disponível; usa volumes distribuídos e LUNs para obter um melhor desempenho; usa volumes espelhados e LUNs para obter melhor disponibilidade; e usa pacotes para tornar os modos de falha limpos e contidos.</span><span class="sxs-lookup"><span data-stu-id="76413-111">Free-from-care virtual disks provide storage that appears self-configuring, self-healing, and available; uses striped volumes and LUNs to achieve better performance; uses mirrored volumes and LUNs to achieve better availability; and uses packs to make the failure modes clean and contained.</span></span> <span data-ttu-id="76413-112">Esse nível de configuração é ideal ao substituir discos do sistema antigos, pequenos e lentos por discos novos, grandes e rápidos é a rotina.</span><span class="sxs-lookup"><span data-stu-id="76413-112">This configuration level is ideal when replacing old, small, slow system disks with new, large, fast disks is routine.</span></span> <span data-ttu-id="76413-113">Ele também é ideal para espelhamento de dados com Hot Sparing automatizado — um único eixo sobressalente pode proteger muitos eixos.</span><span class="sxs-lookup"><span data-stu-id="76413-113">It is also ideal for mirroring data with automated hot sparing—a single spare spindle can protect many spindles.</span></span> <span data-ttu-id="76413-114">Para obter detalhes, consulte [Hot Sparing](hot-sparing.md).</span><span class="sxs-lookup"><span data-stu-id="76413-114">For details, see [Hot Sparing](hot-sparing.md).</span></span>

    <span data-ttu-id="76413-115">SANs de pequena escala dependem da flexibilidade e da automação oferecidas por esse nível de configuração, como os dispositivos NAS (armazenamento anexado à rede).</span><span class="sxs-lookup"><span data-stu-id="76413-115">Small-scale SANs depend on the flexibility and automation that is offered by this configuration level, as do Network Attached Storage (NAS) appliances.</span></span> <span data-ttu-id="76413-116">Discos virtuais livres da própria simplificam a tarefa de consolidar o armazenamento de aplicativos — por exemplo, o armazenamento para SQL e Exchange — sem consolidar os servidores.</span><span class="sxs-lookup"><span data-stu-id="76413-116">Free-from-care virtual disks simplify the task of consolidating application storage—for example, the storage for SQL and Exchange—without consolidating the servers.</span></span>

-   <span data-ttu-id="76413-117">Os discos virtuais corporativos contêm configurações corporativas muito grandes ou complexas com requisitos adicionais específicos do site ou do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="76413-117">Enterprise virtual disks contain very large or complex enterprise configurations with additional site-specific or application-specific requirements.</span></span> <span data-ttu-id="76413-118">Os administradores ajustam o subsistema de armazenamento para um único aplicativo que pode ser executado com pouca frequência, como um trabalho mensal de relatórios em lote em um sistema de transação de ordem demorada.</span><span class="sxs-lookup"><span data-stu-id="76413-118">Administrators tune the storage subsystem for a single application that might run only infrequently, such as a monthly batch reporting job on an order-taking transaction system.</span></span> <span data-ttu-id="76413-119">Os discos virtuais corporativos devem ser dimensionados, mostrar a atividade em tempo real do subsistema de armazenamento e atender aos requisitos de administradores práticos.</span><span class="sxs-lookup"><span data-stu-id="76413-119">Enterprise virtual disks must scale, show the real-time activity of the storage subsystem, and satisfy the requirements of hands-on administrators.</span></span>

<span data-ttu-id="76413-120">Para obter informações adicionais sobre espelhos, faixas e outras opções de configuração no VDS, consulte [Associação de volume e LUN](volume-and-lun-binding.md).</span><span class="sxs-lookup"><span data-stu-id="76413-120">For additional information about mirrors, stripes, and the other configuration options in VDS, see [Volume and LUN Binding](volume-and-lun-binding.md).</span></span> <span data-ttu-id="76413-121">Uma técnica de configuração avançada, chamada de empilhamento, permite combinar as configurações associadas aos volumes e LUNs existentes.</span><span class="sxs-lookup"><span data-stu-id="76413-121">An advanced configuration technique, called stacking, enables you to combine the configurations that are associated with existing volumes and LUNs.</span></span> <span data-ttu-id="76413-122">Para obter detalhes, consulte [empilhamento de configuração](configuration-stacking.md).</span><span class="sxs-lookup"><span data-stu-id="76413-122">For details, see [Configuration Stacking](configuration-stacking.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="76413-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="76413-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76413-124">Serviço de Disco Virtual</span><span class="sxs-lookup"><span data-stu-id="76413-124">Virtual Disk Service</span></span>](virtual-disk-service-portal.md)
</dt> <dt>

[<span data-ttu-id="76413-125">Modelo de objeto VDS</span><span class="sxs-lookup"><span data-stu-id="76413-125">VDS Object Model</span></span>](vds-object-model.md)
</dt> <dt>

[<span data-ttu-id="76413-126">Hot Sparing</span><span class="sxs-lookup"><span data-stu-id="76413-126">Hot Sparing</span></span>](hot-sparing.md)
</dt> <dt>

[<span data-ttu-id="76413-127">Associação de volume e LUN</span><span class="sxs-lookup"><span data-stu-id="76413-127">Volume and LUN Binding</span></span>](volume-and-lun-binding.md)
</dt> <dt>

[<span data-ttu-id="76413-128">Empilhamento de configuração</span><span class="sxs-lookup"><span data-stu-id="76413-128">Configuration Stacking</span></span>](configuration-stacking.md)
</dt> </dl>

 

 
