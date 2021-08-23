---
description: Um grande problema na portação de aplicativos de um ambiente de Sockets de Berkeley para um Windows ambiente envolve o bloqueio; ou seja, invocar uma função que não retorna até que a operação associada seja concluída.
ms.assetid: 13aedad7-5f3b-4d73-b8e5-be3a095294bc
title: Windows Rotinas de bloqueio de soquetes 1.1 e EINPROGRESS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4028549862412b80d1343851fb2a147da804095821fdefab4b6aae0eb6ec5f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641216"
---
# <a name="windows-sockets-11-blocking-routines-and-einprogress"></a>Windows Rotinas de bloqueio de soquetes 1.1 e EINPROGRESS

Um grande problema na portação de aplicativos de um ambiente de Sockets de Berkeley para um Windows ambiente envolve o bloqueio; ou seja, invocar uma função que não retorna até que a operação associada seja concluída. Um problema surge quando a operação leva um tempo arbitrariamente longo para ser concluída: um exemplo é uma função [**recv,**](/windows/desktop/api/winsock/nf-winsock-recv) que pode bloquear até que os dados foram recebidos do sistema par. O comportamento padrão dentro do modelo de Soquetes Berkeley é que um soquete opere no modo de bloqueio, a menos que o programador solicita explicitamente que as operações sejam tratadas como não desbloqueio. Windows Os ambientes de soquetes 1.1 não podiam assumir o agendamento preemptivo. Portanto, era altamente recomendável que os programadores usem as operações não desbloqueio (assíncronas), se possível, com Windows Sockets 1.1. Como isso nem sempre foi possível, as instalações de pseudo-bloqueio descritas a seguir foram fornecidas.

> [!Note]  
> Windows Os soquetes 2 só são executados em sistemas operacionais preemptivos de 32 bits em que deadlocks não são um problema. As práticas de programação recomendadas para Windows Soquetes 1.1 não são necessárias Windows Sockets 2.

 

Mesmo em um soquete de bloqueio, algumas funções – [**bind**](/windows/desktop/api/winsock/nf-winsock-bind), [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)e [**getpeername,**](/windows/desktop/api/winsock/nf-winsock-getpeername) por exemplo – são concluídas imediatamente. Não há nenhuma diferença entre um bloqueio e uma operação de não desbloqueio para essas funções. Outras operações, como [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), podem ser concluídas imediatamente ou levar um tempo arbitrário para ser concluída, dependendo de várias condições de transporte. Quando aplicadas a um soquete de bloqueio, essas operações são conhecidas como operações de bloqueio. As seguintes funções podem bloquear:

-   [**Recv**](/windows/desktop/api/winsock/nf-winsock-recv)
-   [**Recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)
-   [**Enviar**](/windows/desktop/api/Winsock2/nf-winsock2-send)
-   [**Sendto**](/windows/desktop/api/winsock/nf-winsock-sendto)

Com os soquetes Windows 1.1 de 16 bits, uma operação de bloqueio que não pode ser concluída imediatamente é manipulada pelo pseudo-bloqueio da seguinte forma.

O provedor de serviços inicia a operação e, em seguida, entra em um loop no qual ele envia todas as mensagens Windows (inging the processor to another thread, se necessário) e, em seguida, verifica a conclusão da função Windows Sockets. Se a função tiver sido concluída ou se [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall) tiver sido invocado, a função de bloqueio será concluída com um resultado apropriado.

Um provedor de serviços deve permitir a instalação de uma função de gancho de bloqueio que não processa mensagens para evitar a possibilidade de novas mensagens de entrada enquanto uma operação de bloqueio está pendente. A função de gancho de bloqueio mais simples retornaria **FALSE.** Se uma DLL de soquetes do Windows depender de mensagens para a operação interna, ela poderá executar **PeekMessage**(**hMyWnd**...) antes de executar o gancho de bloqueio do aplicativo para que ele possa obter suas mensagens sem afetar o restante do sistema.

Em um ambiente do Windows Sockets 1.1 de 16 bits, se uma mensagem Windows for recebida para um processo para o qual uma operação de bloqueio está em andamento, há um risco de o aplicativo tentar emitir outra chamada Windows Sockets. Devido à dificuldade de gerenciar essa condição com segurança, o Windows Sockets 1.1 não dá suporte a esse comportamento de aplicativo. Um aplicativo não tem permissão para fazer mais de uma chamada de função Windows Sockets aninhada. Somente uma chamada de função pendente é permitida para uma tarefa específica. As únicas exceções são duas funções fornecidas para ajudar o programador nessa situação: [**WSAIsBlocking**](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) e [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).

A [**função WSAIsBlocking**](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) pode ser chamada a qualquer momento para determinar se uma chamada de bloqueio Windows Sockets 1.1 está em andamento. Da mesma forma, [**a função WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall) pode ser chamada a qualquer momento para cancelar uma chamada de bloqueio em andamento. Qualquer outro aninhamento de Windows funções Sockets falha com o erro WSAEINPROGRESS.

É necessário enfatizar que essa restrição se aplica a operações de bloqueio e não desbloqueio. Para Windows soquetes 2 que negociam a versão 2.0 ou superior no momento da chamada ao [**WSAStartup,**](/windows/desktop/api/winsock/nf-winsock-wsastartup)nenhuma restrição no aninhamento de operações é finalizada. As operações podem ser aninhadas em circunstâncias raras, como durante um retorno de chamada de aceitação condicional [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) ou se um provedor de serviços, por sua vez, invocar uma função Windows Sockets 2.

Embora esse mecanismo seja suficiente para aplicativos simples, ele não pode dar suporte aos requisitos complexos de expedição de mensagens de aplicativos mais avançados (por exemplo, aqueles que usam o modelo MDI). Para esses aplicativos, a API Windows Sockets inclui a função [**WSASetBlockingHook**](/windows/desktop/api/winsock2/nf-winsock2-wsasetblockinghook), que permite que o aplicativo especifique uma rotina especial que pode ser chamada em vez da rotina de expedição de mensagens padrão descrita na discussão anterior.

O provedor Windows Sockets chamará o gancho de bloqueio somente se todas as seguintes ações são verdadeiras:

-   A rotina é definida como sendo capaz de bloquear.
-   O soquete especificado é um soquete de bloqueio.
-   A solicitação não pode ser concluída imediatamente.

Um soquete é definido como bloqueio por padrão, mas a função [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) com o IOCTL **FIONBIO** ou a [**função WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) pode definir um soquete para o modo de não desbloqueio.

O gancho de bloqueio nunca é chamado e o aplicativo não precisa se preocupar com os problemas de nova entrada que o gancho de bloqueio pode introduzir, se um aplicativo seguir estas diretrizes:

-   Ele usa apenas soquetes que não são bloqueados.
-   Ele usa as rotinas [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) e/ou **WSAAsyncGetXByY** em vez de selecionar e **as rotinas getXbyY.** [](/windows/desktop/api/Winsock2/nf-winsock2-select)

Se um aplicativo Windows Sockets 1.1 invocar uma operação assíncrona ou não desbloqueada que leva um ponteiro para um objeto de memória (um buffer ou uma variável global, por exemplo) como um argumento Windows, é responsabilidade do aplicativo garantir que o objeto está disponível para soquetes em toda a operação. O aplicativo não deve invocar nenhuma Windows que possa afetar o mapeamento ou a viabilidade de endereço da memória envolvida.

 

 



