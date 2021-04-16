---
title: Exemplos de serviços Web do Windows
description: Os exemplos a seguir mostram como usar a API de serviços Web do Windows.
ms.assetid: 8a557ef0-a88a-4257-a181-57f2dca9022f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e74aec03c4822fb9ba270076b5127dd37d145fb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105808287"
---
# <a name="windows-web-services-examples"></a>Exemplos de serviços Web do Windows

Os exemplos a seguir mostram como usar a API de serviços Web do Windows.

-   [Exemplos de modelo de serviço](service-model-examples.md)
-   [Exemplos de camada de canal de TCP](tcp-channel-layer-examples.md)
-   [Exemplos de camada de canal HTTP](http-channel-layer-examples.md)
-   [Exemplos de camada de canal UDP](udp-channel-layer-examples.md)
-   [Exemplos de camada de canal de pipe nomeado](named-pipes-channel-layer-examples.md)
-   [Exemplos de mensagem](message-examples.md)
-   [Exemplos de XML](xml-examples.md)
-   [Exemplos de modelo assíncrono](async-model-examples.md)
-   [Exemplos de camada de canal de segurança](security-channel-layer-examples.md)
-   [Exemplos de replicação de arquivo](file-replication-examples.md)

## <a name="service-model-examples"></a>Exemplos de modelo de serviço

Serviço de calculadora: cliente: [HttpCalculatorClientExample](httpcalculatorclientexample.md), servidor: [HttpCalculatorServiceExample](httpcalculatorserviceexample.md).

Serviço de calculadora com segurança de transporte SSL: cliente: [HttpCalculatorWithSslClientExample](httpcalculatorwithsslclientexample.md), servidor: [HttpCalculatorWithSslServiceExample](httpcalculatorwithsslserviceexample.md).

Serviço de calculadora com nome de usuário sobre SSL com segurança de modo misto: cliente: [HttpCalculatorWithUsernameOverSslClientExample](httpcalculatorwithusernameoversslclientexample.md), servidor: [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md).

Serviço de calculadora com Kerberos sobre SSL com segurança de modo misto: cliente: [HttpCalculatorWithKerberosOverSslClientExample](httpcalculatorwithkerberosoversslclientexample.md), servidor: [HttpCalculatorWithKerberosOverSslServiceExample](httpcalculatorwithkerberosoversslserviceexample.md).

Serviço de ordem de compra: cliente: [HttpPurchaseOrderClientExample](httppurchaseorderclientexample.md), servidor: [HttpPurchaseOrderServiceExample](httppurchaseorderserviceexample.md).

Serviço de ordem de compra com segurança de transporte SSL: cliente: [HttpPurchaseOrderWithSslClientExample](httppurchaseorderwithsslclientexample.md), servidor: [HttpPurchaseOrderWithSslServiceExample](httppurchaseorderwithsslserviceexample.md).

Serviço de ordem de compra com nome de usuário sobre segurança de modo misto SSL: cliente: [HttpPurchaseOrderWithUsernameOverSslClientExample](httppurchaseorderwithusernameoversslclientexample.md), servidor: [HttpPurchaseOrderWithUserNameOverSslServiceExample](httppurchaseorderwithusernameoversslserviceexample.md).

Serviço de pedido de compra com Kerberos sobre SSL segurança de modo misto: cliente: [HttpPurchaseOrderWithKerberosOverSslClientExample](httppurchaseorderwithkerberosoversslclientexample.md), servidor: [HttpPurchaseOrderWithKerberosOverSslServiceExample](httppurchaseorderwithkerberosoversslserviceexample.md).

Serviço de ordem de compra não tipado: servidor: [UnTypedServiceExample](untypedserviceexample.md). Cliente: [UnTypedClientExample](untypedclientexample.md)

Calculadora de sessão: servidor: [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md). Cliente:[SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md).

Calculadora usando uma implementação de canal e ouvinte personalizado: servidor:[HttpCalculatorWithLayeredChannelServiceExample](httpcalculatorwithlayeredchannelserviceexample.md). Cliente:[HttpCalculatorWithLayeredChannelClientExample](httpcalculatorwithlayeredchannelclientexample.md).

Calculadora usando um canal codificado: servidor:[HttpCalculatorWithEncodedChannelServiceExample](httpcalculatorwithencodedchannelserviceexample.md). Cliente:[HttpCalculatorWithEncodedChannelClientExample](httpcalculatorwithencodedchannelclientexample.md).

Serviço que lida com solicitações HTTP brutas (não SOAP): cliente:[HttpRawClientExample](httprawclientexample.md). Servidor:[HttpRawServiceExample](httprawserviceexample.md).

Notificação de anulação de operação de serviço: servidor: [BlockingServiceExample](blockingserviceexample.md). Cliente:[ServiceCancellationExample](servicecancellationexample.md).

Chamar cancelamento: servidor: [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md). Cliente:[CallAbandonExample](callabandonexample.md).

Crie manualmente uma descrição de política e use-a para criar um proxy de serviço: [PolicyTemplateExample](policytemplateexample.md).

## <a name="tcp-channel-layer-examples"></a>Exemplos de camada de canal de TCP

Um exemplo de TCP que envia mensagens usando um padrão unidirecional: cliente: [OneWayTcpClientExample](onewaytcpclientexample.md), servidor: [OneWayTcpServerExample](onewaytcpserverexample.md)

Um exemplo de TCP que envia mensagens usando um padrão de solicitação-resposta: cliente: [RequestReplyTcpClientExample](requestreplytcpclientexample.md), servidor: [RequestReplyTcpServerExample](requestreplytcpserverexample.md)

Um exemplo de fluxo de TCP: cliente: [StreamingTcpClientExample](streamingtcpclientexample.md), servidor: [StreamingTcpServerExample](streamingtcpserverexample.md)

Um exemplo de TCP de streaming assíncrono: cliente: [AsyncStreamingTcpClientExample](asyncstreamingtcpclientexample.md), servidor: [AsyncStreamingTcpServerExample](asyncstreamingtcpserverexample.md)

## <a name="http-channel-layer-examples"></a>Exemplos de camada de canal HTTP

Um exemplo de HTTP: cliente: [HttpClientExample](httpclientexample.md), servidor: [HttpServerExample](httpserverexample.md)

Um exemplo de HTTP que usa as APIs de streaming: Client: [StreamingHttpClientExample](streaminghttpclientexample.md), Server: [StreamingHttpServerExample](streaminghttpserverexample.md)

## <a name="udp-channel-layer-examples"></a>Exemplos de camada de canal UDP

Um exemplo de UDP que envia mensagens usando um padrão unidirecional: cliente: [OneWayUdpClientExample](onewayudpclientexample.md), servidor: [OneWayUdpServerExample](onewayudpserverexample.md)

Um exemplo de UDP que envia mensagens usando um padrão de resposta de solicitação multicast: Client: [MulticastUdpClientExample](multicastudpclientexample.md), Server: [MulticastUdpServerExample](multicastudpserverexample.md) o seguinte é o mesmo exemplo, mas usando o endereçamento IPv6: Client: [MulticastUdpClientExample6](multicastudpclientexample6.md), Server: [MulticastUdpServerExample6](multicastudpserverexample6.md)

## <a name="named-pipes-channel-layer-examples"></a>Exemplos de camada de canal de pipes nomeados

Um exemplo de pipes nomeados que envia mensagens usando um padrão de solicitação-resposta: cliente: [RequestReplyNamedPipesClientExample](requestreplynamedpipesclientexample.md), servidor: [RequestReplyNamedPipesServerExample](requestreplynamedpipesserverexample.md)

Um exemplo de pipes nomeados de streaming: Client: [StreamingNamedPipesClientExample](streamingnamedpipesclientexample.md), Server: [StreamingNamedPipesServerExample](streamingnamedpipesserverexample.md)

## <a name="message-examples"></a>Exemplos de mensagem

Um exemplo que usa cabeçalhos de mensagem personalizados: [CustomHeaderExample](customheaderexample.md)

Um exemplo que codifica e decodifica uma mensagem: [MessageEncodingExample](messageencodingexample.md)

Um exemplo que encaminha uma mensagem: [ForwardMessageExample](forwardmessageexample.md)

## <a name="xml-examples"></a>Exemplos de XML

Um exemplo que grava e lê XML usando um buffer XML [ReadWriteXmlExample](readwritexmlexample.md)

Um exemplo que grava e lê dados binários usando MTOM, WsWriteBytes, WsPushBytes e WsPullBytes [ReadWriteBytesXmlExample](readwritebytesxmlexample.md)

Um exemplo que navega em um buffer XML [NavigateXmlExample](navigatexmlexample.md)

Um exemplo que lê um nó de documento XML por nó [ReadXmlExample](readxmlexample.md)

Um exemplo que localiza e exibe um atributo XML [ReadAttributeExample](readattributeexample.md)

Um exemplo que grava e lê uma matriz de elementos [ReadWriteArrayExample](readwritearrayexample.md)

Um exemplo que insere um elemento em um buffer XML [InsertElementExample](insertelementexample.md)

Um exemplo que mostra o uso de algumas funções auxiliares de buffer XML [XmlBufferExample](xmlbufferexample.md)

Um exemplo que grava e lê o tipo derivado usando funções auxiliares geradas por Wsutil [DerivedTypeExample](derivedtypeexample.md)

## <a name="async-model-examples"></a>Exemplos de modelo assíncrono

Um exemplo que ilustra o modelo para funções assíncronas. [AsyncModelExample](asyncmodelexample.md)

## <a name="security-channel-layer-examples"></a>Exemplos de camada de canal de segurança

Segurança de transporte do Windows sobre TCP: cliente: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md), servidor: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).

Segurança de transporte do Windows em pipes nomeados: cliente: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), servidor: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).

Segurança de transporte SSL: cliente: [HttpClientWithSslExample](httpclientwithsslexample.md), servidor: [HttpServerWithSslExample](httpserverwithsslexample.md).

Nome de usuário sobre SSL de modo misto de segurança: cliente: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md), servidor: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md).

Nome de usuário sobre SSL de modo misto de segurança: cliente: [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md), servidor: [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md).

## <a name="metadata-example"></a>Exemplo de metadados

Os exemplos a seguir mostram como processar documentos WSDL e de política com o objetivo de extrair informações sobre a qual protocolo um ponto de extremidade dá suporte.

Nome de usuário sobre segurança de modo misto SSL: [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md). Token emitido sobre segurança de modo misto SSL: [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md). Certificado X509 sobre segurança de modo misto SSL: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).

## <a name="ws-metadata-exchange-example"></a>Exemplo de troca de WS-Metadata

Os exemplos a seguir mostram como habilitar WS-MetadataExchange no [ \_ \_ host de serviço WS](ws-service-host.md).

Serviço TCP com WS-MetadataExchange habilitado: [MetadataExchangeSample](metadataexchangesample.md). O cliente moniker do serviço WCF que chama o serviço TCP com WS-MetadataExchange habilitado: [ServiceMonikerSample](servicemonikersample.md).

## <a name="custom-headers-and-service-model"></a>Modelo de serviço e cabeçalhos personalizados

Os exemplos a seguir mostram como usar cabeçalhos personalizados com [ \_ \_ proxy de serviço WS](ws-service-proxy.md) e [ \_ \_ host de serviço WS](ws-service-host.md) , respectivamente.

Cliente: [HttpCustomHeaderPurchaseOrderClientExample](httpcustomheaderpurchaseorderclientexample.md), servidor: [HttpCustomHeaderPurchaseOrderServiceExample](httpcustomheaderpurchaseorderserviceexample.md).

## <a name="file-replication-sample"></a>Exemplo de replicação de arquivo

Um exemplo abrangente que demonstra como implementar um serviço de replicação de arquivo: ferramenta: [FileRepToolExample](filereptoolexample.md), serviço: [FileRepServiceExample](filerepserviceexample.md).

## <a name="wcf-public-service-interoperation"></a>Interoperação de serviço público do WCF

Um cliente do Windows Web Services se comunica com um cliente do serviço WCF: [WcfPublicServiceSample](wcfpublicservicesample.md).

## <a name="custom-http-proxy"></a>Proxy HTTP personalizado

Um cliente do Windows Web Services se comunica com um serviço TerraService do ASMX usando o cliente proxy personalizado: [AsmxTerraServiceSampleWithCustomProxy](asmxterraservicesamplewithcustomproxy.md)

 

 




