---
description: Enviar e receber dados PGM é semelhante ao envio ou recebimento de dados em qualquer soquete. Há considerações específicas para PGM, descritas nos parágrafos a seguir.
ms.assetid: 51b447ad-b6da-424b-91df-e5be9ce225a5
title: Enviando e recebendo dados PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 130b38ea52e5d0679b988e55f8292b9752a4bf15d0514a8277a2e0b3b2327001
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740567"
---
# <a name="sending-and-receiving-pgm-data"></a>Enviando e recebendo dados PGM

Enviar e receber dados PGM é semelhante ao envio ou recebimento de dados em qualquer soquete. Há considerações específicas para PGM, descritas nos parágrafos a seguir.

## <a name="sending-pgm-data"></a>Enviando dados PGM

Depois que uma sessão de remetente PGM é criada, os dados são enviados usando as várias funções de envio de soquetes do Windows: [**enviar**](/windows/desktop/api/Winsock2/nf-winsock2-send), enviar , [**enviar**](/windows/desktop/api/winsock/nf-winsock-sendto), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)e [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto). Como Windows soquetes são alças do sistema de arquivos, outras funções, como [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile) e funções CRT, também podem transmitir dados. O snippet de código a seguir ilustra uma operação de remetente PGM:


```C++
LONG        error;
    //:
error = send (s, pSendBuffer, SendLength, 0);
if (error == SOCKET_ERROR)
{
    fprintf (stderr, "send() failed: Error = %d\n",
             WSAGetLastError());
}
```



Ao usar o modo de mensagem (SOCK RDM), cada chamada para uma função de envio resulta em uma mensagem discreta, o que às vezes não é desejável; um aplicativo pode querer enviar uma mensagem de \_ 2 megabyte com várias chamadas para enviar . [](/windows/desktop/api/Winsock2/nf-winsock2-send) Nessas circunstâncias, o remetente pode definir a opção de soquete [RM \_ SET MESSAGE \_ \_ BOUNDARY](socket-options.md) para indicar o tamanho da mensagem a seguir.

Se a janela de envio estiver cheia, um novo envio do aplicativo não será aceito até que a janela tenha sido avançada. A tentativa de enviar em um soquete sem bloqueio falha com WSAEBLOCKBLOCK; um soquete de bloqueio simplesmente bloqueia até que a janela avance para o ponto em que os dados solicitados podem ser armazenados em buffer e enviados. Na E/S sobrecarada, a operação não é concluída até que a janela avance o suficiente para acomodar os novos dados.

## <a name="receiving-pgm-data"></a>Recebendo dados PGM

Depois que uma sessão de receptor PGM é criada, os dados são recebidos usando as várias funções de recebimento de soquetes do Windows: [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)e [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom). Como Windows de soquetes também são alças de arquivo, as funções [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) e CRT também podem ser usadas para receber dados de sessão PGM. O transporte encaminha os dados para o receptor conforme eles chegam, desde que os dados estão em sequência. O transporte garante que os dados retornados são contíguos e livres de duplicatas. O snippet de código a seguir ilustra uma operação de recebimento de PGM:


```C++
LONG        BytesRead;
    //:
BytesRead = recv (sockR, pTestBuffer, MaxBufferSize, 0);
if (BytesRead == 0)
{
    fprintf(stdout, "Session was terminated\n");
}
else if (BytesRead == SOCKET_ERROR)
{
    fprintf(stderr, "recv() failed: Error = %d\n",
            WSAGetLastError());
}
```



Ao usar o modo de mensagem (SOCK RDM), o transporte indica quando uma mensagem parcial é recebida, com o erro WSAEMSGSIZE ou definindo o sinalizador PARTIAL do MSG ao retornar das funções \_ \_ [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) e [**WSARecvFrom.**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) Quando o último fragmento da mensagem completa é retornado ao cliente, o erro ou sinalizador não é indicado.

Quando a sessão é encerrada normalmente, a operação de recebimento falha com WSAEDISCON. Quando ocorre perda de dados no transporte, o PGM em buffer temporariamente os pacotes fora de sequência e tenta recuperar os dados perdidos. Se a perda de dados for irrecuperável, a operação de recebimento falhará com WSAECONNRESET e a sessão será encerrada. A sessão pode ser redefinida devido a uma variedade de condições, incluindo as seguintes:

-   O receptor ou a taxa de conexão de entrada é muito lento para acompanhar a taxa de dados de entrada.
-   Ocorre perda excessiva de dados, possivelmente devido a condições transitórias de rede, como problemas de roteamento, instabilidade de rede e assim por diante.
-   Ocorre um erro irrecuperável no remetente.
-   A utilização excessiva de recursos ocorre no computador local, como exceder o máximo de armazenamento de buffer interno permitido ou encontrar uma condição de falta de recursos.
-   Ocorre um erro de verificação de consistência de dados.
-   A falha em um PGM de componente depende de, como TCP/IP ou Windows Soquetes.

O primeiro e o segundo itens na lista acima podem fazer com que o receptor executa um buffer excessivo antes de ficar sem recursos ou antes de, por fim, passar para além da janela do remetente.

## <a name="terminating-a-pgm-session"></a>Encerrando uma sessão PGM

O remetente ou receptor PGM pode parar de enviar ou receber dados chamando [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket). O receptor deve chamar **closesocket nos** soquetes de escuta e recebimento para evitar vazamentos de alça. Chamar [](/windows/desktop/api/winsock/nf-winsock-shutdown) o desligamento no remetente antes de chamar **closesocket** garante que todos os dados são enviados e garante que os dados de reparo são mantidos até que a janela de envio avance após a última sequência de dados, mesmo que o próprio aplicativo seja encerrado.

 

 
