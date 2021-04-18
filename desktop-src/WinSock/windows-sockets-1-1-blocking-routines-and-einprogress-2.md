---
description: Um grande problema na portabilidade de aplicativos de um ambiente de soquetes Berkeley para um ambiente Windows envolve o bloqueio; ou seja, invocando uma função que não retorna até que a operação associada seja concluída.
ms.assetid: 13aedad7-5f3b-4d73-b8e5-be3a095294bc
title: Rotinas de bloqueio do Windows Sockets 1,1 e EINPROGRESS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea6d45b4d25578505a3cb4ab4beb7c2c2fe90e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789410"
---
# <a name="windows-sockets-11-blocking-routines-and-einprogress"></a>Rotinas de bloqueio do Windows Sockets 1,1 e EINPROGRESS

Um grande problema na portabilidade de aplicativos de um ambiente de soquetes Berkeley para um ambiente Windows envolve o bloqueio; ou seja, invocando uma função que não retorna até que a operação associada seja concluída. Um problema surge quando a operação leva um tempo arbitrariamente longo para ser concluída: um exemplo é uma função de [**recebimento**](/windows/desktop/api/winsock/nf-winsock-recv) , que pode ser bloqueada até que os dados sejam recebidos do sistema de mesmo nível. O comportamento padrão dentro do modelo Berkeley Sockets é para um soquete operar no modo de bloqueio, a menos que o programador solicite explicitamente que as operações sejam tratadas como sem bloqueio. Os ambientes do Windows Sockets 1,1 não podem assumir o agendamento preventivo. Portanto, era altamente recomendável que os programadores usem as operações de não bloqueio (assíncrono), se possível, com o Windows Sockets 1,1. Como isso nem sempre foi possível, os recursos de pseudo-bloqueio descritos no seguinte foram fornecidos.

> [!Note]  
> O Windows Sockets 2 só é executado em sistemas operacionais de 32 bits preemptivos em que os deadlocks não são um problema. As práticas de programação recomendadas para o Windows Sockets 1,1 não são necessárias no Windows Sockets 2.

 

Mesmo em um soquete de bloqueio, algumas funções — [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind), [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)e [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) , por exemplo, são concluídas imediatamente. Não há nenhuma diferença entre uma operação de bloqueio e de não bloqueio para essas funções. Outras operações, como [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), podem ser concluídas imediatamente ou levar um tempo arbitrário para serem concluídas, dependendo de várias condições de transporte. Quando aplicado a um soquete de bloqueio, essas operações são conhecidas como operações de bloqueio. As seguintes funções podem bloquear:

-   [**recebidos**](/windows/desktop/api/winsock/nf-winsock-recv)
-   [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)
-   [**Enviar**](/windows/desktop/api/Winsock2/nf-winsock2-send)
-   [**Enviar**](/windows/desktop/api/winsock/nf-winsock-sendto)

Com o Windows Sockets de 16 bits 1,1, uma operação de bloqueio que não pode ser concluída imediatamente é manipulada pelo pseudo-bloqueio da seguinte maneira.

O provedor de serviços inicia a operação e, em seguida, entra em um loop no qual ele distribui todas as mensagens do Windows (produzindo o processador para outro thread, se necessário) e, em seguida, verifica a conclusão da função do Windows Sockets. Se a função tiver sido concluída, ou se [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall) tiver sido invocado, a função de bloqueio será concluída com um resultado apropriado.

Um provedor de serviços deve permitir a instalação de uma função de gancho de bloqueio que não processe mensagens para evitar a possibilidade de mensagens reentrante enquanto uma operação de bloqueio estiver pendente. A função de gancho de bloqueio mais simples retornaria **false**. Se uma DLL do Windows Sockets depender de mensagens para operação interna, ela poderá executar **PeekMessage**(**hMyWnd**...) antes de executar o gancho de bloqueio de aplicativo para que ele possa obter suas mensagens sem afetar o restante do sistema.

Em um ambiente Windows Sockets 1,1 de 16 bits, se uma mensagem do Windows for recebida para um processo para o qual uma operação de bloqueio está em andamento, haverá um risco de que o aplicativo tente emitir outra chamada do Windows Sockets. Devido à dificuldade de gerenciar essa condição com segurança, o Windows Sockets 1,1 não oferece suporte a esse comportamento de aplicativo. Um aplicativo não tem permissão para fazer mais de uma chamada de função aninhada do Windows Sockets. Apenas uma chamada de função pendente é permitida para uma tarefa específica. As únicas exceções são duas funções que são fornecidas para auxiliar o programador nessa situação: [**WSAIsBlocking**](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) e [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).

A função [**WSAIsBlocking**](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) pode ser chamada a qualquer momento para determinar se uma chamada de bloqueio do Windows sockets 1,1 está em andamento. Da mesma forma, a função [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall) pode ser chamada a qualquer momento para cancelar uma chamada de bloqueio em andamento. Qualquer outro aninhamento das funções do Windows Sockets falha com o erro WSAEINPROGRESS.

Deve-se enfatizar que essa restrição se aplica a operações de bloqueio e não bloqueio. Para aplicativos do Windows Sockets 2 que negociam a versão 2,0 ou superior no momento da chamada de [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup), nenhuma restrição sobre o aninhamento das operações é encerrada. As operações podem se tornar aninhadas em raras circunstâncias, como durante um retorno de chamada de aceitação condicional [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) ou se um provedor de serviços, por sua vez, invoca uma função do Windows Sockets 2.

Embora esse mecanismo seja suficiente para aplicativos simples, ele não oferece suporte aos requisitos complexos de expedição de mensagens de aplicativos mais avançados (por exemplo, aqueles que usam o modelo MDI). Para tais aplicativos, a API do Windows Sockets inclui a função [**WSASetBlockingHook**](/windows/desktop/api/winsock2/nf-winsock2-wsasetblockinghook), que permite ao aplicativo especificar uma rotina especial que pode ser chamada em vez da rotina de expedição de mensagem padrão descrita na discussão anterior.

O provedor do Windows Sockets chamará o gancho de bloqueio somente se todas as seguintes opções forem verdadeiras:

-   A rotina é aquela que é definida como sendo capaz de bloquear.
-   O soquete especificado é um soquete de bloqueio.
-   A solicitação não pode ser concluída imediatamente.

Um soquete é definido como bloqueio por padrão, mas a função [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) com o IOCTL **FIONBIO** ou a função [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) pode definir um soquete para o modo de não bloqueio.

O gancho de bloqueio nunca é chamado e o aplicativo não precisa se preocupar com os problemas de nova entrada que o gancho de bloqueio pode introduzir, se um aplicativo seguir estas diretrizes:

-   Ele usa apenas soquetes de não bloqueio.
-   Ele usa as rotinas [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) e/ou **WSAAsyncGetXByY** em vez de [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) e **getXbyY** .

Se um aplicativo do Windows Sockets 1,1 invocar uma operação assíncrona ou sem bloqueio que usa um ponteiro para um objeto de memória (um buffer ou uma variável global, por exemplo) como um argumento, é responsabilidade do aplicativo garantir que o objeto esteja disponível para o Windows Sockets durante a operação. O aplicativo não deve invocar nenhuma função do Windows que possa afetar a viabilidade de mapeamento ou endereço da memória envolvida.

 

 



