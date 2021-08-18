---
description: Uma WS-Discovery usada por um cliente para pesquisar serviços na rede por nome.
ms.assetid: b963bd2a-47cb-4f8d-8272-a586e6d6a047
title: Resolver mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54887db566ee428e6bfe9ec2de9016a637884b092611a85e607c55aaa4176abc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991606"
---
# <a name="resolve-message"></a>Resolver mensagem

Uma mensagem Resolver é uma WS-Discovery usada por um cliente para pesquisar serviços na rede por nome. Um cliente só enviará uma mensagem Resolver quando [](get--metadata-exchange--http-request-and-message.md) uma mensagem HTTP (como uma solicitação obter troca de metadados ou uma mensagem de serviço) for enviada. Para obter mais informações sobre Resolver mensagens, consulte a seção 6.1 da [Especificação WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Uma mensagem Resolver é enviada pelo multicast UDP para a porta 3702. Não há suporte para mensagens unicast Resolve.

Os clientes DPWS enviam mensagens resolver. A lista a seguir mostra cenários em que o WSDAPI enviará uma mensagem Resolver.

-   Um cliente de Descoberta de Funções enviará uma mensagem Resolver se nenhum XAddrs estiver incluído em uma [mensagem ProbeMatches.](probematches-message.md)
-   Um cliente que chama [**os métodos IWSDiscoveryProvider::SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid) enviará uma mensagem Resolver.
-   Um cliente que [**chama WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) poderá enviar uma mensagem Resolver se um endereço de dispositivo lógico for passado para *pszDeviceId*.
-   Um cliente que [**chama WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) enviará uma mensagem Resolver se a função for chamada com o parâmetro pDeviceAddress definido como **NULL.**

> [!Note]  
> Este tópico mostra uma mensagem DPWS de exemplo gerada por clientes e hosts WSDAPI. O WSDAPI analisará e aceitará outras mensagens compatíveis com DPWS que não estão em conformidade com este exemplo. Não use este exemplo para verificar a interoperabilidade do DPWS; use a [WSDBIT (Ferramenta de Interoperabilidade Básica) do WSDAPI.](https://msdn.microsoft.com/library/cc264250.aspx)

 

A mensagem SOAP a seguir mostra uma mensagem resolver de exemplo.

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

Uma mensagem Resolver tem os seguintes pontos de foco.



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
<td>A ação Resolver SOAP identifica a mensagem como uma mensagem Resolver.</td>
</tr>
<tr class="even">
<td>MessageID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
</wsa:MessageID></code></pre></td>
<td>Contém o identificador de mensagem, que é referenciado em uma <a href="resolvematches-message.md">mensagem ResolveMatches.</a></td>
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

[Mensagens de descoberta e Exchange metadados](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Mensagem ResolveMatches](resolvematches-message.md)
</dt> </dl>

 

 



