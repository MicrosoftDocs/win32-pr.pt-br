---
description: Para depurar um processo que já está em execução, o depurador deve usar DebugActiveProcess com o identificador de processo. Para recuperar uma lista de identificadores de processo, use a função EnumProcesses ou Process32First.
ms.assetid: 2662411f-a69a-442b-a177-a27ea025bb01
title: Depurando um processo em execução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f3cf141da9905c76659c2ae11e9b82e2e2f5fee9bd934dce835b129678995ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279346"
---
# <a name="debugging-a-running-process"></a>Depurando um processo em execução

Para depurar um processo que já está em execução, o depurador deve usar [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) com o identificador de processo. Para recuperar uma lista de identificadores de processo, use a função [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) ou [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) .

[**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) anexa o depurador ao processo ativo. Nesse caso, somente o processo ativo pode ser depurado; seus processos filho não podem. O depurador deve ter acesso apropriado ao processo em execução para usar o **DebugActiveProcess**. Para obter mais informações sobre direitos de acesso, consulte [controle de acesso](../secauthz/access-control.md).

Depois que o depurador tiver sido criado ou anexado ao processo que pretende depurar, o sistema notificará o depurador de todos os eventos de depuração que ocorrem no processo e, se especificado, em qualquer processo filho. Para obter mais informações sobre eventos de depuração, consulte [Debugging Events](debugging-events.md).

Para desanexar do processo que está sendo depurado, o depurador deve usar a função [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop) .

 

 
