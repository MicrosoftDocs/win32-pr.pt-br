---
description: Cada novo thread ou fibra recebe seu próprio espaço de pilha que consiste em memória reservada e inicialmente confirmada.
ms.assetid: abb2d5c1-040b-4c36-aae5-3517b6a8c540
title: Tamanho da pilha de threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4204e0bffa13fb43b6ea9520b60c0505372bad6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921904"
---
# <a name="thread-stack-size"></a>Tamanho da pilha de threads

Cada novo thread ou fibra recebe seu próprio espaço de pilha que consiste em memória reservada e inicialmente confirmada. O tamanho da memória reservada representa a alocação de pilha total na memória virtual. Como tal, o tamanho reservado é limitado ao intervalo de endereços virtuais. As páginas inicialmente confirmadas não utilizam memória física até que sejam referenciadas; no entanto, eles removem páginas do limite de confirmação total do sistema, que é o tamanho do arquivo de paginação mais o tamanho da memória física. O sistema confirma páginas adicionais da memória da pilha reservada conforme necessário, até que a pilha atinja o tamanho reservado menos uma página (que é usada como uma página de proteção para evitar o estouro de pilha) ou o sistema está tão baixo na memória que a operação falha.

É melhor escolher o tamanho de uma pilha menor possível e confirmar a pilha necessária para que o thread ou a fibra sejam executados de forma confiável. Todas as páginas reservadas para a pilha não podem ser usadas para nenhuma outra finalidade.

Uma pilha é liberada quando seu thread é encerrado. Ele não será liberado se o thread for encerrado por outro thread.

O tamanho padrão da memória da pilha reservada e inicialmente confirmada é especificado no cabeçalho do arquivo executável. A criação de thread ou fibra falhará se não houver memória suficiente para reservar ou confirmar o número de bytes solicitados. O tamanho de reserva de pilha padrão usado pelo vinculador é 1 MB. Para especificar um tamanho de reserva de pilha padrão diferente para todos os threads e fibras, use a instrução STACKSIZE no arquivo de definição de módulo (. def). O sistema operacional arredonda o tamanho especificado para o múltiplo mais próximo da granularidade de alocação do sistema (normalmente 64 KB). Para recuperar a granularidade de alocação do sistema atual, use a função [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) .

Para alterar o espaço de pilha confirmada inicialmente, use o parâmetro *dwStackSize* da função [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread), [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)ou [**CreateFiber**](/windows/desktop/api/WinBase/nf-winbase-createfiber) . Esse valor é arredondado para a página mais próxima. Em geral, o tamanho da reserva é o tamanho de reserva padrão especificado no cabeçalho do executável. No entanto, se o tamanho inicialmente confirmado especificado por *dwStackSize* for maior ou igual ao tamanho de reserva padrão, o tamanho da reserva será esse novo tamanho de confirmação arredondado para o múltiplo mais próximo de 1 MB.

Para alterar o tamanho da pilha reservada, defina o parâmetro *dwCreationFlags* de [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) ou [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) como Stack \_ Size \_ param como \_ \_ uma \_ reserva e use o parâmetro *dwStackSize* . Nesse caso, o tamanho inicialmente confirmado é o tamanho padrão especificado no cabeçalho do executável. Para fibras, use o parâmetro *dwStackReserveSize* de [**CreateFiberEx**](/windows/desktop/api/WinBase/nf-winbase-createfiberex). O tamanho confirmado é especificado no parâmetro *dwStackCommitSize* .

A função [**SetThreadStackGuarantee**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadstackguarantee) define o tamanho mínimo da pilha associada ao thread de chamada ou à fibra que estará disponível durante qualquer exceção de estouro de pilha.

 

 
