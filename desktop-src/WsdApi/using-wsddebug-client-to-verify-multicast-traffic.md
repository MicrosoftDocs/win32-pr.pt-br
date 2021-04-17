---
description: Se o host genérico e o cliente puderem ver uns aos outros na rede, mas o host e o cliente reais não puderem, é provável que o problema esteja nas mensagens enviadas entre os pontos de extremidade pela rede.
ms.assetid: 1b0943fb-076e-4feb-9a4f-36a06bdd19ae
title: Usando o cliente de depuração WSD para verificar o tráfego multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55f03e06baefc40bad843a5193b2cec604383251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790236"
---
# <a name="using-wsd-debug-client-to-verify-multicast-traffic"></a>Usando o cliente de depuração WSD para verificar o tráfego multicast

Se o host genérico e o cliente puderem ver uns aos outros na rede, mas o host e o cliente reais não puderem, é provável que o problema esteja nas mensagens enviadas entre os pontos de extremidade pela rede. Para obter mais informações sobre o host e o cliente genérico, consulte [usando um host genérico e um cliente para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md). Como os rastreamentos de rede completos podem ser difíceis de coletar, filtrar e ler, a ferramenta de cliente de depuração WSD pode ser usada para imprimir os lados de multicast das mensagens de WS-Discovery.

O cliente de depuração WSD no modo multicast só pode inspecionar metade das mensagens, pois o cliente não pode imprimir mensagens unicast. Se o tráfego unicast for de interesse, pule diretamente para [inspecionar rastreamentos de rede para o WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md).

Este procedimento mostra um método que exibirá todo o tráfego de multicast na rede. Para exibir somente o tráfego multicast de e para o dispositivo, consulte a seção [filtrando resultados do cliente de depuração WSD](#filtering-wsd-debug-client-results) abaixo.

**Para usar o cliente de depuração WSD para verificar o tráfego multicast**

1.  Configure o host e o cliente para serem executados na rede (ou seja, certifique-se de que o host e o cliente funcionarão em computadores diferentes).
2.  Abra um prompt de comando e execute o seguinte comando: **WSDDebug \_client.exe/Mode multicast**
3.  Reproduza a falha iniciando o host e o cliente ou pressionando F5 no Gerenciador de rede.
4.  Verifique se as mensagens estão sendo multicast.

Se as mensagens necessárias forem exibidas na saída do cliente de depuração WSD, a falha do aplicativo poderá estar no conteúdo da mensagem de multicast ou na existência ou no conteúdo das mensagens de resposta unicast correspondentes. Continue a solução de problemas seguindo as instruções em [inspecionar rastreamentos de rede para o WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md).

Se as mensagens necessárias forem exibidas na saída do cliente de depuração WSD, é provável que a origem do problema do aplicativo tenha sido identificada. É provável que o tráfego multicast não esteja sendo transmitido na rede. Essa falha pode ocorrer quando o aplicativo não enumera os adaptadores multicast corretamente. Os aplicativos devem enviar explicitamente o tráfego multicast em todas as interfaces de rede; caso contrário, os pacotes podem não ser gerados para a interface de loopback ou para outras interfaces. Para verificar se os pacotes não aparecem na rede, siga as instruções em [inspecionando os rastreamentos de rede para a descoberta de WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md) e procure evidências de mensagens de multicast ausentes.

## <a name="verifying-that-messages-are-being-multicast"></a>Verificando se as mensagens estão sendo multicast

Sempre verifique se as mensagens de [investigação](probe-message.md) estão sendo multicast. Opcionalmente, verifique se as mensagens de [saudação](hello-message.md) e de [resolução](resolve-message.md) estão sendo multicast. Observe que nem todos os aplicativos usam as mensagens de resolução. Para obter mais informações sobre os padrões de mensagem usados por clientes e hosts, consulte [padrões de mensagens de descoberta e de metadados do Exchange](discovery-and-metadata-exchange-message-patterns.md) e [introdução com a solução de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md).

As mensagens devem ser disparadas para serem enviadas conforme descrito na etapa 3 acima. O cliente de depuração WSD exibe a mensagem SOAP bruta como saída. Como todas as mensagens impressas pelo cliente de depuração WSD no modo multicast são recebidas por um soquete de multicast, o endereço de destino da mensagem não é exibido.

O exemplo de saída de cliente de depuração WSD a seguir mostra uma mensagem de investigação. O elemento <WSA: Action> identifica a mensagem como uma mensagem de investigação. Inspecione o campo <WSA: Action> para verificar se a mensagem recebida era uma mensagem de investigação.

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

A saída de cliente de depuração WSD de exemplo a seguir mostra uma mensagem de saudação. O elemento <WSA: Action> identifica a mensagem como uma mensagem de saudação.

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

## <a name="filtering-wsd-debug-client-results"></a>Filtrando resultados do cliente de depuração WSD

A filtragem dos resultados do cliente de depuração WSD pode ajudar a identificar o tráfego de incidentes que envolve o dispositivo. A filtragem só é necessária em redes com ruídos.

Há duas maneiras de filtrar os resultados. Os endereços IP a serem filtrados podem ser identificados explicitamente ao iniciar o cliente de depuração WSD. Como alternativa, os endereços IP podem ser especificados após o cliente ter sido iniciado. Esta seção descreve os dois métodos.

**Para especificar os endereços IP a serem filtrados ao iniciar o cliente de depuração WSD**

1.  Configure o host e o cliente para serem executados na rede (ou seja, certifique-se de que o host e o cliente funcionarão em computadores diferentes).
2.  Colete os endereços IP do dispositivo. Se o dispositivo tiver vários endereços (por exemplo, ele tem endereços IPv4 e IPv6), todos os endereços deverão ser coletados.
3.  Abra um prompt de comando e execute o seguinte comando: **WSDDebug \_client.exe/Mode multicast/IP adicionar***<device IP>*

*<device IP>* é um endereço IP. A lista a seguir mostra alguns formatos de exemplo para esse endereço IP.

-   192.168.0.1
-   :: 1
-   mydevice.contoso.com

O cliente de depuração WSD resolve automaticamente os nomes de host fornecidos no prompt de comando.

**Para filtrar os resultados após iniciar o cliente de depuração WSD**

1.  Configure o host e o cliente para serem executados na rede (ou seja, certifique-se de que o host e o cliente funcionarão em computadores diferentes).
2.  Colete os endereços IP do dispositivo. Se o dispositivo tiver vários endereços (por exemplo, ele tem endereços IPv4 e IPv6), todos os endereços deverão ser coletados.
3.  Abra um prompt de comando e execute o seguinte comando: **WSDDebug \_client.exe/Mode multicast**
4.  No prompt de comando do cliente de depuração WSD, execute o seguinte comando: **IP Add***<device IP>*
5.  Repita a etapa 4 até que todos os endereços IP do dispositivo tenham sido adicionados.

O procedimento a seguir pressupõe que o cliente de depuração WSD foi iniciado e a filtragem por endereço IP está ocorrendo.

**Para verificar se os endereços IP corretos estão sendo filtrados**

-   No prompt de comando do cliente de depuração WSD, execute o seguinte comando: **IP Print**

    A lista de endereços IP que estão sendo filtrados é exibida.

O procedimento a seguir pressupõe que o cliente de depuração WSD foi iniciado e a filtragem por endereço IP está ocorrendo.

**Para desabilitar a filtragem**

-   No prompt de comando do cliente de depuração WSD, execute o seguinte comando: **IP Clear**

    Todo o tráfego de multicast agora será mostrado na saída de depuração.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Procedimentos de diagnóstico do WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Introdução com a solução de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



