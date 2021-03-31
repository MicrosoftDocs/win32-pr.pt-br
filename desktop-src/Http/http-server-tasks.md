---
title: Tarefas do servidor HTTP
description: Normalmente, as tarefas do servidor HTTP são executadas em uma ordem específica; ou seja, uma tarefa deve ser concluída e a saída obtida antes do início da próxima tarefa.
ms.assetid: 08f8e7e9-23b9-403f-b00c-8912919d65b1
keywords:
- Tarefas do servidor HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22455dbda21aca32b26f586eed6e51cef7509af2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637263"
---
# <a name="http-server-tasks"></a>Tarefas do servidor HTTP

Normalmente, as tarefas do servidor HTTP são executadas em uma ordem específica; ou seja, uma tarefa deve ser concluída e a saída obtida antes do início da próxima tarefa.

Uma página de tarefas é criada para apresentar o código de exemplo sobre tarefas específicas que um aplicativo de servidor HTTP executa. Uma página de tarefas é vinculada ao arquivo de extensão C do exemplo de servidor HTTP. Quando você instala o PSDK na unidade C: \\ de um computador local, o aplicativo de exemplo do servidor completo é instalado em C: \\ arquivos de programas \\ Microsoft SDK \\ Samples \\ netds \\ http \\ Server.

A lista a seguir identifica as tarefas do servidor HTTP:

-   [Inicializar o serviço HTTP](#initialize-the-http-service)
-   [Registrar as URLs para escuta em](#register-the-urls-to-listen-on)
-   [Chamar a rotina para receber uma solicitação](#call-the-routine-to-receive-a-request)
-   [Receber a solicitação](#receive-the-request)
-   [Manipular a solicitação HTTP](#handle-the-http-request)
-   [Enviar a resposta HTTP](#send-the-http-response)
-   [Enviar a resposta HTTP POST](#send-the-http-post-response)
-   [Limpar a API do servidor HTTP](#clean-up-the-http-server-api)

## <a name="initialize-the-http-service"></a>Inicializar o serviço HTTP

O serviço HTTP é inicializado usando a função [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) e o identificador para a fila de solicitações é criado usando [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle). O servidor deve ser inicializado antes que qualquer outra função de servidor possa ser chamada. A fila de solicitações deve ser criada antes que o serviço possa registrar URLs para escutar solicitações HTTP de entrada.

Para obter mais informações e um exemplo de código, consulte [inicializar o serviço http](http-server-sample-application.md).

## <a name="register-the-urls-to-listen-on"></a>Registrar as URLs para escuta em

Para a API do servidor HTTP escutar solicitações de entrada, as URLs específicas são registradas com a API chamando a função [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) . As solicitações de entrada que correspondem a essas URLs são roteadas para a fila de solicitações especificada nesta chamada.

Para obter mais informações e um exemplo de código, consulte [registrar as URLs a serem escutadas](http-server-sample-application.md).

## <a name="call-the-routine-to-receive-a-request"></a>Chamar a rotina para receber uma solicitação

A função DoReceiveRequest aloca o buffer de solicitação, inicializa a ID da solicitação e inicia o loop para receber solicitações.

Para obter mais informações e um exemplo de código, consulte [chamar a rotina para receber uma solicitação](http-server-sample-application.md).

## <a name="receive-the-request"></a>Receber a solicitação

A API do servidor HTTP fornece uma estrutura de solicitação para armazenar a solicitação de entrada analisada. Essa estrutura é alocada pelo aplicativo e inicializada quando uma solicitação de entrada é recebida. O aplicativo chama a função [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) para receber a solicitação. Se o buffer de solicitação for muito pequeno para receber a solicitação, o aplicativo poderá aumentar o tamanho do buffer e chamar **HttpReceiveHttpRequest** novamente para receber a solicitação inteira.

Para obter mais informações e um exemplo de código, consulte [receber uma solicitação](http-server-sample-application.md).

## <a name="handle-the-http-request"></a>Manipular a solicitação HTTP

O aplicativo de exemplo mostra como lidar com os verbos de solicitação HTTP GET e POST. O aplicativo enviará um erro 503 (**não \_ implementado**) se os verbos estiverem presentes na solicitação que o aplicativo não manipula.

Observe que a URL a ser usada no tratamento de solicitações é a URL processada contida no membro **CookedUrl** da estrutura [**http \_ Request \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) . Não a URL não processada no membro **pRawUrl** , que é exclusivamente para fins de acompanhamento e estatística.

Para obter mais informações e um exemplo de código, consulte [manipular a solicitação HTTP](http-server-sample-application.md).

## <a name="send-the-http-response"></a>Enviar a resposta HTTP

A estrutura de resposta é alocada e inicializada com o código de status e uma frase de motivo na \_ \_ macro inicializar resposta http. Um cabeçalho HTTP conhecido é adicionado à estrutura de resposta da macro adicionar \_ \_ cabeçalho conhecido e o corpo da entidade é adicionado à resposta de um bloco de dados da memória. A função [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) é chamada para enviar a resposta. Neste exemplo, o aplicativo envia uma resposta simples de 200 OK para a solicitação GET.

Para obter mais informações e um exemplo de código, consulte [Enviar uma resposta http](http-server-sample-application.md).

## <a name="send-the-http-post-response"></a>Enviar a resposta HTTP POST

A solicitação POST requer mais processamento do que a solicitação GET. O corpo da entidade de solicitação é recebido chamando a função [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) . O aplicativo envia a resposta e o corpo da entidade de resposta em chamadas separadas para a API do servidor HTTP. Os cabeçalhos de resposta são enviados com o [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse). O corpo da entidade é enviado em um bloco de dados de um identificador de arquivo com a função [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) .

Para obter mais informações e um exemplo de código, consulte [Enviar uma resposta http post](http-server-sample-application.md).

## <a name="clean-up-the-http-server-api"></a>Limpar a API do servidor HTTP

As operações de limpeza para a API do servidor HTTP incluem:

-   Removendo todas as URLs registradas.
-   Fechando o identificador para a fila de solicitações.
-   Encerrando os recursos criados pela API do servidor HTTP.

O aplicativo chama a função [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl) para cancelar o registro de URLs registradas pela função [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) inicial. O aplicativo também chama [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) para cada chamada para [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) com as configurações de sinalizador correspondentes. Essa chamada encerra todos os recursos criados pela chamada para **HttpInitialize**.

Para obter mais informações e um exemplo de código, consulte [limpar a API do servidor http](http-server-sample-application.md).

 

 




