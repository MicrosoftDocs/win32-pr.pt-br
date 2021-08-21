---
title: Visão geral da API do Servidor HTTP
description: Este tópico identifica uma sequência típica de operações que usam a API do servidor HTTP.
ms.assetid: 1245fd98-8370-4f1b-8c86-de9be5e678bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d24defe190c073f7ca359309baf6731d466459d9bb7cfbd9ffc05268ded11ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150329"
---
# <a name="http-server-api-overview"></a>Visão geral da API do Servidor HTTP

A lista a seguir identifica uma sequência típica de operações que usam a API do servidor HTTP:

-   Inicialize a API do Servidor HTTP usando a [**função HttpInitialize.**](/windows/desktop/api/Http/nf-http-httpinitialize)
-   Crie uma fila de solicitações usando a [**função HttpCreateHttpHandle.**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle)
-   Registre uma ou mais URLs usando a [**função HttpAddUrl.**](/windows/desktop/api/Http/nf-http-httpaddurl)
-   Receba solicitações de entrada direcionadas para URLs registradas usando a função [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) e envie respostas HTTP para essas solicitações usando a [**função HttpSendHttpResponse.**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)
-   (Opcional) Ao enviar uma resposta, envie um corpo de entidade adicional usando a [**função HttpSendResponseEntityBody.**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)
-   Execute operações de limpeza usando as [**funções HttpRemoveUrl,**](/windows/desktop/api/Http/nf-http-httpremoveurl) [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) e [**HttpTerminate.**](/windows/desktop/api/Http/nf-http-httpterminate)

Em operações que usam URLs, observe que é a URL processada contida no membro **CookedUrl** da estrutura [**HTTP REQUEST \_ \_ V1**](/windows/desktop/api/Http/ns-http-http_request_v1) que deve ser usada. Não a URL não processada no membro **pRawUrl,** que é exclusivamente para fins estatísticos e de acompanhamento.

Cada aplicativo cria sua própria fila de solicitação. Um aplicativo obtém seu handle de fila de solicitação [**de HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle). Ele passa esse alça para a [**função HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) para adicionar uma URL à fila de solicitação. O aplicativo recebe uma notificação de uma solicitação de entrada e a recupera da fila de solicitação chamando a [**função HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) com o alça da fila de solicitação. Você pode usar essa função para receber os headers de solicitação ou os headers e o corpo da entidade. [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) também retorna um identificador de solicitação (RequestId) para a solicitação recebida que é exclusiva para o identificador de solicitação.

> [!Note]  
> É responsabilidade do aplicativo examinar todos os títulos de solicitação relevantes, incluindo os títulos de negociação de conteúdo, se eles estão sendo usados, e falhar solicitações conforme apropriado com base no conteúdo do título. A API do Servidor HTTP garante apenas que cada linha de cabeçalho seja finalizado corretamente e não contenha caracteres ilícitos.

 

Use a [**função HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) com o handle da fila de solicitação para recuperar partes subsequentes do corpo da entidade de uma solicitação, se for o caso.

> [!Note]  
> A API do Servidor HTTP decodifica mensagens em partes no lado do recebimento, mas não executa a codificação em partes no lado do envio. Se o em partes for necessário no lado do envio, o aplicativo deverá implementá-lo. Para obter mais informações sobre codificação em partes, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

 

Use a [**função HttpReceiveClientCertificate**](/windows/desktop/api/Http/nf-http-httpreceiveclientcertificate) com aplicativos que servem URLs usando um esquema seguro ("**https**") para, opcionalmente, recuperar as informações de certificado do cliente.

As respostas são enviadas com a [**função HttpSendHttpResponse.**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) Essa função usa a RequestId da solicitação correspondente para enviar a resposta. Uma resposta pode ser enviada em várias chamadas à API ao longo do tempo chamando a função [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) com a RequestId da solicitação recebida originalmente.

> [!Note]  
> Por padrão, [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) usa "Microsoft-HTTPAPI/1.0" como o cabeçalho "Server:". Se um aplicativo especificar um cabeçalho de servidor em uma resposta, esse valor será colocado como a primeira parte do cabeçalho do servidor, seguido por um espaço e, em seguida, "Microsoft-HTTPAPI/1.0".

 

Em geral, a API do Servidor HTTP oculta detalhes do gerenciamento de conexões e seu estabelecimento e rebaixamento de aplicativos. No entanto, um aplicativo pode, opcionalmente, detectar o encerramento de uma conexão chamando [**HttpWaitForDisconnect.**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)

Os aplicativos devem ser limpos usando as seguintes etapas:

-   Quando o aplicativo não está escutando ou respondendo a uma URL, a URL é removida usando a [**função HttpRemoveURL.**](/windows/desktop/api/Http/nf-http-httpremoveurl)
-   Quando o aplicativo terminar de usar a fila de solicitação, feche o handle da fila de solicitação usando a [**função CloseHandle.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)
-   Quando o aplicativo for concluído usando a API do Servidor HTTP, chame a [**função HttpTerminate.**](/windows/desktop/api/Http/nf-http-httpterminate)

 

 