---
title: Buffers de função de gerenciamento de rede
description: A biblioteca de tempo de execução RPC manipula os buffers exigidos pelas funções de gerenciamento de rede de recuperação de dados de 32 bits da seguinte maneira.
ms.assetid: f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385382d12aa5b5c8c7c93b9a833f684d913c5783
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159955"
---
# <a name="network-management-function-buffers"></a>Buffers de função de gerenciamento de rede

A biblioteca de tempo de execução RPC manipula os buffers exigidos pelas funções de gerenciamento de rede de recuperação de dados de 32 bits da seguinte maneira:

-   **Enviando dados para o servidor** (dados especificados por \[ em \] parâmetros).

    O chamador deve alocar e desalocar o buffer para a estrutura de informações relevante (ou estruturas) e passar uma variável de ponteiro para a função. O chamador não precisa especificar o comprimento do buffer.

    Exemplo: [ **NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)

-   **Recuperando dados do servidor** (dados especificados por \[ parâmetros de saída \] ).

    O sistema aloca o buffer para as informações retornadas. O chamador deve passar uma variável de ponteiro para a função na entrada. Após o retorno bem-sucedido, o ponteiro recebe o endereço do buffer alocado pelo sistema que contém as informações retornadas. Isso simplifica o código de chamada, porque o chamador não precisa estimar o tamanho do buffer ou redimensionar o buffer e emitir a função novamente.

    Quando o chamador terminar de processar as informações retornadas, ele deverá liberar a memória alocada pelo sistema chamando a função [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) . Para obter mais informações sobre como especificar tamanhos de buffer, consulte [comprimentos de buffer de função de gerenciamento de rede](network-management-function-buffer-lengths.md).

    Exemplo: [ **NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)

 

 




