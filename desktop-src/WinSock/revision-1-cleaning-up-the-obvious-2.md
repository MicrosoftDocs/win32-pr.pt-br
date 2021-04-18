---
description: Nesta versão do programa de exemplo, foram feitas algumas alterações óbvias que adotarão o desempenho inicial para melhorar a performance.
ms.assetid: ef9d594c-31fe-44c0-b707-47c01e2c5bf0
title: 'Revisão um: limpando o óbvio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 631bea7395000531cce542b41ace3b3aab9afff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764225"
---
# <a name="revision-one-cleaning-up-the-obvious"></a><span data-ttu-id="3937b-103">Revisão um: limpando o óbvio</span><span class="sxs-lookup"><span data-stu-id="3937b-103">Revision One: Cleaning up the Obvious</span></span>

<span data-ttu-id="3937b-104">Nesta versão do programa de exemplo, foram feitas algumas alterações óbvias que adotarão o desempenho inicial para melhorar a performance.</span><span class="sxs-lookup"><span data-stu-id="3937b-104">In this version of the example program, a few obvious changes have been made that will take initial strides at improving performance.</span></span> <span data-ttu-id="3937b-105">Esta versão do código está longe de ser ajustada pelo desempenho, mas é uma boa etapa incremental que permite examinar os efeitos de abordagens incrementalmente melhores.</span><span class="sxs-lookup"><span data-stu-id="3937b-105">This version of the code is far from performance-tuned, but it is a good incremental step that enables examination of the effects of incrementally better approaches.</span></span>

> [!WARNING]
> <span data-ttu-id="3937b-106">Este exemplo do aplicativo fornece desempenho intencionalmente insatisfatório, a fim de ilustrar as melhorias de desempenho possíveis com alterações no código.</span><span class="sxs-lookup"><span data-stu-id="3937b-106">This example of the application provides intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="3937b-107">Não use este exemplo de código em seu aplicativo; Ele é apenas para fins ilustrativos.</span><span class="sxs-lookup"><span data-stu-id="3937b-107">Do not use this code sample in your application; it is for illustration purposes only.</span></span>

 


```C++
#include <windows.h>

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    BYTE tmp[3];
    tmp[0] = (BYTE)row;
    tmp[1] = (BYTE)col;
    tmp[2] = (BYTE)bAlive;
    bind( s, ... );
    connect( s, ... );
    send( s, &tmp, 3 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



## <a name="changes-in-this-version"></a><span data-ttu-id="3937b-108">Alterações nesta versão</span><span class="sxs-lookup"><span data-stu-id="3937b-108">Changes in this Version</span></span>

<span data-ttu-id="3937b-109">Esta versão reflete as seguintes alterações:</span><span class="sxs-lookup"><span data-stu-id="3937b-109">This version reflects the following changes:</span></span>

-   <span data-ttu-id="3937b-110">SNDBUF removido = 0.</span><span class="sxs-lookup"><span data-stu-id="3937b-110">Removed SNDBUF=0.</span></span> <span data-ttu-id="3937b-111">Os atrasos de 200 milissegundos devido a envios não armazenados em buffer e a confirmações atrasadas são removidos.</span><span class="sxs-lookup"><span data-stu-id="3937b-111">The 200 millisecond delays due to unbuffered sends and delayed acknowledgments are removed.</span></span>
-   <span data-ttu-id="3937b-112">Removido o comportamento enviar-enviar-receber.</span><span class="sxs-lookup"><span data-stu-id="3937b-112">Removed the Send-Send-Receive behavior.</span></span> <span data-ttu-id="3937b-113">Essa alteração elimina atrasos de 200 milissegundos devido a Nagle e interações de ACK atrasadas.</span><span class="sxs-lookup"><span data-stu-id="3937b-113">This change eliminates 200-millisecond delays due to Nagle and delayed ACK interactions.</span></span>
-   <span data-ttu-id="3937b-114">Suposição little-endian removida.</span><span class="sxs-lookup"><span data-stu-id="3937b-114">Removed little-endian assumption.</span></span> <span data-ttu-id="3937b-115">Os bytes agora estão em ordem.</span><span class="sxs-lookup"><span data-stu-id="3937b-115">The bytes are now in order.</span></span>

## <a name="remaining-problems"></a><span data-ttu-id="3937b-116">Problemas restantes</span><span class="sxs-lookup"><span data-stu-id="3937b-116">Remaining Problems</span></span>

<span data-ttu-id="3937b-117">Nesta versão, os seguintes problemas permanecem:</span><span class="sxs-lookup"><span data-stu-id="3937b-117">In this version, the following problems remain:</span></span>

-   <span data-ttu-id="3937b-118">O aplicativo ainda é muito conectado.</span><span class="sxs-lookup"><span data-stu-id="3937b-118">The application is still connect heavy.</span></span> <span data-ttu-id="3937b-119">Como os mais de 600 milissegundos são removidos, o aplicativo agora atinge a taxa sustentada de 12 conexões por segundo.</span><span class="sxs-lookup"><span data-stu-id="3937b-119">Since the 600+ millisecond delays are removed, the application now hits the 12 connects-per-second sustained rate.</span></span> <span data-ttu-id="3937b-120">Muitas conexões simultâneas agora se tornam um problema.</span><span class="sxs-lookup"><span data-stu-id="3937b-120">Many concurrent connections now becomes an issue.</span></span>
-   <span data-ttu-id="3937b-121">O aplicativo ainda é FAT; as células inalteradas ainda são propagadas para o servidor.</span><span class="sxs-lookup"><span data-stu-id="3937b-121">The application is still fat; unchanged cells are still propagated to the server.</span></span>
-   <span data-ttu-id="3937b-122">O aplicativo ainda exibe streaming ruim; envios de 3 bytes ainda são pequenos envios.</span><span class="sxs-lookup"><span data-stu-id="3937b-122">The application still exhibits poor streaming; 3-byte sends are still small sends.</span></span>
-   <span data-ttu-id="3937b-123">O aplicativo agora envia 2 bytes/RTT, que é igual a 4 KB/s em Ethernet conectada diretamente.</span><span class="sxs-lookup"><span data-stu-id="3937b-123">The application now sends 2 bytes/RTT, which equals 4 KB/s on directly connected Ethernet.</span></span> <span data-ttu-id="3937b-124">Isso não é rápido, mas o tempo de espera provavelmente causará problemas primeiro.</span><span class="sxs-lookup"><span data-stu-id="3937b-124">This is not too fast, but TIME-WAIT will likely cause problems first.</span></span>
-   <span data-ttu-id="3937b-125">A sobrecarga está abaixo de 99,3%, que ainda não é uma boa porcentagem de sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="3937b-125">The overhead is down to 99.3%, which is still not a good overhead percentage.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="3937b-126">Principais métricas de desempenho</span><span class="sxs-lookup"><span data-stu-id="3937b-126">Key Performance Metrics</span></span>

<span data-ttu-id="3937b-127">As principais métricas de desempenho a seguir são expressas em RTT (tempo de ida e volta), Goodput e sobrecarga de protocolo.</span><span class="sxs-lookup"><span data-stu-id="3937b-127">The following key performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="3937b-128">Consulte o tópico [terminologia de rede](network-terminology-2.md) para obter uma explicação desses termos.</span><span class="sxs-lookup"><span data-stu-id="3937b-128">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

<span data-ttu-id="3937b-129">Esta versão reflete as seguintes métricas de desempenho:</span><span class="sxs-lookup"><span data-stu-id="3937b-129">This version reflect the following performance metrics:</span></span>

-   <span data-ttu-id="3937b-130">Tempo da célula — 2 × RTT</span><span class="sxs-lookup"><span data-stu-id="3937b-130">Cell Time—2×RTT</span></span>
-   <span data-ttu-id="3937b-131">Goodput – 2 bytes/RTT</span><span class="sxs-lookup"><span data-stu-id="3937b-131">Goodput—2 bytes/RTT</span></span>
-   <span data-ttu-id="3937b-132">Sobrecarga de protocolo — 99.3%</span><span class="sxs-lookup"><span data-stu-id="3937b-132">Protocol Overhead—99.3 percent</span></span>

## <a name="related-topics"></a><span data-ttu-id="3937b-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3937b-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3937b-134">Melhorando um aplicativo lento</span><span class="sxs-lookup"><span data-stu-id="3937b-134">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="3937b-135">Terminologia de rede</span><span class="sxs-lookup"><span data-stu-id="3937b-135">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="3937b-136">A versão de linha de base: um aplicativo com muito mau desempenho</span><span class="sxs-lookup"><span data-stu-id="3937b-136">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="3937b-137">Revisão 2: redesignação para menos conexões</span><span class="sxs-lookup"><span data-stu-id="3937b-137">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="3937b-138">Revisão 3: envio de bloco compactado</span><span class="sxs-lookup"><span data-stu-id="3937b-138">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> <dt>

[<span data-ttu-id="3937b-139">Aprimoramentos futuros</span><span class="sxs-lookup"><span data-stu-id="3937b-139">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 



