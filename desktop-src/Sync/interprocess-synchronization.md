---
description: Vários processos podem ter identificadores para o mesmo objeto de evento, mutex, semáforo ou temporizador, para que esses objetos possam ser usados para realizar a sincronização entre processos.
ms.assetid: 1738e586-580f-4b74-95dc-ede300b6ac9a
title: Sincronização entre processos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c18fb26d6a64fdc2d785d16c7bccb8b007c3f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749193"
---
# <a name="interprocess-synchronization"></a><span data-ttu-id="e5f07-103">Sincronização entre processos</span><span class="sxs-lookup"><span data-stu-id="e5f07-103">Interprocess Synchronization</span></span>

<span data-ttu-id="e5f07-104">Vários processos podem ter identificadores para o mesmo objeto de evento, mutex, semáforo ou temporizador, para que esses objetos possam ser usados para realizar a sincronização entre processos.</span><span class="sxs-lookup"><span data-stu-id="e5f07-104">Multiple processes can have handles to the same event, mutex, semaphore, or timer object, so these objects can be used to accomplish interprocess synchronization.</span></span> <span data-ttu-id="e5f07-105">O processo que cria um objeto pode usar o identificador retornado pela função de criação ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**createsemáforo**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)ou [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)).</span><span class="sxs-lookup"><span data-stu-id="e5f07-105">The process that creates an object can use the handle returned by the creation function ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea), or [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)).</span></span> <span data-ttu-id="e5f07-106">Outros processos podem abrir um identificador para o objeto usando seu nome ou por meio de herança ou duplicação.</span><span class="sxs-lookup"><span data-stu-id="e5f07-106">Other processes can open a handle to the object by using its name, or through inheritance or duplication.</span></span> <span data-ttu-id="e5f07-107">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="e5f07-107">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="e5f07-108">Nomes de objeto</span><span class="sxs-lookup"><span data-stu-id="e5f07-108">Object Names</span></span>](object-names.md)
-   [<span data-ttu-id="e5f07-109">Herança de objetos</span><span class="sxs-lookup"><span data-stu-id="e5f07-109">Object Inheritance</span></span>](object-inheritance.md)
-   [<span data-ttu-id="e5f07-110">Duplicação de objeto</span><span class="sxs-lookup"><span data-stu-id="e5f07-110">Object Duplication</span></span>](object-duplication.md)

 

 
