---
description: Cada processo no Microsoft Windows de 32 bits tem seu próprio espaço de endereço virtual que permite lidar com até 4 gigabytes de memória.
ms.assetid: f259f3cb-81c0-4b5f-b6fa-9681a278019a
title: Sobre o gerenciamento de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b2cc91b2a907fa5f9db24f42393be51bb8795200357eff0b612f8241219361
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869966"
---
# <a name="about-memory-management"></a>Sobre o gerenciamento de memória

Cada processo no Microsoft Windows de 32 bits tem seu próprio espaço de endereço virtual que permite lidar com até 4 gigabytes de memória. Cada processo em 64 bits Windows tem um espaço de endereço virtual de 8 terabytes. Todos os threads de um processo podem acessar seu espaço de endereço virtual. No entanto, os threads não podem acessar a memória que pertence a outro processo, que protege um processo de ser corrompido por outro processo.

Para obter informações sobre o espaço de endereço virtual e as funções de gerenciamento de memória, consulte os tópicos a seguir.

-   [Espaço de Endereço Virtual](virtual-address-space.md)
-   [Pools de memória](memory-pools.md)
-   [Informações de desempenho de memória](memory-performance-information.md)
-   [Funções de memória virtual](virtual-memory-functions.md)
-   [Funções de heap](heap-functions.md)
-   [Mapeamento de arquivos](file-mapping.md)
-   [Suporte à memória grande](large-memory-support.md)
-   [Funções globais e locais](global-and-local-functions.md)
-   [Funções de biblioteca C padrão](standard-c-library-functions.md)
-   [Comparando métodos de alocação de memória](comparing-memory-allocation-methods.md)

 

 



