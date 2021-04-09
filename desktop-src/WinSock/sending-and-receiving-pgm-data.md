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
# <a name="sending-and-receiving-pgm-data"></a><span data-ttu-id="282eb-104">Enviando e recebendo dados do PGM</span><span class="sxs-lookup"><span data-stu-id="282eb-104">Sending and Receiving PGM Data</span></span>

<span data-ttu-id="282eb-105">O envio e o recebimento de dados do PGM são semelhantes ao envio ou recebimento de dados em qualquer soquete.</span><span class="sxs-lookup"><span data-stu-id="282eb-105">Sending and receiving PGM data is similar to sending or receiving data on any socket.</span></span> <span data-ttu-id="282eb-106">Há considerações específicas para o PGM, descritas nos parágrafos a seguir.</span><span class="sxs-lookup"><span data-stu-id="282eb-106">There are considerations specific to PGM, outlined in the following paragraphs.</span></span>

## <a name="sending-pgm-data"></a><span data-ttu-id="282eb-107">Enviando dados do PGM</span><span class="sxs-lookup"><span data-stu-id="282eb-107">Sending PGM Data</span></span>

<span data-ttu-id="282eb-108">Depois que uma sessão de emissor de PGM é criada, os dados são enviados usando as várias funções de envio do Windows Sockets: [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send), [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)e [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto).</span><span class="sxs-lookup"><span data-stu-id="282eb-108">Once a PGM sender session is created, data is sent using the various Windows Sockets send functions: [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send), [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), and [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto).</span></span> <span data-ttu-id="282eb-109">Como os identificadores do Windows Sockets são identificadores do sistema de arquivos, outras funções como o [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile) e as funções CRT também podem transmitir dados.</span><span class="sxs-lookup"><span data-stu-id="282eb-109">Since Windows Sockets handles are file system handles, other functions such as [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile) and CRT functions can also transmit data.</span></span> <span data-ttu-id="282eb-110">O trecho de código a seguir ilustra uma operação de emissor de PGM:</span><span class="sxs-lookup"><span data-stu-id="282eb-110">The following code snippet illustrates a PGM sender operation:</span></span>


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



<span data-ttu-id="282eb-111">Ao usar o modo de mensagem (SOCK \_ RDM), cada chamada para uma função de envio resulta em uma mensagem discreta, que às vezes não é desejável; um aplicativo pode querer enviar uma mensagem de 2 megabytes com várias chamadas para [**Enviar**](/windows/desktop/api/Winsock2/nf-winsock2-send).</span><span class="sxs-lookup"><span data-stu-id="282eb-111">When using message mode (SOCK\_RDM), each call to a send function results in a discrete message, which sometimes isn't desirable; an application may want to send a 2 megabyte message with multiple calls to [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send).</span></span> <span data-ttu-id="282eb-112">Em tais circunstâncias, o remetente pode definir a opção de soquete de [ \_ limite de \_ mensagem \_ do conjunto RM](socket-options.md) para indicar o tamanho da mensagem que segue.</span><span class="sxs-lookup"><span data-stu-id="282eb-112">In such circumstances, the sender can set the [RM\_SET\_MESSAGE\_BOUNDARY](socket-options.md) socket option to indicate the size of the message that followings.</span></span>

<span data-ttu-id="282eb-113">Se a janela de envio estiver cheia, um novo envio do aplicativo não será aceito até que a janela seja avançada.</span><span class="sxs-lookup"><span data-stu-id="282eb-113">If the send window is full, a new send from the application is not accepted until window has been advanced.</span></span> <span data-ttu-id="282eb-114">A tentativa de envio em um soquete sem bloqueio falha com WSAEWOULDBLOCK; um soquete de bloqueio simplesmente bloqueia até que a janela avance até o ponto em que os dados solicitados podem ser armazenados em buffer e enviados.</span><span class="sxs-lookup"><span data-stu-id="282eb-114">Attempting to send on a non-blocking socket fails with WSAEWOULDBLOCK; a blocking socket simply blocks until the window advances to the point where the requested data can be buffered and sent.</span></span> <span data-ttu-id="282eb-115">Em e/s sobreposta, a operação não é concluída até que a janela avance o suficiente para acomodar os novos dados.</span><span class="sxs-lookup"><span data-stu-id="282eb-115">In overlapped I/O, the operation does not complete until the window advances enough to accommodate the new data.</span></span>

## <a name="receiving-pgm-data"></a><span data-ttu-id="282eb-116">Recebendo dados do PGM</span><span class="sxs-lookup"><span data-stu-id="282eb-116">Receiving PGM Data</span></span>

<span data-ttu-id="282eb-117">Depois que uma sessão de receptor de PGM é criada, os dados são recebidos usando as várias funções de recebimento do Windows Sockets: [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)e [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom).</span><span class="sxs-lookup"><span data-stu-id="282eb-117">Once a PGM receiver session is created, data is received using the various Windows Sockets receive functions: [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), and [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom).</span></span> <span data-ttu-id="282eb-118">Como os identificadores do Windows Sockets também são identificadores de arquivo, as funções [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) e CRT também podem ser usadas para receber dados da sessão PGM.</span><span class="sxs-lookup"><span data-stu-id="282eb-118">Since Windows Sockets handles are also file handles, the [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) and CRT functions can also be used to receive PGM session data.</span></span> <span data-ttu-id="282eb-119">O transporte encaminha dados até o receptor, pois ele chega enquanto os dados estão em sequência.</span><span class="sxs-lookup"><span data-stu-id="282eb-119">The transport forwards data up to the receiver as it arrives as long as the data is in sequence.</span></span> <span data-ttu-id="282eb-120">O transporte garante que os dados retornados sejam contíguos e livres de duplicatas.</span><span class="sxs-lookup"><span data-stu-id="282eb-120">The transport guarantees that the data returned is contiguous and free of duplicates.</span></span> <span data-ttu-id="282eb-121">O trecho de código a seguir ilustra uma operação de recebimento de PGM:</span><span class="sxs-lookup"><span data-stu-id="282eb-121">The following code snippet illustrates a PGM receive operation:</span></span>


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



<span data-ttu-id="282eb-122">Ao usar o modo de mensagem (SOCK \_ RDM), o transporte indica quando uma mensagem parcial é recebida, seja com o Erro WSAEMSGSIZE ou definindo o \_ sinalizador parcial msg ao retornar das funções [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) e [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) .</span><span class="sxs-lookup"><span data-stu-id="282eb-122">When using message mode (SOCK\_RDM), the transport indicates when a partial message is received, either with the WSAEMSGSIZE error, or by setting the MSG\_PARTIAL flag upon return from the [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) and [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) functions.</span></span> <span data-ttu-id="282eb-123">Quando o último fragmento da mensagem completa for retornado ao cliente, o erro ou o sinalizador não será indicado.</span><span class="sxs-lookup"><span data-stu-id="282eb-123">When the last fragment of the full message is returned to the client, the error or flag is not indicated.</span></span>

<span data-ttu-id="282eb-124">Quando a sessão é encerrada normalmente, a operação de recebimento falha com WSAEDISCON.</span><span class="sxs-lookup"><span data-stu-id="282eb-124">When the session is terminated gracefully, the receive operation fails with WSAEDISCON.</span></span> <span data-ttu-id="282eb-125">Quando ocorre a perda de dados no transporte, o PGM armazena temporariamente os pacotes fora de sequência e tenta recuperar os dados perdidos.</span><span class="sxs-lookup"><span data-stu-id="282eb-125">When data loss occurs in the transport, PGM temporarily buffers the out-of-sequence packets and attempts to recover the lost data.</span></span> <span data-ttu-id="282eb-126">Se a perda de dados for irrecuperável, a operação de recebimento falhará com WSAECONNRESET e a sessão será encerrada.</span><span class="sxs-lookup"><span data-stu-id="282eb-126">If the data-loss is unrecoverable, the receive operation fail with WSAECONNRESET, and the session is terminated.</span></span> <span data-ttu-id="282eb-127">A sessão pode ser redefinida devido a uma variedade de condições, incluindo as seguintes:</span><span class="sxs-lookup"><span data-stu-id="282eb-127">The session can be reset due to a variety of conditions, including the following:</span></span>

-   <span data-ttu-id="282eb-128">O receptor ou a taxa de conexão de entrada está muito lenta para acompanhar a taxa de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="282eb-128">The receiver or the incoming connection rate is too slow to keep pace with the incoming data rate.</span></span>
-   <span data-ttu-id="282eb-129">Ocorre uma perda excessiva de dados, possivelmente devido a condições transitórias de rede, como problemas de roteamento, instabilidade de rede e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="282eb-129">Excessive data loss occurs, possibly due to transient network conditions, such as routing problems, network instability, and so forth.</span></span>
-   <span data-ttu-id="282eb-130">Um erro irrecuperável ocorre no remetente.</span><span class="sxs-lookup"><span data-stu-id="282eb-130">An unrecoverable error occurs on the sender.</span></span>
-   <span data-ttu-id="282eb-131">A utilização excessiva de recursos ocorre no computador local, como exceder o máximo de armazenamento de buffer interno permitido ou encontrar uma condição de indisponibilidade de recursos.</span><span class="sxs-lookup"><span data-stu-id="282eb-131">Excessive resource utilization occurs on the local computer, such as exceeding the maximum allowed internal buffer storage, or encountering an out-of-resources condition.</span></span>
-   <span data-ttu-id="282eb-132">Ocorre um erro de verificação de consistência de dados.</span><span class="sxs-lookup"><span data-stu-id="282eb-132">A data consistency check error occurs.</span></span>
-   <span data-ttu-id="282eb-133">A falha em um componente PGM depende de, por exemplo, TCP/IP ou Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="282eb-133">Failure in a component PGM depends on, such as TCP/IP or Windows Sockets.</span></span>

<span data-ttu-id="282eb-134">O primeiro e o segundo itens na lista acima podem fazer com que o receptor execute buffer excessivo antes de ficar sem recursos ou antes de passar para fora além da janela do remetente.</span><span class="sxs-lookup"><span data-stu-id="282eb-134">Both the first and second items in the above list could result in the receiver performing excessive buffering before running out of resources, or before ultimately moving beyond the sender's window.</span></span>

## <a name="terminating-a-pgm-session"></a><span data-ttu-id="282eb-135">Finalizando uma sessão PGM</span><span class="sxs-lookup"><span data-stu-id="282eb-135">Terminating A PGM Session</span></span>

<span data-ttu-id="282eb-136">O remetente ou destinatário do PGM pode parar de enviar ou receber dados chamando [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket).</span><span class="sxs-lookup"><span data-stu-id="282eb-136">The PGM sender or receiver can stop sending or receiving data by calling [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).</span></span> <span data-ttu-id="282eb-137">O receptor deve chamar **fechamento** nos soquetes de escuta e de recebimento para evitar vazamentos de identificador.</span><span class="sxs-lookup"><span data-stu-id="282eb-137">The receiver must call **closesocket** on both the listening and receiving sockets to prevent handle leaks.</span></span> <span data-ttu-id="282eb-138">Chamar o [**desligamento**](/windows/desktop/api/winsock/nf-winsock-shutdown) no remetente antes de chamar **fechamento** garante que todos os dados sejam enviados e garante que os dados de reparo sejam mantidos até que a janela de envio seja adiantada após a última sequência de dados, mesmo que o próprio aplicativo seja encerrado.</span><span class="sxs-lookup"><span data-stu-id="282eb-138">Calling [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) on the sender before calling **closesocket** ensures all data gets sent, and ensures repair data is maintained until the send window advances past the last data sequence, even if the application itself terminates.</span></span>

 

 
