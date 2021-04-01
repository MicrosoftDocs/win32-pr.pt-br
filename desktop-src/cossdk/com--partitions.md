---
description: Você pode usar o serviço de partições COM+ para instalar versões diferentes de um aplicativo COM+ em um computador e executá-las simultaneamente.
ms.assetid: fd22a64c-f2d8-48af-86e1-985e21b0f8fa
title: Partições COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd4e1efdd42ac407d8937c4090c59e65472ed69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826260"
---
# <a name="com-partitions"></a><span data-ttu-id="f5f2f-103">Partições COM+</span><span class="sxs-lookup"><span data-stu-id="f5f2f-103">COM+ Partitions</span></span>

<span data-ttu-id="f5f2f-104">Você pode usar o serviço de partições COM+ para instalar versões diferentes de um aplicativo COM+ em um computador e executá-las simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-104">You can use the COM+ partitions service to install different versions of a COM+ application on a computer and run them simultaneously.</span></span>

<span data-ttu-id="f5f2f-105">**Windows XP:** A capacidade de criar, configurar ou delegar partições COM+ não está disponível.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-105">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="f5f2f-106">A partição global é a única partição COM+ disponível.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-106">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="f5f2f-107">\* \* Windows 2000: \* \* o serviço de partições COM+ não está disponível no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-107">\*\*Windows 2000:  \*\* The COM+ partitions service is not available in Windows 2000.</span></span>

<span data-ttu-id="f5f2f-108">Os tópicos a seguir fornecem informações sobre o serviço de partições COM+.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-108">The following topics provide information about the COM+ partitions service.</span></span>



| <span data-ttu-id="f5f2f-109">Tópico</span><span class="sxs-lookup"><span data-stu-id="f5f2f-109">Topic</span></span>                                                               | <span data-ttu-id="f5f2f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5f2f-110">Description</span></span>                                                                 |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="f5f2f-111">Conceitos de partições COM+</span><span class="sxs-lookup"><span data-stu-id="f5f2f-111">COM+ Partitions Concepts</span></span>](com--partitions-concepts.md)<br/> | <span data-ttu-id="f5f2f-112">Fornece uma visão geral do uso de partições COM+.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-112">Provides an overview of using COM+ partitions.</span></span><br/>                   |
| [<span data-ttu-id="f5f2f-113">Tarefas de partições COM+</span><span class="sxs-lookup"><span data-stu-id="f5f2f-113">COM+ Partitions Tasks</span></span>](com--partitions-tasks.md)<br/>       | <span data-ttu-id="f5f2f-114">Fornece instruções para criar e gerenciar partições COM+.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-114">Provides instructions for creating and managing COM+ partitions.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="f5f2f-115">O serviço de partições COM+ não está habilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-115">The COM+ partitions service is not enabled by default.</span></span> <span data-ttu-id="f5f2f-116">Para usar o serviço de partições COM+, você deve habilitá-lo por meio da ferramenta de administração de serviços de componentes ou alterando a propriedade PartitionsEnabled na coleção [**LocalComputer**](localcomputer.md) para true.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-116">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

 

 




