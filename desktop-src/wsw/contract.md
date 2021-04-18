---
title: Contrato
description: Um contrato de serviço transporta metadados que definem como um serviço trata as mensagens do canal.
ms.assetid: 670530bf-344b-4480-8357-8984d80c0c68
keywords:
- Contratar serviços Web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7120346dac4d11c21955cd2430ed0a7dc277e88c
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104558340"
---
# <a name="contract"></a>Contrato

Um contrato de serviço transporta metadados que definem como um serviço trata as mensagens do canal.


Um [**\_ \_ contrato de serviço do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) transporta metadados para um serviço para manipular uma [ \_ mensagem WS](ws-message.md).

![Diagrama mostrando WS_SERVICE_CONTRACT metadados em uma mensagem para um ponto de extremidade de serviço.](images/servicecontractintro.png)

Ele tem uma [**\_ \_ Descrição de contrato WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) e uma tabela de funções. Um aplicativo pode opcionalmente especificar [**o \_ \_ retorno de \_ \_ chamada de recebimento de mensagem de serviço WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback).

Se uma [**\_ \_ Descrição de contrato WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) e uma tabela de função não forem fornecidas, o aplicativo será necessário para especificar o [**retorno de \_ \_ \_ \_ chamada de recebimento de mensagem de serviço WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback).

![Diagrama mostrando as operações de serviço adicionar e subtrair no contrato de serviço ICalculator.](images/servicecontract.png)


``` syntax
static WS_SERVICE_CONTRACT calculatorContract = 
{
    &calculatorContractDescription, 
    NULL, 
    &calculatorFunctions, 
};
```

Consulte o exemplo de [calculadora](httpcalculatorserviceexample.md) para obter detalhes.

Descrição do contrato

[**WS \_ \_Descrição do contrato**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) é metadados que definem o tipo de contrato do serviço. Gerado por [wsutil.exe](web-service-compiler-tool.md).

Em termos de WSDL, uma [**\_ \_ Descrição do contrato WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) é mapeada para um WSDL: portType. Para cada WSDL: portType no documento WSDL, uma **Descrição de \_ contrato \_ WS** diferente será gerada.

Uma descrição de contrato é composta de em ou mais [operações de serviço](service-operation.md). Essas operações são fornecidas como uma matriz de [**\_ \_ Descrição da operação do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).

![Diagrama mostrando um WS_CONTRACT_DESCRIPTION como uma matriz de WS_OPERATION_DESCRIPTIONs.](images/porttypetocontract.png)

``` syntax
<wsdl:definitions xmlns:soap="https://schemas.xmlsoap.org/wsdl/soap/" 
xmlns:wsu="https://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="https://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="https://Example.org" 
xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="https://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="https://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xsd="https://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="https://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="https://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="https://www.w3.org/2005/08/addressing" 
xmlns:wsx="https://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="https://Example.org" 
xmlns:wsdl="https://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ICalculator">
  <wsdl:operation name="Add">
   <wsdl:input wsaw:Action="https://Example.org/ICalculator/Add" 
   message="tns:ICalculator_Add_InputMessage" />
   <wsdl:output wsaw:Action="https://Example.org/ICalculator/AddResponse" 
   message="tns:ICalculator_Add_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

Para obter detalhes da conversão WSDL: portType na [**\_ \_ Descrição do contrato WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) , consulte a [seção saída WSDL](wsdl-support.md).

Exemplo: [ **\_ \_ Descrição do contrato WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)

``` syntax
static WS_CONTRACT_DESCRIPTION contractDescriptionICalculator =
{
    WsCountOf(serviceOperationsICalculator),
    serviceOperationsICalculator
};
```

Tabela de funções

A tabela de funções é uma estrutura de ponteiros de função que representa cada uma das [operações de serviço](service-operation.md) no contrato de serviço. A definição da tabela de funções também é gerada pelo [wsutil.exe](web-service-compiler-tool.md).

Exemplo: tabela de funções

``` syntax
 // Function Table
struct CalculatorServiceFunctionTable
{
      AddOperation Add;
      SubtractOperation Subtract;
};

// Populate the Function Table
static const CalculatorServiceFunctionTable calculatorFunctions = {Add, Subtract};
```

Usando o [ **\_ retorno de \_ \_ \_ chamada de recebimento de mensagem do serviço WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)

[**WS \_ O \_ \_ retorno de \_ chamada de recebimento de mensagem de serviço**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback) tem uma função mutuamente exclusiva.

Se uma [**\_ \_ Descrição do contrato WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) for especificada no [**\_ \_ contrato do serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract), isso se tornará o manipulador de mensagens padrão para todas as ações que não têm suporte na **\_ \_ Descrição do contrato WS** especificado. Caso contrário, se a **\_ \_ Descrição do contrato WS** não for especificada no **\_ \_ contrato do serviço WS**, e o retorno de chamada de [**\_ recebimento de mensagem do serviço \_ \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback) for especificado no **\_ \_ contrato de serviço WS** , todas as [mensagens](ws-message.md) recebidas serão passadas para esse retorno de chamada.

Para obter mais exemplos, consulte

-   [Exemplo de serviço não tipado](untypedserviceexample.md)
-   [Exemplo de serviço de calculadora](httpcalculatorserviceexample.md)
-   [Operações de serviço](service-operation.md)

As seguintes chamadas de retorno fazem parte do contrato:

-   [**\_retorno de \_ chamada de recebimento de mensagem de serviço WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)
-   [**\_retorno de \_ chamada de stub de serviço WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_stub_callback)

As seguintes estruturas fazem parte do contrato:

-   [**\_Descrição do contrato WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)
-   [**\_contrato de serviço WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract)

 

 




