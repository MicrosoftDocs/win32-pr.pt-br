---
title: Buffers de Stub-Allocated
description: Em vez de forçar uma chamada distinta para cada nó da árvore ou do grafo, você pode direcionar os stubs para computar o tamanho dos dados e alocar e liberar memória fazendo uma única chamada para o usuário de MIDL \_ \_ alocar ou o usuário de MIDL \_ \_ gratuito.
ms.assetid: 9911649d-00e8-47d8-b512-7d9b185d1e09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956acf6452c1a4e7d04afcd1da263439436e3bad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007892"
---
# <a name="stub-allocated-buffers"></a>Buffers de Stub-Allocated

Em vez de forçar uma chamada distinta para cada nó da árvore ou do grafo, você pode direcionar os stubs para computar o tamanho dos dados e alocar e liberar memória fazendo uma única chamada para o usuário de [MIDL \_ \_ alocar](/windows/desktop/Midl/midl-user-allocate-1) ou o [usuário de MIDL \_ \_ gratuito](/windows/desktop/Midl/midl-user-free-1). O atributo ACF **\[ ALLOCATE (todos os \_ nós \] )** direciona os stubs para alocar ou liberar todos os nós em uma única chamada para o usuário fornecido – funções de gerenciamento de memória.

Por exemplo, um aplicativo RPC pode usar a seguinte estrutura de dados de árvore binária:

``` syntax
/* IDL file fragment */
typedef struct _TREE_TYPE 
{
    short sNumber;
    struct _TREE_TYPE * pLeft;
    struct _TREE_TYPE * pRight;
} TREE_TYPE;

typedef TREE_TYPE * P_TREE_TYPE;
```

O atributo ACF **\[ alocar (todos os \_ nós) \]** aplicados a esse tipo de dados aparece na declaração de **typedef** no ACF como:

``` syntax
/* ACF file fragment */
typedef [allocate(all_nodes)] P_TREE_TYPE;
```

O atributo **\[ ALLOCATE \]** só pode ser aplicado a tipos de ponteiro. O atributo **\[ \] ALLOCATE** ACF é uma extensão da Microsoft para o DCE IDL e, dessa forma, não estará disponível se você COMPILAR com a opção MIDL **/OSF** Quando a **\[ alocação (todos os \_ nós) \]** é aplicada a um tipo de ponteiro, os stubs gerados pelo compilador MIDL atravessam a estrutura de dados especificada para determinar o tamanho da alocação. Os stubs fazem uma única chamada para alocar a quantidade inteira de memória necessária para o gráfico ou a árvore. Um aplicativo cliente pode liberar memória com muito mais eficiência, fazendo uma única chamada para o **\_ usuário MIDL \_ livre**. No entanto, o desempenho do stub do servidor é geralmente aumentado ao usar a alocação de memória nó a nó porque os stubs de servidor geralmente podem usar a memória privada que não requer nenhuma alocação.

Para obter informações adicionais, consulte [alocação e desalocação de nó por nó](node-by-node-allocation-and-deallocation.md).

 

 