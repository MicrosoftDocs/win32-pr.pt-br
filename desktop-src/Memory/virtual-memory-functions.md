---
description: As funções de memória virtual permitem que um processo manipule ou determine o status das páginas em seu espaço de endereço virtual.
ms.assetid: 9488a854-1ef0-488f-b3d1-57c1acb82a88
title: Funções de memória virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bee6839a00c573a3724cd22b3d304fef4276db29507c89802b42602120180bd5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105706"
---
# <a name="virtual-memory-functions"></a>Funções de memória virtual

As funções de memória virtual permitem que um processo manipule ou determine o status das páginas em seu espaço de endereço virtual. Eles podem executar as seguintes operações:

-   Reserve um intervalo do espaço de endereço virtual de um processo. Reservar espaço de endereço não aloca nenhum armazenamento físico, mas impede que outras operações de alocação usem o intervalo especificado. Ele não afeta os espaços de endereço virtual de outros processos. A reserva de páginas impede o consumo desnecessário de armazenamento físico, permitindo que um processo reserve um intervalo de seu espaço de endereço no qual uma estrutura de dados dinâmicos pode crescer. O processo pode alocar armazenamento físico para esse espaço, conforme necessário.
-   Fazer commit de um intervalo de páginas reservadas no espaço de endereço virtual de um processo para que o armazenamento físico (na RAM ou no disco) seja acessível somente para o processo de alocação.
-   Especifique leitura/gravação, somente leitura ou nenhum acesso para um intervalo de páginas comprometidas. Isso difere das funções de alocação padrão que sempre alocam páginas com acesso de leitura/gravação.
-   Liberar um intervalo de páginas reservadas, disponibilizando o intervalo de endereços virtuais para operações de alocação subsequentes pelo processo de chamada.
-   Descommita uma variedade de páginas confirmadas, liberando seu armazenamento físico e disponibilizando-o para alocação subsequente por qualquer processo.
-   Bloqueie uma ou mais páginas de memória comprometida na MEMÓRIA FÍSICA (RAM) para que o sistema não possa trocar as páginas para o arquivo de paginação.
-   Obtenha informações sobre um intervalo de páginas no espaço de endereço virtual do processo de chamada ou um processo especificado.
-   Altere a proteção de acesso para um intervalo especificado de páginas comprometidas no espaço de endereço virtual do processo de chamada ou em um processo especificado.

Para obter mais informações, consulte estes tópicos.

-   [Alocando memória virtual](allocating-virtual-memory.md)
-   [Comparando métodos de alocação de memória](comparing-memory-allocation-methods.md)
-   [Liberando memória virtual](freeing-virtual-memory.md)
-   [Trabalhando com páginas](working-with-pages.md)
-   [Funções de gerenciamento de memória](memory-management-functions.md)

 

 



