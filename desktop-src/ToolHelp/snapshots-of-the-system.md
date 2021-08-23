---
title: Instantâneos do sistema
description: Os instantâneos estão no núcleo das funções de ajuda da ferramenta. Um instantâneo é uma cópia somente leitura do estado atual de uma ou mais das listas a seguir que residem em processos de memória do sistema, threads, módulos e heaps.
ms.assetid: a8122960-f078-4efb-8e01-bf6fb69ee0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30dde3a4383bf56bdef46c59c55611ffe9b22a7a201abb4f0f11af85594c4f0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137409"
---
# <a name="snapshots-of-the-system"></a>Instantâneos do sistema

Os instantâneos estão no núcleo das funções de ajuda da ferramenta. Um instantâneo é uma cópia somente leitura do estado atual de uma ou mais das seguintes listas que residem na memória do sistema: processos, threads, módulos e heaps.

Processos que usam funções de ajuda de ferramenta acessam essas listas de instantâneos em vez de diretamente do sistema operacional. As listas na memória do sistema mudam quando os processos são iniciados e encerrados, os threads são criados e destruídos, os módulos executáveis são carregados e descarregados da memória do sistema e os heaps são criados e destruídos. O uso de informações de um instantâneo impede inconsistências. Caso contrário, as alterações em uma lista poderão fazer com que um thread percorria incorretamente a lista ou causaria uma violação de acesso (uma falha de GP). Por exemplo, se um aplicativo percorrer a lista de threads enquanto outros threads são criados ou encerrados, as informações que o aplicativo está usando para percorrer a lista de threads poderão ficar desatualizadas e poderão causar um erro para o aplicativo que atravessa a lista.

Para tirar um instantâneo da memória do sistema, use a [**função CreateToolhelp32Snapshot.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) Você pode controlar o conteúdo de um instantâneo especificando um ou mais dos seguintes valores ao chamar essa função:

-   **TH32CS \_ SNAPHEAPLIST**
-   **TH32CS \_ SNAPMODULE**
-   **TH32CS \_ SNAPPROCESS**
-   **TH32CS \_ SNAPTHREAD**

Os **valores TH32CS \_ SNAPHEAPLIST** e **TH32CS \_ SNAPMODULE** são específicos do processo. Quando esses valores são especificados, as listas de heap e módulo do processo especificado são incluídas no instantâneo. Se você especificar zero como o identificador do processo, o processo atual será usado. O **valor TH32CS \_ SNAPTHREAD** sempre cria um instantâneo em todo o sistema, mesmo que um identificador de processo seja passado para [**CreateToolhelp32Snapshot.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)

Para enumerar o estado do heap ou do módulo para todos os processos, especifique o valor **TH32CS \_ SNAPALL** e o identificador de processo do processo atual. Em seguida, para cada processo adicional no instantâneo, chame [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) novamente, especificando seu identificador de processo e o **valor TH32CS \_ SNAPHEAPLIST** ou **TH32CS \_ SNAPMODULE.**

Você pode recuperar um código de status de erro estendido [**para CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) usando a [**função GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

Quando o processo terminar de usar um instantâneo, destrua-o usando a [**função CloseHandle.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) Se você não destruir um instantâneo, o processo irá vazamento de memória até que ele saia, momento em que o sistema recupera a memória.

> [!Note]  
> O alça de instantâneo atua como um alça de arquivo e está sujeito às mesmas regras em relação aos processos e threads nos quais ele pode ser usado. Para especificar que o handle é herdável, crie o instantâneo usando o **valor TH32CS \_ INHERIT.**

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tirar um instantâneo e exibir processos](taking-a-snapshot-and-viewing-processes.md)
</dt> </dl>

 

 