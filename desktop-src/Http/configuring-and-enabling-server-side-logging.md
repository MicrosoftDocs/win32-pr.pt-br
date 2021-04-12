---
title: Configurando e habilitando o registro no lado do servidor
description: Configurando e habilitando o registro no lado do servidor
ms.assetid: d67d8f9a-6d8a-43f2-a1ef-75f69c04b1ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e56247ee306d5a8804663e00162224df1d3f3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363976"
---
# <a name="configuring-and-enabling-server-side-logging"></a>Configurando e habilitando o registro no lado do servidor

O aplicativo habilita o log na sessão do servidor ou no grupo de URLs antes de enviar a resposta com [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse). O exemplo a seguir mostra como configurar e habilitar o log do W3C do tipo servidor:

1.  O aplicativo Inicializa a estrutura de [**\_ \_ informações de log http**](/windows/desktop/api/Http/ns-http-http_logging_info) com **HttpLoggingTypeW3C** especificado no membro de **formato** e um bitmask das constantes de [**\_ \_ campo de log http**](http-log-field--constants.md) no membro **Fields** .
2.  O aplicativo chama [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) ou [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) com **HttpServerLoggingProperty** especificado no parâmetro *Property* e um ponteiro para a estrutura [**de \_ \_ informações de log http**](/windows/desktop/api/Http/ns-http-http_logging_info) no parâmetro *pPropertyInformation* .

O bitmask das constantes [**do \_ \_ campo de log http**](http-log-field--constants.md) contém os campos que podem ser registrados no arquivo de log do W3C. Observe que definir a propriedade **HttpServerLoggingProperty** em uma sessão de servidor ou em um grupo de URLs não significa que as respostas HTTP serão registradas em log. O registro em log é realizado por solicitação quando o W3C é habilitado na chamada para [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) ou [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody).

Para habilitar o log de resposta do W3C por solicitação, o aplicativo executa as seguintes etapas:

1.  O aplicativo Inicializa os membros dos [**dados de \_ \_ campos de \_ log http**](/windows/desktop/api/Http/ns-http-http_log_fields_data) com as informações de campo que serão registradas para essa resposta.
2.  O membro **base. Type** da estrutura [**de \_ \_ \_ dados de campos de log http**](/windows/desktop/api/Http/ns-http-http_log_fields_data) deve ser inicializado para **HttpLogDataTypeFields**. O campo **base. Type** garante a extensibilidade futura da estrutura e da API.
3.  O aplicativo chama [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) ou [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) com um ponteiro para a estrutura de [**\_ dados dos \_ campos \_ de log http**](/windows/desktop/api/Http/ns-http-http_log_fields_data) no parâmetro *pLogData* . O aplicativo deve digitar o ponteiro para [**dados de \_ log \_ PHTTP**](/windows/desktop/api/Http/ns-http-http_log_data).

 

 




