---
title: Configurando propriedades
description: Configurando propriedades
ms.assetid: 9d659887-a696-4344-9c71-a2cc6131d8b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f898467f92f669596b4a8b1a4e68581c343ea883
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363973"
---
# <a name="configuring-properties"></a>Configurando propriedades

A API do servidor HTTP versão 2,0 permite que os aplicativos configurem manualmente filas de solicitação, sessões de servidor e grupos de URLs. A sessão de servidor é o objeto de nível superior que contém informações de configuração que se aplicam a todos os grupos de URLs criados sob eles. O aplicativo cria uma sessão de servidor com um ou mais grupos de URLs sob ela e, em seguida, associa o grupo de URLs a uma fila de solicitações.

Para obter mais informações sobre objetos de configuração específicos na API do servidor HTTP versão 2,0, consulte:

-   [Configurando a sessão do servidor](configuring-the-server-session.md)
-   [Configurando o grupo de URLs](configuring-the-url-group.md)
-   [Configurando os timers de longa duração da API do servidor HTTP](configuring-the-http-server-api-wide-timers.md)

As propriedades dos objetos de configuração são definidas com [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty), [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) e [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) , conforme mostrado no diagrama a seguir. A associação entre a fila de solicitações e o grupo de URLs pode ser alterada sob demanda, enquanto a associação entre a sessão do servidor e os grupos de URLs não pode ser alterada. Os grupos de URLs devem ser associados a uma fila de solicitações para receber solicitações.

![Propriedades para os objetos de configuração](images/configpropinv2.png)

A tabela a seguir lista as propriedades que podem ser definidas em cada objeto de configuração. Em geral, se nenhuma configuração de propriedade for definida pelo aplicativo, as configurações padrão da API do servidor HTTP serão aplicadas. As propriedades de configuração definidas pelo aplicativo na sessão de servidor substituem as configurações de toda a API do servidor HTTP. As configurações definidas no grupo de URLs substituem as configurações de sessão do servidor e as configurações da fila de solicitações substituem as configurações padrão da API do servidor HTTP.



| Objeto Configuration | Propriedade                                                                                                                                                      |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sessão de servidor       | HttpServerStateProperty HttpServerLoggingProperty HttpServerQosProperty HttpServerTimeoutsProperty HttpServerAuthenticationProperty                           |
| Grupo de URLs            | HttpServerStateProperty HttpServerAuthenticationProperty HttpServerLoggingProperty HttpServerQosProperty HttpServerBindingProperty HttpServerTimeoutsProperty |
| Fila de solicitação        | HttpServerStateProperty HttpServerQueueLengthProperty HttpServer503VerbosityProperty                                                                          |



 

As propriedades de sessão de servidor são definidas na enumeração de [ \_ \_ Propriedades do servidor http](/windows/desktop/api/Http/ne-http-http_server_property) . A tabela a seguir lista as estruturas de propriedade que são definidas para cada tipo de propriedade e a API de servidor HTTP padrão quando essas propriedades não são definidas pelo aplicativo.



| Propriedade                                                    | Estrutura                                                                     | Padrão de API do servidor HTTP    |
|-------------------------------------------------------------|-------------------------------------------------------------------------------|----------------------------|
| HttpServerAuthenticatonProperty                             | [**\_informações de \_ autenticação do servidor http \_**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) | Sem Autenticação          |
| HttpServerLoggingProperty                                   | [**\_informações de log http \_**](/windows/desktop/api/Http/ns-http-http_logging_info)                              | Sem registro em log                 |
| HttpServerQosProperty->HttpQosSettingTypeConnectionLimit | [**\_informações de \_ limite de conexão http \_**](/windows/desktop/api/Http/ns-http-http_connection_limit_info)           | Sem limite                   |
| HttpServerTimeoutsProperty                                  | [**\_informações de limite de tempo limite http \_ \_**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info)                 | 120 s.                   |
| HttpServerQosProperty->HttpQosSettingTypeBandwidth       | [**informações de limite de largura de \_ banda http \_ \_**](/windows/desktop/api/Http/ns-http-http_bandwidth_limit_info)             | Sem limite                   |
| HttpServerQueueLengthProperty                               | ULONG                                                                         | 1000                       |
| HttpServerStateProperty                                     | [**\_informações de estado http \_**](/windows/desktop/api/Http/ns-http-http_state_info)                                  | habilitado                    |
| HttpServer503VerbosityProperty                              | [**\_Detalhes da \_ resposta HTTP 503 \_**](/windows/desktop/api/Http/ne-http-http_503_response_verbosity)         | HttpResponseVerbosityBasic |
| HttpServerBindingProperty                                   | [**\_informações de associação http \_**](/windows/desktop/api/Http/ns-http-http_binding_info)                              | Nenhum                       |



 

A tabela a seguir lista os valores mínimo e máximo para as configurações de API do servidor HTTP.



| Propriedade                                              | Máximo e mínimo da API do servidor HTTP                        |
|-------------------------------------------------------|------------------------------------------------------------|
| HttpServerQosProperty->HttpQosSettingTypeBandwidth | Min = mín. de \_ \_ limitação de largura de banda permitida máx. \_ \_ = None |
| HttpServerQueueLengthProperty                         | Min = 0xA Max = 0xFFFF                                     |



 

 

 




