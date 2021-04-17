---
description: Uma WS-Discovery mensagem usada para anunciar a presença de um dispositivo ou serviço na rede.
ms.assetid: a7402e02-9bdc-49ec-ba93-8a32f55b9dd8
title: Mensagem de saudação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6504f25d360de055d7c0715266472e212540a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787763"
---
# <a name="hello-message"></a>Mensagem de saudação

Uma mensagem de saudação é uma WS-Discovery mensagem usada para anunciar a presença de um dispositivo ou serviço na rede. As mensagens de saudação também são enviadas em outros cenários. Para obter mais informações sobre mensagens de saudação, consulte a seção 4,1 da [especificação do WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Uma mensagem de saudação é enviada por multicast UDP para a porta 3702. Esta mensagem não é solicitada.

> [!Note]  
> Este tópico mostra uma mensagem DPWS de exemplo gerada por clientes e hosts WSDAPI. O WSDAPI analisará e aceitará outras mensagens em conformidade com o DPWS que não estão em conformidade com este exemplo. Não use este exemplo para verificar a interoperabilidade do DPWS; em vez disso, use a [ferramenta de interoperabilidade básica do WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

A mensagem SOAP a seguir mostra uma mensagem de saudação de exemplo.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery"
    xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof">
<soap:Header>
    <wsa:To>
        urn:schemas-xmlsoap-org:ws:2005:04:discovery
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Hello
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:0f5d604c-81ac-4abc-8010-51dbffad55f2
    </wsa:MessageID>
    <wsd:AppSequence InstanceId="2"
        SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
        MessageNumber="14">
    </wsd:AppSequence>
</soap:Header>
<soap:Body>
    <wsd:Hello>
        <wsa:EndpointReference>
            <wsa:Address>
                urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsa:Address>
        </wsa:EndpointReference>
        <wsd:Types>wsdp:Device</wsd:Types>
        <wsd:MetadataVersion>2</wsd:MetadataVersion>
    </wsd:Hello>
</soap:Body>
```

Uma mensagem de saudação tem os seguintes pontos de foco.



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
<td>Olá</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Hello
</wsa:Action></code></pre></td>
<td>A ação de saudação SOAP identifica a mensagem como uma mensagem de saudação.</td>
</tr>
<tr class="even">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;2&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;14&quot;>
</wsd:AppSequence></code></pre></td>
<td>Contém informações de sequenciamento de aplicativo, o que ajuda a manter a sequência de mensagens, mesmo que elas sejam recebidas fora de ordem. O AppSequence é validado conforme descrito em <a href="appsequence-validation-rules.md">regras de validação do AppSequence</a>.</td>
</tr>
<tr class="odd">
<td>Endereço</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Contém o endereço do ponto de extremidade. Esse endereçado pode ser referenciado em uma mensagem de <a href="resolve-message.md">resolução</a> .</td>
</tr>
<tr class="even">
<td>Tipos</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:Types>wsdp:Device</wsd:Types></code></pre></td>
<td>Contém os tipos de WS-Discovery anunciados pelo host.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Descoberta e mensagens de troca de metadados](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Adeus mensagem](bye-message.md)
</dt> </dl>

 

 



