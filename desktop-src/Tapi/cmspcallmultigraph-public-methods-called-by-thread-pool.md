---
description: A lista a seguir contém os métodos públicos CMSPCallMultiGraph chamados pelo pool de threads.
ms.assetid: f0a5f621-99c4-40f0-8a0e-0e43792e00a1
title: Métodos públicos CMSPCallMultiGraph, chamados pelo pool de threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3878298024164a4c940b96dceb88e0ff005d59ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757000"
---
# <a name="cmspcallmultigraph-public-methods-called-by-thread-pool"></a><span data-ttu-id="996f9-103">Métodos públicos CMSPCallMultiGraph, chamados pelo pool de threads</span><span class="sxs-lookup"><span data-stu-id="996f9-103">CMSPCallMultiGraph Public Methods, Called by Thread Pool</span></span>



| <span data-ttu-id="996f9-104">Métodos públicos CMSPCallMultiGraph</span><span class="sxs-lookup"><span data-stu-id="996f9-104">CMSPCallMultiGraph public methods</span></span>                                   | <span data-ttu-id="996f9-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="996f9-105">Description</span></span>                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="996f9-106">**DispatchGraphEvent**</span><span class="sxs-lookup"><span data-stu-id="996f9-106">**DispatchGraphEvent**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) | <span data-ttu-id="996f9-107">Chamado quando o grafo de filtro sinaliza um evento.</span><span class="sxs-lookup"><span data-stu-id="996f9-107">Called when the filter graph signals an event.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="996f9-108">**HandleGraphEvent**</span><span class="sxs-lookup"><span data-stu-id="996f9-108">**HandleGraphEvent**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-handlegraphevent)     | <span data-ttu-id="996f9-109">Chamado pelo método estático [**DispatchGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) .</span><span class="sxs-lookup"><span data-stu-id="996f9-109">Called by the [**DispatchGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) static method.</span></span> <span data-ttu-id="996f9-110">Enfileira [**ProcessGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent) no thread de trabalho principal do MSP.</span><span class="sxs-lookup"><span data-stu-id="996f9-110">Queues [**ProcessGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent) on the main MSP worker thread.</span></span> |
| [<span data-ttu-id="996f9-111">**ProcessGraphEvent**</span><span class="sxs-lookup"><span data-stu-id="996f9-111">**ProcessGraphEvent**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent)   | <span data-ttu-id="996f9-112">Permite que a instância do objeto de chamada MSP manipule o evento Filter Graph.</span><span class="sxs-lookup"><span data-stu-id="996f9-112">Allows the MSP call object instance to handle the filter graph event.</span></span>                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="996f9-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="996f9-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="996f9-114">**CMSPCallMultiGraph**</span><span class="sxs-lookup"><span data-stu-id="996f9-114">**CMSPCallMultiGraph**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallmultigraph)
</dt> </dl>

 

 



