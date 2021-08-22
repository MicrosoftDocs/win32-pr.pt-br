---
description: Para determinar o tamanho de uma página no computador atual, use a função GetSystemInfo.
ms.assetid: 953ddfc4-6126-41fb-81a3-0ce1f0fb223f
title: Trabalhando com páginas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e47e8a352b13c12b38acca1a93f12886d83d24c4d43faa213a88cf5855b18c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067656"
---
# <a name="working-with-pages"></a>Trabalhando com páginas

Para determinar o tamanho de uma página no computador atual, use a [**função GetSystemInfo.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)

As [**funções VirtualQuery**](/windows/win32/api/memoryapi/nf-memoryapi-virtualquery) e [**VirtualQueryEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualqueryex) retornam informações sobre uma região de páginas consecutivas começando em um endereço especificado no espaço de endereço de um processo. **O VirtualQuery** retorna informações sobre a memória no processo de chamada. **VirtualQueryEx** retorna informações sobre a memória em um processo especificado e é usado para dar suporte a depurador que precisam de informações sobre um processo que está sendo depurado. A região de páginas é limitada pelo endereço especificado arredondado para baixo até o limite de página mais próximo. Ele se estende por todas as páginas subsequentes com os seguintes atributos em comum:

-   O estado de todas as páginas é o mesmo: comprometido, reservado ou gratuito.
-   Se a página inicial não for gratuita, todas as páginas na região fazem parte da mesma alocação inicial de páginas que foram reservadas por uma chamada para [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc).
-   A proteção de acesso de todas as páginas é a mesma (ou seja, **PAGE \_ READONLY,** **PAGE \_ READWRITE** ou **PAGE \_ NOACCESS**).

A [**função VirtualLock**](/windows/win32/api/memoryapi/nf-memoryapi-virtuallock) permite que um processo bloqueie uma ou mais páginas de memória comprometida na memória física (RAM), impedindo que o sistema permute as páginas para o arquivo de paginação. Ele pode ser usado para garantir que os dados críticos sejam acessíveis sem acesso ao disco. O bloqueio de páginas na memória é perigoso porque restringe a capacidade do sistema de gerenciar a memória. O uso excessivo **do VirtualLock** pode prejudicar o desempenho do sistema, fazendo com que o código executável seja trocado para o arquivo de paging. A [**função VirtualUnlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) desbloqueia a memória bloqueada pelo **VirtualLock.**

A [**função VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) permite que um processo modifique a proteção de acesso de qualquer página comprometida no espaço de endereço de um processo. Por exemplo, um processo pode alocar páginas de leitura/gravação para armazenar dados confidenciais e, em seguida, pode alterar o acesso para somente leitura ou nenhum acesso para proteger contra substituição acidental. **O VirtualProtect** normalmente é usado com páginas alocadas por [**VirtualAlloc,**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)mas também funciona com páginas confirmadas por qualquer uma das outras funções de alocação. No entanto, **o VirtualProtect** altera a proteção de páginas inteiras e os ponteiros retornados pelas outras funções não são necessariamente alinhados nos limites da página. A [**função VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) é semelhante a **VirtualProtect**, exceto que ela altera a proteção da memória em um processo especificado. Alterar a proteção é útil para depurador no acesso à memória de um processo que está sendo depurado.

 

 
