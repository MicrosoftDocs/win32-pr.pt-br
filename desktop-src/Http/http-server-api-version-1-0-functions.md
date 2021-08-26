---
title: Funções da API do Servidor HTTP versão 1.0
description: A API do Servidor HTTP fornece as seguintes funções para escrever aplicativos.
ms.assetid: 1da9907d-a09d-41e1-aca1-9a8e2b91296f
keywords:
- Funções da API do Servidor HTTP versão 1.0
- Funções HTTP, API do Servidor HTTP versão 1.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8520753e56e995b5751b55ff71cf49f8e82d414e702b2df255c2901e69c397fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047196"
---
# <a name="http-server-api-version-10-functions"></a>Funções da API do Servidor HTTP versão 1.0

A API do Servidor HTTP fornece as seguintes funções para escrever aplicativos.

## <a name="general"></a>Geral



| Função                                             | Descrição                                                                                                                       |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) | Cria uma fila de solicitação HTTP e retorna um handle para ela.                                                                         |
| [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize)             | Inicializa a API do Servidor HTTP para uso pelo processo de chamada.                                                                   |
| [**HttpPrepareUrl**](/windows/desktop/api/Http/nf-http-httpprepareurl)             | Analisa, analisa e normaliza uma URL Unicode ou punycode não normalizada para que seja seguro e válido usar em outras funções HTTP. |
| [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate)               | Direciona a API do Servidor HTTP para limpar todos os recursos associados a um processo específico.                                       |



 

## <a name="cache-management"></a>Gerenciamento de Cache



| Função                                                       | Descrição                                                                                            |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**HttpAddFragmentToCache**](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache)       | Armazena em cache um fragmento de dados para que ele possa ser usado para compor uma resposta dinâmica sem ler do disco. |
| [**HttpFlushResponseCache**](/windows/desktop/api/Http/nf-http-httpflushresponsecache)       | Remove fragmentos armazenados em cache especificados do cache HTTP.                                                |
| [**HttpReadFragmentFromCache**](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache) | Recupera um fragmento de resposta armazenado em cache especificado.                                                        |



 

## <a name="configuration"></a>Configuração



| Função                                                                 | Descrição                                                       |
|--------------------------------------------------------------------------|-------------------------------------------------------------------|
| [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) | Exclui informações especificadas do armazenamento de configuração HTTP.  |
| [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration)   | Consulta o armazenamento de configuração HTTP para obter informações especificadas.   |
| [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration)       | Define valores especificados no armazenamento de configuração da API do Servidor HTTP. |



 

## <a name="input-and-output"></a>Entrada e saída



| Função                                                             | Descrição                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------|
| [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)             | Recupera uma solicitação HTTP de uma fila de solicitação especificada.      |
| [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) | Recupera dados do corpo da entidade de uma solicitação HTTP específica.       |
| [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)                 | Envia uma resposta HTTP para uma solicitação HTTP específica.          |
| [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)     | Envia dados do corpo da entidade de uma resposta HTTP.                    |
| [**HttpWaitForDisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)               | Notifica o aplicativo quando um cliente HTTP foi desconectado. |



 

## <a name="ssl"></a>SSL



| Função                                                             | Descrição                                             |
|----------------------------------------------------------------------|---------------------------------------------------------|
| [**HttpReceiveClientCertificate**](/windows/desktop/api/Http/nf-http-httpreceiveclientcertificate) | Recupera o certificado do cliente para uma conexão SSL. |



 

## <a name="url-registration"></a>Registro de URL



| Função                               | Descrição                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl)       | Registra uma URL para que as solicitações HTTP para ela sejam roteadas para uma fila de solicitação especificada.           |
| [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl) | O cancelamento do registro de uma URL especificada, de modo que as solicitações para ela não sejam mais roteadas para uma fila especificada. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estruturas da API do Servidor HTTP versão 1.0](http-server-api-version-1-0-structures.md)
</dt> </dl>

 

 




