---
description: A versão de linha de base de um aplicativo com baixo desempenho no Windows Sockets (Winsock).
ms.assetid: 923884c4-f1bd-4f72-983e-6158f368e0dd
title: 'A versão de linha de base: um aplicativo com muito mau desempenho'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c094be5fd5cf6e3b9eaeb07c7ff38880e651dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781255"
---
# <a name="the-baseline-version-a-very-poor-performing-application"></a><span data-ttu-id="0bd46-103">A versão de linha de base: um aplicativo com muito mau desempenho</span><span class="sxs-lookup"><span data-stu-id="0bd46-103">The Baseline Version: A Very Poor Performing Application</span></span>

<span data-ttu-id="0bd46-104">O exemplo de código inicial e de baixa execução usado para calcular as atualizações é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="0bd46-104">The initial, poor performing code sample used to calculate the updates is as follows:</span></span>

> [!Note]  
> <span data-ttu-id="0bd46-105">Para simplificar, não há nenhum tratamento de erros nos exemplos a seguir.</span><span class="sxs-lookup"><span data-stu-id="0bd46-105">For simplicity, there is no error handling in the following examples.</span></span> <span data-ttu-id="0bd46-106">Qualquer aplicativo de produção sempre verifica valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="0bd46-106">Any production application always checks return values.</span></span>

 

> [!WARNING]
> <span data-ttu-id="0bd46-107">Os primeiros exemplos do aplicativo fornecem um desempenho intencionalmente insatisfatório, a fim de ilustrar as melhorias de desempenho possíveis com alterações no código.</span><span class="sxs-lookup"><span data-stu-id="0bd46-107">The first few examples of the application provide intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="0bd46-108">Não use esses exemplos de código em seu aplicativo; Eles são apenas para fins ilustrativos.</span><span class="sxs-lookup"><span data-stu-id="0bd46-108">Do not use these code samples in your application; they are for illustration purposes only.</span></span>

 


```C++
#include <windows.h>

BOOL Map[ROWS][COLS];

void LifeUpdate()
{
    ComputeNext( Map );
    for( int i = 0 ; i < ROWS ; ++i )     //serialized
        for( int j = 0 ; j < COLS ; ++j )
            Set( i, j, Map[i][j] );    //chatty
}

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    setsockopt( s, SO_SNDBUF, &Zero, sizeof(int) );
    bind( s, ... );
    connect( s, ... );
    send( s, &row, 1 );
    send( s, &col, 1 );
    send( s, &bAlive, 1 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



<span data-ttu-id="0bd46-109">Nesse estado, o aplicativo tem o pior desempenho de rede possível.</span><span class="sxs-lookup"><span data-stu-id="0bd46-109">In this state, the application has the worst possible network performance.</span></span> <span data-ttu-id="0bd46-110">Os problemas com esta versão do aplicativo de exemplo incluem:</span><span class="sxs-lookup"><span data-stu-id="0bd46-110">The problems with this version of the sample application include:</span></span>

-   <span data-ttu-id="0bd46-111">O aplicativo é informativo.</span><span class="sxs-lookup"><span data-stu-id="0bd46-111">The application is chatty.</span></span> <span data-ttu-id="0bd46-112">Cada transação é muito pequena — as células não precisam ser atualizadas uma a uma.</span><span class="sxs-lookup"><span data-stu-id="0bd46-112">Each transaction is too small — cells do not need to be updated one by one.</span></span>
-   <span data-ttu-id="0bd46-113">As transações são estritamente serializadas, embora as células possam ser atualizadas simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="0bd46-113">The transactions are strictly serialized, even though the cells could be updated concurrently.</span></span>
-   <span data-ttu-id="0bd46-114">O buffer de envio é definido como zero e o aplicativo incorre em um atraso de 200 milissegundos para cada envio — três vezes por célula.</span><span class="sxs-lookup"><span data-stu-id="0bd46-114">The send buffer is set to zero, and the application incurs a 200-millisecond delay for each send — three times per cell.</span></span>
-   <span data-ttu-id="0bd46-115">O aplicativo é muito conectado, conectando uma vez para cada célula.</span><span class="sxs-lookup"><span data-stu-id="0bd46-115">The application is very connect heavy, connecting once for each cell.</span></span> <span data-ttu-id="0bd46-116">Os aplicativos são limitados no número de conexões por segundo para um determinado destino devido ao estado de espera de tempo, mas isso não é um problema aqui, uma vez que cada transação leva mais de 600 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="0bd46-116">Applications are limited in the number of connections per second for a given destination because of TIME-WAIT state, but that is not an issue here, since each transaction takes over 600 milliseconds.</span></span>
-   <span data-ttu-id="0bd46-117">O aplicativo é FAT; muitas transações não têm efeito sobre o estado do servidor, pois muitas células não são alteradas de Update para Update.</span><span class="sxs-lookup"><span data-stu-id="0bd46-117">The application is fat; many transactions have no effect on the server state, because many cells do not change from update to update.</span></span>
-   <span data-ttu-id="0bd46-118">O aplicativo exibe streaming ruim; pequenos envios consomem muita CPU e RAM.</span><span class="sxs-lookup"><span data-stu-id="0bd46-118">The application exhibits poor streaming; small sends consume a lot of CPU and RAM.</span></span>
-   <span data-ttu-id="0bd46-119">O aplicativo assume uma representação little-endian para seus envios.</span><span class="sxs-lookup"><span data-stu-id="0bd46-119">The application assumes little-endian representation for its sends.</span></span> <span data-ttu-id="0bd46-120">Essa é uma suposição natural para a plataforma atual do Windows, mas pode ser perigosa para código de vida longa.</span><span class="sxs-lookup"><span data-stu-id="0bd46-120">This is a natural assumption for the current Windows platform, but can be dangerous for long-lived code.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="0bd46-121">Principais métricas de desempenho</span><span class="sxs-lookup"><span data-stu-id="0bd46-121">Key Performance Metrics</span></span>

<span data-ttu-id="0bd46-122">As métricas de desempenho a seguir são expressas em RTT (tempo de ida e volta), Goodput e sobrecarga de protocolo.</span><span class="sxs-lookup"><span data-stu-id="0bd46-122">The following performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="0bd46-123">Consulte o tópico [terminologia de rede](network-terminology-2.md) para obter uma explicação desses termos.</span><span class="sxs-lookup"><span data-stu-id="0bd46-123">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

-   <span data-ttu-id="0bd46-124">A hora da célula, o tempo de rede para uma atualização de célula única, requer 4 \* RTT + 600 milissegundos para interações de Nagle e de ACK atrasada.</span><span class="sxs-lookup"><span data-stu-id="0bd46-124">Cell time, network time for a single cell update, requires 4\*RTT + 600 milliseconds for Nagle and delayed ACK interactions.</span></span>
-   <span data-ttu-id="0bd46-125">Goodput é menor que 6 bytes.</span><span class="sxs-lookup"><span data-stu-id="0bd46-125">Goodput is less than 6 bytes.</span></span>
-   <span data-ttu-id="0bd46-126">A sobrecarga de protocolo é 99,6%.</span><span class="sxs-lookup"><span data-stu-id="0bd46-126">Protocol Overhead is 99.6%.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0bd46-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0bd46-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bd46-128">Melhorando um aplicativo lento</span><span class="sxs-lookup"><span data-stu-id="0bd46-128">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="0bd46-129">Terminologia de rede</span><span class="sxs-lookup"><span data-stu-id="0bd46-129">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="0bd46-130">Revisão 1: limpando o óbvio</span><span class="sxs-lookup"><span data-stu-id="0bd46-130">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="0bd46-131">Revisão 2: redesignação para menos conexões</span><span class="sxs-lookup"><span data-stu-id="0bd46-131">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="0bd46-132">Revisão 3: envio de bloco compactado</span><span class="sxs-lookup"><span data-stu-id="0bd46-132">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> <dt>

[<span data-ttu-id="0bd46-133">Aprimoramentos futuros</span><span class="sxs-lookup"><span data-stu-id="0bd46-133">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 



