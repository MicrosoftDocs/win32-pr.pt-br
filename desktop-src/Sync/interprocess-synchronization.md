---
description: Vários processos podem ter identificador para o mesmo evento, mutex, semáforo ou objeto de temporizador, para que esses objetos possam ser usados para realizar a sincronização entre processos.
ms.assetid: 1738e586-580f-4b74-95dc-ede300b6ac9a
title: Sincronização entre processos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0caf4818a05d526a70a1e3257ec6f86d0279f39ce3cf05a4411e49991db6ba15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886346"
---
# <a name="interprocess-synchronization"></a>Sincronização entre processos

Vários processos podem ter identificador para o mesmo evento, mutex, semáforo ou objeto de temporizador, para que esses objetos possam ser usados para realizar a sincronização entre processos. O processo que cria um objeto pode usar o identificador retornado pela função de criação ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex,**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)ou [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)). Outros processos podem abrir um identificador para o objeto usando seu nome ou por meio de herança ou duplicação. Para obter mais informações, consulte estes tópicos:

-   [Nomes de objeto](object-names.md)
-   [Herança de objetos](object-inheritance.md)
-   [Duplicação de objeto](object-duplication.md)

 

 
