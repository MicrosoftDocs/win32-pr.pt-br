---
description: O IP Helper fornece recursos para gerenciar o roteamento de rede. Use as funções a seguir para gerenciar a tabela de roteamento de IP e para obter outras informações de roteamento.
ms.assetid: 879b90e3-aecc-492e-9b22-9ebbf505a610
title: Gerenciando o roteamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ec199de19b4c8d724fbe6a2e77c3fac7dc19b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827048"
---
# <a name="managing-routing"></a><span data-ttu-id="3a003-104">Gerenciando o roteamento</span><span class="sxs-lookup"><span data-stu-id="3a003-104">Managing Routing</span></span>

<span data-ttu-id="3a003-105">O IP Helper fornece recursos para gerenciar o roteamento de rede.</span><span class="sxs-lookup"><span data-stu-id="3a003-105">IP Helper provides features to manage network routing.</span></span> <span data-ttu-id="3a003-106">Use as funções a seguir para gerenciar a tabela de roteamento de IP e para obter outras informações de roteamento.</span><span class="sxs-lookup"><span data-stu-id="3a003-106">Use the following functions to manage the IP routing table, and to obtain other routing information.</span></span>

<span data-ttu-id="3a003-107">Recupere o conteúdo da tabela de roteamento de IP fazendo uma chamada para a função [**GetIpForwardTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipforwardtable) .</span><span class="sxs-lookup"><span data-stu-id="3a003-107">Retrieve the contents of the IP routing table by making a call to the [**GetIpForwardTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipforwardtable) function.</span></span> <span data-ttu-id="3a003-108">Manipule entradas específicas na tabela de roteamento de IP usando as funções [**CreateIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipforwardentry), [**DeleteIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)e [**SetIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipforwardentry) .</span><span class="sxs-lookup"><span data-stu-id="3a003-108">Manipulate specific entries in the IP routing table using the [**CreateIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipforwardentry), [**DeleteIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry), and [**SetIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipforwardentry) functions.</span></span> <span data-ttu-id="3a003-109">Use a função **CreateIpForwardEntry** para adicionar uma nova entrada da tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="3a003-109">Use the **CreateIpForwardEntry** function to add a new routing table entry.</span></span> <span data-ttu-id="3a003-110">Use a função **DeleteIpForwardEntry** para remover uma entrada existente.</span><span class="sxs-lookup"><span data-stu-id="3a003-110">Use the **DeleteIpForwardEntry** function to remove an existing entry.</span></span> <span data-ttu-id="3a003-111">A função **SetIpForwardEntry** modifica uma entrada existente.</span><span class="sxs-lookup"><span data-stu-id="3a003-111">The **SetIpForwardEntry** function modifies an existing entry.</span></span>

<span data-ttu-id="3a003-112">Os recursos de gerenciamento de roteador do auxiliar de IP podem ser usados para recuperar informações sobre como os datagramas são roteados pela rede.</span><span class="sxs-lookup"><span data-stu-id="3a003-112">The router management capabilities of IP Helper can be used to retrieve information about how datagrams are routed over the network.</span></span> <span data-ttu-id="3a003-113">A função [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute) recupera a melhor rota para um endereço de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="3a003-113">The [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute) function retrieves the best route to a specified destination address.</span></span> <span data-ttu-id="3a003-114">A função [**GetBestInterface**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestinterface) recupera o índice da interface usada pela melhor rota para um endereço de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="3a003-114">The [**GetBestInterface**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestinterface) function retrieves the index of the interface used by the best route to a specified destination address.</span></span> <span data-ttu-id="3a003-115">Por fim, a função [**GetRTTAndHopCount**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getrttandhopcount) recupera o tempo de ida e volta (RTT) e o número de saltos para um endereço de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="3a003-115">Lastly, the [**GetRTTAndHopCount**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getrttandhopcount) function retrieves the round-trip time (RTT) and number of hops to a specified destination address.</span></span>

 

 



