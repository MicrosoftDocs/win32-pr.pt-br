---
title: Provedor ADSI de WinNT
description: O provedor ADSI da Microsoft implementa um conjunto de objetos ADSI para dar suporte a várias interfaces ADSI.
ms.assetid: 6341be08-2e53-4708-a403-09c86fcc31a8
ms.tgt_platform: multiple
keywords:
- ADSI do provedor do ADSI Winnt
- ADSI do provedor de serviços WinNT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9748e17185417eb382281774c31554cb983742
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363657"
---
# <a name="adsi-winnt-provider"></a><span data-ttu-id="df077-105">Provedor ADSI de WinNT</span><span class="sxs-lookup"><span data-stu-id="df077-105">ADSI WinNT Provider</span></span>

<span data-ttu-id="df077-106">O provedor ADSI da Microsoft implementa um conjunto de objetos ADSI para dar suporte a várias interfaces ADSI.</span><span class="sxs-lookup"><span data-stu-id="df077-106">The Microsoft ADSI provider implements a set of ADSI objects to support various ADSI interfaces.</span></span> <span data-ttu-id="df077-107">O nome do namespace para o provedor do Windows é "WinNT" e esse provedor é conhecido como o provedor de WinNT.</span><span class="sxs-lookup"><span data-stu-id="df077-107">The namespace name for the Windows provider is "WinNT" and this provider is commonly referred to as the WinNT provider.</span></span> <span data-ttu-id="df077-108">Para acessar o provedor WinNT, associe-se a qualquer um dos [objetos ADSI do Winnt](adsi-objects-of-winnt.md)usando o [ADsPath WinNT](winnt-adspath.md).</span><span class="sxs-lookup"><span data-stu-id="df077-108">To access the WinNT provider, bind to any of the [ADSI objects of WinNT](adsi-objects-of-winnt.md), using the [WinNT AdsPath](winnt-adspath.md).</span></span>

<span data-ttu-id="df077-109">O provedor WinNT está incluído no componente do sistema ADSI para Windows e Windows Server.</span><span class="sxs-lookup"><span data-stu-id="df077-109">The WinNT provider is included in the ADSI system component for Windows and Windows Server.</span></span>

> [!Note]  
> <span data-ttu-id="df077-110">O provedor WinNT padrão não pode ser considerado totalmente seguro para thread.</span><span class="sxs-lookup"><span data-stu-id="df077-110">The default WinNT provider cannot be assumed to be completely thread-safe.</span></span> <span data-ttu-id="df077-111">Os gravadores de aplicativos multissegmentados devem lidar com multithreading para coordenar corretamente qualquer acesso entre threads por meio do uso adequado de objetos de sincronização, como semáforos, exclusões mútuas, seções críticas e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="df077-111">Writers of multithreaded applications should handle multithreading to properly coordinate any access between threads through the proper use of synchronization objects such as semaphores, mutexes, critical sections, and so on.</span></span>

 

 

 




