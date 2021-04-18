---
title: Funções ApiBuffer
description: As funções de ApiBuffer de gerenciamento de rede são usadas para gerenciar a alocação de memória usada por um aplicativo com funções de gerenciamento de rede.
ms.assetid: bf2fe8aa-dda6-4f6b-9c52-d7a96b96da18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b316c6b2ee2d4095c15d5e859dd0069978c7ff91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105756716"
---
# <a name="apibuffer-functions"></a>Funções ApiBuffer

As funções de ApiBuffer de gerenciamento de rede são usadas para gerenciar a alocação de memória usada por um aplicativo com funções de gerenciamento de rede. No entanto, em geral, para outra memória usada por um aplicativo, você deve usar as [funções de gerenciamento de memória](/windows/desktop/Memory/memory-management-functions) em vez dessas funções ApiBuffer.

As funções ApiBuffer são listadas a seguir.



| Função                                                 | Descrição                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**NetApiBufferAllocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | Aloca memória a partir do heap. Chame essa função quando precisar de compatibilidade com a função **NetApiBufferFree** . |
| [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | Libera a memória alocada pela função **NetApiBufferAllocate** e outras funções de gerenciamento de rede.                   |
| [**NetApiBufferReallocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | Altera o tamanho de um buffer alocado por uma chamada para a função **NetApiBufferAllocate** .                                |
| [**NetApiBufferSize**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | Retorna o tamanho, em bytes, de um buffer alocado por uma chamada para a função **NetApiBufferAllocate** .                     |



 

Para funções remotas que retornam informações para o chamador, a biblioteca de tempo de execução RPC aloca o buffer que contém as informações de retorno. Quando o chamador terminar de processar as informações, ele deverá chamar a função [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) para liberar o buffer alocado.

 

 