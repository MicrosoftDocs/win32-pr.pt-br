---
description: Tarefas de partições COM+
ms.assetid: ebcbfced-7d7a-46dc-a728-cdb920ccb874
title: Tarefas de partições COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055976effb5d6a93523bab9d570aec685872ab91
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163968"
---
# <a name="com-partitions-tasks"></a><span data-ttu-id="beee0-103">Tarefas de partições COM+</span><span class="sxs-lookup"><span data-stu-id="beee0-103">COM+ Partitions Tasks</span></span>

<span data-ttu-id="beee0-104">Os tópicos a seguir nesta seção fornecem instruções passo a passo para usar partições COM+.</span><span class="sxs-lookup"><span data-stu-id="beee0-104">The following topics in this section provide step-by-step instructions for using COM+ partitions.</span></span>

<span data-ttu-id="beee0-105">**Windows XP:** A capacidade de criar, configurar ou delegar partições COM+ não está disponível.</span><span class="sxs-lookup"><span data-stu-id="beee0-105">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="beee0-106">A partição global é a única partição COM+ disponível.</span><span class="sxs-lookup"><span data-stu-id="beee0-106">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="beee0-107">\* \* Windows 2000: \* \* o serviço de partições COM+ não está disponível no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="beee0-107">\*\*Windows 2000:  \*\* The COM+ partitions service is not available in Windows 2000.</span></span>



| <span data-ttu-id="beee0-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="beee0-108">Topic</span></span>                                                                                                         | <span data-ttu-id="beee0-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="beee0-109">Description</span></span>                                                                                    |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="beee0-110">Criando e configurando partições COM+</span><span class="sxs-lookup"><span data-stu-id="beee0-110">Creating and Configuring COM+ Partitions</span></span>](creating-and-configuring-com--partitions.md)<br/>           | <span data-ttu-id="beee0-111">Descreve como criar e configurar uma partição COM+.</span><span class="sxs-lookup"><span data-stu-id="beee0-111">Describes how to create and configure a COM+ partition.</span></span><br/>                             |
| [<span data-ttu-id="beee0-112">Gerenciando partições locais</span><span class="sxs-lookup"><span data-stu-id="beee0-112">Managing Local Partitions</span></span>](managing-local-partitions.md)<br/>                                         | <span data-ttu-id="beee0-113">Descreve como gerenciar partições COM+ que não estão dentro de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="beee0-113">Describes how to manage COM+ partitions that are not within Active Directory.</span></span><br/>       |
| [<span data-ttu-id="beee0-114">Gerenciando partições no Active Directory</span><span class="sxs-lookup"><span data-stu-id="beee0-114">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)<br/>     | <span data-ttu-id="beee0-115">Descreve como gerenciar partições COM+ que são especificadas dentro de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="beee0-115">Describes how to manage COM+ partitions that are specified within Active Directory.</span></span><br/> |
| [<span data-ttu-id="beee0-116">Configurando direitos administrativos para uma partição</span><span class="sxs-lookup"><span data-stu-id="beee0-116">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)<br/> | <span data-ttu-id="beee0-117">Descreve como definir privilégios de segurança para uma partição COM+.</span><span class="sxs-lookup"><span data-stu-id="beee0-117">Describes how to set security privileges for a COM+ partition.</span></span><br/>                      |
| [<span data-ttu-id="beee0-118">Agrupando aplicativos em partições</span><span class="sxs-lookup"><span data-stu-id="beee0-118">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)<br/>                 | <span data-ttu-id="beee0-119">Descreve como configurar aplicativos COM+ para pertencer a uma partição COM+.</span><span class="sxs-lookup"><span data-stu-id="beee0-119">Describes how to configure COM+ applications to belong to a COM+ partition.</span></span> <br/>        |
| [<span data-ttu-id="beee0-120">Coletando métricas de partição</span><span class="sxs-lookup"><span data-stu-id="beee0-120">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)<br/>                                   | <span data-ttu-id="beee0-121">Descreve como coletar dados sobre partições COM+.</span><span class="sxs-lookup"><span data-stu-id="beee0-121">Describes how to collect data about COM+ partitions.</span></span><br/>                                |
| [<span data-ttu-id="beee0-122">Configurando o cache de partição</span><span class="sxs-lookup"><span data-stu-id="beee0-122">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)<br/>                             | <span data-ttu-id="beee0-123">Descreve como configurar o cache de partição COM+.</span><span class="sxs-lookup"><span data-stu-id="beee0-123">Describes how to configure the COM+ partition cache.</span></span><br/>                                |



 

> [!Note]  
> <span data-ttu-id="beee0-124">O serviço de partições COM+ não está habilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="beee0-124">The COM+ Partitions service is not enabled by default.</span></span> <span data-ttu-id="beee0-125">Para usar o serviço de partições COM+, você deve habilitá-lo por meio da ferramenta de administração de serviços de componentes ou alterando a propriedade PartitionsEnabled na coleção [**LocalComputer**](localcomputer.md) para true.</span><span class="sxs-lookup"><span data-stu-id="beee0-125">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="beee0-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="beee0-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="beee0-127">Conceitos de partições COM+</span><span class="sxs-lookup"><span data-stu-id="beee0-127">COM+ Partitions Concepts</span></span>](com--partitions-concepts.md)
</dt> </dl>

 

 




