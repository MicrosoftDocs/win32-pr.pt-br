---
title: Operação de serviço
description: A operação de serviço é o código e os metadados associados a uma operação específica de um serviço.
ms.assetid: 788940a0-b1d9-45d7-a4b5-6f0926026c7d
keywords:
- Serviços Web de operação de serviço para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e7883c0988189db3d977a78615c024dc92df36
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "103930078"
---
# <a name="service-operation"></a>Operação de serviço

A operação de serviço é o código e os metadados associados a uma operação específica de um serviço.


Em termos de WSDL, cada WSDL: Operation definida no documento WSDL para um determinado portType é uma operação de serviço.

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

Cada operação de serviço no modelo de serviço é fornecida como uma [**\_ \_ Descrição de operação WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description). \_A descrição da operação WS \_ é gerada pelo [wsutil.exe](web-service-compiler-tool.md).

Para cada WSDL: Operation, a ferramenta gera uma [**\_ \_ Descrição de operação WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)separada.

![Diagrama mostrando como wsutil.exe gera um WS_CONTRACT_DESCRIPTION.](images/porttypetocontract.png)

``` syntax
static WS_OPERATION_DESCRIPTION serviceOperationsICalculator[] =
{
    {
        // Add Method
        &messageDescriptionAddICalculator,
        &messageDescriptionAddResponseICalculator,
        WsCountOf(parametersAddICalculator),
        ICalculator_Add_Stub 
    }
};
```

Em termos de código, cada operação de serviço tem uma função associada a ele. A definição dessa função é diferente para clientes e servidores.

As operações de serviço são classificadas em,

-   [Operações de serviço no lado do cliente](client-side-service-operations.md)
-   [Operações de serviço no servidor](server-side-service-operations.md)

Essa classificação é principalmente baseada no layout de assinatura do servidor e nas implementações do lado do cliente das operações de serviço.

Consulte também a [seção suporte a WSDL](wsdl-support.md).

As seguintes enumerações são usadas com operações de serviço:

-   [**\_tipo de parâmetro do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_parameter_type)
-   [**\_motivo de \_ cancelamento do serviço WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_cancel_reason)
-   [**\_opção de \_ mensagem de operação de serviço WS \_ \_**](/windows/win32/api/webservices/ne-webservices-ws_charset)

As seguintes estruturas são usadas com operações de serviço:

-   [**\_Descrição da mensagem WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)
-   [**\_Descrição da operação WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)
-   [**\_Descrição do parâmetro WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description)

 

 




