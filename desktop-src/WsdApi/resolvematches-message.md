---
description: Uma WS-Discovery mensagem enviada em resposta a um cliente resolve a mensagem por um serviço correspondente.
ms.assetid: 0eaa4348-968e-4b45-9509-8b15476edaa1
title: Mensagem ResolveMatches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1daffe985f3956e57ad69fd7c4fc4d199f0b24bd5fdab5677b7ef83765e5fcdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756796"
---
# <a name="resolvematches-message"></a>Mensagem ResolveMatches

Uma mensagem ResolveMatches é uma mensagem WS-Discovery enviada em resposta a uma mensagem de [resolução](resolve-message.md) de um cliente por um serviço correspondente. Para obter mais informações sobre mensagens ResolveMatches, consulte a seção 6,2 da [especificação do WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Uma mensagem ResolveMatches é enviada por UDP unicast para a porta 3702 (a porta da qual a mensagem de [resolução](resolve-message.md) do cliente foi enviada). ResolveMatches deve ser enviado dentro de 4 segundos da mensagem de resolução; caso contrário, Windows Firewall pode descartar o pacote.

Qualquer aplicativo DPWS que envie mensagens de [resolução](resolve-message.md) receberá mensagens ResolveMatches.

> [!Note]  
> Este tópico mostra uma mensagem DPWS de exemplo gerada por clientes e hosts WSDAPI. O WSDAPI analisará e aceitará outras mensagens em conformidade com o DPWS que não estão em conformidade com este exemplo. Não use este exemplo para verificar a interoperabilidade do DPWS; em vez disso, use a [ferramenta de interoperabilidade básica do WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

A mensagem SOAP a seguir mostra um exemplo de mensagem ResolveMatches.

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
        https://schemas.xmlsoap.org/ws/2005/04/discovery/ResolveMatches
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:64ddd01c-b0d6-4afd-aba6-6f1f161ce9d4
    </wsa:MessageID>
    <wsa:RelatesTo>
        urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
    </wsa:RelatesTo>
    <wsd:AppSequence InstanceId="1"
        SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
        MessageNumber="6">
    </wsd:AppSequence>
</soap:Header>
<soap:Body>
    <wsd:ResolveMatches>
        <wsd:ResolveMatch>
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
        </wsd:ResolveMatch>
    </wsd:ResolveMatches>
</soap:Body>
</soap:Envelope>
```

Uma mensagem ResolveMatches tem os seguintes pontos de foco.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
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
<td>ResolveMatches</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/ResolveMatches
</wsa:Action></code></pre></td>
<td>A ação SOAP ResolveMatches identifica a mensagem como uma mensagem ResolveMatches.</td>
</tr>
<tr class="even">
<td>RelatesTo</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:RelatesTo>
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
</wsa:RelatesTo></code></pre></td>
<td>O identificador da mensagem à qual o serviço está respondendo. Esse cabeçalho corresponde a MessageId na mensagem de <a href="resolve-message.md">resolução</a> .</td>
</tr>
<tr class="odd">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;1&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;6&quot;>
</wsd:AppSequence></code></pre></td>
<td>Contém informações de sequenciamento de aplicativo, o que ajuda a manter a sequência de mensagens, mesmo que elas sejam recebidas fora de ordem. O AppSequence é validado conforme descrito em <a href="appsequence-validation-rules.md">regras de validação do AppSequence</a>.</td>
</tr>
<tr class="even">
<td>Endereço</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Contém o endereço do ponto de extremidade que está sendo resolvido.</td>
</tr>
<tr class="odd">
<td>XAddrs</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs></code></pre></td>
<td>XAddrs são endereços de transporte que podem ser usados para comunicação entre o cliente e o serviço. Os endereço são validados conforme descrito em <a href="xaddr-validation-rules.md">regras de validação do XAddr</a>.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[descoberta e metadados Exchange mensagens](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Resolver mensagem](resolve-message.md)
</dt> </dl>

 

 



