---
description: Uma WS-Discovery enviada por um serviço em resposta a uma mensagem de investigação de clientes.
ms.assetid: 58d3d016-ae29-4090-9b88-e1125db59c95
title: Mensagem ProbeMatches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa395557aac7c67a82163066cf1bfbb854348e1c
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627862"
---
# <a name="probematches-message"></a>Mensagem ProbeMatches

Uma mensagem ProbeMatches é uma WS-Discovery enviada por um serviço em resposta à mensagem [Probe de um](probe-message.md) cliente. Para obter mais informações sobre mensagens ProbeMatches, consulte a seção 5.3 da [Especificação WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Uma mensagem ProbeMatches é enviada pelo unicast UDP para a porta da qual a mensagem [Probe](probe-message.md) do cliente foi enviada. ProbeMatches deve ser enviado dentro de 4 segundos da mensagem Probe; caso contrário, Windows Firewall poderá soltar o pacote.

Se nenhum XAddrs estiver incluído na mensagem ProbeMatches, o cliente poderá enviar uma mensagem Resolver por multicast UDP para [a](resolve-message.md) porta 3702. O cliente só enviará uma mensagem Resolver quando [](get--metadata-exchange--http-request-and-message.md) uma mensagem HTTP (como uma solicitação obter troca de metadados ou uma mensagem de serviço) for enviada.

Qualquer aplicativo DPWS que envia [mensagens probe](probe-message.md) receberá mensagens ProbeMatches.

> [!Note]  
> Este tópico mostra uma mensagem DPWS de exemplo gerada por clientes e hosts WSDAPI. O WSDAPI analisará e aceitará outras mensagens compatíveis com DPWS que não estão em conformidade com este exemplo. Não use este exemplo para verificar a interoperabilidade do DPWS; use a [WSDBIT (Ferramenta de Interoperabilidade Básica) do WSDAPI.](https://msdn.microsoft.com/library/cc264250.aspx)

 

A mensagem SOAP a seguir mostra uma mensagem ProbeMatches de exemplo.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery"
    xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof">
<soap:Header>
    <wsa:To>
        https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/ProbeMatches
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:967d0036-fe69-40ad-8191-dd1fc8ef64ab
    </wsa:MessageID>
    <wsa:RelatesTo>
        urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
    </wsa:RelatesTo>
    <wsd:AppSequence InstanceId="1"
        SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
        MessageNumber="9">
    </wsd:AppSequence>
</soap:Header>
<soap:Body>
    <wsd:ProbeMatches>
        <wsd:ProbeMatch>
            <wsa:EndpointReference>
                <wsa:Address>
                    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
                </wsa:Address>
            </wsa:EndpointReference>
            <wsd:Types>wsdp:Device</wsd:Types>
            <wsd:XAddrs>
                https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsd:XAddrs>
            <wsd:MetadataVersion>2</wsd:MetadataVersion>
        </wsd:ProbeMatch>
    </wsd:ProbeMatches>
</soap:Body>
</soap:Envelope>
```

Uma mensagem ProbeMatches tem os seguintes pontos de foco.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Ponto de foco</th>
<th>XML</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Probematches</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/ProbeMatches
</wsa:Action></code></pre></td>
<td>A ação SOAP ProbeMatches identifica a mensagem como uma mensagem ProbeMatches.</td>
</tr>
<tr class="even">
<td>RelatesTo</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:RelatesTo>
    urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
</wsa:RelatesTo></code></pre></td>
<td>O identificador da mensagem à qual o serviço está respondendo. Esse header corresponde à MessageId na <a href="probe-message.md">mensagem Probe.</a></td>
</tr>
<tr class="odd">
<td>Appsequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;1&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;9&quot;>
</wsd:AppSequence></code></pre></td>
<td>Contém informações de sequenciamento de aplicativos, o que ajuda a manter a sequência de mensagens, mesmo que elas sejam recebidas fora de ordem. O AppSequence é validado conforme descrito em Regras de validação do <a href="appsequence-validation-rules.md">AppSequence.</a></td>
</tr>
<tr class="even">
<td>Endereço</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Contém o endereço do ponto de extremidade. Esse endereçado pode ser referenciado em uma <a href="resolve-message.md">mensagem Resolver.</a></td>
</tr>
<tr class="odd">
<td>XAddrs</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs></code></pre></td>
<td>XAddrs são endereços de transporte que podem ser usados para comunicação entre cliente e serviço. Os complementos são validados conforme descrito em <a href="xaddr-validation-rules.md">Regras de Validação XAddr.</a></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mensagens de descoberta e Exchange metadados](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Mensagem de investigação](probe-message.md)
</dt> </dl>

 

 



