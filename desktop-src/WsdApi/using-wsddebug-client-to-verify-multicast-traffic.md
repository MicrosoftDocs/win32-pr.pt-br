---
description: Se o host genérico e o cliente puderem ver uns aos outros na rede, mas o host e o cliente reais não puderem, é provável que o problema esteja nas mensagens enviadas entre os pontos de extremidade pela rede.
ms.assetid: 1b0943fb-076e-4feb-9a4f-36a06bdd19ae
title: Usando o cliente de depuração WSD para verificar o tráfego multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a814ac97512ef4b0691c22d3238d151372023a7
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380660"
---
# <a name="using-wsd-debug-client-to-verify-multicast-traffic"></a><span data-ttu-id="127ea-103">Usando o cliente de depuração WSD para verificar o tráfego multicast</span><span class="sxs-lookup"><span data-stu-id="127ea-103">Using WSD Debug Client to Verify Multicast Traffic</span></span>

<span data-ttu-id="127ea-104">Se o host genérico e o cliente puderem ver uns aos outros na rede, mas o host e o cliente reais não puderem, é provável que o problema esteja nas mensagens enviadas entre os pontos de extremidade pela rede.</span><span class="sxs-lookup"><span data-stu-id="127ea-104">If the generic host and client can see each other on the network but the actual host and client cannot, it is likely that the problem is in the messages sent between the endpoints over the network.</span></span> <span data-ttu-id="127ea-105">Para obter mais informações sobre o host e o cliente genérico, consulte [usando um host genérico e um cliente para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="127ea-105">For more information about the generic host and client, see [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span> <span data-ttu-id="127ea-106">Como os rastreamentos de rede completos podem ser difíceis de coletar, filtrar e ler, a ferramenta de cliente de depuração WSD pode ser usada para imprimir os lados de multicast das mensagens de WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="127ea-106">Because full network traces can be difficult to collect, filter, and read, the WSD Debug Client tool can be used to print the multicast sides of WS-Discovery messages.</span></span>

<span data-ttu-id="127ea-107">O cliente de depuração WSD no modo multicast só pode inspecionar metade das mensagens, pois o cliente não pode imprimir mensagens unicast.</span><span class="sxs-lookup"><span data-stu-id="127ea-107">The WSD Debug Client in multicast mode can only inspect half of the messages, since the client cannot print unicast messages.</span></span> <span data-ttu-id="127ea-108">Se o tráfego unicast for de interesse, pule diretamente para [inspecionar rastreamentos de rede para o WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="127ea-108">If unicast traffic is of interest, skip directly to [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>

<span data-ttu-id="127ea-109">Este procedimento mostra um método que exibirá todo o tráfego de multicast na rede.</span><span class="sxs-lookup"><span data-stu-id="127ea-109">This procedure shows a method that will display all multicast traffic on the network.</span></span> <span data-ttu-id="127ea-110">Para exibir somente o tráfego multicast de e para o dispositivo, consulte a seção [filtrando resultados do cliente de depuração WSD](#filtering-wsd-debug-client-results) abaixo.</span><span class="sxs-lookup"><span data-stu-id="127ea-110">To display only multicast traffic to and from the device, see the [Filtering WSD Debug Client Results](#filtering-wsd-debug-client-results) section below.</span></span>

<span data-ttu-id="127ea-111">**Para usar o cliente de depuração WSD para verificar o tráfego multicast**</span><span class="sxs-lookup"><span data-stu-id="127ea-111">**To use the WSD Debug Client to verify multicast traffic**</span></span>

1.  <span data-ttu-id="127ea-112">Configure o host e o cliente para serem executados na rede (ou seja, certifique-se de que o host e o cliente funcionarão em computadores diferentes).</span><span class="sxs-lookup"><span data-stu-id="127ea-112">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="127ea-113">Abra um prompt de comando e execute o seguinte comando: **WSDDebug \_client.exe/Mode multicast**</span><span class="sxs-lookup"><span data-stu-id="127ea-113">Open a command prompt and run the following command: **WSDDebug\_client.exe /mode multicast**</span></span>
3.  <span data-ttu-id="127ea-114">Reproduza a falha iniciando o host e o cliente ou pressionando F5 no Gerenciador de rede.</span><span class="sxs-lookup"><span data-stu-id="127ea-114">Reproduce the failure by starting the host and client or by pressing F5 in the Network Explorer.</span></span>
4.  <span data-ttu-id="127ea-115">Verifique se as mensagens estão sendo multicast.</span><span class="sxs-lookup"><span data-stu-id="127ea-115">Verify that messages are being multicast.</span></span>

<span data-ttu-id="127ea-116">Se as mensagens necessárias forem exibidas na saída do cliente de depuração WSD, a falha do aplicativo poderá estar no conteúdo da mensagem de multicast ou na existência ou no conteúdo das mensagens de resposta unicast correspondentes.</span><span class="sxs-lookup"><span data-stu-id="127ea-116">If the required messages are displayed in the WSD Debug Client output, then the application failure may be in the multicast message content, or in the existence or content of the corresponding unicast response messages.</span></span> <span data-ttu-id="127ea-117">Continue a solução de problemas seguindo as instruções em [inspecionar rastreamentos de rede para o WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="127ea-117">Continue troubleshooting by following the instructions in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>

<span data-ttu-id="127ea-118">Se as mensagens necessárias forem exibidas na saída do cliente de depuração WSD, é provável que a origem do problema do aplicativo tenha sido identificada.</span><span class="sxs-lookup"><span data-stu-id="127ea-118">If the required messages are displayed in the WSD Debug Client output, then it is likely that the source of the application problem has been identified.</span></span> <span data-ttu-id="127ea-119">É provável que o tráfego multicast não esteja sendo transmitido na rede.</span><span class="sxs-lookup"><span data-stu-id="127ea-119">It is likely that the multicast traffic is not being transmitted on the network.</span></span> <span data-ttu-id="127ea-120">Essa falha pode ocorrer quando o aplicativo não enumera os adaptadores multicast corretamente.</span><span class="sxs-lookup"><span data-stu-id="127ea-120">This failure can happen when the application does not enumerate multicast adapters correctly.</span></span> <span data-ttu-id="127ea-121">Os aplicativos devem enviar explicitamente o tráfego multicast em todas as interfaces de rede; caso contrário, os pacotes podem não ser gerados para a interface de loopback ou para outras interfaces.</span><span class="sxs-lookup"><span data-stu-id="127ea-121">Applications must explicitly send multicast traffic over all network interfaces; otherwise, packets may not be generated for the loopback interface or for other interfaces.</span></span> <span data-ttu-id="127ea-122">Para verificar se os pacotes não aparecem na rede, siga as instruções em [inspecionando os rastreamentos de rede para a descoberta de WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md) e procure evidências de mensagens de multicast ausentes.</span><span class="sxs-lookup"><span data-stu-id="127ea-122">To verify that the packets are not appearing on the network, follow the instructions in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) and look for evidence of missing multicast messages.</span></span>

## <a name="verifying-that-messages-are-being-multicast"></a><span data-ttu-id="127ea-123">Verificando se as mensagens estão sendo multicast</span><span class="sxs-lookup"><span data-stu-id="127ea-123">Verifying that messages are being multicast</span></span>

<span data-ttu-id="127ea-124">Sempre verifique se as mensagens de [investigação](probe-message.md) estão sendo multicast.</span><span class="sxs-lookup"><span data-stu-id="127ea-124">Always verify that [Probe](probe-message.md) messages are being multicast.</span></span> <span data-ttu-id="127ea-125">Opcionalmente, verifique se as mensagens de [saudação](hello-message.md) e de [resolução](resolve-message.md) estão sendo multicast.</span><span class="sxs-lookup"><span data-stu-id="127ea-125">Optionally, verify that [Hello](hello-message.md) and [Resolve](resolve-message.md) messages are being multicast.</span></span> <span data-ttu-id="127ea-126">Observe que nem todos os aplicativos usam as mensagens de resolução.</span><span class="sxs-lookup"><span data-stu-id="127ea-126">Note that not all applications use Resolve messages.</span></span> <span data-ttu-id="127ea-127">Para obter mais informações sobre os padrões de mensagem usados por clientes e hosts, consulte [padrões de mensagens de descoberta e de metadados do Exchange](discovery-and-metadata-exchange-message-patterns.md) e [introdução com a solução de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="127ea-127">For more information about message patterns used by clients and hosts, see [Discovery and Metadata Exchange Message Patterns](discovery-and-metadata-exchange-message-patterns.md) and [Getting Started with WSDAPI Troubleshooting](getting-started-with-wsdapi-troubleshooting.md).</span></span>

<span data-ttu-id="127ea-128">As mensagens devem ser disparadas para serem enviadas conforme descrito na etapa 3 acima.</span><span class="sxs-lookup"><span data-stu-id="127ea-128">Messages must be triggered in order to be sent as described in step 3 above.</span></span> <span data-ttu-id="127ea-129">O cliente de depuração WSD exibe a mensagem SOAP bruta como saída.</span><span class="sxs-lookup"><span data-stu-id="127ea-129">The WSD Debug Client displays the raw SOAP message as output.</span></span> <span data-ttu-id="127ea-130">Como todas as mensagens impressas pelo cliente de depuração WSD no modo multicast são recebidas por um soquete de multicast, o endereço de destino da mensagem não é exibido.</span><span class="sxs-lookup"><span data-stu-id="127ea-130">Because all messages printed by WSD Debug Client in multicast mode are received over a multicast socket, the message destination address is not displayed.</span></span>

<span data-ttu-id="127ea-131">O exemplo de saída de cliente de depuração WSD a seguir mostra uma mensagem de investigação.</span><span class="sxs-lookup"><span data-stu-id="127ea-131">The following sample WSD Debug Client output shows a Probe message.</span></span> <span data-ttu-id="127ea-132">O \<wsa:Action> elemento identifica a mensagem como uma mensagem de investigação.</span><span class="sxs-lookup"><span data-stu-id="127ea-132">The \<wsa:Action> element identifies the message as a Probe message.</span></span> <span data-ttu-id="127ea-133">Inspecione o \<wsa:Action> campo para verificar se a mensagem recebida era uma mensagem de investigação.</span><span class="sxs-lookup"><span data-stu-id="127ea-133">Inspect the \<wsa:Action> field to verify that the received message was a Probe message.</span></span>

``` syntax
UDP message at 05/08/07 10:06:55 from soap.udp://[127.0.0.1:49334]
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="h
ttp://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsd="https://schemas.xmlso
ap.org/ws/2005/04/discovery" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/d
evprof"><soap:Header><wsa:To>urn:schemas-xmlsoap-org:ws:2005:04:discovery</wsa:T
o><wsa:Action>https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe</wsa:Action>
<wsa:MessageID>urn:uuid:256ad815-1576-4e59-8efc-4c1e0f15fdd2</wsa:MessageID></so
ap:Header><soap:Body><wsd:Probe><wsd:Types>wsdp:Device</wsd:Types></wsd:Probe></
soap:Body></soap:Envelope>
```

<span data-ttu-id="127ea-134">A saída de cliente de depuração WSD de exemplo a seguir mostra uma mensagem de saudação.</span><span class="sxs-lookup"><span data-stu-id="127ea-134">The following sample WSD Debug Client output shows a Hello message.</span></span> <span data-ttu-id="127ea-135">O \<wsa:Action> elemento identifica a mensagem como uma mensagem de saudação.</span><span class="sxs-lookup"><span data-stu-id="127ea-135">The \<wsa:Action> element identifies the message as a Hello message.</span></span>

``` syntax
UDP message at 05/08/07 10:10:49 from soap.udp://[[::1]:49343]
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="h
ttp://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsd="https://schemas.xmlso
ap.org/ws/2005/04/discovery" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/d
evprof"><soap:Header><wsa:To>urn:schemas-xmlsoap-org:ws:2005:04:discovery</wsa:T
o><wsa:Action>https://schemas.xmlsoap.org/ws/2005/04/discovery/Hello</wsa:Action>
<wsa:MessageID>urn:uuid:8999e29a-b056-4345-9e13-f42dbedab28a</wsa:MessageID><wsd
:AppSequence InstanceId="1" SequenceId="urn:uuid:abb0a2a1-6efc-4242-b8e7-c02484a
6eea2" MessageNumber="1"></wsd:AppSequence></soap:Header><soap:Body><wsd:Hello><
wsa:EndpointReference><wsa:Address>urn:uuid:02a76d74-82d0-43e6-ab09-16f54ab81ac6
</wsa:Address></wsa:EndpointReference><wsd:Types>wsdp:Device</wsd:Types><wsd:Met
adataVersion>1</wsd:MetadataVersion></wsd:Hello></soap:Body></soap:Envelope>
```

## <a name="filtering-wsd-debug-client-results"></a><span data-ttu-id="127ea-136">Filtrando resultados do cliente de depuração WSD</span><span class="sxs-lookup"><span data-stu-id="127ea-136">Filtering WSD Debug Client Results</span></span>

<span data-ttu-id="127ea-137">A filtragem dos resultados do cliente de depuração WSD pode ajudar a identificar o tráfego de incidentes que envolve o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="127ea-137">Filtering the WSD Debug Client results can help identify incident traffic involving the device.</span></span> <span data-ttu-id="127ea-138">A filtragem só é necessária em redes com ruídos.</span><span class="sxs-lookup"><span data-stu-id="127ea-138">Filtering is only necessary on noisy networks.</span></span>

<span data-ttu-id="127ea-139">Há duas maneiras de filtrar os resultados.</span><span class="sxs-lookup"><span data-stu-id="127ea-139">There are two ways to filter results.</span></span> <span data-ttu-id="127ea-140">Os endereços IP a serem filtrados podem ser identificados explicitamente ao iniciar o cliente de depuração WSD.</span><span class="sxs-lookup"><span data-stu-id="127ea-140">The IP addresses to filter can be explicitly identified when starting the WSD Debug Client.</span></span> <span data-ttu-id="127ea-141">Como alternativa, os endereços IP podem ser especificados após o cliente ter sido iniciado.</span><span class="sxs-lookup"><span data-stu-id="127ea-141">Alternatively, the IP addresses can be specified after the client has started.</span></span> <span data-ttu-id="127ea-142">Esta seção descreve os dois métodos.</span><span class="sxs-lookup"><span data-stu-id="127ea-142">This section describes both methods.</span></span>

<span data-ttu-id="127ea-143">**Para especificar os endereços IP a serem filtrados ao iniciar o cliente de depuração WSD**</span><span class="sxs-lookup"><span data-stu-id="127ea-143">**To specify IP addresses to filter when starting WSD Debug Client**</span></span>

1.  <span data-ttu-id="127ea-144">Configure o host e o cliente para serem executados na rede (ou seja, certifique-se de que o host e o cliente funcionarão em computadores diferentes).</span><span class="sxs-lookup"><span data-stu-id="127ea-144">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="127ea-145">Colete os endereços IP do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="127ea-145">Collect the IP address(es) of the device.</span></span> <span data-ttu-id="127ea-146">Se o dispositivo tiver vários endereços (por exemplo, ele tem endereços IPv4 e IPv6), todos os endereços deverão ser coletados.</span><span class="sxs-lookup"><span data-stu-id="127ea-146">If the device has multiple addresses (for example, it has both IPv4 and IPv6 addresses) all addresses must be collected.</span></span>
3.  <span data-ttu-id="127ea-147">Abra um prompt de comando e execute o seguinte comando: \**WSDDebug \_client.exe/Mode multicast/IP adicionar\*\*\*<device IP>*</span><span class="sxs-lookup"><span data-stu-id="127ea-147">Open a command prompt and run the following command: **WSDDebug\_client.exe /mode multicast /ip add** *<device IP>*</span></span>

<span data-ttu-id="127ea-148">*<device IP>* é um endereço IP.</span><span class="sxs-lookup"><span data-stu-id="127ea-148">*<device IP>* is an IP address.</span></span> <span data-ttu-id="127ea-149">A lista a seguir mostra alguns formatos de exemplo para esse endereço IP.</span><span class="sxs-lookup"><span data-stu-id="127ea-149">The following list shows some sample formats for this IP address.</span></span>

-   <span data-ttu-id="127ea-150">192.168.0.1</span><span class="sxs-lookup"><span data-stu-id="127ea-150">192.168.0.1</span></span>
-   <span data-ttu-id="127ea-151">:: 1</span><span class="sxs-lookup"><span data-stu-id="127ea-151">::1</span></span>
-   <span data-ttu-id="127ea-152">mydevice.contoso.com</span><span class="sxs-lookup"><span data-stu-id="127ea-152">mydevice.contoso.com</span></span>

<span data-ttu-id="127ea-153">O cliente de depuração WSD resolve automaticamente os nomes de host fornecidos no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="127ea-153">The WSD Debug Client automatically resolves hostnames supplied at the command prompt.</span></span>

<span data-ttu-id="127ea-154">**Para filtrar os resultados após iniciar o cliente de depuração WSD**</span><span class="sxs-lookup"><span data-stu-id="127ea-154">**To filter results after starting WSD Debug Client**</span></span>

1.  <span data-ttu-id="127ea-155">Configure o host e o cliente para serem executados na rede (ou seja, certifique-se de que o host e o cliente funcionarão em computadores diferentes).</span><span class="sxs-lookup"><span data-stu-id="127ea-155">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="127ea-156">Colete os endereços IP do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="127ea-156">Collect the IP address(es) of the device.</span></span> <span data-ttu-id="127ea-157">Se o dispositivo tiver vários endereços (por exemplo, ele tem endereços IPv4 e IPv6), todos os endereços deverão ser coletados.</span><span class="sxs-lookup"><span data-stu-id="127ea-157">If the device has multiple addresses (for example, it has both IPv4 and IPv6 addresses) all addresses must be collected.</span></span>
3.  <span data-ttu-id="127ea-158">Abra um prompt de comando e execute o seguinte comando: **WSDDebug \_client.exe/Mode multicast**</span><span class="sxs-lookup"><span data-stu-id="127ea-158">Open a command prompt and run the following command: **WSDDebug\_client.exe /mode multicast**</span></span>
4.  <span data-ttu-id="127ea-159">No prompt de comando do cliente de depuração WSD, execute o seguinte comando: \**IP Add\*\*\*<device IP>*</span><span class="sxs-lookup"><span data-stu-id="127ea-159">At the WSD Debug Client command prompt, run the following command: **ip add** *<device IP>*</span></span>
5.  <span data-ttu-id="127ea-160">Repita a etapa 4 até que todos os endereços IP do dispositivo tenham sido adicionados.</span><span class="sxs-lookup"><span data-stu-id="127ea-160">Repeat step 4 until all device IP addresses have been added.</span></span>

<span data-ttu-id="127ea-161">O procedimento a seguir pressupõe que o cliente de depuração WSD foi iniciado e a filtragem por endereço IP está ocorrendo.</span><span class="sxs-lookup"><span data-stu-id="127ea-161">The following procedure assumes that the WSD Debug Client has been started and filtering by IP address is occurring.</span></span>

<span data-ttu-id="127ea-162">**Para verificar se os endereços IP corretos estão sendo filtrados**</span><span class="sxs-lookup"><span data-stu-id="127ea-162">**To verify that the correct IP addresses are being filtered**</span></span>

-   <span data-ttu-id="127ea-163">No prompt de comando do cliente de depuração WSD, execute o seguinte comando: **IP Print**</span><span class="sxs-lookup"><span data-stu-id="127ea-163">At the WSD Debug Client command prompt, run the following command: **ip print**</span></span>

    <span data-ttu-id="127ea-164">A lista de endereços IP que estão sendo filtrados é exibida.</span><span class="sxs-lookup"><span data-stu-id="127ea-164">The list of IP addresses being filtered appears.</span></span>

<span data-ttu-id="127ea-165">O procedimento a seguir pressupõe que o cliente de depuração WSD foi iniciado e a filtragem por endereço IP está ocorrendo.</span><span class="sxs-lookup"><span data-stu-id="127ea-165">The following procedure assumes that the WSD Debug Client has been started and filtering by IP address is occurring.</span></span>

<span data-ttu-id="127ea-166">**Para desabilitar a filtragem**</span><span class="sxs-lookup"><span data-stu-id="127ea-166">**To disable filtering**</span></span>

-   <span data-ttu-id="127ea-167">No prompt de comando do cliente de depuração WSD, execute o seguinte comando: **IP Clear**</span><span class="sxs-lookup"><span data-stu-id="127ea-167">At the WSD Debug Client command prompt, run the following command: **ip clear**</span></span>

    <span data-ttu-id="127ea-168">Todo o tráfego de multicast agora será mostrado na saída de depuração.</span><span class="sxs-lookup"><span data-stu-id="127ea-168">All multicast traffic will now be shown in the debug output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="127ea-169">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="127ea-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="127ea-170">Procedimentos de diagnóstico do WSDAPI</span><span class="sxs-lookup"><span data-stu-id="127ea-170">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="127ea-171">Introdução com a solução de problemas de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="127ea-171">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



