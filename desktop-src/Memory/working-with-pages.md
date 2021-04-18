---
description: Para determinar o tamanho de uma página no computador atual, use a função GetSystemInfo.
ms.assetid: 953ddfc4-6126-41fb-81a3-0ce1f0fb223f
title: Trabalhando com páginas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66c12c99ada03dca1e17c72c2a5f0d5360b6a98d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502059"
---
# <a name="working-with-pages"></a>Trabalhando com páginas

Para determinar o tamanho de uma página no computador atual, use a função [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) .

As funções [**VirtualQuery**](/windows/win32/api/memoryapi/nf-memoryapi-virtualquery) e [**VirtualQueryEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualqueryex) retornam informações sobre uma região de páginas consecutivas que começam em um endereço especificado no espaço de endereço de um processo. **VirtualQuery** retorna informações sobre a memória no processo de chamada. **VirtualQueryEx** retorna informações sobre a memória em um processo especificado e é usada para dar suporte a depuradores que precisam de informações sobre um processo que está sendo depurado. A região de páginas é limitada pelo endereço especificado arredondado para baixo até o limite de página mais próximo. Ele se estende por todas as páginas subsequentes com os seguintes atributos em comum:

-   O estado de todas as páginas é o mesmo: confirmada, reservada ou gratuita.
-   Se a página inicial não for gratuita, todas as páginas na região serão parte da mesma alocação inicial de páginas que foram reservadas por uma chamada para o [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc).
-   A proteção de acesso de todas as páginas é a mesma (ou seja, a **página \_ ReadOnly**, a **página \_ ReadWrite** ou a **página \_ NoAccess**).

A função [**VirtualLock**](/windows/win32/api/memoryapi/nf-memoryapi-virtuallock) permite que um processo bloqueie uma ou mais páginas de memória confirmada na memória física (RAM), impedindo que o sistema permutasse as páginas para o arquivo de paginação. Ele pode ser usado para garantir que os dados críticos estejam acessíveis sem acesso ao disco. O bloqueio de páginas na memória é perigoso porque restringe a capacidade do sistema de gerenciar memória. O uso excessivo de **VirtualLock** pode prejudicar o desempenho do sistema, fazendo com que o código executável seja trocado para o arquivo de paginação. A função [**VirtualUnlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) desbloqueia a memória bloqueada pelo **VirtualLock**.

A função [**usar VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) permite que um processo modifique a proteção de acesso de qualquer página confirmada no espaço de endereço de um processo. Por exemplo, um processo pode alocar páginas de leitura/gravação para armazenar dados confidenciais e, em seguida, pode alterar o acesso para somente leitura ou sem acesso para proteger contra a substituição acidental. O **usar VirtualProtect** normalmente é usado com páginas alocadas pelo [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), mas também funciona com páginas confirmadas por qualquer uma das outras funções de alocação. No entanto, o **usar VirtualProtect** altera a proteção de páginas inteiras e os ponteiros retornados pelas outras funções não são necessariamente alinhados aos limites da página. A função [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) é semelhante a **usar VirtualProtect**, exceto que ela altera a proteção da memória em um processo especificado. A alteração da proteção é útil para os depuradores no acesso à memória de um processo que está sendo depurado.

 

 
