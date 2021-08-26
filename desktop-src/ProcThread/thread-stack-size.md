---
description: Cada novo thread ou fibra recebe seu próprio espaço de pilha que consiste em memória reservada e inicialmente comprometida.
ms.assetid: abb2d5c1-040b-4c36-aae5-3517b6a8c540
title: Tamanho da pilha de threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ff392577d529ab03a3859a0c6b0a94057ff8d8e0dc3c09fef86176d5c8950ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031406"
---
# <a name="thread-stack-size"></a>Tamanho da pilha de threads

Cada novo thread ou fibra recebe seu próprio espaço de pilha que consiste em memória reservada e inicialmente comprometida. O tamanho da memória reservada representa a alocação total de pilha na memória virtual. Assim, o tamanho reservado é limitado ao intervalo de endereços virtuais. As páginas inicialmente comprometidas não utilizam memória física até que sejam referenciadas; no entanto, eles removem páginas do limite total de confirmação do sistema, que é o tamanho do arquivo de página mais o tamanho da memória física. O sistema confirma páginas adicionais da memória de pilha reservada conforme necessário, até que a pilha atinja o tamanho reservado menos uma página (que é usada como uma página de proteção para evitar o estouro de pilha) ou o sistema está tão baixo na memória que a operação falha.

É melhor escolher o menor tamanho possível de uma pilha e fazer commit da pilha necessária para que o thread ou fibra seja executado de forma confiável. Todas as páginas reservadas para a pilha não podem ser usadas para nenhuma outra finalidade.

Uma pilha é liberada quando seu thread sai. Ele não será liberado se o thread for encerrado por outro thread.

O tamanho padrão para a memória de pilha reservada e inicialmente comprometida é especificado no header de arquivo executável. A criação de thread ou fibra falhará se não houver memória suficiente para reservar ou fazer commit do número de bytes solicitados. O tamanho da reserva de pilha padrão usado pelo vinculador é de 1 MB. Para especificar um tamanho de reserva de pilha padrão diferente para todos os threads e fibra, use a instrução STACKSIZE no arquivo de definição de módulo (.def). O sistema operacional eleva o tamanho especificado para o múltiplo mais próximo da granularidade de alocação do sistema (normalmente 64 KB). Para recuperar a granularidade de alocação do sistema atual, use a [**função GetSystemInfo.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)

Para alterar o espaço de pilha inicialmente comprometido, use o parâmetro *dwStackSize* da função [**CreateThread,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)ou [**CreateFiber.**](/windows/desktop/api/WinBase/nf-winbase-createfiber) Esse valor é arredondado para cima até a página mais próxima. Em geral, o tamanho da reserva é o tamanho de reserva padrão especificado no header executável. No entanto, se o tamanho inicialmente confirmado especificado por *dwStackSize* for maior ou igual ao tamanho de reserva padrão, o tamanho da reserva será esse novo tamanho de confirmação arredondado para o múltiplo mais próximo de 1 MB.

Para alterar o tamanho da pilha reservada, defina o parâmetro *dwCreationFlags* de [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) ou [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) como STACK SIZE PARAM IS A RESERVATION e use o parâmetro \_ \_ \_ \_ \_ *dwStackSize.* Nesse caso, o tamanho confirmado inicialmente é o tamanho padrão especificado no header executável. Para fibra, use o *parâmetro dwStackReserveSize* [**de CreateFiberEx.**](/windows/desktop/api/WinBase/nf-winbase-createfiberex) O tamanho confirmado é especificado no *parâmetro dwStackCommitSize.*

A [**função SetThreadStackGuarantee**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadstackguarantee) define o tamanho mínimo da pilha associada ao thread de chamada ou fibra que estará disponível durante quaisquer exceções de estouro de pilha.

 

 
