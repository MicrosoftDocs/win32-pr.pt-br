---
description: Uma WS-Transfer usada para solicitar metadados.
ms.assetid: 18bf27aa-6ae5-4419-ae68-6df9eda10cd4
title: Solicitação e mensagem HTTP Get (metadados Exchange)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9cf6241b38f7fa81cc5d9a7c21a0f5e1a406aa
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885255"
---
# <a name="get-metadata-exchange-http-request-and-message"></a>Solicitação e mensagem HTTP Get (metadados Exchange)

Uma mensagem Get é uma WS-Transfer usada para solicitar metadados. Para obter mais informações sobre Obter mensagens, consulte a seção 3.1 da [Especificação de Transferência WS.](https://specs.xmlsoap.org/ws/2004/09/transfer/WS-Transfer.pdf) Como a troca de metadados é feita por HTTP, uma mensagem Get é o payload de uma solicitação HTTP.

Os clientes DPWS enviam mensagens Get. Clientes de Descoberta de Funções, clientes WSDAPI que chamam [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)e clientes WSDAPI que chamam [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) enviam essa mensagem.

> [!Note]  
> Este tópico mostra uma mensagem DPWS de exemplo gerada por clientes e hosts WSDAPI. O WSDAPI analisará e aceitará outras mensagens compatíveis com DPWS que não estão em conformidade com este exemplo. Não use este exemplo para verificar a interoperabilidade do DPWS; use a [WSDBIT (Ferramenta de Interoperabilidade Básica) do WSDAPI.](https://msdn.microsoft.com/library/cc264250.aspx)

 

O exemplo a seguir mostra um exemplo obter solicitação HTTP.

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

Uma solicitação Obter HTTP tem os seguintes pontos de foco.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Ponto de foco</th>
<th>Linha de header</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Caminho da URL</td>
<td><pre class="syntax" data-space="preserve"><code>POST /37f86d35-e6ac-4241-964f-1d9ae46fb366</code></pre></td>
<td>O caminho da URL em que a solicitação OBTER HTTP foi postada.</td>
</tr>
<tr class="even">
<td>Host e porta</td>
<td><pre class="syntax" data-space="preserve"><code>Host: 192.168.0.2:5357</code></pre></td>
<td>O host e a porta em que a solicitação Get HTTP foi direcionada.</td>
</tr>
</tbody>
</table>



 

A mensagem SOAP a seguir mostra uma mensagem Get de exemplo.

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
<td>Para</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:To&gt;
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
&lt;/wsa:To&gt;</code></pre></td>
<td>O identificador do dispositivo que está sendo solicitado a metadados.</td>
</tr>
<tr class="even">
<td>Obter</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Action&gt;
    https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
</wsa:Action</code></pre></td>
<td>A ação Obter SOAP identifica a mensagem como uma mensagem Get.</td>
</tr>
<tr class="odd">
<td>MessageID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:027bec45-c37c-466c-936c-68f648abe2bb
</wsa:MessageID></code></pre></td>
<td>Contém o identificador de mensagem, que é referenciado em uma <a href="getresponse--metadata-exchange--message.md">mensagem GetResponse.</a></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mensagens de descoberta e Exchange metadados](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Mensagem GetResponse](getresponse--metadata-exchange--message.md)
</dt> </dl>

 

 



