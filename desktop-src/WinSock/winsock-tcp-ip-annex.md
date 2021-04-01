---
description: Esta seção descreve as funções do protocolo TCP/IP, as estruturas de dados e os controles.
ms.assetid: ff92750b-453e-4328-821c-1098de8e6125
title: Anexo TCP/IP do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4fd86a016ed80d9c71ac1647323508cb4dc7b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164862"
---
# <a name="winsock-tcpip-annex"></a><span data-ttu-id="bc58b-103">Anexo TCP/IP do Winsock</span><span class="sxs-lookup"><span data-stu-id="bc58b-103">Winsock TCP/IP Annex</span></span>

<span data-ttu-id="bc58b-104">Esta seção descreve as funções do protocolo TCP/IP, as estruturas de dados e os controles.</span><span class="sxs-lookup"><span data-stu-id="bc58b-104">This section describes Transmission Control Protocol/Internet Protocol (TCP/IP) functions, data structures, and controls.</span></span>



| <span data-ttu-id="bc58b-105">Elemento</span><span class="sxs-lookup"><span data-stu-id="bc58b-105">Element</span></span>          | <span data-ttu-id="bc58b-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc58b-106">Description</span></span>                                                                                                                                 |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc58b-107">Nome (s) de protocolo</span><span class="sxs-lookup"><span data-stu-id="bc58b-107">Protocol name(s)</span></span> | <span data-ttu-id="bc58b-108">TCP, UDP</span><span class="sxs-lookup"><span data-stu-id="bc58b-108">TCP, UDP</span></span>                                                                                                                                    |
| <span data-ttu-id="bc58b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc58b-109">Description</span></span>      | <span data-ttu-id="bc58b-110">Fornece serviços de transporte pela camada de rede IP: UDP para datagramas não confiáveis, TCP para fluxos de bytes confiáveis e orientados a conexões.</span><span class="sxs-lookup"><span data-stu-id="bc58b-110">Provides transport services over the IP networking layer: UDP for unreliable datagrams, TCP for reliable, connection-oriented byte streams.</span></span> |
| <span data-ttu-id="bc58b-111">Família de endereços</span><span class="sxs-lookup"><span data-stu-id="bc58b-111">Address family</span></span>   | <span data-ttu-id="bc58b-112">**AF \_ INET**, **AF \_ INET6**</span><span class="sxs-lookup"><span data-stu-id="bc58b-112">**AF\_INET**, **AF\_INET6**</span></span>                                                                                                                 |
| <span data-ttu-id="bc58b-113">Arquivo de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bc58b-113">Header file</span></span>      | <span data-ttu-id="bc58b-114">*Ws2tcpip. h*</span><span class="sxs-lookup"><span data-stu-id="bc58b-114">*Ws2tcpip.h*</span></span>                                                                                                                                |



 

<span data-ttu-id="bc58b-115">Dois tipos básicos de serviços de transporte são oferecidos: datagrams (UDP) não confiáveis e orientado a conexão confiável – fluxos de bytes (TCP).</span><span class="sxs-lookup"><span data-stu-id="bc58b-115">Two basic types of transport services are offered: unreliable datagrams (UDP), and reliable connection oriented–byte streams (TCP).</span></span> <span data-ttu-id="bc58b-116">Além disso, um soquete bruto tem suporte opcional.</span><span class="sxs-lookup"><span data-stu-id="bc58b-116">In addition, a raw socket is optionally supported.</span></span> <span data-ttu-id="bc58b-117">Os soquetes brutos permitem que um aplicativo se comunique por meio de protocolos diferentes de TCP e UDP, como ICMP.</span><span class="sxs-lookup"><span data-stu-id="bc58b-117">Raw sockets allow an application to communicate through protocols other than TCP and UDP such as ICMP.</span></span> <span data-ttu-id="bc58b-118">Os soquetes brutos têm suporte nas famílias de endereços **\_ inet** e **AF \_ INET6** de AF, com algumas limitações.</span><span class="sxs-lookup"><span data-stu-id="bc58b-118">Raw sockets are supported on the **AF\_INET** and **AF\_INET6** address families with some limitations.</span></span>

<span data-ttu-id="bc58b-119">Esta seção aborda extensões para Winsock que são específicas para protocolos TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="bc58b-119">This section covers extensions to Winsock that are specific to TCP/IP protocols.</span></span> <span data-ttu-id="bc58b-120">Ele também descreve aspectos de funções Winsock base que exigem uma consideração especial ou que podem apresentar um comportamento exclusivo ao usar TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="bc58b-120">It also describes aspects of base Winsock functions that require special consideration or that may exhibit unique behavior when using TCP/IP.</span></span>

 

 



