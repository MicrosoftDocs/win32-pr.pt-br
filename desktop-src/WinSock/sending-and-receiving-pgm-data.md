---
description: O envio e o recebimento de dados do PGM são semelhantes ao envio ou recebimento de dados em qualquer soquete. Há considerações específicas para o PGM, descritas nos parágrafos a seguir.
ms.assetid: 51b447ad-b6da-424b-91df-e5be9ce225a5
title: Enviando e recebendo dados do PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab73999c33c97c6ba528552af6d746d54fb605df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091380"
---
# <a name="sending-and-receiving-pgm-data"></a>Enviando e recebendo dados do PGM

O envio e o recebimento de dados do PGM são semelhantes ao envio ou recebimento de dados em qualquer soquete. Há considerações específicas para o PGM, descritas nos parágrafos a seguir.

## <a name="sending-pgm-data"></a>Enviando dados do PGM

Depois que uma sessão de emissor de PGM é criada, os dados são enviados usando as várias funções de envio do Windows Sockets: [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send), [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)e [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto). Como os identificadores do Windows Sockets são identificadores do sistema de arquivos, outras funções como o [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile) e as funções CRT também podem transmitir dados. O trecho de código a seguir ilustra uma operação de emissor de PGM:


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



Ao usar o modo de mensagem (SOCK \_ RDM), cada chamada para uma função de envio resulta em uma mensagem discreta, que às vezes não é desejável; um aplicativo pode querer enviar uma mensagem de 2 megabytes com várias chamadas para [**Enviar**](/windows/desktop/api/Winsock2/nf-winsock2-send). Em tais circunstâncias, o remetente pode definir a opção de soquete de [ \_ limite de \_ mensagem \_ do conjunto RM](socket-options.md) para indicar o tamanho da mensagem que segue.

Se a janela de envio estiver cheia, um novo envio do aplicativo não será aceito até que a janela seja avançada. A tentativa de envio em um soquete sem bloqueio falha com WSAEWOULDBLOCK; um soquete de bloqueio simplesmente bloqueia até que a janela avance até o ponto em que os dados solicitados podem ser armazenados em buffer e enviados. Em e/s sobreposta, a operação não é concluída até que a janela avance o suficiente para acomodar os novos dados.

## <a name="receiving-pgm-data"></a>Recebendo dados do PGM

Depois que uma sessão de receptor de PGM é criada, os dados são recebidos usando as várias funções de recebimento do Windows Sockets: [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)e [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom). Como os identificadores do Windows Sockets também são identificadores de arquivo, as funções [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) e CRT também podem ser usadas para receber dados da sessão PGM. O transporte encaminha dados até o receptor, pois ele chega enquanto os dados estão em sequência. O transporte garante que os dados retornados sejam contíguos e livres de duplicatas. O trecho de código a seguir ilustra uma operação de recebimento de PGM:


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



Ao usar o modo de mensagem (SOCK \_ RDM), o transporte indica quando uma mensagem parcial é recebida, seja com o Erro WSAEMSGSIZE ou definindo o \_ sinalizador parcial msg ao retornar das funções [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) e [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) . Quando o último fragmento da mensagem completa for retornado ao cliente, o erro ou o sinalizador não será indicado.

Quando a sessão é encerrada normalmente, a operação de recebimento falha com WSAEDISCON. Quando ocorre a perda de dados no transporte, o PGM armazena temporariamente os pacotes fora de sequência e tenta recuperar os dados perdidos. Se a perda de dados for irrecuperável, a operação de recebimento falhará com WSAECONNRESET e a sessão será encerrada. A sessão pode ser redefinida devido a uma variedade de condições, incluindo as seguintes:

-   O receptor ou a taxa de conexão de entrada está muito lenta para acompanhar a taxa de dados de entrada.
-   Ocorre uma perda excessiva de dados, possivelmente devido a condições transitórias de rede, como problemas de roteamento, instabilidade de rede e assim por diante.
-   Um erro irrecuperável ocorre no remetente.
-   A utilização excessiva de recursos ocorre no computador local, como exceder o máximo de armazenamento de buffer interno permitido ou encontrar uma condição de indisponibilidade de recursos.
-   Ocorre um erro de verificação de consistência de dados.
-   A falha em um componente PGM depende de, por exemplo, TCP/IP ou Windows Sockets.

O primeiro e o segundo itens na lista acima podem fazer com que o receptor execute buffer excessivo antes de ficar sem recursos ou antes de passar para fora além da janela do remetente.

## <a name="terminating-a-pgm-session"></a>Finalizando uma sessão PGM

O remetente ou destinatário do PGM pode parar de enviar ou receber dados chamando [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket). O receptor deve chamar **fechamento** nos soquetes de escuta e de recebimento para evitar vazamentos de identificador. Chamar o [**desligamento**](/windows/desktop/api/winsock/nf-winsock-shutdown) no remetente antes de chamar **fechamento** garante que todos os dados sejam enviados e garante que os dados de reparo sejam mantidos até que a janela de envio seja adiantada após a última sequência de dados, mesmo que o próprio aplicativo seja encerrado.

 

 
