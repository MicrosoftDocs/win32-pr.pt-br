---
title: Metadados de serviço
description: O host do serviço WWSAPI dá suporte a WS-MetadataExchange para seus pontos de extremidade.
ms.assetid: 5a6feb34-7fff-4000-b3be-63112b22905a
keywords:
- Metadados de serviço nativos-Web-Services
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebf15614ac9e89a4e08fdd19102492d0121e65d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104454466"
---
# <a name="service-metadata"></a>Metadados de serviço

O host do serviço WWSAPI dá suporte a WS-MetadataExchange para seus pontos de extremidade. Você habilita essa troca de metadados no host de serviço com as seguintes etapas:

-   Especifique documentos de metadados na propriedade de [**\_ \_ metadados do serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) no [ \_ \_ host do serviço WS](ws-service-host.md).
-   Especifique o nome do serviço na propriedade de [**\_ \_ metadados do serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) no [ \_ \_ host do serviço WS](ws-service-host.md).
-   Especifique a porta para pontos de extremidade individuais usando a propriedade [**de \_ \_ metadados de \_ propriedade \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) de ponto de extremidade de serviço WS no [**ponto de \_ \_ extremidade do serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).
-   Habilite uma ou mais estruturas de [**\_ ponto de \_ extremidade de serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) para atender às solicitações de WS-MetadataExchange.
-   Opcionalmente, especifique **o \_ \_ sufixo de \_ \_ \_ \_ URL \_ da propriedade de ponto de extremidade de serviço WS** na enumeração de [**\_ \_ \_ \_ ID de Propriedade do ponto de extremidade**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) do serviço WS para atender às solicitações de Ws-MetadataExchange em um endereço específico.


Especificando os documentos de metadados/nome do serviço no host de serviço

A primeira etapa é especificar os documentos de metadados no host de serviço. Faça isso reunindo os documentos individuais como uma matriz de \_ \_ cadeias de caracteres XML \* do WS. Essas cadeias de caracteres podem ser o esquema XML, o WSDL ou o documento WS-Policy. Isso é especificado por meio da propriedade de [**\_ metadados de \_ propriedade \_ do serviço WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) .

Opcionalmente, um aplicativo também pode especificar o nome do serviço e o namespace como parte [**dos \_ \_ metadados do serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata). Se o documento de metadados não especificar o elemento de serviço para o nome de serviço fornecido, o modelo de serviço irá gerar um elemento de serviço com as portas WSDL correspondentes para o serviço.

``` syntax
WS_SERVICE_METADATA_DOCUMENT document = {0};
WS_STRING documentName = WS_STRING_VALUE(L&quot;a.wsdl&quot;);
document.name = &documentName;
document.content = &wsdlDocument
WS_SERVICE_METADATA_DOCUMENT** metadataDocuments [] = {&document};
WS_SERVICE_METADATA serviceMetadata = {0};
// Specify Metadata documents
serviceMetadata.count = WsCountOf(metadataDocuments);
serviceMetadata.documents = &metadataDocuments;
// Specify service name
serviceMetadata.serviceName = &serviceName;
serviceMetadata.serviceNs = &serviceNamespace;


WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_METADATA;
serviceProperties[0].value =  &serviceMetadata;
serviceProperties[0].ValueSize = sizeof(serviceMetadata);
```

Observe que nenhuma verificação dos documentos de metadados individuais será executada nos documentos. É responsabilidade do aplicativo validar o conteúdo dos documentos e garantir que todos os caminhos de importações sejam relativamente especificados.

O namespace especificado é usado para localizar o documento no qual o elemento de serviço será adicionado pelo host de serviço.

Adição do elemento de serviço ao documento WSDL

O host de serviço fornece recursos para que o aplicativo adicione um elemento de serviço em seu nome, se um já não estiver especificado. Para habilitar esse comportamento, um aplicativo deve especificar os campos serivceName e serviceNs na estrutura [**de \_ \_ metadados do serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) . Se ServiceName e serviceNs forem **nulos** , nenhum elemento de serviço será adicionado ao documento WSDL. Ambos são usados para identificar o documento no qual o ServiceElement será adicionado.

Se a propriedade de [**\_ metadados de \_ propriedade \_ do serviço WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) não for especificada, nenhum metadado transhanging ocorrerá no host de serviço.

Especificando a porta no ponto de \_ extremidade do serviço WS \_

Para que [**um \_ ponto de \_ extremidade de serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) esteja disponível como uma porta dentro do elemento de serviço no documento WSDL, o aplicativo deve especificar a propriedade de [**\_ \_ \_ \_ metadados de propriedade de ponto de extremidade de serviço WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) .

``` syntax
WS_SERVICE_ENDPOINT_METADATA endpointPort = {0}
endpointPort.name = &portName;
endpointPort.bindingName = &bindingName;
endpointPort.bindingNs = &bindingNs;

WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA;
serviceProperties[0].value =  &endpointPort;
serviceProperties[0].valueSize = sizeof(endpointPort);
```

Supõe-se que a referência ao nome de associação e ao namespace exista nos documentos especificados no host de serviço como parte dos \_ metadados de Propriedade do serviço WS \_ \_ . O tempo de execução não verifica isso em nome do aplicativo.

Habilitar serviço de WS-MetadataExchange no \_ ponto de extremidade de serviço WS \_

Para atender às solicitações de WS-MetadataExchange, o host de serviço deve ter pelo menos um ponto de extremidade habilitado para atender a solicitações de WS-MetadataExchange. Isso é feito definindo a versão apropriada para WS-MetadataExchange no ponto de [**\_ \_ extremidade do serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_MEX;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

Habilitar serviço GET HTTP no ponto de extremidade de \_ serviço WS \_

Para solicitações GET de CreateHttp, o host de serviço deve ter pelo menos um ponto de extremidade habilitado para atender a solicitações de WS-MetadataExchange. Isso é feito definindo a versão apropriada para WS-MetadataExchange no ponto de [**\_ \_ extremidade do serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_HTTP_GET;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

Especificando o sufixo de URL para solicitações de Ws-MetadataExchange

Opcionalmente, um aplicativo pode habilitar apenas a aceitação de solicitações para WS-MetadataExchange em um caminho específico. Isso é feito especificando um sufixo para o ponto de extremidade de serviço WS especificado \_ \_ . Esse sufixo é concatenado no estado em que se encontra para a URL real para o \_ ponto de extremidade do serviço WS \_ . A cadeia de caracteres concatenada é usada como a URL correspondente ao cabeçalho ' to ' recebido.

``` syntax
const WS_STRING suffix = WS_STRING_VALUE(L&quot;mex&quot;);
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_URL_SUFFIX;
serviceProperties[0].value =  &suffix;
serviceProperties[0].valueSize = sizeof(suffix);
```

Os elementos da API a seguir estão relacionados ao serviço metadados.

| Enumeração                                                       | Descrição                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_tipo de \_ troca de metadados WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_exchange_type) | Habilita ou desabilita a manutenção de WS-MetadataExchange e HTTP GET no ponto de extremidade. |



 



| Estrutura                                                               | Descrição                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**\_metadados de \_ ponto de extremidade de serviço WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_metadata) | Representa o elemento Port para o ponto de extremidade.                         |
| [**\_metadados do serviço WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata)                    | Especifica a matriz de documentos de metadados de serviço.                       |
| [**\_documento de \_ metadados do serviço WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata_document) | Especifica os documentos individuais que compõem os metadados do serviço. |



 

 

 




