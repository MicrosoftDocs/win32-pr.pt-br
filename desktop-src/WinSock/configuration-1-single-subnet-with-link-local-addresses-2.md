---
description: A primeira configuração não requer nenhuma configuração adicional além da instalação do protocolo Microsoft IPv6 Technology Preview.
ms.assetid: ceed4983-e088-44e8-9cfc-26afb3c35ba0
title: 'Configuração 1: sub-rede única com endereços de link local'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d09feb44c222b7213da18a6745fc632f3903209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010494"
---
# <a name="configuration-1-single-subnet-with-link-local-addresses"></a><span data-ttu-id="980c8-103">Configuração 1: sub-rede única com endereços de link local</span><span class="sxs-lookup"><span data-stu-id="980c8-103">Configuration 1: Single Subnet with Link-local Addresses</span></span>

<span data-ttu-id="980c8-104">A primeira configuração não requer nenhuma configuração adicional além da instalação do protocolo Microsoft IPv6 Technology Preview.</span><span class="sxs-lookup"><span data-stu-id="980c8-104">The first configuration requires no additional configuration beyond installing the Microsoft IPv6 Technology Preview protocol.</span></span> <span data-ttu-id="980c8-105">Essa configuração consiste em pelo menos dois nós na mesma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="980c8-105">This configuration consists of at least two nodes on the same subnet.</span></span> <span data-ttu-id="980c8-106">Na terminologia IPv6, os dois nós estão no mesmo link sem roteadores intermediários.</span><span class="sxs-lookup"><span data-stu-id="980c8-106">In IPv6 terminology, the two nodes are on the same link with no intermediate routers.</span></span>

<span data-ttu-id="980c8-107">A ilustração a seguir mostra a configuração de dois nós em uma única sub-rede usando endereços de link local.</span><span class="sxs-lookup"><span data-stu-id="980c8-107">The following illustration shows the configuration of two nodes on a single subnet using link-local addresses.</span></span>

![dois nós usando endereços de link local.](images/v6mig-1.png)

<span data-ttu-id="980c8-109">Por padrão, o IPv6 configura endereços IP de link local para cada interface correspondente aos adaptadores de rede Ethernet instalados.</span><span class="sxs-lookup"><span data-stu-id="980c8-109">By default, IPv6 configures link-local IP addresses for each interface corresponding to installed Ethernet network adapters.</span></span> <span data-ttu-id="980c8-110">Os endereços de link local têm o prefixo FE80::/64.</span><span class="sxs-lookup"><span data-stu-id="980c8-110">Link-local addresses have the prefix fe80::/64.</span></span> <span data-ttu-id="980c8-111">Os últimos 64 bits do endereço IPv6 são conhecidos como o identificador de interface e são derivados do endereço MAC de 48 bits do adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="980c8-111">The last 64 bits of the IPv6 address is known as the interface identifier and is derived from the 48-bit MAC address of the network adapter.</span></span>

<span data-ttu-id="980c8-112">Para criar o identificador de interface IPv6 do endereço Ethernet MAC de 48 bits (6 bytes):</span><span class="sxs-lookup"><span data-stu-id="980c8-112">To create the IPv6 interface identifier from the 48-bit (6-byte) Ethernet MAC address:</span></span>

-   <span data-ttu-id="980c8-113">Os dígitos hexadecimais 0xFF-FE são inseridos entre o terceiro e o quarto byte do endereço MAC.</span><span class="sxs-lookup"><span data-stu-id="980c8-113">The hex digits 0xff-fe are inserted between the third and fourth byte of the MAC address.</span></span>
-   <span data-ttu-id="980c8-114">O bit Universal/local, o segundo bit de ordem inferior do primeiro byte do endereço MAC, é complementado.</span><span class="sxs-lookup"><span data-stu-id="980c8-114">The Universal/Local bit, the second low-order bit of the first byte of the MAC address, is complemented.</span></span> <span data-ttu-id="980c8-115">Se for 1, ele será ativado como 0 e, se for 0, será ativado como 1.</span><span class="sxs-lookup"><span data-stu-id="980c8-115">If it is a 1, it is turned to 0, and if it is a 0, it is turned to 1.</span></span>

<span data-ttu-id="980c8-116">Por exemplo, para o endereço MAC 00-60-08-52-F9-D8:</span><span class="sxs-lookup"><span data-stu-id="980c8-116">For example, for the MAC address 00-60-08-52-f9-d8:</span></span>

-   <span data-ttu-id="980c8-117">Os dígitos hexadecimais 0xFF-FE são inseridos entre 0x08 (o terceiro byte) e 0x52 (o quarto byte) do endereço MAC, que formam o endereço de 64 bits 00-60-08-FF-FE-52-F9-D8.</span><span class="sxs-lookup"><span data-stu-id="980c8-117">The hex digits 0xff-fe are inserted between 0x08 (the third byte) and 0x52 (the fourth byte) of the MAC address, forming the 64-bit address 00-60-08-ff-fe-52-f9-d8.</span></span>
-   <span data-ttu-id="980c8-118">O bit Universal/local, o segundo bit de ordem inferior de 0x00 (o primeiro byte) do endereço MAC é complementado.</span><span class="sxs-lookup"><span data-stu-id="980c8-118">The Universal/Local bit, the second low-order bit of 0x00 (the first byte) of the MAC address is complemented.</span></span> <span data-ttu-id="980c8-119">O segundo bit de ordem inferior de 0x00 é 0, que, quando complementado, se torna 1.</span><span class="sxs-lookup"><span data-stu-id="980c8-119">The second low-order bit of 0x00 is 0 which, when complemented, becomes 1.</span></span> <span data-ttu-id="980c8-120">O resultado é que, para o primeiro byte, 0x00 torna-se 0x02.</span><span class="sxs-lookup"><span data-stu-id="980c8-120">The result is that for the first byte, 0x00 becomes 0x02.</span></span>

<span data-ttu-id="980c8-121">Portanto, o identificador de interface IPv6 correspondente ao endereço Ethernet MAC de 00-60-08-52-F9-D8 é 02-60-08-FF-FE-52-F9-D8.</span><span class="sxs-lookup"><span data-stu-id="980c8-121">Therefore, the IPv6 interface identifier corresponding to the Ethernet MAC address of 00-60-08-52-f9-d8 is 02-60-08-ff-fe-52-f9-d8.</span></span>

<span data-ttu-id="980c8-122">O endereço de vínculo local de um nó é a combinação do prefixo FE80::/64 e o identificador de interface de 64 bits expressos na notação hexadecimal de dois-pontos do IPv6.</span><span class="sxs-lookup"><span data-stu-id="980c8-122">The link-local address of a node is the combination of the prefix fe80::/64 and the 64-bit interface identifier expressed in IPv6 colon-hexadecimal notation.</span></span> <span data-ttu-id="980c8-123">Portanto, o endereço de link local deste nó de exemplo com o prefixo FE80::/64 e o identificador de interface 02-60-08-FF-FE-52-F9-D8 é FE80:: 260:8FF: FE52: F9D8.</span><span class="sxs-lookup"><span data-stu-id="980c8-123">Therefore, the link-local address of this example node with the prefix fe80::/64 and the interface identifier 02-60-08-ff-fe-52-f9-d8 is fe80::260:8ff:fe52:f9d8.</span></span>

<span data-ttu-id="980c8-124">Você pode exibir seu endereço local do link usando IPv6 se, conforme demonstrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="980c8-124">You can view your link local address by using ipv6 if, as demonstrated in the following example:</span></span>

<span data-ttu-id="980c8-125">**IPv6 se**</span><span class="sxs-lookup"><span data-stu-id="980c8-125">**ipv6 if**</span></span>

``` syntax
Interface 4 (site 1): Local Area Connection
  uses Neighbor Discovery
  link-level address: 00-10-5a-aa-20-a2
    preferred address fe80::210:5aff:feaa:20a2, infinite/infinite
    multicast address ff02::1, 1 refs, not reportable
    multicast address ff02::1:ffaa:20a2, 1 refs, last reporter
  link MTU 1500 (true link MTU 1500)
  current hop limit 128
  reachable time 43500ms (base 30000ms)
  retransmission interval 1000ms
  DAD transmits 1
Interface 3 (site 1): 6-over-4 Virtual Interface
  uses Neighbor Discovery
  link-level address: 10.0.0.2
    preferred address fe80::a00:2, infinite/infinite
    multicast address ff02::1, 1 refs, not reportable
    multicast address ff02::1:ff00:2, 1 refs, last reporter
  link MTU 1280 (true link MTU 65515)
  current hop limit 128
  reachable time 34000ms (base 30000ms)
  retransmission interval 1000ms
  DAD transmits 1
Interface 2 (site 0): Tunnel Pseudo-Interface
  does not use Neighbor Discovery
  link-level address: 0.0.0.0
    preferred address ::10.0.0.2, infinite/infinite
  link MTU 1280 (true link MTU 65515)
  current hop limit 128
  reachable time 0ms (base 0ms)
  retransmission interval 0ms
  DAD transmits 0
Interface 1 (site 0): Loopback Pseudo-Interface
  does not use Neighbor Discovery
  link-level address:
    preferred address ::1, infinite/infinite
  link MTU 1500 (true link MTU 1500)
  current hop limit 1
  reachable time 0ms (base 0ms)
  retransmission interval 0ms
  DAD transmits 0
```

<span data-ttu-id="980c8-126">A interface 4 é uma interface correspondente a um adaptador Ethernet instalado com um endereço de link local de FE80:: 210:5AFF: FEAA: 20A2.</span><span class="sxs-lookup"><span data-stu-id="980c8-126">Interface 4 is an interface corresponding to an installed Ethernet adapter with a link-local address of fe80::210:5aff:feaa:20a2.</span></span>

<span data-ttu-id="980c8-127">Para obter mais informações sobre o endereçamento IPv6 e uma visão geral dos conceitos do IPv6, consulte a introdução ao IPv6 white paper.</span><span class="sxs-lookup"><span data-stu-id="980c8-127">For more information on IPv6 addressing and an overview of IPv6 concepts, see the Introduction to IPv6 white paper.</span></span>

## <a name="testing-connectivity-between-two-link-local-hosts"></a><span data-ttu-id="980c8-128">Testando a conectividade entre dois hosts de link local</span><span class="sxs-lookup"><span data-stu-id="980c8-128">Testing Connectivity Between Two Link-local Hosts</span></span>

<span data-ttu-id="980c8-129">Você pode fazer um ping simples (uma troca de mensagens de resposta de eco e de solicitação de eco ICMPv6) usando o IPv6 entre dois hosts de link local.</span><span class="sxs-lookup"><span data-stu-id="980c8-129">You can do a simple ping (an exchange of ICMPv6 Echo Request and Echo Reply messages) using IPv6 between two link-local hosts.</span></span>

<span data-ttu-id="980c8-130">**Para executar ping usando o IPv6 entre dois hosts de link local**</span><span class="sxs-lookup"><span data-stu-id="980c8-130">**To ping using IPv6 between two link-local hosts**</span></span>

1.  <span data-ttu-id="980c8-131">Instale o Microsoft IPv6 Technology Preview para Windows em dois hosts do Windows (host A e host B) que estão no mesmo link (sub-rede).</span><span class="sxs-lookup"><span data-stu-id="980c8-131">Install the Microsoft IPv6 Technology Preview for Windows on two Windows hosts (Host A and Host B) that are on the same link (subnet).</span></span>
2.  <span data-ttu-id="980c8-132">Use o IPv6 se estiver no host a para obter o endereço de vínculo local para a interface Ethernet.</span><span class="sxs-lookup"><span data-stu-id="980c8-132">Use ipv6 if on Host A to obtain the link-local address for the Ethernet interface.</span></span>

    <span data-ttu-id="980c8-133">Exemplo: o endereço de link local do host A é FE80:: 210:5AFF: FEAA: 20A2.</span><span class="sxs-lookup"><span data-stu-id="980c8-133">Example: The link-local address of Host A is fe80::210:5aff:feaa:20a2.</span></span>

3.  <span data-ttu-id="980c8-134">Use o IPv6 se estiver no host B para obter o endereço de link local para a interface Ethernet.</span><span class="sxs-lookup"><span data-stu-id="980c8-134">Use ipv6 if on Host B to obtain the link-local address for the Ethernet interface.</span></span>

    <span data-ttu-id="980c8-135">Exemplo: o endereço de link local do host B é FE80:: 260:97FF: FE02:6EA5.</span><span class="sxs-lookup"><span data-stu-id="980c8-135">Example: The link-local address of Host B is fe80::260:97ff:fe02:6ea5.</span></span>

4.  <span data-ttu-id="980c8-136">No host A, execute ping no host B usando Ping6.exe.</span><span class="sxs-lookup"><span data-stu-id="980c8-136">From Host A, ping Host B using Ping6.exe.</span></span>

    <span data-ttu-id="980c8-137">Exemplo: ping6 FE80:: 260:97FF: FE02:6EA5</span><span class="sxs-lookup"><span data-stu-id="980c8-137">Example: ping6 fe80::260:97ff:fe02:6ea5</span></span>

<span data-ttu-id="980c8-138">Para especificar o endereço de origem do qual as mensagens de solicitação de eco são enviadas, você também pode usar a opção Ping6.exe-s.</span><span class="sxs-lookup"><span data-stu-id="980c8-138">To specify the source address from which the Echo Request messages are sent, you can also use the Ping6.exe -s option.</span></span> <span data-ttu-id="980c8-139">Por exemplo, para enviar solicitações de eco para o host B do endereço IPv6 de FE80:: 210:5AFF: FEAA: 20A2, use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="980c8-139">For example, to send Echo Requests to Host B from the IPv6 address of fe80::210:5aff:feaa:20a2, use the following command:</span></span>

<span data-ttu-id="980c8-140">**ping6-s FE80:: 210:5AFF: FEAA: 20A2% 4 FE80:: 260:97FF: FE02:6EA5**</span><span class="sxs-lookup"><span data-stu-id="980c8-140">**ping6 -s fe80::210:5aff:feaa:20a2%4 fe80::260:97ff:fe02:6ea5**</span></span>

<span data-ttu-id="980c8-141">Ao executar ping de um endereço de link local ou site local, é recomendável especificar o Scope-ID para tornar o endereço de destino inambíguo.</span><span class="sxs-lookup"><span data-stu-id="980c8-141">When pinging a link-local or site-local address, it is recommended to specify the scope-ID to make the destination address unambiguous.</span></span> <span data-ttu-id="980c8-142">A notação para especificar o Scope-ID é o endereço% Scope-ID.</span><span class="sxs-lookup"><span data-stu-id="980c8-142">The notation to specify the scope-ID is address%scope-ID.</span></span> <span data-ttu-id="980c8-143">Para endereços de vínculo local, o Scope-ID é igual ao número da interface, conforme exibido no comando IPv6 If.</span><span class="sxs-lookup"><span data-stu-id="980c8-143">For link-local addresses, the scope-ID is equal to the interface number as displayed in the ipv6 if command.</span></span> <span data-ttu-id="980c8-144">Para endereços de site local, o Scope-ID é igual ao número do site, conforme exibido no comando IPv6 If.</span><span class="sxs-lookup"><span data-stu-id="980c8-144">For site-local addresses, the scope-ID is equal to the site number as displayed in the ipv6 if command.</span></span> <span data-ttu-id="980c8-145">Por exemplo, para enviar mensagens de solicitação de eco para o host B usando o escopo-ID 4, use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="980c8-145">For example, to send Echo Request messages to Host B using scope-ID 4, use the following command:</span></span>

<span data-ttu-id="980c8-146">**ping6 FE80:: 260:97FF: FE02:6EA5% 4**</span><span class="sxs-lookup"><span data-stu-id="980c8-146">**ping6 fe80::260:97ff:fe02:6ea5%4**</span></span>

## <a name="related-topics"></a><span data-ttu-id="980c8-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="980c8-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="980c8-148">Configurações recomendadas para IPv6</span><span class="sxs-lookup"><span data-stu-id="980c8-148">Recommended Configurations for IPv6</span></span>](recommended-configurations-2.md)
</dt> </dl>

 

 



