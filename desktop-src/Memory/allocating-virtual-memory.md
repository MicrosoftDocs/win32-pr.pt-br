---
description: As funções de memória virtual manipulam páginas de memória. As funções usam o tamanho de uma página no computador atual para arredondar tamanhos e endereços especificados.
ms.assetid: 509cd529-ff79-4b07-9e09-3c5ae65f6cba
title: Alocando memória virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f42b4f7eb9d5de3c8c5e9339c9e5931a89e371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296723"
---
# <a name="allocating-virtual-memory"></a>Alocando memória virtual

As funções de memória virtual manipulam páginas de memória. As funções usam o tamanho de uma página no computador atual para arredondar tamanhos e endereços especificados.

A função do [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) executa uma das seguintes operações:

-   Reserva uma ou mais páginas livres.
-   Confirma uma ou mais páginas reservadas.
-   Reserva e confirma uma ou mais páginas livres.

Você pode especificar o endereço inicial das páginas a serem reservadas ou confirmadas ou pode permitir que o sistema determine o endereço. A função arredonda o endereço especificado para o limite de página apropriado. As páginas reservadas não são acessíveis, mas as páginas confirmadas podem ser alocadas com o acesso à página **\_ ReadWrite**, à **página \_ ReadOnly** ou à **página \_ NoAccess** . Quando as páginas são confirmadas, os encargos de memória são alocados do tamanho geral da RAM e dos arquivos de paginação no disco, mas cada página é inicializada e carregada na memória física somente na primeira tentativa de ler ou gravar nessa página. Você pode usar referências de ponteiro normais para acessar a memória confirmada pela função do [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) .

 

 
