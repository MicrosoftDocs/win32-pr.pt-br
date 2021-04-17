---
description: Uma WS-Discovery mensagem usada por um cliente para procurar serviços na rede por nome.
ms.assetid: b963bd2a-47cb-4f8d-8272-a586e6d6a047
title: Resolver mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3390d97aad972f001b98587c6b5e7cd7ac708b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780278"
---
# <a name="resolve-message"></a>Resolver mensagem

Uma mensagem de resolução é uma WS-Discovery mensagem usada por um cliente para procurar serviços na rede por nome. Um cliente só enviará uma mensagem de resolução quando uma mensagem HTTP (como uma solicitação de troca de metadados [Get](get--metadata-exchange--http-request-and-message.md) ou uma mensagem de serviço) for enviada. Para obter mais informações sobre como resolver mensagens, consulte a seção 6,1 da [especificação do WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Uma mensagem de resolução é enviada pelo multicast UDP para a porta 3702. Não há suporte para mensagens de resolução de unicast.

Os clientes do DPWS enviam mensagens de resolução. A lista a seguir mostra cenários em que o WSDAPI enviará uma mensagem de resolução.

-   Um cliente de descoberta de função envia uma mensagem de resolução se nenhum XAddrs estiver incluído em uma mensagem [ProbeMatches](probematches-message.md) .
-   Um cliente que chama os métodos [**IWSDiscoveryProvider:: SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid) enviará uma mensagem de resolução.
-   Um cliente que chama [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) pode enviar uma mensagem de resolução se um endereço de dispositivo lógico for passado para *pszDeviceId*.
-   Um cliente que chama [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) enviará uma mensagem de resolução se a função for chamada com o parâmetro pDeviceAddress definido como **NULL**.

> [!Note]  
> Este tópico mostra uma mensagem DPWS de exemplo gerada por clientes e hosts WSDAPI. O WSDAPI analisará e aceitará outras mensagens em conformidade com o DPWS que não estão em conformidade com este exemplo. Não use este exemplo para verificar a interoperabilidade do DPWS; em vez disso, use a [ferramenta de interoperabilidade básica do WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

A mensagem SOAP a seguir mostra uma mensagem de resolução de exemplo.

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
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Resolve
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
    </wsa:MessageID>
</soap:Header>
<soap:Body>
    <wsd:Resolve>
        <wsa:EndpointReference>
            <wsa:Address>
                urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsa:Address>
        </wsa:EndpointReference>
    </wsd:Resolve>
</soap:Body>
</soap:Envelope>
```

Uma mensagem de resolução tem os seguintes pontos de foco.



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
<td>Resolver</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Resolve
</wsa:Action></code></pre></td>
<td>A ação resolver SOAP identifica a mensagem como uma mensagem de resolução.</td>
</tr>
<tr class="even">
<td>MessageID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
</wsa:MessageID></code></pre></td>
<td>Contém o identificador da mensagem, que é referenciado em uma mensagem <a href="resolvematches-message.md">ResolveMatches</a> .</td>
</tr>
<tr class="odd">
<td>Endereço</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Contém o endereço do ponto de extremidade que está sendo resolvido.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Descoberta e mensagens de troca de metadados](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Mensagem ResolveMatches](resolvematches-message.md)
</dt> </dl>

 

 



