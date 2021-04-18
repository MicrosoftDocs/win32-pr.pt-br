---
description: As funções de memória virtual permitem que um processo manipule ou determine o status das páginas em seu espaço de endereço virtual.
ms.assetid: 9488a854-1ef0-488f-b3d1-57c1acb82a88
title: Funções de memória virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c76866fd10dac01315622e8a4faef7bea436a61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780620"
---
# <a name="virtual-memory-functions"></a>Funções de memória virtual

As funções de memória virtual permitem que um processo manipule ou determine o status das páginas em seu espaço de endereço virtual. Eles podem executar as seguintes operações:

-   Reserve um intervalo de espaço de endereço virtual de um processo. Reservar espaço de endereço não aloca nenhum armazenamento físico, mas impede que outras operações de alocação usem o intervalo especificado. Ele não afeta os espaços de endereço virtual de outros processos. Reservar páginas impede o consumo de armazenamento físico necessário, ao mesmo tempo em que permite que um processo Reserve um intervalo de seu espaço de endereço no qual uma estrutura de dados dinâmica pode crescer. O processo pode alocar armazenamento físico para esse espaço, conforme necessário.
-   Confirme um intervalo de páginas reservadas no espaço de endereço virtual de um processo para que o armazenamento físico (na RAM ou no disco) seja acessível somente para o processo de alocação.
-   Especifique leitura/gravação, somente leitura ou nenhum acesso para um intervalo de páginas confirmadas. Isso difere das funções de alocação padrão que sempre alocam páginas com acesso de leitura/gravação.
-   Libere uma variedade de páginas reservadas, tornando o intervalo de endereços virtuais disponíveis para operações de alocação subsequentes pelo processo de chamada.
-   Desconfirme um intervalo de páginas confirmadas, liberando seu armazenamento físico e disponibilizando-a para alocação subsequente por qualquer processo.
-   Bloqueie uma ou mais páginas de memória confirmada na RAM (memória física) para que o sistema não possa trocar as páginas no arquivo de paginação.
-   Obtenha informações sobre um intervalo de páginas no espaço de endereço virtual do processo de chamada ou um processo especificado.
-   Alterar a proteção de acesso para um intervalo especificado de páginas confirmadas no espaço de endereço virtual do processo de chamada ou um processo especificado.

Para obter mais informações, consulte os tópicos a seguir.

-   [Alocando memória virtual](allocating-virtual-memory.md)
-   [Comparando métodos de alocação de memória](comparing-memory-allocation-methods.md)
-   [Liberando memória virtual](freeing-virtual-memory.md)
-   [Trabalhando com páginas](working-with-pages.md)
-   [Funções de gerenciamento de memória](memory-management-functions.md)

 

 



