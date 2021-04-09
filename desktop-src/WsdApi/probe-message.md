---
description: Uma WS-Discovery mensagem usada por um cliente para procurar serviços na rede por tipo de serviço.
ms.assetid: a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7
title: Mensagem de investigação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913c163be8d82297a642b1a97a7d28e0c403ca08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091364"
---
# <a name="probe-message"></a>Mensagem de investigação

Uma mensagem de investigação é uma WS-Discovery mensagem usada por um cliente para procurar serviços na rede por tipo de serviço. Para obter mais informações sobre mensagens de investigação, consulte a seção 5,2 da [especificação do WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Uma mensagem de investigação é enviada por multicast UDP para a porta 3702. Não há suporte para mensagens de investigação de unicast.

Os clientes do DPWS enviam mensagens de investigação. A lista a seguir mostra cenários em que o WSDAPI enviará uma mensagem de investigação.

-   Os clientes de descoberta de função enviam mensagens de investigação.
-   Clientes WSDAPI que chamam [**IWSDiscoveryProvider:: SearchByAddress**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyaddress) enviam mensagens de investigação.
-   Clientes WSDAPI que chamam [**IWSDiscoveryProvider:: SearchByType**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype) enviam mensagens de investigação.
-   Os aplicativos que usam a descoberta direcionada enviam mensagens de investigação por HTTP ou HTTPS.

> [!Note]  
> Este tópico mostra uma mensagem DPWS de exemplo gerada por clientes e hosts WSDAPI. O WSDAPI analisará e aceitará outras mensagens em conformidade com o DPWS que não estão em conformidade com este exemplo. Não use este exemplo para verificar a interoperabilidade do DPWS; em vez disso, use a [ferramenta de interoperabilidade básica do WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

A mensagem SOAP a seguir mostra um exemplo de mensagem de investigação.

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
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
    </wsa:MessageID>
</soap:Header>
<soap:Body>
    <wsd:Probe>
        <wsd:Types>wsdp:Device</wsd:Types>
    </wsd:Probe>
</soap:Body>
```

Uma mensagem de investigação tem os seguintes pontos de foco.



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
<td>Investigação</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe
</wsa:Action></code></pre></td>
<td>A ação SOAP de investigação identifica a mensagem como uma mensagem de investigação.</td>
</tr>
<tr class="even">
<td>MessageID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
</wsa:MessageID></code></pre></td>
<td>Contém o identificador da mensagem, que é referenciado pelo elemento RelatesTo em uma mensagem <a href="probematches-message.md">ProbeMatches</a> .</td>
</tr>
<tr class="odd">
<td>Tipos</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:Types>wsdp:Device</wsd:Types></code></pre></td>
<td>Contém os tipos de WS-Discovery para os quais o cliente está pesquisando. Este elemento não deve ficar vazio.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Descoberta e mensagens de troca de metadados](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Mensagem ProbeMatches](probematches-message.md)
</dt> </dl>

 

 



