---
title: Problemas multi-threaded
description: Problemas multi-threaded
ms.assetid: 17e74d2a-af4f-4188-89fa-b4f50abc424f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0910e1602d00d3429bb9e4c7a1667bf8113cd659
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364512"
---
# <a name="multi-threaded-issues"></a><span data-ttu-id="43e00-103">Problemas multi-threaded</span><span class="sxs-lookup"><span data-stu-id="43e00-103">Multi-Threaded Issues</span></span>

<span data-ttu-id="43e00-104">O OLE fornece suporte para aplicativos multissegmentados, permitindo que os aplicativos façam chamadas OLE de vários threads.</span><span class="sxs-lookup"><span data-stu-id="43e00-104">OLE provides support for multithreaded applications, allowing applications to make OLE calls from multiple threads.</span></span> <span data-ttu-id="43e00-105">Esse suporte multithread é chamado de modelo de apartamento, é importante que todos os componentes OLE que usam vários threads sigam esse modelo.</span><span class="sxs-lookup"><span data-stu-id="43e00-105">This multithreaded support is called the apartment model, it is important that all OLE components using multiple threads follow this model.</span></span> <span data-ttu-id="43e00-106">O modelo de apartamento requer que os ponteiros de interface sejam empacotados (usando [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface)e [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)) quando passados entre threads.</span><span class="sxs-lookup"><span data-stu-id="43e00-106">The apartment model requires that interface pointers are marshaled (using [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface), and [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)) when passed between threads.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43e00-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="43e00-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43e00-108">Processos, threads e Apartments</span><span class="sxs-lookup"><span data-stu-id="43e00-108">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> </dl>

 

 




