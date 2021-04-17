---
description: O suporte a páginas grandes permite que aplicativos de servidor estabeleçam regiões de memória de página grande, o que é particularmente útil em janelas de 64 bits.
ms.assetid: 060115af-38d1-499c-b30c-47cd0cf42d20
title: Suporte a Large-Page
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4578b5127e6613f2ff4b6e0b8a7cffcc53c9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758424"
---
# <a name="large-page-support"></a>Suporte a Large-Page

O suporte a páginas grandes permite que aplicativos de servidor estabeleçam regiões de memória de página grande, o que é particularmente útil em janelas de 64 bits. Cada conversão de página grande usa um único buffer de conversão dentro da CPU. O tamanho desse buffer normalmente é de três ordens de magnitude maiores do que o tamanho da página nativa; Isso aumenta a eficiência do buffer de conversão, o que pode aumentar o desempenho da memória acessada com frequência.

O procedimento a seguir descreve como usar o suporte a páginas grandes.

**Para usar o suporte de página grande**

1.  Obtenha o privilégio **SeLockMemoryPrivilege** chamando a função [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) . Para obter mais informações, consulte [atribuindo privilégios a uma conta](../secbp/assigning-privileges-to-an-account.md) e [alterando privilégios em um token](../secbp/changing-privileges-in-a-token.md).
2.  Recupere o tamanho mínimo de página grande chamando a função [**GetLargePageMinimum**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) .
3.  Inclua o valor de **\_ \_ páginas grandes do mem** ao chamar a função do [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) . O tamanho e o alinhamento devem ser um múltiplo do mínimo de página grande.

Ao escrever aplicativos que usam memória de página grande, tenha em mente as seguintes considerações:

-   Regiões de memória de página grande podem ser difíceis de obter depois que o sistema estiver em execução por um longo tempo porque o espaço físico para cada página grande deve ser contíguo, mas a memória pode ter se tornado fragmentada. A alocação de páginas grandes sob essas condições pode afetar significativamente o desempenho do sistema. Portanto, os aplicativos devem evitar a criação de alocações de página grande repetidas e, em vez disso, alocar todas as páginas grandes uma vez, na inicialização.
-   A memória é sempre de leitura/gravação e não paginável (sempre residente na memória física).
-   A memória faz parte do processo de bytes particulares, mas não faz parte do conjunto de trabalho, pois o conjunto de trabalho por definição contém apenas memória paginável.
-   As alocações de página grande não estão sujeitas aos limites de trabalho.
-   A memória de página grande deve ser reservada e confirmada como uma única operação. Em outras palavras, as páginas grandes não podem ser usadas para confirmar um intervalo de memória reservado anteriormente.
-   O WOW64 em sistemas baseados em Intel Itanium não oferece suporte a aplicativos de 32 bits que usam esse recurso. Os aplicativos devem ser recompilados como aplicativos nativos de 64 bits.

 

 
