---
description: Uma WS-Transfer mensagem usada para solicitar metadados.
ms.assetid: 18bf27aa-6ae5-4419-ae68-6df9eda10cd4
title: Get (troca de metadados) solicitação e mensagem HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ad240a51fdbabf4184b8769f4e3cca6daa4244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790334"
---
# <a name="get-metadata-exchange-http-request-and-message"></a>Get (troca de metadados) solicitação e mensagem HTTP

Uma mensagem Get é uma WS-Transfer que é usada para solicitar metadados. Para obter mais informações sobre como obter mensagens, consulte a seção 3,1 da [especificação WS-Transfer](https://specs.xmlsoap.org/ws/2004/09/transfer/WS-Transfer.pdf). Como a troca de metadados é feita por HTTP, uma mensagem Get é a carga de uma solicitação HTTP.

Os clientes do DPWS enviam mensagens Get. Clientes de descoberta de função, clientes WSDAPI chamando [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)e clientes WSDAPI chamando [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) enviam esta mensagem.

> [!Note]  
> Este tópico mostra uma mensagem DPWS de exemplo gerada por clientes e hosts WSDAPI. O WSDAPI analisará e aceitará outras mensagens em conformidade com o DPWS que não estão em conformidade com este exemplo. Não use este exemplo para verificar a interoperabilidade do DPWS; em vez disso, use a [ferramenta de interoperabilidade básica do WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

O exemplo a seguir mostra um exemplo de solicitação HTTP Get.

``` syntax
POST /37f86d35-e6ac-4241-964f-1d9ae46fb366
HTTP/1.1
Content-Type: application/soap+xml
User-Agent: WSDAPI
Host: 192.168.0.2:5357
Content-Length: 658
Connection: Keep-Alive
Cache-Control: no-cache
Pragma: no-cache
```

Uma solicitação GET HTTP tem os seguintes pontos de foco.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Ponto de foco</th>
<th>Linha de cabeçalho</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Caminho da URL</td>
<td><pre class="syntax" data-space="preserve"><code>POST /37f86d35-e6ac-4241-964f-1d9ae46fb366</code></pre></td>
<td>O caminho da URL onde a solicitação HTTP Get foi postada.</td>
</tr>
<tr class="even">
<td>Host e porta</td>
<td><pre class="syntax" data-space="preserve"><code>Host: 192.168.0.2:5357</code></pre></td>
<td>O host e a porta em que a solicitação HTTP Get foi direcionada.</td>
</tr>
</tbody>
</table>



 

A mensagem SOAP a seguir mostra um exemplo de mensagem Get.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing">
<soap:Header>
    <wsa:To>
        urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:027bec45-c37c-466c-936c-68f648abe2bb
    </wsa:MessageID>
    <wsa:ReplyTo>
        <wsa:Address>
            https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        </wsa:Address>
    </wsa:ReplyTo>
    <wsa:From>
        <wsa:Address>
            urn:uuid:49e131df-351a-4ece-9a6f-6a862d31cffa
        </wsa:Address>
    </wsa:From>
</soap:Header>
<soap:Body>
</soap:Body>
```

Uma mensagem Get tem os seguintes pontos de foco.



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
<td>Para</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:To>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:To></code></pre></td>
<td>O identificador do dispositivo que está sendo solicitado para os metadados.</td>
</tr>
<tr class="even">
<td>Obter</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
</wsa:Action</code></pre></td>
<td>A ação obter SOAP identifica a mensagem como uma mensagem Get.</td>
</tr>
<tr class="odd">
<td>MessageID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:027bec45-c37c-466c-936c-68f648abe2bb
</wsa:MessageID></code></pre></td>
<td>Contém o identificador da mensagem, que é referenciado em uma mensagem <a href="getresponse--metadata-exchange--message.md">GetResponse</a> .</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Descoberta e mensagens de troca de metadados](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Mensagem GetResponse](getresponse--metadata-exchange--message.md)
</dt> </dl>

 

 



