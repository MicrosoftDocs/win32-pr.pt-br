---
title: Visão geral da API do servidor HTTP
description: Este tópico identifica uma sequência típica de operações que usam a API do servidor HTTP.
ms.assetid: 1245fd98-8370-4f1b-8c86-de9be5e678bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c99af3e4914c5496c2adea10b3ac658f75f3018
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105761726"
---
# <a name="http-server-api-overview"></a>Visão geral da API do servidor HTTP

A lista a seguir identifica uma sequência típica de operações que usam a API do servidor HTTP:

-   Inicialize a API do servidor HTTP usando a função [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) .
-   Crie uma fila de solicitações usando a função [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) .
-   Registre uma ou mais URLs usando a função [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) .
-   Receba solicitações de entrada direcionadas a URLs registradas usando a função [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) e envie respostas HTTP para essas solicitações usando a função [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) .
-   Adicional Ao enviar uma resposta, envie um corpo de entidade adicional usando a função [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) .
-   Execute operações de limpeza usando as funções [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl), [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) e [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) .

Em operações que usam URLs, observe que é a URL processada contida no membro **CookedUrl** da estrutura [**http \_ Request \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) que deve ser usada. Não a URL não processada no membro **pRawUrl** , que é exclusivamente para fins de acompanhamento e estatística.

Cada aplicativo cria sua própria fila de solicitações. Um aplicativo obtém o identificador da fila de solicitações de [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle). Ele passa esse identificador para a função [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) para adicionar uma URL à fila de solicitações. O aplicativo recebe a notificação de uma solicitação de entrada e a recupera da fila de solicitações chamando a função [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) com o identificador da fila de solicitações. Você pode usar essa função para receber os cabeçalhos de solicitação ou os cabeçalhos e o corpo da entidade. [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) também retorna um identificador de solicitação (RequestId) para a solicitação recebida que é exclusiva para o identificador de solicitação.

> [!Note]  
> É responsabilidade do aplicativo examinar todos os cabeçalhos de solicitação relevantes, incluindo cabeçalhos de negociação de conteúdo, se estiverem sendo usados, e falhar solicitações conforme apropriado com base no conteúdo do cabeçalho. A API do servidor HTTP garante apenas que cada linha de cabeçalho seja corretamente encerrada e não contenha caracteres ilegais.

 

Use a função [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) com o identificador da fila de solicitações para recuperar partes subsequentes do corpo da entidade de uma solicitação, se houver.

> [!Note]  
> A API do servidor HTTP decodifica mensagens em partes no lado do recebimento, mas não executa a codificação em partes no lado de envio. Se o agrupamento for necessário no lado de envio, o aplicativo deverá implementá-lo. Para obter mais informações sobre a codificação em partes, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

 

Use a função [**HttpReceiveClientCertificate**](/windows/desktop/api/Http/nf-http-httpreceiveclientcertificate) com aplicativos que atendem URLs usando um esquema seguro ("**https**") para, opcionalmente, recuperar as informações de certificado do cliente.

As respostas são enviadas com a função [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) . Essa função usa RequestId da solicitação correspondente para enviar a resposta. Uma resposta pode ser enviada em várias chamadas de API ao longo do tempo chamando a função [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) com a RequestId da solicitação recebida originalmente.

> [!Note]  
> Por padrão, [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) usa "Microsoft-HTTPAPI/1.0" como o cabeçalho "Server:". Se um aplicativo especificar um cabeçalho de servidor em uma resposta, esse valor será colocado como a primeira parte do cabeçalho do servidor, seguido de um espaço e, em seguida, "Microsoft-HTTPAPI/1.0".

 

Em geral, a API do servidor HTTP oculta os detalhes do gerenciamento de conexão e seus estabelecimentos e subdivisão dos aplicativos. No entanto, um aplicativo pode opcionalmente detectar a terminação de uma conexão chamando [**HttpWaitForDisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect).

Os aplicativos devem ser limpos usando as seguintes etapas:

-   Quando o aplicativo não está escutando ou respondendo a uma URL, a URL é removida usando a função [**HttpRemoveURL**](/windows/desktop/api/Http/nf-http-httpremoveurl) .
-   Quando o aplicativo for concluído usando a fila de solicitações, feche o identificador da fila de solicitações usando a função [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .
-   Quando o aplicativo for concluído usando a API do servidor HTTP, chame a função [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) .

 

 