---
title: Funções da API do servidor HTTP versão 1,0
description: A API do servidor HTTP fornece as seguintes funções para gravar aplicativos.
ms.assetid: 1da9907d-a09d-41e1-aca1-9a8e2b91296f
keywords:
- Funções da API do servidor HTTP versão 1,0
- Funções HTTP, API do servidor HTTP versão 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050821e40695268d6e3fa2c946d2e8859748db2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160252"
---
# <a name="http-server-api-version-10-functions"></a>Funções da API do servidor HTTP versão 1,0

A API do servidor HTTP fornece as seguintes funções para gravar aplicativos.

## <a name="general"></a>Geral



| Função                                             | Descrição                                                                                                                       |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) | Cria uma fila de solicitação HTTP e retorna um identificador a ela.                                                                         |
| [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize)             | Inicializa a API do servidor HTTP para uso pelo processo de chamada.                                                                   |
| [**HttpPrepareUrl**](/windows/desktop/api/Http/nf-http-httpprepareurl)             | Analisa, analisa e normaliza uma URL Unicode ou Punycode não normalizada para que seja segura e válida para uso em outras funções HTTP. |
| [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate)               | Direciona a API do servidor HTTP para limpar todos os recursos associados a um processo específico.                                       |



 

## <a name="cache-management"></a>Gerenciamento de cache



| Função                                                       | Descrição                                                                                            |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**HttpAddFragmentToCache**](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache)       | Armazena em cache um fragmento de dados para que ele possa ser usado para compor uma resposta dinâmica sem ler do disco. |
| [**HttpFlushResponseCache**](/windows/desktop/api/Http/nf-http-httpflushresponsecache)       | Remove os fragmentos em cache especificados do cache HTTP.                                                |
| [**HttpReadFragmentFromCache**](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache) | Recupera um fragmento de resposta armazenado em cache especificado.                                                        |



 

## <a name="configuration"></a>Configuração



| Função                                                                 | Descrição                                                       |
|--------------------------------------------------------------------------|-------------------------------------------------------------------|
| [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) | Exclui as informações especificadas do repositório de configuração de HTTP.  |
| [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration)   | Consulta o repositório de configuração HTTP para obter informações especificadas.   |
| [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration)       | Define valores especificados no repositório de configuração da API do servidor HTTP. |



 

## <a name="input-and-output"></a>Entrada e saída



| Função                                                             | Descrição                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------|
| [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)             | Recupera uma solicitação HTTP de uma fila de solicitações especificada.      |
| [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) | Recupera os dados do corpo da entidade de uma solicitação HTTP específica.       |
| [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)                 | Envia uma resposta HTTP para uma solicitação HTTP específica.          |
| [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)     | Envia dados de corpo de entidade de uma resposta HTTP.                    |
| [**HttpWaitForDisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)               | Notifica o aplicativo quando um cliente HTTP é desconectado. |



 

## <a name="ssl"></a>SSL



| Função                                                             | Descrição                                             |
|----------------------------------------------------------------------|---------------------------------------------------------|
| [**HttpReceiveClientCertificate**](/windows/desktop/api/Http/nf-http-httpreceiveclientcertificate) | Recupera o certificado do cliente para uma conexão SSL. |



 

## <a name="url-registration"></a>Registro de URL



| Função                               | Descrição                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl)       | Registra uma URL para que as solicitações HTTP para ele sejam roteadas para uma fila de solicitações especificada.           |
| [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl) | Cancela o registro de uma URL especificada, para que as solicitações para ela não sejam mais roteadas para uma fila especificada. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estruturas da API do servidor HTTP versão 1,0](http-server-api-version-1-0-structures.md)
</dt> </dl>

 

 




