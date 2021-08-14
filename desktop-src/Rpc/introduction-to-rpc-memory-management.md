---
title: Introdução ao gerenciamento de memória RPC
description: Introdução ao gerenciamento de memória RPC (chamada de procedimento remoto).
ms.assetid: 3474d79c-93ef-4221-b9ea-9173978e2929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a169f87bbd8a9747dd7a4983a26f1122cf575e95434ed0dd3be346bae12b9a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928922"
---
# <a name="introduction-to-rpc-memory-management"></a>Introdução ao gerenciamento de memória RPC

No contexto de RPC, o gerenciamento de memória envolve:

-   Alocar e desalocar a memória necessária para simular um único espaço de endereço conceitual entre o cliente e o servidor nos espaços de endereço diferentes dos threads do cliente e do servidor.
-   Determinar qual componente de software é responsável por gerenciar a memória — o aplicativo ou o stub gerado por MIDL.
-   Selecionando atributos de MIDL que afetam o gerenciamento de memória: atributos direcionais, atributos de ponteiro, atributos de matriz e os atributos de ACF \[ [ \_ contagem de bytes](/windows/desktop/Midl/byte-count) \] , \[ [alocação](/windows/desktop/Midl/allocate) \] e \[ [habilitação de \_ alocação](/windows/desktop/Midl/enable-allocate) \] .

Quando um programa chama uma função ou um procedimento em seu espaço de endereço, o gerenciamento de memória é mais direto do que em um aplicativo distribuído. Para ilustrar, o diagrama a seguir ilustra uma árvore binária. Para passar essa estrutura de dados para um procedimento em seu espaço de endereço, um programa simplesmente passa um ponteiro para a raiz da árvore.

![uma árvore binária, com ponteiros para estruturar dados armazenados na raiz da árvore](images/bintree.png)

Os aplicativos RPC cliente/servidor compartilham dados em dois espaços de memória diferentes. Esses espaços de memória podem ou não estar no mesmo computador. De qualquer forma, o cliente e o servidor não têm acesso direto ao espaço de memória uns dos outros. O RPC depende da capacidade de simular o espaço de endereço do programa cliente no espaço de endereço do programa do servidor. Ele também deve retornar dados, incluindo dados novos e alterados, do servidor para a memória do cliente.

Em casos como a árvore binária representada no diagrama anterior, não é suficiente passar um ponteiro para o nó raiz para um procedimento remoto. O programa ou os stubs devem passar a árvore inteira para o espaço de endereço do servidor para que o procedimento remoto opere nele.

 

 