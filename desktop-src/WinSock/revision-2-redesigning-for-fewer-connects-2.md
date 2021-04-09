---
description: Nesta revisão, o aplicativo de exemplo é reprojetado para eliminar conexões desnecessárias.
ms.assetid: 0db6ded4-0a59-454e-824e-8cd7f0dc9fec
title: 'Revisão dois: redesignação para menos conexões'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8d5a8c8648f43f9ddac93c9d17f667b4b97011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091310"
---
# <a name="revision-two-redesigning-for-fewer-connects"></a><span data-ttu-id="ecdbb-103">Revisão dois: redesignação para menos conexões</span><span class="sxs-lookup"><span data-stu-id="ecdbb-103">Revision Two: Redesigning for Fewer Connects</span></span>

<span data-ttu-id="ecdbb-104">Nesta revisão, o aplicativo de exemplo é reprojetado para eliminar conexões desnecessárias.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-104">In this revision, the sample application is redesigned to eliminate unnecessary connects.</span></span>

> [!WARNING]
> <span data-ttu-id="ecdbb-105">Esses exemplos do aplicativo também fornecem um desempenho intencionalmente insatisfatório, a fim de ilustrar as melhorias de desempenho possíveis com alterações no código.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-105">This examples of the application also provide intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="ecdbb-106">Não use este exemplo de código em seu aplicativo; Ele é apenas para fins ilustrativos.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-106">Do not use this code sample in your application; it is for illustration purposes only.</span></span>

 


```C++
ComputeNext( Map );
bind( s, ... );
connect( s, ... );
for(int i=0 ; i < ROWS ; ++i)
  for(int j=0 ; j < COLS ; ++j)
  {
    BYTE tmp[3];
    tmp[0] = i;
    tmp[1] = j;
    tmp[2] = Map[i][j];
    send( s, tmp, 3 );
    recv( s, &byRet, 1 );
  }
closesocket( s );
```



## <a name="remaining-problems"></a><span data-ttu-id="ecdbb-107">Problemas restantes</span><span class="sxs-lookup"><span data-stu-id="ecdbb-107">Remaining Problems</span></span>

<span data-ttu-id="ecdbb-108">As alterações na revisão dois remodelaram o aplicativo para fazer apenas uma conexão por atualização.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-108">The changes in Revision Two redesigned the application to make only one connect per update.</span></span> <span data-ttu-id="ecdbb-109">O aplicativo ainda inclui os seguintes problemas de desempenho:</span><span class="sxs-lookup"><span data-stu-id="ecdbb-109">The application still includes the following performance issues:</span></span>

-   <span data-ttu-id="ecdbb-110">O aplicativo ainda é serializado e informativo.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-110">The application is still serialized and chatty.</span></span>
-   <span data-ttu-id="ecdbb-111">O aplicativo ainda tem um design de Fat; Há muitos envios que não exigem nenhuma operação neste design.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-111">The application still has a fat design; there are many sends that require no operation in this design.</span></span>
-   <span data-ttu-id="ecdbb-112">Os envios ainda são apenas 3 bytes, o que é um streaming ruim.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-112">The sends are still only 3 bytes, which is poor streaming.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="ecdbb-113">Principais métricas de desempenho</span><span class="sxs-lookup"><span data-stu-id="ecdbb-113">Key Performance Metrics</span></span>

<span data-ttu-id="ecdbb-114">As métricas de desempenho a seguir são expressas em RTT (tempo de ida e volta), Goodput e sobrecarga de protocolo.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-114">The following performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="ecdbb-115">Consulte o tópico [terminologia de rede](network-terminology-2.md) para obter uma explicação desses termos.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-115">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

<span data-ttu-id="ecdbb-116">Esta versão reflete as seguintes métricas de desempenho:</span><span class="sxs-lookup"><span data-stu-id="ecdbb-116">This version reflects the following performance metrics:</span></span>

-   <span data-ttu-id="ecdbb-117">Tempo da célula — 1 \* RTT</span><span class="sxs-lookup"><span data-stu-id="ecdbb-117">Cell Time — 1\*RTT</span></span>
-   <span data-ttu-id="ecdbb-118">Goodput – 4 bytes/RTT</span><span class="sxs-lookup"><span data-stu-id="ecdbb-118">Goodput — 4 bytes/RTT</span></span>
-   <span data-ttu-id="ecdbb-119">Sobrecarga de protocolo — 96,8%</span><span class="sxs-lookup"><span data-stu-id="ecdbb-119">Protocol Overhead — 96.8%</span></span>

## <a name="related-topics"></a><span data-ttu-id="ecdbb-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ecdbb-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecdbb-121">Melhorando um aplicativo lento</span><span class="sxs-lookup"><span data-stu-id="ecdbb-121">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="ecdbb-122">Terminologia de rede</span><span class="sxs-lookup"><span data-stu-id="ecdbb-122">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="ecdbb-123">A versão de linha de base: um aplicativo com muito mau desempenho</span><span class="sxs-lookup"><span data-stu-id="ecdbb-123">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="ecdbb-124">Revisão 1: limpando o óbvio</span><span class="sxs-lookup"><span data-stu-id="ecdbb-124">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="ecdbb-125">Revisão 3: envio de bloco compactado</span><span class="sxs-lookup"><span data-stu-id="ecdbb-125">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> <dt>

[<span data-ttu-id="ecdbb-126">Aprimoramentos futuros</span><span class="sxs-lookup"><span data-stu-id="ecdbb-126">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 



