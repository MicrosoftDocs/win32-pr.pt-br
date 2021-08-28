---
title: Tarefas do servidor HTTP
description: Normalmente, as tarefas do servidor HTTP são executadas em uma ordem específica; ou seja, uma tarefa deve ser concluída e a saída obtida antes do início da próxima tarefa.
ms.assetid: 08f8e7e9-23b9-403f-b00c-8912919d65b1
keywords:
- Tarefas do servidor HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d89f72074ba870981421e228b0ff271505b3fce1e30cd49e79d58463570c0b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830056"
---
# <a name="http-server-tasks"></a>Tarefas do servidor HTTP

Normalmente, as tarefas do servidor HTTP são executadas em uma ordem específica; ou seja, uma tarefa deve ser concluída e a saída obtida antes do início da próxima tarefa.

Uma página de tarefa é criada para apresentar um código de exemplo sobre tarefas específicas executadas por um aplicativo servidor HTTP. Uma página de tarefas é vinculada ao arquivo de extensão C do exemplo de servidor HTTP. Quando você instala o PSDK na unidade C: de um computador local, o aplicativo de exemplo de servidor completo é instalado em C: Arquivos de Programas Exemplos do \\ \\ SDK da Microsoft \\ \\ \\ netds \\ http \\ server.

A lista a seguir identifica as tarefas do Servidor HTTP:

-   [Inicializar o serviço HTTP](#initialize-the-http-service)
-   [Registrar as URLs para escutar](#register-the-urls-to-listen-on)
-   [Chamar a rotina para receber uma solicitação](#call-the-routine-to-receive-a-request)
-   [Receber a solicitação](#receive-the-request)
-   [Manipular a solicitação HTTP](#handle-the-http-request)
-   [Enviar a resposta HTTP](#send-the-http-response)
-   [Enviar a resposta HTTP POST](#send-the-http-post-response)
-   [Limpar a API do Servidor HTTP](#clean-up-the-http-server-api)

## <a name="initialize-the-http-service"></a>Inicializar o serviço HTTP

O serviço HTTP é inicializado usando a [**função HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) e o handle para a fila de solicitações é criado usando [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle). O servidor deve ser inicializado antes que outras funções de servidor possam ser chamadas. A fila de solicitação deve ser criada antes que o serviço possa registrar URLs para escutar solicitações HTTP de entrada.

Para obter mais informações e um exemplo de código, [consulte Inicializar o serviço HTTP](http-server-sample-application.md).

## <a name="register-the-urls-to-listen-on"></a>Registrar as URLs para escutar

Para que a API do Servidor HTTP escute solicitações de entrada, URLs específicas são registradas com a API chamando a [**função HttpAddUrl.**](/windows/desktop/api/Http/nf-http-httpaddurl) As solicitações de entrada que corresponderem a essas URLs são roteadas para a fila de solicitação especificada nesta chamada.

Para obter mais informações e um exemplo de código, consulte [Registrar as URLs para escutar em](http-server-sample-application.md).

## <a name="call-the-routine-to-receive-a-request"></a>Chamar a rotina para receber uma solicitação

A função DoReceiveRequest aloca o buffer de solicitação, inicializa a ID da solicitação e inicia o loop para receber solicitações.

Para obter mais informações e um exemplo de código, consulte [Chamar a rotina para receber uma solicitação](http-server-sample-application.md).

## <a name="receive-the-request"></a>Receber a solicitação

A API do Servidor HTTP fornece uma estrutura de solicitação para armazenar a solicitação de entrada analisado. Essa estrutura é alocada pelo aplicativo e inicializada quando uma solicitação de entrada é recebida. O aplicativo chama a [**função HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) para receber a solicitação. Se o buffer de solicitação for muito pequeno para receber a solicitação, o aplicativo poderá aumentar o tamanho do buffer e chamar **HttpReceiveHttpRequest** novamente para receber toda a solicitação.

Para obter mais informações e um exemplo de código, consulte [Receber uma solicitação](http-server-sample-application.md).

## <a name="handle-the-http-request"></a>Manipular a solicitação HTTP

O aplicativo de exemplo mostra como lidar com os verbos de solicitação HTTP GET e POST. O aplicativo envia um erro 503 (**NOT \_ IMPLEMENTED**) se os verbos estão presentes na solicitação que o aplicativo não trata.

Observe que a URL a ser usada no tratamento de solicitações é a URL processada contida no membro **CookedUrl** da estrutura [**HTTP REQUEST \_ \_ V1.**](/windows/desktop/api/Http/ns-http-http_request_v1) Não a URL não processada no membro **pRawUrl,** que é exclusivamente para fins estatísticos e de acompanhamento.

Para obter mais informações e um exemplo de código, [consulte Manipular a solicitação HTTP](http-server-sample-application.md).

## <a name="send-the-http-response"></a>Enviar a resposta HTTP

A estrutura de resposta é alocada e inicializada com o código de status e uma frase de motivo na macro INITIALIZE \_ HTTP \_ RESPONSE. Um cabeçalho HTTP conhecido é adicionado à estrutura de resposta na macro ADD KNOWN HEADER e o corpo da entidade é adicionado à resposta de um bloco de \_ \_ dados da memória. A [**função HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) é chamada para enviar a resposta. Neste exemplo, o aplicativo envia uma resposta 200 OK simples para a solicitação GET.

Para obter mais informações e um exemplo de código, [consulte Enviar uma resposta HTTP.](http-server-sample-application.md)

## <a name="send-the-http-post-response"></a>Enviar a resposta HTTP POST

A solicitação POST requer mais processamento do que a solicitação GET. O corpo da entidade de solicitação é recebido chamando a [**função HttpReceiveRequestEntityBody.**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) O aplicativo envia a resposta e o corpo da entidade de resposta em chamadas separadas para a API do servidor HTTP. Os cabeçalhos de resposta são enviados com [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse). O corpo da entidade é enviado em um bloco de dados de um alçamento de arquivo com a [**função HttpSendResponseEntityBody.**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)

Para obter mais informações e um exemplo de código, [consulte Enviar uma resposta HTTP POST](http-server-sample-application.md).

## <a name="clean-up-the-http-server-api"></a>Limpar a API do Servidor HTTP

As operações de limpeza para a API do Servidor HTTP incluem:

-   Removendo todas as URLs registradas.
-   Fechar o alça para a fila de solicitação.
-   Encerrando os recursos criados pela API do Servidor HTTP.

O aplicativo chama a [**função HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl) para desregister URLs registradas pela [**função HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) inicial. O aplicativo também chama [**HttpTerminate para**](/windows/desktop/api/Http/nf-http-httpterminate) cada chamada para [**HttpInitialize com**](/windows/desktop/api/Http/nf-http-httpinitialize) configurações de sinalizador correspondentes. Essa chamada encerra todos os recursos criados pela chamada para **HttpInitialize.**

Para obter mais informações e um exemplo de código, consulte [Limpar a API do servidor HTTP.](http-server-sample-application.md)

 

 




