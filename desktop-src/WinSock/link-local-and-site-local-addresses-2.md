---
description: Os endereços IPv6 de link local e local são chamados de endereços no escopo.
ms.assetid: d31882f6-b747-47c7-83cb-a9a03fe11cb8
title: Link IPv6-local e endereços locais do site
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb80b8e201adf382b10dd31fe5607de903d6c588
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814014"
---
# <a name="ipv6-link-local-and-site-local-addresses"></a><span data-ttu-id="b69c8-103">Link IPv6-local e endereços locais do site</span><span class="sxs-lookup"><span data-stu-id="b69c8-103">IPv6 Link-local and Site-local Addresses</span></span>

<span data-ttu-id="b69c8-104">Os endereços IPv6 de link local e local são chamados de endereços no escopo.</span><span class="sxs-lookup"><span data-stu-id="b69c8-104">IPv6 link-local and site-local addresses are called scoped addresses.</span></span> <span data-ttu-id="b69c8-105">A API do Windows Sockets (Winsock) dá suporte ao membro da **\_ \_ ID de escopo sin6** na estrutura [**SOCKADDR \_ In6**](sockaddr-2.md) para uso com endereços com escopo.</span><span class="sxs-lookup"><span data-stu-id="b69c8-105">The Windows Sockets (Winsock) API supports the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure for use with scoped addresses.</span></span> <span data-ttu-id="b69c8-106">Para endereços de link local IPv6 (FE80::/10 prefix), o membro de **\_ \_ ID de escopo sin6** na estrutura **SOCKADDR \_ In6** é o número da interface.</span><span class="sxs-lookup"><span data-stu-id="b69c8-106">For IPv6 link-local addresses (fe80::/10 prefix), the **sin6\_scope\_id** member in the **sockaddr\_in6** structure is the interface number.</span></span> <span data-ttu-id="b69c8-107">Para endereços locais de site IPv6 (FEC0::/10 prefix), o membro de **\_ \_ ID de escopo sin6** na estrutura **SOCKADDR \_ In6** é um identificador de site.</span><span class="sxs-lookup"><span data-stu-id="b69c8-107">For IPv6 site-local addresses (fec0::/10 prefix), the **sin6\_scope\_id** member in the **sockaddr\_in6** structure is a site identifier.</span></span>

<span data-ttu-id="b69c8-108">Um exemplo de um endereço IPv6 de link local na interface \# 5 é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b69c8-108">An example of a link-local IPv6 address on interface \#5 is the following:</span></span>

``` syntax
fe80::208:74ff:feda:625c%5
```

<span data-ttu-id="b69c8-109">O comando a seguir está disponível no Windows XP com Service Pack 1 (SP1) e posterior para consultar e configurar o IPv6 em um computador local:</span><span class="sxs-lookup"><span data-stu-id="b69c8-109">The following command is available on Windows XP with Service Pack 1 (SP1) and later to query and configure IPv6 on a local computer:</span></span>

-   [<span data-ttu-id="b69c8-110">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="b69c8-110">Netsh.exe</span></span>](netsh-exe.md)

<span data-ttu-id="b69c8-111">As alterações de configuração feitas usando os comandos Netsh.exe são permanentes e não são perdidas quando o computador ou o protocolo IPv6 é reiniciado.</span><span class="sxs-lookup"><span data-stu-id="b69c8-111">Configuration changes made using the Netsh.exe commands are permanent and are not lost when the computer or the IPv6 protocol is restarted.</span></span>

<span data-ttu-id="b69c8-112">Antes do Windows XP com Service Pack 1 (SP1), a configuração e o gerenciamento de IPv6 usavam várias ferramentas de linha de comando mais antigas (Net.exe, Ipv6.exe e Ipsec6.exe) para configurar e gerenciar o IPv6.</span><span class="sxs-lookup"><span data-stu-id="b69c8-112">Prior to Windows XP with Service Pack 1 (SP1), IPv6 configuration and management used several older command-line tools (Net.exe, Ipv6.exe, and Ipsec6.exe) to configure and manage IPv6.</span></span> <span data-ttu-id="b69c8-113">Usando essas ferramentas mais antigas, as alterações de IPv6 não são permanentes e são perdidas quando o computador ou o protocolo IPv6 foi reiniciado.</span><span class="sxs-lookup"><span data-stu-id="b69c8-113">Using these older tools, the IPv6 changes are not permanent and are lost when the computer or the IPv6 protocol was restarted.</span></span> <span data-ttu-id="b69c8-114">Essas ferramentas de linha de comando mais antigas só têm suporte no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b69c8-114">These older command-line tools are only supported on Windows XP.</span></span>

<span data-ttu-id="b69c8-115">No Windows XP com SP1, o comando a seguir exibirá a lista de interfaces IPv6 em um computador local, incluindo o índice da interface, o nome da interface e várias outras propriedades da interface.</span><span class="sxs-lookup"><span data-stu-id="b69c8-115">On Windows XP with SP1, the following command will display the list of IPv6 interfaces on a local computer including the interface index, the interface name, and various other interface properties.</span></span>

<span data-ttu-id="b69c8-116">**netsh interface ipv6 show interface**</span><span class="sxs-lookup"><span data-stu-id="b69c8-116">**netsh interface ipv6 show interface**</span></span>

<span data-ttu-id="b69c8-117">No Windows XP com SP1, o comando a seguir alterará o identificador de site associado a um índice de interface.</span><span class="sxs-lookup"><span data-stu-id="b69c8-117">On Windows XP with SP1, the following command will change the site identifier associated with an interface index.</span></span>

<span data-ttu-id="b69c8-118">**netsh interface ipv6 set interface <InterfaceIndex or Name> SiteId = valor**</span><span class="sxs-lookup"><span data-stu-id="b69c8-118">**netsh interface ipv6 set interface <InterfaceIndex or Name> siteid=value**</span></span>

<span data-ttu-id="b69c8-119">No Windows XP, o comando mais antigo a seguir também alterará o identificador de site associado a um endereço de site local para 3.</span><span class="sxs-lookup"><span data-stu-id="b69c8-119">On Windows XP, the following older command will also change the site identifier associated with a site-local address to 3.</span></span>

<span data-ttu-id="b69c8-120">**IPv6 RTU FEC0::/10 3**</span><span class="sxs-lookup"><span data-stu-id="b69c8-120">**ipv6 rtu fec0::/10 3**</span></span>

<span data-ttu-id="b69c8-121">Se você estiver enviando ou se conectando a um endereço com escopo, o membro de **\_ \_ ID de escopo sin6** na estrutura [**\_ In6 SOCKADDR**](sockaddr-2.md) pode ser deixado não especificado (zero), o que representa um endereço de escopo ambíguo.</span><span class="sxs-lookup"><span data-stu-id="b69c8-121">If you are sending or connecting to a scoped address, then the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure can be left unspecified (zero) which represents an ambiguous scoped address.</span></span> <span data-ttu-id="b69c8-122">Por exemplo, o endereço de link local a seguir é ambíguo:</span><span class="sxs-lookup"><span data-stu-id="b69c8-122">For example, the following link-local address is ambiguous:</span></span>

``` syntax
fe80::10
```

<span data-ttu-id="b69c8-123">Se você estiver ligando a um endereço de escopo, o membro **de \_ \_ ID de escopo sin6** na [**estrutura \_ In6 SOCKADDR**](sockaddr-2.md) deverá conter um valor diferente de zero que especifica um número de interface válido para um endereço de vínculo local ou um identificador de site para um endereço de site local.</span><span class="sxs-lookup"><span data-stu-id="b69c8-123">If you are binding to a scoped address, then the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure must contain a nonzero value that specifies a valid interface number for a link-local address or a site identifier for a site-local address.</span></span>

## <a name="ambiguous-scoped-addresses"></a><span data-ttu-id="b69c8-124">Endereços com escopo ambíguo</span><span class="sxs-lookup"><span data-stu-id="b69c8-124">Ambiguous Scoped Addresses</span></span>

<span data-ttu-id="b69c8-125">Se você estiver enviando ou se conectando a um endereço com escopo e não tiver especificado o membro de **\_ \_ ID de escopo sin6** na estrutura [**\_ In6 SOCKADDR**](sockaddr-2.md) , o endereço com escopo será ambíguo.</span><span class="sxs-lookup"><span data-stu-id="b69c8-125">If you are sending or connecting to a scoped address and have not specified the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure, then the scoped address is ambiguous.</span></span> <span data-ttu-id="b69c8-126">Para resolver isso, o protocolo IPv6 primeiro determina se você asboundu o soquete a um endereço de origem.</span><span class="sxs-lookup"><span data-stu-id="b69c8-126">To resolve this, the IPv6 protocol first determines whether you have bound the socket to a source address.</span></span> <span data-ttu-id="b69c8-127">Nesse caso, o endereço de origem associado resolve a ambiguidade fornecendo um número de interface ou identificador de site.</span><span class="sxs-lookup"><span data-stu-id="b69c8-127">If so, the bound source address resolves the ambiguity by supplying an interface number or site identifier.</span></span>

<span data-ttu-id="b69c8-128">Se você estiver enviando ou se conectando a um endereço com escopo e não tiver especificado o membro de **\_ \_ ID de escopo sin6** nem associado a um endereço de origem, o protocolo IPv6 verificará a tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="b69c8-128">If you are sending or connecting to a scoped address and have neither specified the **sin6\_scope\_id** member nor bound a source address, then the IPv6 protocol checks the routing table.</span></span> <span data-ttu-id="b69c8-129">Por exemplo, o comando a seguir exibirá a tabela de roteamento IPv6 em um computador local:</span><span class="sxs-lookup"><span data-stu-id="b69c8-129">For example, the following command will display the IPv6 routing table on a local computer:</span></span>

<span data-ttu-id="b69c8-130">**netsh interface ipv6 show route**</span><span class="sxs-lookup"><span data-stu-id="b69c8-130">**netsh interface ipv6 show route**</span></span>

``` syntax
No   Manual   256  fe80::/64      13  Local Area Connection
No   Manual   256  fe80::/64      14  Wireless Network Connection
```

<span data-ttu-id="b69c8-131">Isso indica que os endereços de link local são tratados como on-link para a interface \# 13 e \# 14 por padrão.</span><span class="sxs-lookup"><span data-stu-id="b69c8-131">This indicates that link-local addresses are treated as on-link to interface \#13 and \#14 by default.</span></span>

<span data-ttu-id="b69c8-132">A ambiguidade surge quando um computador local tem vários adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="b69c8-132">Ambiguity arises when a local computer has multiple network adapters.</span></span> <span data-ttu-id="b69c8-133">Por exemplo, o comando **netsh** acima indica que há duas interfaces de rede (conexão de área local e conexão de rede sem fio).</span><span class="sxs-lookup"><span data-stu-id="b69c8-133">For example, the **netsh** command above indicates there are two network interfaces (Local Area Connection and Wireless Network Connection).</span></span> <span data-ttu-id="b69c8-134">Quando um aplicativo especifica um endereço de destino local (FE80:: 10, por exemplo) sem uma ID de escopo, não fica claro qual adaptador usar para enviar o pacote.</span><span class="sxs-lookup"><span data-stu-id="b69c8-134">When an application specifies a destination link-local address (fe80::10, for example) without a scope ID, it is not clear which adapter to use to send the packet.</span></span> <span data-ttu-id="b69c8-135">Somente um link-local unicast (FE80::/64) ou um endereço de destino de multicast de escopo de link (FF00::/8) pode ser prejudicado de não ter uma ID de escopo ao enviar um pacote.</span><span class="sxs-lookup"><span data-stu-id="b69c8-135">Only a link-local unicast (fe80::/64) or a link-scope multicast (ff00::/8) IPv6 destination address can suffer from not having a scope ID when sending a packet.</span></span>

## <a name="neighbor-discovery"></a><span data-ttu-id="b69c8-136">Descoberta de vizinhos</span><span class="sxs-lookup"><span data-stu-id="b69c8-136">Neighbor Discovery</span></span>

<span data-ttu-id="b69c8-137">Se você não tiver especificado o membro de **\_ \_ ID de escopo sin6** na estrutura [**\_ In6 SOCKADDR**](sockaddr-2.md) , não tiver associado um endereço de origem e não tiver especificado uma rota para endereços de vínculo local, o protocolo IPv6 tentará a descoberta de vizinho para resolver o endereço de destino-local.</span><span class="sxs-lookup"><span data-stu-id="b69c8-137">If you have not specified the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure, have not bound a source address, and have not specified a route for link-local addresses, then the IPv6 protocol will try Neighbor Discovery to resolve the destination link-local address.</span></span> <span data-ttu-id="b69c8-138">Para um determinado pacote que está sendo enviado, uma interface é tentada.</span><span class="sxs-lookup"><span data-stu-id="b69c8-138">For a given packet being sent, one interface is tried.</span></span> <span data-ttu-id="b69c8-139">Essa primeira interface que é tentada é considerada a interface mais preferencial.</span><span class="sxs-lookup"><span data-stu-id="b69c8-139">This first interface that is tried is considered the most preferred interface.</span></span> <span data-ttu-id="b69c8-140">Se a descoberta de vizinho não resolver o endereço de vínculo local em uma interface, o pacote a ser enviado será descartado e o sistema se lembrará de que o endereço de link local de destino não estará acessível nessa interface.</span><span class="sxs-lookup"><span data-stu-id="b69c8-140">If Neighbor Discovery fails to resolve the link-local address on an interface, the packet to be sent is dropped and the system remembers that the destination link-local address is not reachable over that interface.</span></span> <span data-ttu-id="b69c8-141">No próximo pacote a ser enviado em todas as mesmas condições, uma interface diferente é tentada para a descoberta de vizinho.</span><span class="sxs-lookup"><span data-stu-id="b69c8-141">On the next packet to be sent under all of the same conditions, a different interface is tried for Neighbor Discovery.</span></span> <span data-ttu-id="b69c8-142">Esse processo continua em cada uma das interfaces em um computador local para cada novo pacote até que a descoberta de vizinho responda ao endereço local de destino ou todas as interfaces possíveis tenham sido tentadas e falharam.</span><span class="sxs-lookup"><span data-stu-id="b69c8-142">This process continues through each of the interfaces on a local computer for each new packet until Neighbor Discovery responds for the destination link-local address or all of the possible interfaces have been tried and failed.</span></span> <span data-ttu-id="b69c8-143">Cada vez que uma tentativa de resolver o vizinho falha, uma interface é eliminada para esse vizinho.</span><span class="sxs-lookup"><span data-stu-id="b69c8-143">Each time an attempt to resolve the neighbor fails, one interface is eliminated for that neighbor.</span></span>

<span data-ttu-id="b69c8-144">Se o endereço de link local de destino for resolvido, essa interface será usada para enviar o pacote atual.</span><span class="sxs-lookup"><span data-stu-id="b69c8-144">If the destination link-local address resolves, then that interface is used to send the current packet.</span></span> <span data-ttu-id="b69c8-145">Essa interface também é usada para todos os pacotes de escopo ambíguos subseqüentes que são enviados para o mesmo endereço de destino de link local.</span><span class="sxs-lookup"><span data-stu-id="b69c8-145">This interface is also used for any subsequent ambiguously-scoped packets that are sent to the same link-local destination address.</span></span>

<span data-ttu-id="b69c8-146">Se a descoberta de vizinhos falhar ao resolver o endereço de destino-local em todas as interfaces, o sistema tentará enviar o pacote na interface mais preferencial (a primeira interface tentada).</span><span class="sxs-lookup"><span data-stu-id="b69c8-146">If Neighbor Discovery fails to resolve the destination link-local address on all interfaces, the system then tries to send the packet on the most preferred interface (the first interface tried).</span></span> <span data-ttu-id="b69c8-147">A pilha de rede continua tentando resolver o endereço do link-local de destino na interface mais preferencial.</span><span class="sxs-lookup"><span data-stu-id="b69c8-147">The network stack keeps trying to resolve the destination link-local address on the most preferred interface.</span></span> <span data-ttu-id="b69c8-148">Após um período de tempo após a falha da descoberta de vizinho em todas as interfaces, a pilha de rede reiniciará o processo novamente e tentará resolver o endereço do link-local de destino em todas as interfaces.</span><span class="sxs-lookup"><span data-stu-id="b69c8-148">After a period of time after Neighbor Discovery has failed on all interfaces, the network stack will restart the process again and try to resolve the destination link-local address on all of the interfaces.</span></span> <span data-ttu-id="b69c8-149">Atualmente, esse intervalo de tempo quando a descoberta de vizinho é tentada novamente em todas as interfaces é de 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="b69c8-149">Currently, this time interval when Neighbor Discovery is again tried on all interfaces is 60 seconds.</span></span> <span data-ttu-id="b69c8-150">No entanto, esse intervalo de tempo pode ser alterado em versões do Windows e não deve ser considerado por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b69c8-150">However, this time interval may change on versions of Windows and should not be assumed by an application.</span></span>

> [!Note]  
> <span data-ttu-id="b69c8-151">Se um aplicativo associar o mesmo endereço de vínculo local a uma interface diferente depois que a descoberta de vizinho tiver resolvido o endereço de vínculo local, isso não substituirá a interface pelo endereço de destino de link local retornado pela descoberta de vizinho.</span><span class="sxs-lookup"><span data-stu-id="b69c8-151">If an application binds the same link-local address to a different interface after Neighbor Discovery has resolved the link-local address, that will not override the interface with the link-local destination address returned by Neighbor Discovery.</span></span>

 

<span data-ttu-id="b69c8-152">Para obter mais informações sobre a descoberta de vizinho para IP versão 6, consulte [RFC4861](https://tools.ietf.org/html/rfc4861) publicado pela IETF.</span><span class="sxs-lookup"><span data-stu-id="b69c8-152">For more information on Neighbor Discovery for IP version 6, see [RFC4861](https://tools.ietf.org/html/rfc4861) published by the IETF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b69c8-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b69c8-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b69c8-154">Prefixos de site IPv6</span><span class="sxs-lookup"><span data-stu-id="b69c8-154">IPv6 Site Prefixes</span></span>](site-prefixes-2.md)
</dt> <dt>

[<span data-ttu-id="b69c8-155">Ipv6.exe</span><span class="sxs-lookup"><span data-stu-id="b69c8-155">Ipv6.exe</span></span>](ipv6-exe-2.md)
</dt> <dt>

[<span data-ttu-id="b69c8-156">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="b69c8-156">Netsh.exe</span></span>](netsh-exe.md)
</dt> <dt>

[<span data-ttu-id="b69c8-157">Usando IPv6</span><span class="sxs-lookup"><span data-stu-id="b69c8-157">Using IPv6</span></span>](using-ipv6-2.md)
</dt> </dl>

 

 



