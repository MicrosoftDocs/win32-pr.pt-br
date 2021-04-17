---
description: Calculando a sobrecarga com netstat
ms.assetid: d96a8fba-8d76-443f-be49-81a8ad7050fa
title: Calculando a sobrecarga com netstat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7843c3cd445bee66e25a9f191ae4b78093faea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784517"
---
# <a name="calculating-overhead-with-netstat"></a><span data-ttu-id="46a0e-103">Calculando a sobrecarga com netstat</span><span class="sxs-lookup"><span data-stu-id="46a0e-103">Calculating Overhead with Netstat</span></span>

<span data-ttu-id="46a0e-104">O cálculo da sobrecarga com o netstat deve ser executado em uma rede silenciosa para evitar que outros tráfegos de rede distorcem os dados, como difusão ou tráfego multicast.</span><span class="sxs-lookup"><span data-stu-id="46a0e-104">Calculating overhead with Netstat should be performed on a quiet network to avoid other network traffic from skewing the data, such as broadcast or multicast traffic.</span></span>

<span data-ttu-id="46a0e-105">**Para calcular a sobrecarga de rede de um aplicativo usando netstat**</span><span class="sxs-lookup"><span data-stu-id="46a0e-105">**To calculate an application's network overhead using Netstat**</span></span>

1.  <span data-ttu-id="46a0e-106">Recupere as estatísticas de interface atuais usando netstat.</span><span class="sxs-lookup"><span data-stu-id="46a0e-106">Retrieve the current interface statistics using Netstat.</span></span>
2.  <span data-ttu-id="46a0e-107">Execute o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="46a0e-107">Execute the application.</span></span>
3.  <span data-ttu-id="46a0e-108">Obtenha as estatísticas de interface novamente usando netstat.</span><span class="sxs-lookup"><span data-stu-id="46a0e-108">Get the interface statistics, again using Netstat.</span></span>
4.  <span data-ttu-id="46a0e-109">Calcule o número de bytes recebidos entre as duas medidas netstat.</span><span class="sxs-lookup"><span data-stu-id="46a0e-109">Calculate the number of bytes received between the two Netstat measurements.</span></span>

## <a name="example"></a><span data-ttu-id="46a0e-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="46a0e-110">Example</span></span>

<span data-ttu-id="46a0e-111">O exemplo a seguir demonstra essas etapas, usando TTCP para enviar 10 bytes de dados, um byte por vez.</span><span class="sxs-lookup"><span data-stu-id="46a0e-111">The following example demonstrates these steps, using TTCP to send 10 bytes of data, one byte at a time.</span></span>

<span data-ttu-id="46a0e-112">Primeiro, uma sobrecarga teórica para o aplicativo é calculada.</span><span class="sxs-lookup"><span data-stu-id="46a0e-112">First, a theoretical overhead for the application is calculated.</span></span> <span data-ttu-id="46a0e-113">Para esse teste, todos os pacotes são 60 bytes (o mínimo de Ethernet).</span><span class="sxs-lookup"><span data-stu-id="46a0e-113">For this test, all packets are 60 bytes (the Ethernet minimum).</span></span> <span data-ttu-id="46a0e-114">Essa transferência requer três pacotes para configurar a conexão, 10 pacotes de dados, 10 pacotes de confirmação (a confirmação de atraso é disparada quase todas as vezes) e quatro pacotes para fechar a conexão normalmente.</span><span class="sxs-lookup"><span data-stu-id="46a0e-114">This transfer requires three packets to set up the connection, 10 data packets, 10 acknowledgment packets (delayed ACK is triggered nearly every time), and four packets to close the connection gracefully.</span></span>

<span data-ttu-id="46a0e-115">Isso equivale a 27 pacotes de 60 bytes cada, ou 1620 bytes (3 + 4 + 10 + 10) \* 60 = 1620).</span><span class="sxs-lookup"><span data-stu-id="46a0e-115">This equates to 27 packets of 60 bytes each, or 1620 bytes (3+4+10+10)\*60=1620).</span></span> <span data-ttu-id="46a0e-116">Como apenas 10 bytes de dados são transferidos, a sobrecarga é de 1610 bytes, que tem mais de 99% de sobrecarga de protocolo.</span><span class="sxs-lookup"><span data-stu-id="46a0e-116">Since only 10 bytes of data are transferred, the overhead is 1610 bytes, which is over 99% protocol overhead.</span></span>

### <a name="commands"></a><span data-ttu-id="46a0e-117">Comandos</span><span class="sxs-lookup"><span data-stu-id="46a0e-117">Commands</span></span>

<span data-ttu-id="46a0e-118">**netstat-e**</span><span class="sxs-lookup"><span data-stu-id="46a0e-118">**netstat -e**</span></span>

``` syntax
Interface Statistics
                     Received     Sent
Bytes                392291400    444684566
Unicast packets      487627       570086
Non-unicast packets  1159163      11300
Discards             0            0
Errors               0            0
Unknown protocols    52812
```

<span data-ttu-id="46a0e-119">**Ttcp-t-H0-D-L1-N10-P9 172.31.71.99**</span><span class="sxs-lookup"><span data-stu-id="46a0e-119">**ttcp -t -h0 -D -l1 -n10 -p9 172.31.71.99**</span></span>

``` syntax
ttcp-t: 10 bytes in 2168 real milliseconds = 0 KB/sec
ttcp-t: 10 I/O calls, msec/call = 216, calls/sec = 4, bytes/call = 1
```

<span data-ttu-id="46a0e-120">**netstat-e**</span><span class="sxs-lookup"><span data-stu-id="46a0e-120">**netstat -e**</span></span>

``` syntax
Interface Statistics
                      Received     Sent
Bytes                 39229207     444685382
Unicast packets       487641       570100
Non-unicast packets   1159164      11301
Discards              0            0
Errors                0            0
Unknown protocols     52812
```

### <a name="calculations"></a><span data-ttu-id="46a0e-121">Cálculos</span><span class="sxs-lookup"><span data-stu-id="46a0e-121">Calculations</span></span>

<span data-ttu-id="46a0e-122">**Enviado:** 816 bytes</span><span class="sxs-lookup"><span data-stu-id="46a0e-122">**Sent:** 816 bytes</span></span>

<span data-ttu-id="46a0e-123">**Recebido:** 674 bytes</span><span class="sxs-lookup"><span data-stu-id="46a0e-123">**Received:** 674 bytes</span></span>

<span data-ttu-id="46a0e-124">**Total de bytes:** 1490</span><span class="sxs-lookup"><span data-stu-id="46a0e-124">**Total bytes:** 1490</span></span>

<span data-ttu-id="46a0e-125">**Bytes de usuário:** 10</span><span class="sxs-lookup"><span data-stu-id="46a0e-125">**User bytes:** 10</span></span>

<span data-ttu-id="46a0e-126">**Sobrecarga:** 1480/1490 = 99,3%</span><span class="sxs-lookup"><span data-stu-id="46a0e-126">**Overhead:** 1480/1490 = 99.3%</span></span>

<span data-ttu-id="46a0e-127">\* \* Goodput: \* \* = 5 bytes/segundo (ou 40 bits/s)</span><span class="sxs-lookup"><span data-stu-id="46a0e-127">\*\*Goodput:  \*\*= 5 bytes/second (or 40 bits/s)</span></span>

> [!Note]  
> <span data-ttu-id="46a0e-128">Os bytes reais transferidos não correspondem aos valores teóricos porque os bytes de preenchimento não estão sendo contabilizados nos valores netstat.</span><span class="sxs-lookup"><span data-stu-id="46a0e-128">Actual bytes transferred do not match the theoretical values due to padding bytes not being accounted for in the Netstat values.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="46a0e-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="46a0e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46a0e-130">Comportamento do aplicativo</span><span class="sxs-lookup"><span data-stu-id="46a0e-130">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="46a0e-131">Aplicativos de alto desempenho do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="46a0e-131">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



