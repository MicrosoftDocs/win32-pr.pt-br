---
title: Memory-Management modelos
description: Memory-Management modelos
ms.assetid: 1690901b-2a1e-455b-a440-2674f5e5dfa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a985158f54bf09d149e04c7eebc5853417e39191ca0bb854cb7d1ba5de1e5d86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019976"
---
# <a name="memory-management-models"></a>Memory-Management modelos

Como desenvolvedor, você tem várias opções para saber como a memória é alocada e liberada. Considere uma estrutura de dados complexa que consiste em nós conectados com ponteiros, como uma lista vinculada ou uma árvore. Você pode aplicar atributos que selecionam um dos seguintes modelos:

-   [Alocação e desalocação de](node-by-node-allocation-and-deallocation.md)nó por nó.
-   [Um único buffer linear alocado pelo stub para toda a árvore](stub-allocated-buffers.md).
-   [Gerenciamento de memória de stub do servidor](server-stub-memory-management.md)
-   [Um único buffer linear alocado pelo aplicativo cliente para toda a árvore](application-allocated-buffer.md).
-   [Armazenamento persistente no servidor](persistent-storage-on-the-server.md).

 

 




