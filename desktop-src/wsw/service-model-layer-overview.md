---
title: Visão geral da camada do modelo de serviço
description: A API de Modelo de Serviço WWSAPI modela a comunicação entre um cliente e um serviço como chamadas de método, em vez de como mensagens de dados.
ms.assetid: a1ed1e3c-94ae-4383-9251-83caf2e3ebf3
keywords:
- Visão geral dos Serviços Web da Camada de Modelo de Serviço Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b182678568c7825cbf0b18bbbfd132dd5287d3f05b9ae6a372e6e5c70cd06d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962938"
---
# <a name="service-model-layer-overview"></a>Visão geral da camada do modelo de serviço

A API de Modelo de Serviço WWSAPI modela a comunicação entre um cliente e um serviço como chamadas de método, em vez de como mensagens de dados. Ao contrário da camada de canal [](message.md) [,](channel-layer-overview.md)que dá suporte a trocas de mensagens mais tradicionais entre o cliente e o serviço, o Modelo de Serviço gerencia automaticamente a comunicação por meio de um proxy de serviço no cliente e um host de serviço no serviço. Isso significa que o cliente chama funções geradas e o servidor implementa retornos de chamada.


Por exemplo, considere um serviço de calculadora que executa a adição e subtração em dois números. A adição e subtração são operações naturalmente representadas como chamadas de método.

![Diagrama mostrando como um serviço de calculadora se comunica com um cliente usando chamadas de método para adição e subtração.](images/servicemodelintro.png)

O modelo de serviço representa a comunicação entre o cliente e o serviço como chamadas de método declaradas e, portanto, oculta os detalhes de comunicação da camada de canal subjacente do aplicativo, facilitando a implementação do serviço.

## <a name="specifying-a-service"></a>Especificando um serviço

Um serviço deve ser especificado em termos de seus padrões de troca de mensagens, bem como sua representação de dados de rede. Para serviços, essa especificação geralmente é fornecida como documentos de esquema WSDL e XML.

O documento WSDL é um documento XML que contém a associação de canal e os padrões de troca de mensagens do serviço, enquanto o documento de esquema XML é um documento XML que define a representação de dados das mensagens individuais.

Para o serviço de calculadora e suas operações de adição e subtração, o documento WSDL pode ser parecido com o exemplo a seguir:

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" 
xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="http://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="http://www.w3.org/2005/08/addressing" 
xmlns:wsx="http://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ICalculator">
  <wsdl:operation name="Add">
   <wsdl:input wsaw:Action="http://Example.org/ICalculator/Add" 
   message="tns:ICalculator_Add_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ICalculator/AddResponse" 
   message="tns:ICalculator_Add_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

Da mesma forma, seu esquema XML pode ser definido da seguinte maneira:

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="Add">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="a" type="xs:int" />
    <xs:element minOccurs="0" name="b" type="xs:int" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
 <xs:element name="AddResponse">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="result" type="xs:int" 
    />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema> 
```

## <a name="converting-metadata-to-code"></a>Convertendo metadados em código

O modelo de serviço fornece o [WsUtil.exe](web-service-compiler-tool.md) como uma ferramenta para processar esses documentos de metadados, convertendo um arquivo WSDL em um header C e arquivos de origem.

![Diagrama mostrando como WsUtil.exe converte um arquivo WSDL em um header C e arquivos de origem.](images/doctotool.png)

O [WsUtil.exe](web-service-compiler-tool.md) gera o header e as fontes para implementação de serviço, bem como operações de serviço do lado do cliente para o cliente .

## <a name="calling-the-calculator-service-from-a-client"></a>Chamando o serviço calculadora de um cliente

Assim como na implementação do serviço, o cliente deve incluir o header ou os headers gerados.

``` syntax
#include "CalculatorProxyStub.h"
```

Agora, o aplicativo cliente pode criar e abrir um proxy de serviço para iniciar a comunicação com o serviço de calculadora.

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
WS_STRING uri= WS_STRING_VALUE(L"http://localhost/example");
address.uri = uri;

if (FAILED (hr = WsCreateServiceProxy(WS_CHANNEL_TYPE_REQUEST, WS_HTTP_CHANNEL_BINDING, NULL, NULL, 0, &serviceProxy, error)))
    goto Error;

if (FAILED (hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error)))
    goto Error;
```

O aplicativo pode chamar a operação Adicionar no serviço de calculadora com o seguinte código:

``` syntax
if (FAILED (hr = DefaultBinding_ICalculator_Add(serviceProxy, heap, 1, 2, &result, NULL, 0, NULL, error)))
    goto Error;
```

Consulte o exemplo de código em [HttpCalculatorClientExample](httpcalculatorclientexample.md) para implementação completa do serviço de calculadora.

## <a name="service-model-components"></a>Componentes do modelo de serviço

A interação dos componentes individuais do Modelo de Serviço WWSAPI no exemplo de Calculadora é a seguinte:

-   O cliente cria um [proxy de serviço](service-proxy.md) e o abre.
-   O cliente chama a função Adicionar do serviço e passa o proxy de serviço.
-   A mensagem é serializada de acordo com os metadados de serialização no header e nos arquivos de origem gerados pela ferramenta de metadados ([WsUtil.exe](web-service-compiler-tool.md)).
-   A mensagem é escrita no canal e transmitida pela rede para o serviço.
-   No lado do servidor, o serviço é hospedado dentro de um host de serviço e tem um ponto de extremidade escutando o contrato do ICalculator.
-   Usando os metadados do Modelo de Serviço no stub, o serviço desseliza a mensagem do cliente e a envia para o stub.
-   O serviço do lado do servidor chama o método Add, passando-o ao contexto da operação. Esse contexto de operação contém a referência à mensagem de entrada.

![Diagrama mostrando a interação dos componentes individuais do Modelo de Serviço WWSAPI.](images/servicemodellayout.png)

Componentes

-   [Host de serviço:](service-host.md)hospeda um serviço.
-   [Proxy de](service-proxy.md)serviço: define como um cliente se comunica com um serviço.
-   [Contexto:](context.md)o pacote de propriedades para disponibilizar informações específicas do estado para uma operação de serviço.
-   [Contract:](contract.md)a definição de interface de um serviço. Por exemplo, ICalculator representa um contrato para o serviço de calculadora em nosso código de exemplo.
-   [WsUtil.exe: ](web-service-compiler-tool.md)a ferramenta de metadados do Modelo de Serviço para gerar proxies e stubs.

 

 




