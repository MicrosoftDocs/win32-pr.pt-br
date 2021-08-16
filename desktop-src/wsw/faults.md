---
title: Falhas
description: Uma mensagem de falha é usada para comunicar informações de erro sobre uma falha em um ponto de extremidade remoto.
ms.assetid: d2bada50-2ddd-4f7f-9b25-7bbec77b431b
keywords:
- Serviços Web com falhas para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55cd9e28e9ec9ce2f3068643d44306f542eebabb9b0b0c8860b15e9e986b49b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841766"
---
# <a name="faults"></a>Falhas

Uma mensagem de falha é usada para comunicar informações de erro sobre uma falha em um ponto de extremidade remoto. Uma mensagem de falha é como qualquer outra mensagem, exceto pelo formato do corpo da mensagem ter um formato padrão. As falhas podem ser usadas por protocolos de infraestrutura, como WS-Addressing e protocolos de aplicativo de nível superior.

-   [Visão geral](#overview)
-   [Gerando falhas em um serviço](#generating-faults-in-a-service)
-   [Tratamento de falhas em um cliente](#handling-faults-on-a-client)
-   [Usando falhas com mensagens](#using-faults-with-messages)

## <a name="overview"></a>Visão geral

O conteúdo do corpo de uma mensagem de falha é representado nesta API usando a estrutura [**de \_ falha do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) . Embora uma falha tenha um conjunto fixo de campos usados para fornecer informações sobre a falha (como o [**\_ \_ código de falha do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code) que identifica o tipo de falha e o [**\_ \_ motivo**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason) da falha do WS que contém o texto que descreve a falha), ele também contém um campo de detalhes que pode ser usado para especificar conteúdo XML arbitrário relacionado à falha.

## <a name="generating-faults-in-a-service"></a>Gerando falhas em um serviço

Normalmente, um serviço enviará uma falha devido a algum erro que foi encontrado durante o processamento da solicitação. O modelo usado por essa API é que o código no serviço que encontra o erro de processamento capturará as informações de falha necessárias no objeto de [ \_ erro do WS](ws-error.md) e, em seguida, o código em um nível mais alto na cadeia de chamadas realmente enviará a falha usando as informações capturadas na camada inferior. Esse esquema permite que o código que envia a falha seja isolado de como as situações de erros são mapeadas para falhas e, ao mesmo tempo, permite que informações avançadas de falha sejam enviadas.

As propriedades a seguir podem ser usadas com [**WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty) para capturar informações de falha de um objeto [WS \_ Error](ws-error.md) :

-   [**WS \_ \_ação de \_ propriedade \_ de erro de falha**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Isso especifica a ação a ser usada para a mensagem de falha. Se isso não for especificado, uma ação padrão será fornecida.
-   [**WS \_ \_falha na \_ propriedade \_ do erro de falha**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Isso contém a estrutura de [**\_ falha do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) que é enviada no corpo da mensagem de falha.
-   [**WS \_ \_cabeçalho de \_ propriedade \_ de erro de falha**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Algumas falhas incluem cabeçalhos de mensagem que são adicionados à mensagem de falha para transmitir falhas de processamento relacionadas aos cabeçalhos da mensagem de solicitação. Essa propriedade pode ser usada para especificar um [ \_ \_ buffer XML do WS](ws-xml-buffer.md) que contém um cabeçalho a ser adicionado à mensagem de falha.

Todas as cadeias de caracteres de erro que são adicionadas ao objeto de [ \_ erro WS](ws-error.md) são usadas como o texto na falha que é enviada. As cadeias de caracteres de erro podem ser adicionadas ao objeto de erro usando [**WsAddErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring).

A função [**WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty) pode ser usada para definir essas propriedades do objeto [de \_ erro WS](ws-error.md) .

Para definir o detalhe da falha armazenada no objeto [de \_ erro WS](ws-error.md) , use a função [**WsSetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrordetail) . Essa função pode ser usada para associar conteúdo XML arbitrário à falha.

O [host de serviço](service-host.md) enviará automaticamente as falhas usando as informações acima no objeto [WS \_ Error](ws-error.md) . A propriedade de [**divulgação de falha da \_ propriedade de serviço \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) pode ser usada para controlar o quão detalhado de uma falha será enviada.

Se estiver trabalhando na camada de canal, as falhas poderão ser enviadas para um objeto de [ \_ erro WS](ws-error.md) usando [**WsSendFaultMessageForError**](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror).

## <a name="handling-faults-on-a-client"></a>Tratamento de falhas em um cliente

Se um cliente receber uma falha ao usar um [proxy de serviço](service-proxy.md) ou via [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) ou [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage), o erro de falha de ponto de **extremidade do WS \_ E \_ \_ \_ recebido** será retornado. (para obter mais informações, consulte [Windows valores de retorno de serviços Web](windows-web-services-return-values.md).) Essas funções também preencherão o objeto de [ \_ erro WS](ws-error.md) , fornecido à chamada com informações sobre a falha recebida.

As seguintes propriedades de um objeto de [ \_ erro WS](ws-error.md) podem ser consultadas usando [**WsGetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrorproperty) para obter informações sobre uma falha que foi recebida:

-   [**WS \_ \_ação de \_ propriedade \_ de erro de falha**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Especifica o valor da ação da mensagem de falha.
-   [**WS \_ \_falha na \_ propriedade \_ do erro de falha**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Ela contém a estrutura [**WS \_ Fault**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) que foi desserializada do corpo da mensagem de falha.

Uma falha pode conter conteúdo XML adicional arbitrário nos detalhes da falha. Isso pode ser acessado com o uso da função [**WsGetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrordetail) .

## <a name="using-faults-with-messages"></a>Usando falhas com mensagens

A seção a seguir se aplica ao lidar diretamente com o conteúdo do corpo de uma mensagem de falha.

O conteúdo do corpo de uma mensagem de falha é representado pela estrutura padrão [**WS \_ Fault**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) , que tem suporte interno para serialização.

Por exemplo, o código a seguir pode ser usado para gravar uma falha em um corpo de mensagem:

``` syntax
HRESULT hr;
WS_ELEMENT_DESCRIPTION faultDescription = { NULL, WS_FAULT_TYPE, NULL, NULL };
WS_FAULT fault = { ... };
hr = WsWriteBody(message, &faultDescription, WS_WRITE_REQUIRED_VALUE, &fault, sizeof(fault), error);
```

O código a seguir pode ser usado para ler uma falha de um corpo de mensagem:

``` syntax
HRESULT hr;
WS_ELEMENT_DESCRIPTION faultDescription = { NULL, WS_FAULT_TYPE, NULL, NULL };
WS_FAULT fault;
hr = WsReadBody(message, &faultDescription, WS_READ_REQUIRED_VALUE, &fault, sizeof(fault), error);
```

Para saber se uma mensagem recebida é uma falha ou não, a [**\_ Propriedade WS Message \_ é uma \_ \_ falha**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) pode ser consultada. Essa propriedade é definida com base no fato de o primeiro elemento no corpo ser um elemento Fault durante [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) ou [**WsReadEnvelopeStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopestart).

Para criar uma [**\_ falha WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) , dado [um \_ erro WS](ws-error.md), use a função [**WsCreateFaultFromError**](/windows/desktop/api/WebServices/nf-webservices-wscreatefaultfromerror) .

As seguintes enumerações fazem parte das falhas:

-   [**\_divulgação de falha do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure)
-   [**\_ID da \_ propriedade de erro WS Fault \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id)

As funções a seguir fazem parte das falhas:

-   [**WsCreateFaultFromError**](/windows/desktop/api/WebServices/nf-webservices-wscreatefaultfromerror)
-   [**WsGetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrordetail)
-   [**WsGetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrorproperty)
-   [**WsSetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrordetail)
-   [**WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty)

As seguintes estruturas são parte das falhas:

-   [**WS- \_ falha**](/windows/desktop/api/WebServices/ns-webservices-ws_fault)
-   [**\_código de falha WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code)
-   [**\_Descrição dos \_ detalhes de falha do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_detail_description)
-   [**\_motivo da falha do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason)

 

 




