---
description: Uma WS-Discovery usada por um cliente para pesquisar serviços na rede por tipo de serviço.
ms.assetid: a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7
title: Mensagem de investigação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abaf4b397abec699dd0a116fe5cddd97578543f917a7994287f5000e17079def
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130628"
---
# <a name="probe-message"></a>Mensagem de investigação

Uma mensagem probe é uma WS-Discovery usada por um cliente para pesquisar serviços na rede por tipo de serviço. Para obter mais informações sobre mensagens de investigação, consulte a seção 5.2 da [Especificação WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Uma mensagem probe é enviada pelo multicast UDP para a porta 3702. Não há suporte para mensagens de investigação unicast.

Os clientes DPWS enviam mensagens de investigação. A lista a seguir mostra cenários em que o WSDAPI enviará uma mensagem de investigação.

-   Os clientes de Descoberta de Funções enviam mensagens de investigação.
-   Os clientes WSDAPI que [**chamam IWSDiscoveryProvider::SearchByAddress**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyaddress) enviam mensagens de investigação.
-   Os clientes WSDAPI que [**chamam IWSDiscoveryProvider::SearchByType**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype) enviam mensagens de investigação.
-   Os aplicativos que usam a descoberta direcionada enviam mensagens de investigação por HTTP ou HTTPS.

> [!Note]  
> Este tópico mostra uma mensagem DPWS de exemplo gerada por clientes e hosts WSDAPI. O WSDAPI analisará e aceitará outras mensagens compatíveis com DPWS que não estão em conformidade com este exemplo. Não use este exemplo para verificar a interoperabilidade do DPWS; use a [WSDBIT (Ferramenta de Interoperabilidade Básica) do WSDAPI.](https://msdn.microsoft.com/library/cc264250.aspx)

 

A mensagem SOAP a seguir mostra uma mensagem de investigação de exemplo.

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

Uma mensagem De investigação tem os seguintes pontos de foco.



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
<td>Contém o identificador de mensagem, que é referenciado pelo elemento RelatesTo em uma <a href="probematches-message.md">mensagem ProbeMatches.</a></td>
</tr>
<tr class="odd">
<td>Tipos</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:Types>wsdp:Device</wsd:Types></code></pre></td>
<td>Contém os WS-Discovery para os quais o cliente está pesquisando. Esse elemento não deve estar vazio.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mensagens de descoberta e Exchange metadados](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Mensagem ProbeMatches](probematches-message.md)
</dt> </dl>

 

 



