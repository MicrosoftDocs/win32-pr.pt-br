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
# <a name="processing-requests"></a><span data-ttu-id="ff9c3-103">Solicitações de processamento</span><span class="sxs-lookup"><span data-stu-id="ff9c3-103">Processing Requests</span></span>

<span data-ttu-id="ff9c3-104">Solicitações de processamento incluem quatro etapas:</span><span class="sxs-lookup"><span data-stu-id="ff9c3-104">Processing requests includes four steps:</span></span>

-   <span data-ttu-id="ff9c3-105">Recebendo uma solicitação</span><span class="sxs-lookup"><span data-stu-id="ff9c3-105">Receiving a request</span></span>
-   <span data-ttu-id="ff9c3-106">Manipulando a solicitação</span><span class="sxs-lookup"><span data-stu-id="ff9c3-106">Handling the request</span></span>
-   <span data-ttu-id="ff9c3-107">Enviando a resposta</span><span class="sxs-lookup"><span data-stu-id="ff9c3-107">Sending the response</span></span>
-   <span data-ttu-id="ff9c3-108">Cancelando solicitações que não podem ser processadas</span><span class="sxs-lookup"><span data-stu-id="ff9c3-108">Canceling requests that cannot be processed</span></span>

![Diagrama que mostra o loop de solicitação de processo.](images/processloop.png)

## <a name="receiving-a-request"></a><span data-ttu-id="ff9c3-110">Recebendo uma solicitação</span><span class="sxs-lookup"><span data-stu-id="ff9c3-110">Receiving a Request</span></span>

<span data-ttu-id="ff9c3-111">A API do servidor HTTP fornece uma estrutura de solicitação para armazenar a solicitação de entrada analisada.</span><span class="sxs-lookup"><span data-stu-id="ff9c3-111">The HTTP Server API supplies a request structure to store the parsed incoming request.</span></span> <span data-ttu-id="ff9c3-112">Essa estrutura é alocada pelo aplicativo e inicializada quando uma solicitação de entrada é recebida.</span><span class="sxs-lookup"><span data-stu-id="ff9c3-112">This structure is allocated by the application, and initialized when an incoming request is received.</span></span> <span data-ttu-id="ff9c3-113">O aplicativo chama a função [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) para receber a solicitação.</span><span class="sxs-lookup"><span data-stu-id="ff9c3-113">The application calls the [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) function to receive the request.</span></span> <span data-ttu-id="ff9c3-114">Se o buffer de solicitação for muito pequeno para receber a solicitação, o aplicativo poderá aumentar o tamanho do buffer e chamar **HttpReceiveHttpRequest** novamente para receber a solicitação inteira.</span><span class="sxs-lookup"><span data-stu-id="ff9c3-114">If the request buffer is too small to receive the request, the application can increase the buffer size and call **HttpReceiveHttpRequest** again to receive the entire request.</span></span>

<span data-ttu-id="ff9c3-115">Se a solicitação incluir dados de corpo de entidade a serem recebidos, os aplicativos chamarão [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) com a ID de solicitação retornada no parâmetro *pRequestBuffer* durante a chamada para [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest).</span><span class="sxs-lookup"><span data-stu-id="ff9c3-115">If the request includes entity body data to be received, the applications calls [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) with the request ID returned in the *pRequestBuffer* parameter during the call to [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest).</span></span>

## <a name="handling-the-request"></a><span data-ttu-id="ff9c3-116">Manipulando a solicitação</span><span class="sxs-lookup"><span data-stu-id="ff9c3-116">Handling the Request</span></span>

<span data-ttu-id="ff9c3-117">O aplicativo executa o processamento específico do aplicativo da solicitação e formula uma resposta.</span><span class="sxs-lookup"><span data-stu-id="ff9c3-117">The application performs application-specific processing of the request and formulates a response.</span></span> <span data-ttu-id="ff9c3-118">A API do servidor HTTP impõe nenhum tempo limite para esse processo.</span><span class="sxs-lookup"><span data-stu-id="ff9c3-118">The HTTP Server API imposes no timeout on this process.</span></span>

## <a name="sending-the-response"></a><span data-ttu-id="ff9c3-119">Enviando a resposta</span><span class="sxs-lookup"><span data-stu-id="ff9c3-119">Sending the Response</span></span>

<span data-ttu-id="ff9c3-120">Quando o aplicativo é concluído tratando a solicitação e formular a resposta, ele chama a função [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) para enviar a resposta.</span><span class="sxs-lookup"><span data-stu-id="ff9c3-120">When the application is finished handling the request and formulating the response, it calls the [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) function to send the response.</span></span> <span data-ttu-id="ff9c3-121">Se a resposta incluir dados de corpo de entidade a serem enviados, o aplicativo também chamará [HttpSendResponseEntityBody](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody).</span><span class="sxs-lookup"><span data-stu-id="ff9c3-121">If the response includes entity body data to send, the application also calls [HttpSendResponseEntityBody](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody).</span></span>

## <a name="canceling-requests"></a><span data-ttu-id="ff9c3-122">Cancelando solicitações</span><span class="sxs-lookup"><span data-stu-id="ff9c3-122">Canceling Requests</span></span>

<span data-ttu-id="ff9c3-123">Depois que o aplicativo recebe uma ID de solicitação de sua chamada para [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest), ela pode a qualquer momento cancelar a solicitação chamando [HttpCancelHttpRequest](/windows/desktop/api/Http/nf-http-httpcancelhttprequest).</span><span class="sxs-lookup"><span data-stu-id="ff9c3-123">After the application has received a request ID from its call to [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest), it can at any time cancel the request by calling [HttpCancelHttpRequest](/windows/desktop/api/Http/nf-http-httpcancelhttprequest).</span></span>

 

 




