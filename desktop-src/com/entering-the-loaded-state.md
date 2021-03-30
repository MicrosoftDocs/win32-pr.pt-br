---
title: Inserindo o estado carregado
description: Inserindo o estado carregado
ms.assetid: 841b6f1a-cf9d-4a7e-9732-0701777a9617
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add74927d107d7f6b9fe2d76856adec6697a00c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635549"
---
# <a name="entering-the-loaded-state"></a><span data-ttu-id="36346-103">Inserindo o estado carregado</span><span class="sxs-lookup"><span data-stu-id="36346-103">Entering the Loaded State</span></span>

<span data-ttu-id="36346-104">Quando um objeto entra no estado Loaded, as estruturas na memória que representam o objeto são criadas para que as operações possam ser invocadas nele.</span><span class="sxs-lookup"><span data-stu-id="36346-104">When an object enters the loaded state, the in-memory structures representing the object are created so that operations can be invoked on it.</span></span> <span data-ttu-id="36346-105">O manipulador do objeto ou o servidor em processo é carregado.</span><span class="sxs-lookup"><span data-stu-id="36346-105">The object's handler or in-process server is loaded.</span></span> <span data-ttu-id="36346-106">Esse processo, conhecido como *instanciação*, ocorre quando um objeto é carregado do armazenamento persistente (uma transição do passivo para o estado carregado) ou quando um objeto está sendo criado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="36346-106">This process, referred to as *instantiation*, occurs when an object is loaded from persistent storage (a transition from the passive to the loaded state) or when an object is being created for the first time.</span></span>

<span data-ttu-id="36346-107">Internamente, a instanciação é um processo de duas fases.</span><span class="sxs-lookup"><span data-stu-id="36346-107">Internally, instantiation is a two-phase process.</span></span> <span data-ttu-id="36346-108">Um objeto da classe apropriada é criado, após o qual um método nesse objeto é chamado para executar a inicialização e conceder acesso aos dados do objeto.</span><span class="sxs-lookup"><span data-stu-id="36346-108">An object of the appropriate class is created, after which a method on that object is called to perform initialization and give access to the object's data.</span></span> <span data-ttu-id="36346-109">O método de inicialização é definido em uma das interfaces com suporte do objeto.</span><span class="sxs-lookup"><span data-stu-id="36346-109">The initialization method is defined in one of the object's supported interfaces.</span></span> <span data-ttu-id="36346-110">O método de inicialização específico chamado depende do contexto no qual o objeto está sendo instanciado e o local dos dados de inicialização.</span><span class="sxs-lookup"><span data-stu-id="36346-110">The particular initialization method called depends on the context in which the object is being instantiated and the location of the initialization data.</span></span>

 

 




