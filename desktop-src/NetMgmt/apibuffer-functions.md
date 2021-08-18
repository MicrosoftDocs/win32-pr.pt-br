---
title: Funções ApiBuffer
description: As funções apiBuffer de gerenciamento de rede são usadas para gerenciar a alocação de memória usada por um aplicativo com funções de gerenciamento de rede.
ms.assetid: bf2fe8aa-dda6-4f6b-9c52-d7a96b96da18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b0778c216860fe16a673e1bdcc2ac470cbb52a128f0e08d4d32d98df929bc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912467"
---
# <a name="apibuffer-functions"></a>Funções ApiBuffer

As funções apiBuffer de gerenciamento de rede são usadas para gerenciar a alocação de memória usada por um aplicativo com funções de gerenciamento de rede. No entanto, em geral, para outras memória [usadas](/windows/desktop/Memory/memory-management-functions) por um aplicativo, você deve usar as funções de gerenciamento de memória em vez dessas funções apiBuffer.

As funções ApiBuffer são listadas a seguir.



| Função                                                 | Descrição                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**NetApiBufferAllocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | Aloca memória do heap. Chame essa função quando precisar de compatibilidade com a **função NetApiBufferFree.** |
| [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | Libera a memória alocada pela **função NetApiBufferAllocate** e outras funções de gerenciamento de rede.                   |
| [**NetApiBufferReallocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | Altera o tamanho de um buffer alocado por uma chamada para a **função NetApiBufferAllocate.**                                |
| [**NetApiBufferSize**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | Retorna o tamanho, em bytes, de um buffer alocado por uma chamada para a **função NetApiBufferAllocate.**                     |



 

Para funções remotamente remotas que retornam informações para o chamador, a biblioteca em tempo de executar RPC aloca o buffer que contém as informações de retorno. Quando o chamador terminar de processar as informações, ele deverá chamar a [**função NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) para liberar o buffer alocado.

 

 