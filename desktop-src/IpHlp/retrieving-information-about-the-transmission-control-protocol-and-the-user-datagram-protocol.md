---
description: O IP Helper torna possível acessar informações sobre protocolos de rede que são usados no computador local.
ms.assetid: 3ae07fbd-0b69-42d6-81ab-cc239c354bbb
title: Recuperando informações sobre o protocolo de controle de transmissão e o protocolo de datagrama do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a73893bf379dda6a58f86854028967da806863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663603"
---
# <a name="retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol"></a><span data-ttu-id="dda72-103">Recuperando informações sobre o protocolo de controle de transmissão e o protocolo de datagrama do usuário</span><span class="sxs-lookup"><span data-stu-id="dda72-103">Retrieving Information About the Transmission Control Protocol and the User Datagram Protocol</span></span>

<span data-ttu-id="dda72-104">O IP Helper torna possível acessar informações sobre protocolos de rede que são usados no computador local.</span><span class="sxs-lookup"><span data-stu-id="dda72-104">IP Helper makes it possible to access information about network protocols that are used on the local computer.</span></span> <span data-ttu-id="dda72-105">Use as funções descritas nos parágrafos a seguir para recuperar informações sobre o protocolo TCP e UDP (User Datagram Protocol) no computador local.</span><span class="sxs-lookup"><span data-stu-id="dda72-105">Use the functions described in the following paragraphs to retrieve information about the Transmission Control Protocol (TCP) and User Datagram Protocol (UDP) on the local computer.</span></span>

<span data-ttu-id="dda72-106">A função [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) recupera as estatísticas atuais para TCP.</span><span class="sxs-lookup"><span data-stu-id="dda72-106">The [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) function retrieves the current statistics for TCP.</span></span> <span data-ttu-id="dda72-107">Para obter exemplos de código envolvendo **GetTcpStatistics** , consulte [recuperando informações usando GetTcpStatistics](retrieving-information-using-gettcpstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="dda72-107">For code samples involving **GetTcpStatistics** see [Retrieving Information Using GetTcpStatistics](retrieving-information-using-gettcpstatistics.md).</span></span>

<span data-ttu-id="dda72-108">A função [**GetUdpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics) recupera as estatísticas atuais para UDP.</span><span class="sxs-lookup"><span data-stu-id="dda72-108">The [**GetUdpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics) function retrieves the current statistics for UDP.</span></span>

<span data-ttu-id="dda72-109">A função [**GetTcpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable) recupera a tabela de conexão TCP.</span><span class="sxs-lookup"><span data-stu-id="dda72-109">The [**GetTcpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable) function retrieves the TCP connection table.</span></span> <span data-ttu-id="dda72-110">O [**GetUdpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable) recupera a tabela de ouvinte UDP.</span><span class="sxs-lookup"><span data-stu-id="dda72-110">The [**GetUdpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable) retrieves the UDP listener table.</span></span>

<span data-ttu-id="dda72-111">A função [**SetTcpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry) permite que um desenvolvedor defina o estado de uma conexão TCP especificada para a \_ exclusão de estado de TCP do MIB \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="dda72-111">The [**SetTcpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry) function enables a developer to set the state of a specified TCP connection to MIB\_TCP\_STATE\_DELETE\_TCB.</span></span>

 

 



