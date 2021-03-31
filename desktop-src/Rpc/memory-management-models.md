---
title: Modelos de Memory-Management
description: Modelos de Memory-Management
ms.assetid: 1690901b-2a1e-455b-a440-2674f5e5dfa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8114f11755829be9d5f7b17b751e075701ac0aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916655"
---
# <a name="memory-management-models"></a>Modelos de Memory-Management

Como desenvolvedor, você tem várias opções de como a memória é alocada e liberada. Considere uma estrutura de dados complexa que consiste em nós conectados com ponteiros, como uma lista vinculada ou uma árvore. Você pode aplicar atributos que selecionem um dos seguintes modelos:

-   [Alocação e desalocação de nó por nó](node-by-node-allocation-and-deallocation.md).
-   [Um único buffer linear alocado pelo stub para toda a árvore](stub-allocated-buffers.md).
-   [Gerenciamento de memória de stub de servidor](server-stub-memory-management.md)
-   [Um único buffer linear alocado pelo aplicativo cliente para toda a árvore](application-allocated-buffer.md).
-   [Armazenamento persistente no servidor](persistent-storage-on-the-server.md).

 

 




