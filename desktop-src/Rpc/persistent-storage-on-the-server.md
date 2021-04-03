---
title: Armazenamento persistente no servidor
description: Você pode otimizar seu aplicativo para que o stub do servidor não Libere memória no servidor na conclusão de uma chamada de procedimento remoto.
ms.assetid: 340334e2-94ac-4be2-a16d-38bc4c64e7db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7237fe6136918e5495ee1f22bac0991d71c5dbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916453"
---
# <a name="persistent-storage-on-the-server"></a>Armazenamento persistente no servidor

Você pode otimizar seu aplicativo para que o stub do servidor não Libere memória no servidor na conclusão de uma chamada de procedimento remoto. Por exemplo, quando um identificador de contexto será manipulado por vários procedimentos remotos, você poderá usar o atributo ACF **\[ ALLOCATE (não \_ livre \] )** para manter a memória alocada no servidor.

O atributo **\[ ALLOCATE (não \_ livre \] )** é adicionado à declaração de **typedef** de ACF no ACF. Por exemplo:

``` syntax
/* ACF file fragment */
typedef [allocate(all_nodes, dont_free)] P_TREE_TYPE;
```

Quando o atributo **\[ ALLOCATE (não \_ livre \] )** é especificado, a estrutura de dados de árvore é alocada, mas não liberada, pelo stub do servidor. Quando você torna os ponteiros para essas áreas de dados persistentes disponíveis para outras rotinas — por exemplo, copiando os ponteiros para variáveis globais — os dados retidos podem ser acessados por outras funções de servidor. O atributo **\[ ALLOCATE (não \_ livre \] )** é particularmente útil para manter estruturas de ponteiro persistentes como parte das informações de estado do servidor associadas a um tipo de identificador de contexto.

 

 




