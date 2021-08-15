---
description: As páginas do espaço de endereço virtual de um processo podem estar em um dos estados a seguir.
ms.assetid: a6faa901-2966-4556-90ef-c113b1ba6c6d
title: Estado da página
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ec9c162220cd0c1accdb35e35309082a2e94c4af6023af7e7d9d7cd55be620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386399"
---
# <a name="page-state"></a>Estado da página

As páginas do espaço de endereço virtual de um processo podem estar em um dos estados a seguir.



| Estado     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gratuito      | A página não é comprometida nem reservada. A página não está acessível ao processo. Ele está disponível para ser reservado, confirmado ou simultaneamente reservado e confirmado. Tentar ler ou gravar em uma página gratuita resulta em uma exceção de violação de acesso. <br/> Um processo pode usar a [**função VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) ou [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) para liberar páginas reservadas ou comprometidas de seu espaço de endereço, retornando-as para o estado livre.<br/>                                                                                                                                                                                                                                                                                                                              |
| Reservado  | A página foi reservada para uso futuro. O intervalo de endereços não pode ser usado por outras funções de alocação. A página não está acessível e não tem nenhum armazenamento físico associado a ela. Ele está disponível para ser confirmado. <br/> Um processo pode usar a [**função VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) ou [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) para reservar páginas de seu espaço de endereço e posterior para fazer commit das páginas reservadas. Ele pode usar [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) ou [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) para delimitar páginas comprometidas e devolvê-las ao estado reservado.<br/>                                                                                                                                                                                                                          |
| Confirmado | Os encargos de memória foram alocados do tamanho geral da RAM e dos arquivos de paging no disco. A página é acessível e o acesso é controlado por uma das [constantes de proteção de memória](memory-protection-constants.md). O sistema inicializa e carrega cada página comprometida na memória física somente durante a primeira tentativa de leitura ou gravação nessa página. Quando o processo é encerrado, o sistema libera o armazenamento para páginas comprometidas. <br/> Um processo pode usar [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) ou [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) para fazer commit de páginas físicas de uma região reservada. Eles também podem reservar e fazer commit de páginas simultaneamente.<br/> As [**funções GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) [**e LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) alocam páginas comprometidas com acesso de leitura/gravação.<br/> |



 

 

 
