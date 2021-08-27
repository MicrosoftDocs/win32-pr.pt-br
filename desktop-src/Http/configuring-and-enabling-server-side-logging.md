---
title: Configurando e habilitando o log do lado do servidor
description: Configurando e habilitando o log do lado do servidor
ms.assetid: d67d8f9a-6d8a-43f2-a1ef-75f69c04b1ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c95856cf72379de44211f05bb78fb4c6839f77b2fd6c42b91b26068bc9c5d0d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050806"
---
# <a name="configuring-and-enabling-server-side-logging"></a>Configurando e habilitando o log do lado do servidor

O aplicativo habilita o registro em log na sessão do servidor ou no grupo de URL antes de enviar a resposta com [**HttpSendHttpResponse.**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) O exemplo a seguir mostra como configurar e habilitar o log do lado do servidor do tipo W3C:

1.  O aplicativo inicializa a estrutura [**HTTP LOGGING \_ \_ INFO**](/windows/desktop/api/Http/ns-http-http_logging_info) com **HttpLoggingTypeW3C** especificado no membro Format e um bitmask das constantes [**HTTP LOG \_ \_ FIELD**](http-log-field--constants.md) no membro **Fields.** 
2.  O aplicativo chama [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) [**ou HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) com **HttpServerLoggingProperty** especificado no parâmetro *Property* e um ponteiro para a estrutura [**HTTP LOGGING \_ \_ INFO**](/windows/desktop/api/Http/ns-http-http_logging_info) no parâmetro *pPropertyInformation.*

O bitmask das constantes [**HTTP \_ LOG \_ FIELD**](http-log-field--constants.md) contém os campos que podem ser registrados no arquivo de log do W3C. Observe que definir a propriedade **HttpServerLoggingProperty** em uma sessão de servidor ou um grupo de URL não significa que as respostas HTTP serão registradas. O registro em log é executado por solicitação quando o W3C está habilitado na chamada para [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) ou [**HttpSendResponseEntityBody.**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)

Para habilitar o log de resposta do W3C por solicitação, o aplicativo executa as seguintes etapas:

1.  O aplicativo inicializa os membros dos [**DADOS DE CAMPOS DE LOG HTTP \_ \_ \_**](/windows/desktop/api/Http/ns-http-http_log_fields_data) com as informações de campo que serão registradas para essa resposta.
2.  O **membro Base.Type** da estrutura DE DADOS [**HTTP LOG \_ \_ FIELDS \_**](/windows/desktop/api/Http/ns-http-http_log_fields_data) deve ser inicializado como **HttpLogDataTypeFields.** O **campo Base.Type** garante a extensibilidade futura da estrutura e da API.
3.  O aplicativo chama [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) ou [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) com um ponteiro para a estrutura DE DADOS [**HTTP LOG \_ \_ FIELDS \_**](/windows/desktop/api/Http/ns-http-http_log_fields_data) no parâmetro *pLogData.* O aplicativo deve digitar cast o ponteiro para [**DADOS DE \_ LOG \_ PHTTP.**](/windows/desktop/api/Http/ns-http-http_log_data)

 

 




