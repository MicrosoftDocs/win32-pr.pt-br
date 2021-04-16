---
description: Nesta versão do aplicativo, um envio de bloco compactado dos dados é usado. Essa alteração resulta em uma melhoria significativa no desempenho.
ms.assetid: 3f0a129b-5b67-4334-a0aa-cd80ee7018b9
title: 'Revisão três: envio de bloco compactado'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657579406ed31fce08239c518a6910f525219fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765176"
---
# <a name="revision-three-compressed-block-send"></a><span data-ttu-id="1a210-104">Revisão três: envio de bloco compactado</span><span class="sxs-lookup"><span data-stu-id="1a210-104">Revision Three: Compressed Block Send</span></span>

<span data-ttu-id="1a210-105">Nesta versão do aplicativo, um envio de bloco compactado dos dados é usado.</span><span class="sxs-lookup"><span data-stu-id="1a210-105">In this version of the application, a compressed block send of the data is used.</span></span> <span data-ttu-id="1a210-106">Essa alteração resulta em uma melhoria significativa no desempenho.</span><span class="sxs-lookup"><span data-stu-id="1a210-106">This change results in significant performance improvement.</span></span>


```C++
BYTE tmp[3*ROWS*COLS];
FIELD Old = Map;
ComputeNext( Map );
n=Compact(Map,Old,tmp);
bind( s, ... );
connect( s, ... );
send( s, tmp, 3*n );
//can't do recv(s,tmp,n)
for(int i=0; i < n; )
    recv( s, tmp+i, n-i );
closesocket( s );
```



## <a name="changes-in-this-version"></a><span data-ttu-id="1a210-107">Alterações nesta versão</span><span class="sxs-lookup"><span data-stu-id="1a210-107">Changes in this Version</span></span>

<span data-ttu-id="1a210-108">Esta versão reflete as seguintes alterações:</span><span class="sxs-lookup"><span data-stu-id="1a210-108">This version reflects the following changes:</span></span>

-   <span data-ttu-id="1a210-109">As atualizações de célula não são mais serializadas.</span><span class="sxs-lookup"><span data-stu-id="1a210-109">Cell updates are no longer serialized.</span></span>
-   <span data-ttu-id="1a210-110">Como um bloco Send é usado, o aplicativo não é mais informativo.</span><span class="sxs-lookup"><span data-stu-id="1a210-110">Since a block send is used, the application is no longer chatty.</span></span>
-   <span data-ttu-id="1a210-111">A compactação de dados é usada, resultando em um aplicativo menos Fat.</span><span class="sxs-lookup"><span data-stu-id="1a210-111">Data compression is used, resulting in a less fat application.</span></span>

<span data-ttu-id="1a210-112">Ainda há um problema com esta versão do aplicativo; o risco de deadlock existe porque um grande envio é usado sem recebimentos.</span><span class="sxs-lookup"><span data-stu-id="1a210-112">There is still an issue with this version of the application; the risk of deadlock exists since a large send is used with no receives.</span></span> <span data-ttu-id="1a210-113">O servidor envia um byte para cada 3 bytes recebidos.</span><span class="sxs-lookup"><span data-stu-id="1a210-113">The server sends one byte for every 3 bytes received.</span></span> <span data-ttu-id="1a210-114">Isso poderá causar um deadlock se o tamanho do buffer de recebimento for menor que 1000 bytes para este aplicativo de exemplo.</span><span class="sxs-lookup"><span data-stu-id="1a210-114">This could cause a deadlock if the receive buffer size is less than 1000 bytes for this sample application.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="1a210-115">Principais métricas de desempenho</span><span class="sxs-lookup"><span data-stu-id="1a210-115">Key Performance Metrics</span></span>

<span data-ttu-id="1a210-116">As métricas de desempenho a seguir são expressas em RTT (tempo de ida e volta), Goodput e sobrecarga de protocolo.</span><span class="sxs-lookup"><span data-stu-id="1a210-116">The following performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="1a210-117">Consulte o tópico [terminologia de rede](network-terminology-2.md) para obter uma explicação desses termos.</span><span class="sxs-lookup"><span data-stu-id="1a210-117">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

<span data-ttu-id="1a210-118">Esta versão reflete as seguintes métricas de desempenho:</span><span class="sxs-lookup"><span data-stu-id="1a210-118">This version reflects the following performance metrics:</span></span>

-   <span data-ttu-id="1a210-119">Hora da célula —. 002 \* RTT</span><span class="sxs-lookup"><span data-stu-id="1a210-119">Cell Time — .002\*RTT</span></span>
-   <span data-ttu-id="1a210-120">Goodput – 2 kilobytes/RTT</span><span class="sxs-lookup"><span data-stu-id="1a210-120">Goodput — 2 Kilobytes/RTT</span></span>
-   <span data-ttu-id="1a210-121">Sobrecarga de protocolo – 14%</span><span class="sxs-lookup"><span data-stu-id="1a210-121">Protocol Overhead — 14%</span></span>

<span data-ttu-id="1a210-122">Da sobrecarga de 14%, 6% é dos cabeçalhos de Ethernet e os outros 8% são da inicialização da conexão e da subdivisão.</span><span class="sxs-lookup"><span data-stu-id="1a210-122">Of the 14% overhead, 6% is from the Ethernet headers and the other 8% is from the connection startup and teardown.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a210-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1a210-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a210-124">Melhorando um aplicativo lento</span><span class="sxs-lookup"><span data-stu-id="1a210-124">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="1a210-125">Terminologia de rede</span><span class="sxs-lookup"><span data-stu-id="1a210-125">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="1a210-126">A versão de linha de base: um aplicativo com muito mau desempenho</span><span class="sxs-lookup"><span data-stu-id="1a210-126">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="1a210-127">Revisão 1: limpando o óbvio</span><span class="sxs-lookup"><span data-stu-id="1a210-127">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="1a210-128">Revisão 2: redesignação para menos conexões</span><span class="sxs-lookup"><span data-stu-id="1a210-128">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="1a210-129">Aprimoramentos futuros</span><span class="sxs-lookup"><span data-stu-id="1a210-129">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 



