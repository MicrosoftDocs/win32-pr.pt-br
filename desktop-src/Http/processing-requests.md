---
title: Solicitações de processamento
description: Solicitações de processamento incluem quatro etapas.
ms.assetid: fb170d73-c26d-4bec-abed-b614b7dad322
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e820d425e44daab9d687d1d43b756b833582a092
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "103837553"
---
# <a name="processing-requests"></a>Solicitações de processamento

Solicitações de processamento incluem quatro etapas:

-   Recebendo uma solicitação
-   Manipulando a solicitação
-   Enviando a resposta
-   Cancelando solicitações que não podem ser processadas

![Diagrama que mostra o loop de solicitação de processo.](images/processloop.png)

## <a name="receiving-a-request"></a>Recebendo uma solicitação

A API do servidor HTTP fornece uma estrutura de solicitação para armazenar a solicitação de entrada analisada. Essa estrutura é alocada pelo aplicativo e inicializada quando uma solicitação de entrada é recebida. O aplicativo chama a função [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) para receber a solicitação. Se o buffer de solicitação for muito pequeno para receber a solicitação, o aplicativo poderá aumentar o tamanho do buffer e chamar **HttpReceiveHttpRequest** novamente para receber a solicitação inteira.

Se a solicitação incluir dados de corpo de entidade a serem recebidos, os aplicativos chamarão [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) com a ID de solicitação retornada no parâmetro *pRequestBuffer* durante a chamada para [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest).

## <a name="handling-the-request"></a>Manipulando a solicitação

O aplicativo executa o processamento específico do aplicativo da solicitação e formula uma resposta. A API do servidor HTTP impõe nenhum tempo limite para esse processo.

## <a name="sending-the-response"></a>Enviando a resposta

Quando o aplicativo é concluído tratando a solicitação e formular a resposta, ele chama a função [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) para enviar a resposta. Se a resposta incluir dados de corpo de entidade a serem enviados, o aplicativo também chamará [HttpSendResponseEntityBody](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody).

## <a name="canceling-requests"></a>Cancelando solicitações

Depois que o aplicativo recebe uma ID de solicitação de sua chamada para [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest), ela pode a qualquer momento cancelar a solicitação chamando [HttpCancelHttpRequest](/windows/desktop/api/Http/nf-http-httpcancelhttprequest).

 

 




