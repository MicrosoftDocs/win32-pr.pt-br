---
description: Uma WS-Discovery usada para anunciar a partida de um dispositivo ou serviço da rede.
ms.assetid: 7b9abfcc-28ab-4f29-af69-6dc68e3f51b6
title: Mensagem de adeus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d571e8633690f1a2fee5f6f9c09e1379a7a465
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622472"
---
# <a name="bye-message"></a>Mensagem de adeus

Uma mensagem de WS-Discovery é uma mensagem WS-Discovery usada para anunciar a partida de um dispositivo ou serviço da rede. Para obter mais informações sobre mensagens Bye, consulte a seção 4.2 da [Especificação WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

As mensagens de adeus não são solicitadas. As mensagens são opcionais.

> [!Note]  
> Este tópico mostra uma mensagem DPWS de exemplo gerada por clientes e hosts WSDAPI. O WSDAPI analisará e aceitará outras mensagens compatíveis com DPWS que não estão em conformidade com este exemplo. Não use este exemplo para verificar a interoperabilidade do DPWS; use a [WSDBIT (Ferramenta de Interoperabilidade Básica) do WSDAPI.](https://msdn.microsoft.com/library/cc264250.aspx)

 

A mensagem SOAP a seguir mostra um exemplo de mensagem de Bye.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery">
<soap:Header>
    <wsa:To>
        urn:schemas-xmlsoap-org:ws:2005:04:discovery
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Bye
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:193ccfa0-347d-41a1-9285-f500b6b96a15
    </wsa:MessageID>
    <wsd:AppSequence InstanceId="2"
        SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
        MessageNumber="21">
    </wsd:AppSequence>
</soap:Header>
<soap:Body>
    <wsd:Bye>
        <wsa:EndpointReference>
            <wsa:Address>
                urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsa:Address>
        </wsa:EndpointReference>
    </wsd:Bye>
</soap:Body>
```

Uma mensagem de Bye tem os seguintes pontos de foco.



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
<td>Tchau</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Bye
</wsa:Action></code></pre></td>
<td>A ação Soap de Adeus identifica a mensagem como uma mensagem de Bye.</td>
</tr>
<tr class="even">
<td>Appsequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;2&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;21&quot;>
</wsd:AppSequence></code></pre></td>
<td>Contém informações de sequenciamento de aplicativos, o que ajuda a manter a sequência de mensagens, mesmo que elas sejam recebidas fora de ordem. O AppSequence é validado conforme descrito em Regras de validação do <a href="appsequence-validation-rules.md">AppSequence.</a></td>
</tr>
<tr class="odd">
<td>Endereço</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Contém o endereço do ponto de extremidade que está offline.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mensagens de descoberta e Exchange metadados](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Mensagem olá](hello-message.md)
</dt> </dl>

 

 



