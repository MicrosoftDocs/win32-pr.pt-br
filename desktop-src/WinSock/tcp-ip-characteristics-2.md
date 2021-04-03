---
description: O TCP/IP tem características que permitem que o protocolo opere conforme seus requisitos de implementação padronizados são determinados.
ms.assetid: 6e9b3878-85f0-4572-9c00-a2e7647286ff
title: Características de TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561ab497d6f37c1c84b0203088b29e216ff0a69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828810"
---
# <a name="tcpip-characteristics"></a><span data-ttu-id="c85a2-103">Características de TCP/IP</span><span class="sxs-lookup"><span data-stu-id="c85a2-103">TCP/IP Characteristics</span></span>

<span data-ttu-id="c85a2-104">O TCP/IP tem características que permitem que o protocolo opere conforme seus requisitos de implementação padronizados são determinados.</span><span class="sxs-lookup"><span data-stu-id="c85a2-104">TCP/IP has characteristics that enable the protocol to operate as its standardized implementation requirements dictate.</span></span> <span data-ttu-id="c85a2-105">Essas características podem ser combinadas com opções de desenvolvimento que resultam em baixo desempenho.</span><span class="sxs-lookup"><span data-stu-id="c85a2-105">These characteristics can combine with development choices that result in poor performance.</span></span> <span data-ttu-id="c85a2-106">O impacto que essas características de TCP/IP têm em um aplicativo depende se o aplicativo é transacional ou de streaming.</span><span class="sxs-lookup"><span data-stu-id="c85a2-106">The impact these TCP/IP characteristics have on an application depend on whether the application is transactional or streaming.</span></span>

<span data-ttu-id="c85a2-107">Os aplicativos transacionais são afetados pela sobrecarga necessária para o estabelecimento e o encerramento da conexão.</span><span class="sxs-lookup"><span data-stu-id="c85a2-107">Transactional applications are affected by the overhead required for connection establishment and termination.</span></span> <span data-ttu-id="c85a2-108">Por exemplo, cada vez que uma conexão é estabelecida em uma rede Ethernet, três pacotes de aproximadamente 60 bytes devem ser enviados e aproximadamente um RTT é necessário para a troca.</span><span class="sxs-lookup"><span data-stu-id="c85a2-108">For example, each time a connection is established on an Ethernet network, three packets of approximately 60 bytes each must be sent, and approximately one RTT is required for the exchange.</span></span> <span data-ttu-id="c85a2-109">Quando ocorre a rescisão de uma conexão, quatro pacotes são trocados.</span><span class="sxs-lookup"><span data-stu-id="c85a2-109">When termination of a connection occurs, four packets are exchanged.</span></span> <span data-ttu-id="c85a2-110">Isso é para cada conexão; um aplicativo que abre e fecha as conexões geralmente incorre nessa sobrecarga em cada ocorrência.</span><span class="sxs-lookup"><span data-stu-id="c85a2-110">This is for each connection; an application that opens and closes connections often incurs this overhead on each occurrence.</span></span>

<span data-ttu-id="c85a2-111">Outro aspecto do TCP/IP é o *início lento*, que ocorre sempre que uma conexão é estabelecida.</span><span class="sxs-lookup"><span data-stu-id="c85a2-111">Another aspect of TCP/IP is *slow-start*, which takes place whenever a connection is established.</span></span> <span data-ttu-id="c85a2-112">O início lento é um limite artificial no número de segmentos de dados que podem ser enviados antes de a confirmação desses segmentos ser recebida.</span><span class="sxs-lookup"><span data-stu-id="c85a2-112">Slow-start is an artificial limit on the number of data segments that can be sent before acknowledgment of those segments is received.</span></span> <span data-ttu-id="c85a2-113">O início lento é projetado para limitar o congestionamento da rede.</span><span class="sxs-lookup"><span data-stu-id="c85a2-113">Slow-start is designed to limit network congestion.</span></span> <span data-ttu-id="c85a2-114">Quando uma conexão pela Ethernet é estabelecida, independentemente do tamanho da janela do destinatário, uma transmissão de 4 KB pode levar até 3-4 RTT devido ao início lento.</span><span class="sxs-lookup"><span data-stu-id="c85a2-114">When a connection over Ethernet is established, regardless of the receiver's window size, a 4 KB transmission can take up to 3-4 RTT due to slow-start.</span></span>

<span data-ttu-id="c85a2-115">Uma otimização de TCP/IP chamada de algoritmo Nagle também pode limitar a velocidade de transferência de dados em uma conexão.</span><span class="sxs-lookup"><span data-stu-id="c85a2-115">A TCP/IP optimization called the Nagle Algorithm can also limit data transfer speed on a connection.</span></span> <span data-ttu-id="c85a2-116">O algoritmo Nagle foi projetado para reduzir a sobrecarga de protocolo para aplicativos que enviam pequenas quantidades de dados, como Telnet, que envia um único caractere por vez.</span><span class="sxs-lookup"><span data-stu-id="c85a2-116">The Nagle Algorithm is designed to reduce protocol overhead for applications that send small amounts of data, such as Telnet, which sends a single character at a time.</span></span> <span data-ttu-id="c85a2-117">Em vez de enviar imediatamente um pacote com muitos cabeçalhos e pequenos dados, a pilha aguarda mais dados do aplicativo ou uma confirmação antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="c85a2-117">Rather than immediately send a packet with lots of header and little data, the stack waits for more data from the application, or an acknowledgment, before proceeding.</span></span>

<span data-ttu-id="c85a2-118">As confirmações atrasadas, conhecidas como *ACK atrasada*, também são projetadas no TCP/IP para permitir o acúmulo mais eficiente de confirmações quando os dados de retorno estão em breve do aplicativo do lado de recebimento.</span><span class="sxs-lookup"><span data-stu-id="c85a2-118">Delayed acknowledgments, commonly referred to as *delayed ACK*, are also designed into TCP/IP to enable more efficient piggybacking of acknowledgments when return data is forthcoming from the receiving side application.</span></span> <span data-ttu-id="c85a2-119">Infelizmente, se esses dados não estiverem em breve e o lado de envio estiver aguardando uma confirmação, poderão ocorrer atrasos de aproximadamente 200 milissegundos por envio.</span><span class="sxs-lookup"><span data-stu-id="c85a2-119">Unfortunately, if this data is not forthcoming and the sending side is waiting for an acknowledgment, delays of approximately 200 milliseconds per send can occur.</span></span>

<span data-ttu-id="c85a2-120">Quando uma conexão TCP é fechada, os recursos de conexão no nó que iniciou o fechamento são colocados em um estado de espera, chamado espera de tempo, para proteger contra corrupção de dados se os pacotes duplicados permanecerem na rede.</span><span class="sxs-lookup"><span data-stu-id="c85a2-120">When a TCP connection is closed, connection resources at the node that initiated the close are put into a wait state, called TIME-WAIT, to guard against data corruption if duplicate packets linger in the network.</span></span> <span data-ttu-id="c85a2-121">Isso garante que ambas as extremidades sejam concluídas com a conexão.</span><span class="sxs-lookup"><span data-stu-id="c85a2-121">This ensures both ends are finished with the connection.</span></span> <span data-ttu-id="c85a2-122">Isso pode causar esgotamento de recursos necessários por conexão, como RAM e portas, quando os aplicativos abrem e fecham conexões com frequência.</span><span class="sxs-lookup"><span data-stu-id="c85a2-122">This can cause depletion of resources required per-connection, such as RAM and ports, when applications open and close connections frequently.</span></span>

<span data-ttu-id="c85a2-123">Além de ser afetado pela confirmação atrasada e por outros esquemas de prevenção de congestionamento, os aplicativos de streaming também podem ser afetados por um tamanho de janela de recepção padrão muito pequeno na extremidade de recebimento.</span><span class="sxs-lookup"><span data-stu-id="c85a2-123">Besides being affected by delayed ACK and other congestion avoidance schemes, streaming applications can also be affected by a too-small default receive window size on the receiving end.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c85a2-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c85a2-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c85a2-125">Comportamento do aplicativo</span><span class="sxs-lookup"><span data-stu-id="c85a2-125">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="c85a2-126">Aplicativos de alto desempenho do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="c85a2-126">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="c85a2-127">Algoritmo Nagle</span><span class="sxs-lookup"><span data-stu-id="c85a2-127">Nagle Algorithm</span></span>](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



