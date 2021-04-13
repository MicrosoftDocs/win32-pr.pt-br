---
description: O COM+ apresenta Apartments neutro para simplificar a programação em ambientes multi-threaded. O apartamento neutro é o modelo preferencial para COM+ para componentes sem interface do usuário.
ms.assetid: 679742af-7c04-4b0e-822a-a43e1aafa936
title: Apartments neutro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac3bdff2670e4f99ad94af20278eaca6a38861e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370425"
---
# <a name="neutral-apartments"></a><span data-ttu-id="f30cc-104">Apartments neutro</span><span class="sxs-lookup"><span data-stu-id="f30cc-104">Neutral Apartments</span></span>

<span data-ttu-id="f30cc-105">O COM+ apresenta Apartments neutro para simplificar a programação em ambientes multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="f30cc-105">COM+ introduces neutral apartments to simplify programming in multithreaded environments.</span></span> <span data-ttu-id="f30cc-106">O apartamento neutro é o modelo preferencial para COM+ para componentes sem interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="f30cc-106">The neutral apartment is the preferred model for COM+ for components with no user interface.</span></span>

<span data-ttu-id="f30cc-107">No passado, para evitar gargalos, os desenvolvedores de COM+ que precisam de escalabilidade de servidor precisavam implementar componentes de thread livre; no entanto, os modelos de Threading livre são complicados de implementar, pois eles devem lidar com o acesso de interbloqueio.</span><span class="sxs-lookup"><span data-stu-id="f30cc-107">In the past, to prevent bottlenecks, COM+ developers requiring server scalability had to implement free-threaded components; however, free-threading models are complicated to implement because they must deal with interlocking access.</span></span> <span data-ttu-id="f30cc-108">Em apartments neutros, os objetos seguem as diretrizes para Apartments multithread, mas podem ser executados em qualquer tipo de thread.</span><span class="sxs-lookup"><span data-stu-id="f30cc-108">In neutral apartments, objects follow the guidelines for multithreaded apartments but can execute on any kind of thread.</span></span> <span data-ttu-id="f30cc-109">Quando um thread está sendo executado em um apartamento neutro, o contexto do objeto é recebido sem causar uma alternância de thread.</span><span class="sxs-lookup"><span data-stu-id="f30cc-109">When a thread is running in a neutral apartment, the object's context is received without causing a thread switch.</span></span>

<span data-ttu-id="f30cc-110">Cada processo pode ter apenas um apartamento neutro.</span><span class="sxs-lookup"><span data-stu-id="f30cc-110">Each process can have only one neutral apartment.</span></span> <span data-ttu-id="f30cc-111">Para selecionar um apartamento neutro, use a seguinte configuração do registro:</span><span class="sxs-lookup"><span data-stu-id="f30cc-111">To select a neutral apartment, use the following registry setting:</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         ThreadingModel = Neutral
```

<span data-ttu-id="f30cc-112">Os componentes que têm interfaces de usuário devem continuar usando Apartments de thread único como o modelo preferencial.</span><span class="sxs-lookup"><span data-stu-id="f30cc-112">Components that have user interfaces should continue to use single-threaded apartments as the preferred model.</span></span> <span data-ttu-id="f30cc-113">Para selecionar um apartamento de thread único, use a seguinte configuração de registro:</span><span class="sxs-lookup"><span data-stu-id="f30cc-113">To select a single-threaded apartment, use the following registry setting:</span></span>

<span data-ttu-id="f30cc-114">**ThreadingModel** = apartamento</span><span class="sxs-lookup"><span data-stu-id="f30cc-114">**ThreadingModel** = Apartment</span></span>

 

 



