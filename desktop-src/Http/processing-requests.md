---
title: Solicitações de processamento
description: As solicitações de processamento incluem quatro etapas.
ms.assetid: fb170d73-c26d-4bec-abed-b614b7dad322
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea69ca4e431a4ff1841f08913b33bcb7dd57128f327aaeeac158fb62ea7a7b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996241"
---
# <a name="processing-requests"></a>Solicitações de processamento

As solicitações de processamento incluem quatro etapas:

-   Recebendo uma solicitação
-   Tratando a solicitação
-   Enviando a resposta
-   Cancelando solicitações que não podem ser processadas

![Diagrama que mostra o loop de solicitação de processo.](images/processloop.png)

## <a name="receiving-a-request"></a>Recebendo uma solicitação

A API do Servidor HTTP fornece uma estrutura de solicitação para armazenar a solicitação de entrada analisado. Essa estrutura é alocada pelo aplicativo e inicializada quando uma solicitação de entrada é recebida. O aplicativo chama a [**função HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) para receber a solicitação. Se o buffer de solicitação for muito pequeno para receber a solicitação, o aplicativo poderá aumentar o tamanho do buffer e chamar **HttpReceiveHttpRequest** novamente para receber toda a solicitação.

Se a solicitação incluir dados do corpo da entidade a serem recebidos, os aplicativos chamarão [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) com a ID de solicitação retornada no parâmetro *pRequestBuffer* durante a chamada para [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest).

## <a name="handling-the-request"></a>Tratando a solicitação

O aplicativo executa o processamento específico do aplicativo da solicitação e formula uma resposta. A API do Servidor HTTP não impõe nenhum tempo de vida nesse processo.

## <a name="sending-the-response"></a>Enviando a resposta

Quando o aplicativo terminar de manipular a solicitação e formular a resposta, ele chamará a [**função HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) para enviar a resposta. Se a resposta incluir dados do corpo da entidade a enviar, o aplicativo também [chamará HttpSendResponseEntityBody.](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)

## <a name="canceling-requests"></a>Cancelando solicitações

Depois que o aplicativo tiver recebido uma ID de solicitação de sua chamada para [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest), ele poderá a qualquer momento cancelar a solicitação chamando [HttpCancelHttpRequest.](/windows/desktop/api/Http/nf-http-httpcancelhttprequest)

 

 




