---
title: Comunicação entre processos
description: As técnicas a seguir podem ser usadas para comunicação entre aplicativos de 32 bits e de 64 bits.
ms.assetid: 9a60ccfe-4ccf-44d7-9522-42609d95217b
keywords:
- programação de comunicação entre processos 64 de Windows bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5089440caf6ac537a314e7e920796fadeac5817220ba91f283c297bd0451b705
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734116"
---
# <a name="interprocess-communication-between-32-bit-and-64-bit-applications"></a>Comunicação entre processos entre aplicativos de 32 bits e de 64 bits

As técnicas a seguir podem ser usadas para comunicação entre aplicativos de 32 bits e de 64 bits:

-   as versões de 64 bits do Windows usam identificadores de 32 bits para interoperabilidade. Ao compartilhar um identificador entre os aplicativos de 32 bits e 64 bits, somente os menores bits 32 são significativos, portanto, é seguro truncar o identificador (ao passá-lo de 64 para 32 bits) ou estender a alça (ao passá-lo de 32 para 64 bits). Identificadores que podem ser compartilhados incluem identificadores para objetos de usuário como Windows (**HWND**), identificadores para objetos GDI, como canetas e pincéis (**HBRUSH** e **HPEN**), e identificadores para objetos nomeados, como mutexes, semáforos e identificadores de arquivo.
-   RPC (chamadas de procedimento remoto) podem ser usadas.
-   O COM LocalServers pode ser usado se as DLLs de proxy/stub de 32 bits e de 64 bits estiverem registradas para todas as interfaces usadas.
-   A memória compartilhada poderá ser usada se tipos dependentes de ponteiro forem convertidos corretamente (ou evitados).
-   As funções [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) e [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) podem iniciar processos de 32 bits e 64 bits a partir de processos de 32 bits ou de 64 bits com certas limitações.

Um arquivo executável de 64 bits localizado em% windir% \\ system32 não pode ser iniciado a partir de um processo de 32 bits, pois o redirecionador do sistema de arquivos redireciona o caminho. Não desabilite o redirecionamento para fazer isso; \\em vez disso, use% windir% SysNative. Para obter mais informações, consulte [redirecionador de sistema de arquivos](file-system-redirector.md).

 

 