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
# <a name="interprocess-synchronization"></a>Sincronização entre processos

Vários processos podem ter identificadores para o mesmo objeto de evento, mutex, semáforo ou temporizador, para que esses objetos possam ser usados para realizar a sincronização entre processos. O processo que cria um objeto pode usar o identificador retornado pela função de criação ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**createsemáforo**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)ou [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)). Outros processos podem abrir um identificador para o objeto usando seu nome ou por meio de herança ou duplicação. Para mais informações, consulte os seguintes tópicos:

-   [Nomes de objeto](object-names.md)
-   [Herança de objetos](object-inheritance.md)
-   [Duplicação de objeto](object-duplication.md)

 

 
