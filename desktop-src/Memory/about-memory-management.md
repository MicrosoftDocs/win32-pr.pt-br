---
description: Cada processo no Microsoft Windows de 32 bits tem seu próprio espaço de endereço virtual que permite o endereçamento de até 4 gigabytes de memória.
ms.assetid: f259f3cb-81c0-4b5f-b6fa-9681a278019a
title: Sobre o gerenciamento de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4110bf1d0768f1321fd89ddd1d5a985e3e54aa75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105767626"
---
# <a name="about-memory-management"></a>Sobre o gerenciamento de memória

Cada processo no Microsoft Windows de 32 bits tem seu próprio espaço de endereço virtual que permite o endereçamento de até 4 gigabytes de memória. Cada processo no Windows de 64 bits tem um espaço de endereço virtual de 8 terabytes. Todos os threads de um processo podem acessar seu espaço de endereço virtual. No entanto, os threads não podem acessar a memória que pertence a outro processo, o que protege um processo de ser corrompido por outro processo.

Para obter informações sobre o espaço de endereço virtual e as funções de gerenciamento de memória, consulte os tópicos a seguir.

-   [Espaço de endereço virtual](virtual-address-space.md)
-   [Pools de memória](memory-pools.md)
-   [Informações de desempenho da memória](memory-performance-information.md)
-   [Funções de memória virtual](virtual-memory-functions.md)
-   [Funções de heap](heap-functions.md)
-   [Mapeamento de arquivo](file-mapping.md)
-   [Suporte a memória grande](large-memory-support.md)
-   [Funções globais e locais](global-and-local-functions.md)
-   [Funções da biblioteca C padrão](standard-c-library-functions.md)
-   [Comparando métodos de alocação de memória](comparing-memory-allocation-methods.md)

 

 



