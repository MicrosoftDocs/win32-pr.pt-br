---
description: As páginas do espaço de endereço virtual de um processo podem estar em um dos Estados a seguir.
ms.assetid: a6faa901-2966-4556-90ef-c113b1ba6c6d
title: Estado da página
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82a1e5d3170197cf977f0b1a91898ee150086ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172167"
---
# <a name="page-state"></a>Estado da página

As páginas do espaço de endereço virtual de um processo podem estar em um dos Estados a seguir.



| Estado     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gratuita      | A página não está confirmada nem reservada. A página não está acessível para o processo. Ela está disponível para ser reservada, confirmada ou reservada e confirmada simultaneamente. A tentativa de ler ou gravar em uma página livre resulta em uma exceção de violação de acesso. <br/> Um processo pode usar a função [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) ou [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) para liberar páginas reservadas ou confirmadas de seu espaço de endereço, retornando-as para o estado gratuito.<br/>                                                                                                                                                                                                                                                                                                                              |
| Reservado  | A página foi reservada para uso futuro. O intervalo de endereços não pode ser usado por outras funções de alocação. A página não está acessível e não tem armazenamento físico associado a ela. Ele está disponível para ser confirmado. <br/> Um processo pode usar a função [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) ou [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) para reservar páginas de seu espaço de endereço e posteriormente para confirmar as páginas reservadas. Ele pode usar [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) ou [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) para desconfirmar páginas confirmadas e retorná-las ao estado reservado.<br/>                                                                                                                                                                                                                          |
| Confirmado | Os encargos de memória foram alocados do tamanho geral da RAM e dos arquivos de paginação no disco. A página está acessível e o acesso é controlado por uma das [constantes de proteção de memória](memory-protection-constants.md). O sistema inicializa e carrega cada página confirmada na memória física somente durante a primeira tentativa de ler ou gravar nessa página. Quando o processo é encerrado, o sistema libera o armazenamento para páginas confirmadas. <br/> Um processo pode usar o [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) ou o [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) para confirmar páginas físicas de uma região reservada. Eles também podem reservar e confirmar páginas simultaneamente.<br/> As funções [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) e [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) alocam páginas confirmadas com acesso de leitura/gravação.<br/> |



 

 

 
