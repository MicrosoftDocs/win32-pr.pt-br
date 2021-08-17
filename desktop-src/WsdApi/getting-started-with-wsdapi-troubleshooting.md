---
description: Há duas maneiras de determinar o procedimento de diagnóstico a ser usado.
ms.assetid: d6877063-6cf9-48dc-8208-0f3fc85b6d6b
title: Introdução com a solução de problemas de WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 413146288e6c7fc6e513f994fbe24d6ee9940897f22bcd5a715ae41f77f83c02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738612"
---
# <a name="getting-started-with-wsdapi-troubleshooting"></a>Introdução com a solução de problemas de WSDAPI

Este guia de solução de problemas contém um conjunto de [procedimentos de diagnóstico](wsdapi-diagnostic-procedures.md) que podem ser usados para ajudar a identificar a causa de problemas de aplicativos. Depois que a causa do problema tiver sido identificada com êxito, as soluções sugeridas no procedimento de diagnóstico poderão ser aplicadas para resolver o problema.

Há duas maneiras de determinar o procedimento de diagnóstico a ser usado. Uma delas é ir para a página de solução de problemas do tipo de cliente para exibir uma lista passo a passo de procedimentos de diagnóstico a serem usados para solucionar problemas do cliente. A outra maneira é ir para a referência rápida de solução de problemas abaixo para exibir tabelas de resumo que mostram problemas comuns com aplicativos WSDAPI e os procedimentos a serem usados para diagnosticar os problemas.

## <a name="troubleshooting-by-type-of-client"></a>Solução de problemas por tipo de cliente

Os tópicos a seguir mostram os procedimentos de diagnóstico relevantes por tipo de cliente. Esses tópicos também mostram os padrões de mensagem associados ao tipo de cliente.

-   [Solução de problemas de aplicativos WSDAPI usando a descoberta direcionada](troubleshooting-applications-using-directed-discovery.md)
-   [Solucionando problemas de clientes de descoberta de função](troubleshooting-function-discovery-clients.md)
-   [Solução de problemas de pessoas ao meu redor/reuniões ao meu redor](troubleshooting-people-near-me-meetings-near-me.md)
-   [Solução de problemas do assistente para adicionar impressora](troubleshooting-the-add-printer-wizard.md)
-   [Solucionando problemas do Gerenciador de rede](troubleshooting-the-network-explorer.md)
-   [Solução de problemas do assistente do projetor](troubleshooting-the-projector-wizard.md)
-   [Solução de problemas de outros aplicativos WSDAPI](troubleshooting-wsdapi-applications.md)

## <a name="troubleshooting-quick-reference"></a>Solução de problemas de referência rápida

As tabelas a seguir mostram alguns problemas que podem impedir que clientes e hosts WSDAPI vejam uns aos outros na rede e de trocar os metadados do dispositivo. As tabelas também mostram os procedimentos de diagnóstico a serem executados e os critérios a serem usados para avaliar se o aplicativo sofre de um problema específico.

### <a name="network-environment-problems"></a>Problemas de ambiente de rede



| Problema                                                                                                                                                                                              | Procedimento de diagnóstico                                                                                                                                                                                                                             | Identificação do problema                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| O firewall bloqueia o tráfego de descoberta de rede.                                                                                                                                                       | [inspecionando Configurações de adaptador e Firewall](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | Habilitar a exceção de descoberta de rede no firewall resolve o problema.                                                                                                                      |
| As exceções de firewall específicas ao aplicativo estão bloqueando mensagens.                                                                                                                               | [inspecionando Configurações de adaptador e Firewall](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | A desabilitação do firewall resolve o problema. O WF. msc mostra regras de firewall específicas do aplicativo.                                                                                                      |
| O dispositivo não responde às solicitações UDP enviando uma mensagem [ProbeMatches](probematches-message.md) ou [ResolveMatches](resolvematches-message.md) em tempo hábil (menos de 4 segundos). | [inspecionando Configurações de adaptador e Firewall](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | A desabilitação do firewall resolve o problema e um host genérico que responde em menos de 4 segundos funciona com êxito.                                                                            |
| O contexto de segurança do aplicativo está incorreto (ou seja, o cliente e o host não têm as permissões adequadas na rede).                                                                 | [Usando um host genérico e um cliente para o WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md) ou [usando um host genérico e um cliente para metadados http Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md) | O endereço do dispositivo não é mostrado na saída do cliente de depuração WSD. A execução do aplicativo como administrador resolve o problema.                                                                          |
| Uma política IPSec está bloqueando mensagens.                                                                                                                                                                | [Usando um host genérico e um cliente para o WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md) ou [usando um host genérico e um cliente para metadados http Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md) | O endereço do dispositivo não é mostrado na saída do cliente de depuração WSD. O problema não é resolvido desabilitando o firewall. O problema não pode ser reproduzido em um computador que não esteja sujeito a nenhuma política IPSec. |



 

### <a name="discovery-traffic-problems"></a>Problemas de tráfego de descoberta



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Problema</th>
<th>Procedimento de diagnóstico</th>
<th>Identificação do problema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>As mensagens de <a href="hello-message.md">saudação</a>, <a href="probe-message.md">investigação</a>ou <a href="resolve-message.md">resolução</a> não são transmitidas na rede porque o aplicativo não enumera corretamente as interfaces de rede multicast.</td>
<td><a href="using-wsddebug-client-to-verify-multicast-traffic.md">Usando o cliente de depuração WSD para verificar o tráfego multicast</a></td>
<td>As mensagens Hello, PROBE ou resolve não aparecem na saída do cliente de depuração WSD. Os pacotes não aparecem na rede. Os pacotes não são gerados para a interface de loopback ou para outras interfaces.</td>
</tr>
<tr class="even">
<td>As mensagens de <a href="probe-message.md">investigação</a> não são enviadas pelo multicast UDP para a porta 3702 (para aplicativos que não usam a descoberta direcionada).</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspecionando rastreamentos de rede para o WS-Discovery de UDP</a></td>
<td>A inspeção da mensagem mostra que ela foi enviada para a porta errada.</td>
</tr>
<tr class="odd">
<td>A mensagem de <a href="probe-message.md">investigação</a> não contém um elemento <strong>Types</strong> ou o elemento <strong>Types</strong> está vazio.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspecionando rastreamentos de rede para o WS-Discovery UDP</a> ou <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">inspecionando rastreamentos de rede para aplicativos usando a descoberta direcionada</a></td>
<td>A inspeção da mensagem mostra que o elemento <strong>tipos</strong> não está presente ou vazio.</td>
</tr>
<tr class="even">
<td>O elemento <strong>Types</strong> de uma mensagem de <a href="probe-message.md">investigação</a> não contém os tipos aos quais um host responderá.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspecionando rastreamentos de rede para o WS-Discovery UDP</a> ou <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">inspecionando rastreamentos de rede para aplicativos usando a descoberta direcionada</a></td>
<td>A inspeção da mensagem mostra que o elemento <strong>Types</strong> contém um valor malformado ou incorreto.</td>
</tr>
<tr class="odd">
<td>Uma mensagem <a href="probematches-message.md">ProbeMatches</a> não foi enviada unicast para a porta UDP da qual a <a href="probe-message.md">investigação</a> foi enviada.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspecionando rastreamentos de rede para o WS-Discovery UDP</a> ou <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">inspecionando rastreamentos de rede para aplicativos usando a descoberta direcionada</a></td>
<td>A inspeção da saída mostra que nenhuma mensagem <a href="probematches-message.md">ProbeMatches</a>) foi enviada ou que a mensagem foi enviada para a porta errada.
<blockquote>
[!Note]<br />
Para aplicativos que usam a descoberta direcionada, o <a href="probematches-message.md">ProbeMatches</a> deve ser enviado por http ou HTTPS em resposta à mensagem de <a href="probe-message.md">investigação</a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>A mensagem <a href="probematches-message.md">ProbeMatches</a> não contém um elemento <strong>RelatesTo</strong> , ou o elemento <strong>RelatesTo</strong> está vazio.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspecionando rastreamentos de rede para o WS-Discovery UDP</a> ou <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">inspecionando rastreamentos de rede para aplicativos usando a descoberta direcionada</a></td>
<td>A inspeção da mensagem mostra que o elemento <strong>RelatesTo</strong> não está presente ou vazio.</td>
</tr>
<tr class="odd">
<td>O valor do elemento <strong>RelatesTo</strong> em uma mensagem <a href="probematches-message.md">ProbeMatches</a> não corresponde ao valor do elemento <strong>MessageId</strong> da mensagem de <a href="probe-message.md">investigação</a> correspondente.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspecionando rastreamentos de rede para o WS-Discovery UDP</a> ou <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">inspecionando rastreamentos de rede para aplicativos usando a descoberta direcionada</a></td>
<td>A inspeção da mensagem mostra que o elemento <strong>RelatesTo</strong> contém um valor malformado ou incorreto.</td>
</tr>
<tr class="even">
<td>O elemento <strong>XAddrs</strong> incluído em uma mensagem <a href="probematches-message.md">ProbeMatches</a> não está de acordo com as <a href="xaddr-validation-rules.md">regras de validação XAddr</a>.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspecionando rastreamentos de rede para o WS-Discovery UDP</a> ou <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">inspecionando rastreamentos de rede para aplicativos usando a descoberta direcionada</a></td>
<td>A inspeção da mensagem mostra que os <strong>XAddrs</strong> são inválidos.</td>
</tr>
<tr class="odd">
<td>As mensagens de <a href="resolve-message.md">resolução</a> não são enviadas pelo multicast UDP para a porta 3702 (para aplicativos que não usam a descoberta direcionada).</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspecionando rastreamentos de rede para o WS-Discovery UDP</a> ou <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">inspecionando rastreamentos de rede para aplicativos usando a descoberta direcionada</a></td>
<td>A inspeção da saída mostra que a mensagem de <a href="resolve-message.md">resolução</a> foi enviada para a porta incorreta.</td>
</tr>
<tr class="even">
<td>Uma mensagem <a href="resolvematches-message.md">ResolveMatches</a> não foi enviada unicast para a porta UDP da qual uma mensagem de <a href="resolve-message.md">resolução</a> foi enviada.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspecionando rastreamentos de rede para o WS-Discovery UDP</a> ou <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">inspecionando rastreamentos de rede para aplicativos usando a descoberta direcionada</a></td>
<td>A inspeção da saída mostra que nenhuma mensagem <a href="resolvematches-message.md">ResolveMatches</a> foi enviada ou que a mensagem foi enviada para a porta errada.</td>
</tr>
</tbody>
</table>



 

### <a name="metadata-exchange-problems"></a>Problemas de troca de metadados



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Problema</th>
<th>Procedimento de diagnóstico</th>
<th>Identificação do problema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>O endereço de transporte anunciado pelo host está incorreto.</td>
<td><a href="using-a-generic-host-and-client-for-http-metadata-exchange.md">Usando um host genérico e um cliente para metadados HTTP Exchange</a></td>
<td>A inspeção do XAddrs na saída do cliente de depuração WSD mostra que o endereço de transporte está incorreto ou malformado.</td>
</tr>
<tr class="even">
<td>Não foi possível estabelecer uma conexão TCP para a troca de metadados.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspecionando rastreamentos de rede para metadados HTTP Exchange</a></td>
<td>A saída do analisador de pacotes não mostra a seguinte troca de pacotes:
<ul>
<li>Um pacote TCP SYN enviado do cliente</li>
<li>Um pacote TCP SYN/ACK enviado do host</li>
<li>Um pacote TCP ACK enviado do cliente</li>
</ul></td>
</tr>
<tr class="odd">
<td>O cliente não enviou uma solicitação HTTP GET válida.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspecionando rastreamentos de rede para metadados HTTP Exchange</a></td>
<td>Não há uma solicitação HTTP GET na saída do analisador de pacotes ou a solicitação está malformada.</td>
</tr>
<tr class="even">
<td>O cliente não enviou uma mensagem de <a href="get--metadata-exchange--http-request-and-message.md">obtenção</a> de WS-Transfer válida.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspecionando rastreamentos de rede para metadados HTTP Exchange</a></td>
<td>Não há nenhuma WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">obter</a> mensagem na saída do analisador de pacotes ou a mensagem está malformada.</td>
</tr>
<tr class="odd">
<td>O host não está escutando no caminho da URL especificado na solicitação HTTP GET.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspecionando rastreamentos de rede para metadados HTTP Exchange</a></td>
<td>Não há resposta HTTP na saída do analisador de pacotes.</td>
</tr>
<tr class="even">
<td>A WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">mensagem Get</a> não contém um <strong>elemento To</strong> ou o elemento <strong>To</strong> está vazio.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspecionando rastreamentos de rede para metadados HTTP Exchange</a></td>
<td>A inspeção da mensagem mostra que <strong>o elemento To</strong> não está presente ou vazio.</td>
</tr>
<tr class="odd">
<td>O valor do elemento <strong>To</strong> de uma WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Obter</a> mensagem não corresponderá a um dos endereços de ponto de extremidade do host.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspecionando rastreamentos de rede para metadados HTTP Exchange</a></td>
<td>A inspeção da mensagem mostra que o valor do elemento <strong>To</strong> não corresponderá a um dos endereços de ponto de extremidade anunciados na mensagem <a href="probematches-message.md">ProbeMatches</a> ou <a href="resolvematches-message.md">ResolveMatches</a> do host.</td>
</tr>
<tr class="even">
<td>O host não enviou um cabeçalho de resposta HTTP válido.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspecionando rastreamentos de rede para metadados HTTP Exchange</a></td>
<td>Não há resposta HTTP na saída do analisador de pacotes ou a solicitação está malformada.</td>
</tr>
<tr class="odd">
<td>O cabeçalho de resposta HTTP enviado pelo host indica que a solicitação não pode ser concluída.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspecionando rastreamentos de rede para metadados HTTP Exchange</a></td>
<td>O cabeçalho de resposta tem um código de status diferente de HTTP/1.1 200.</td>
</tr>
<tr class="even">
<td>O host não enviou uma mensagem <a href="getresponse--metadata-exchange--message.md">GetResponse</a> válida.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspecionando rastreamentos de rede para metadados HTTP Exchange</a></td>
<td>Não há nenhuma <a href="getresponse--metadata-exchange--message.md">mensagem GetResponse</a> na saída do analisador de pacotes ou a mensagem está malformada.</td>
</tr>
<tr class="odd">
<td>A <a href="getresponse--metadata-exchange--message.md">mensagem GetResponse</a> não contém um <strong>elemento RelatesTo</strong> ou o elemento <strong>RelatesTo</strong> está vazio.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspecionando rastreamentos de rede para metadados HTTP Exchange</a></td>
<td>A inspeção da mensagem mostra que o <strong>elemento RelatesTo</strong> não está presente ou vazio.</td>
</tr>
<tr class="even">
<td>O valor do <strong>elemento RelatesTo</strong> em uma mensagem <a href="getresponse--metadata-exchange--message.md">GetResponse</a> não corresponde ao valor do <strong>elemento MessageId</strong> da mensagem <a href="get--metadata-exchange--http-request-and-message.md">Get</a> correspondente.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspecionando rastreamentos de rede para metadados HTTP Exchange</a></td>
<td>A inspeção da mensagem mostra que o <strong>elemento RelatesTo</strong> contém um valor incorreto ou malformado.</td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de solução de problemas do WSDAPI](wsdapi-troubleshooting-guide.md)
</dt> </dl>
