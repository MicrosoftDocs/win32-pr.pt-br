---
description: Se o host genérico e o cliente forem bem-sucedidos, mas o host e o cliente reais ainda falharem, é possível que a solicitação de metadados não esteja sendo iniciada. O log de WinHTTP pode ser usado para verificar se as mensagens de saída estão sendo geradas e enviadas corretamente.
ms.assetid: ab4568bd-fc05-4e2a-ac8c-f035e6583a36
title: Usando o log do WinHTTP para verificar o tráfego de obtenção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448e4a127baf90a64291cbd14477c424270b332d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169648"
---
# <a name="using-winhttp-logging-to-verify-get-traffic"></a><span data-ttu-id="d06df-104">Usando o log do WinHTTP para verificar o tráfego de obtenção</span><span class="sxs-lookup"><span data-stu-id="d06df-104">Using WinHTTP Logging to Verify Get Traffic</span></span>

<span data-ttu-id="d06df-105">Se o host genérico e o cliente forem bem-sucedidos, mas o host e o cliente reais ainda falharem, é possível que a solicitação de metadados não esteja sendo iniciada.</span><span class="sxs-lookup"><span data-stu-id="d06df-105">If the generic host and client succeed but the actual host and client still fail, it is possible that the metadata request is not being initiated.</span></span> <span data-ttu-id="d06df-106">O log de [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) pode ser usado para verificar se as mensagens de saída estão sendo geradas e enviadas corretamente.</span><span class="sxs-lookup"><span data-stu-id="d06df-106">[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) logging can be used to verify that outbound messages are being generated and sent correctly.</span></span>

<span data-ttu-id="d06df-107">Os aplicativos cliente baseados em WSDAPI usam o [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) para se conectar a dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d06df-107">WSDAPI-based client applications use [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) to connect to devices.</span></span> <span data-ttu-id="d06df-108">Os hosts de dispositivo baseados em WSDAPI não usam o WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="d06df-108">WSDAPI-based device hosts do not use WinHTTP.</span></span> <span data-ttu-id="d06df-109">Além disso, alguns proxies de terceiros não usam o WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="d06df-109">Also, some third-party proxies do not use WinHTTP.</span></span> <span data-ttu-id="d06df-110">Ao solucionar problemas de um host ou proxy que não usa o WinHTTP, ignore este procedimento de diagnóstico e continue a solução de problemas seguindo os procedimentos em [inspecionar rastreamentos de rede para troca de metadados http](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="d06df-110">When troubleshooting a host or proxy that does not use WinHTTP, skip this diagnostic procedure and continue troubleshooting by following the procedures in [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="d06df-111">O log de [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) não mostra todo o tráfego de nível de TCP.</span><span class="sxs-lookup"><span data-stu-id="d06df-111">[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) logging does not show all TCP-level traffic.</span></span> <span data-ttu-id="d06df-112">Pule para [inspecionar rastreamentos de rede para troca de metadados http](inspecting-network-traces-for-http-metadata-exchange.md) se o tráfego além do tráfego http for de seu interesse.</span><span class="sxs-lookup"><span data-stu-id="d06df-112">Skip to [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md) if traffic besides the HTTP traffic is of interest.</span></span>

<span data-ttu-id="d06df-113">**Para usar o log de WinHTTP para verificar o tráfego de obtenção**</span><span class="sxs-lookup"><span data-stu-id="d06df-113">**To use WinHTTP logging to verify Get traffic**</span></span>

1.  [<span data-ttu-id="d06df-114">Capture os logs do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="d06df-114">Capture the WinHTTP logs.</span></span>](capturing-winhttp-logs.md)
2.  <span data-ttu-id="d06df-115">Inicie o bloco de notas ou outro editor de texto.</span><span class="sxs-lookup"><span data-stu-id="d06df-115">Start Notepad or another text editor.</span></span> <span data-ttu-id="d06df-116">O editor de texto deve ser executado como administrador.</span><span class="sxs-lookup"><span data-stu-id="d06df-116">The text editor must be run as Administrator.</span></span>
3.  <span data-ttu-id="d06df-117">Abra o arquivo de log do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="d06df-117">Open the WinHTTP log file.</span></span>
4.  <span data-ttu-id="d06df-118">Verifique se as solicitações HTTP necessárias e as mensagens de metadados foram enviadas.</span><span class="sxs-lookup"><span data-stu-id="d06df-118">Verify that the required HTTP requests and metadata messages were sent.</span></span>

<span data-ttu-id="d06df-119">Se uma mensagem [Get](get--metadata-exchange--http-request-and-message.md) para o host for encontrada nos logs do WinHTTP, as solicitações de metadados serão enviadas ao WinHTTP com êxito.</span><span class="sxs-lookup"><span data-stu-id="d06df-119">If a [Get](get--metadata-exchange--http-request-and-message.md) message for the host is found in the WinHTTP logs, then the metadata requests are being sent to WinHTTP successfully.</span></span> <span data-ttu-id="d06df-120">Continue a solução de problemas seguindo os procedimentos em [inspecionar rastreamentos de rede para troca de metadados http](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="d06df-120">Continue troubleshooting by following the procedures in [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="d06df-121">Se uma mensagem [Get](get--metadata-exchange--http-request-and-message.md) não puder ser encontrada para o host nos logs do WinHTTP, a solicitação de metadados não será iniciada.</span><span class="sxs-lookup"><span data-stu-id="d06df-121">If a [Get](get--metadata-exchange--http-request-and-message.md) message cannot be found for the host in the WinHTTP logs, then the metadata request is not being initiated.</span></span> <span data-ttu-id="d06df-122">Isso pode acontecer quando o host publica XAddrs inválida.</span><span class="sxs-lookup"><span data-stu-id="d06df-122">This can happen when the host publishes invalid XAddrs.</span></span> <span data-ttu-id="d06df-123">Verifique se o XAddrs no host está em conformidade com as [regras de validação do XAddr](xaddr-validation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="d06df-123">Verify that the XAddrs on the host conform to the [XAddr validation rules](xaddr-validation-rules.md).</span></span>

## <a name="verifying-that-the-required-http-requests-and-metadata-messages-were-sent"></a><span data-ttu-id="d06df-124">Verificando se as solicitações HTTP necessárias e as mensagens de metadados foram enviadas</span><span class="sxs-lookup"><span data-stu-id="d06df-124">Verifying that the required HTTP requests and metadata messages were sent</span></span>

<span data-ttu-id="d06df-125">Os eventos a seguir devem ocorrer para uma troca de metadados bem-sucedida:</span><span class="sxs-lookup"><span data-stu-id="d06df-125">The following events must occur for successful metadata exchange:</span></span>

-   <span data-ttu-id="d06df-126">O cliente WSDAPI gera uma solicitação HTTP de saída.</span><span class="sxs-lookup"><span data-stu-id="d06df-126">The WSDAPI client generates an outbound HTTP request.</span></span> <span data-ttu-id="d06df-127">Essa solicitação é enviada para o host WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="d06df-127">This request is sent to the WSDAPI host.</span></span>
-   <span data-ttu-id="d06df-128">O cliente envia uma mensagem [Get](get--metadata-exchange--http-request-and-message.md) para o host.</span><span class="sxs-lookup"><span data-stu-id="d06df-128">The client sends a [Get](get--metadata-exchange--http-request-and-message.md) message to the host.</span></span>

<span data-ttu-id="d06df-129">Esses eventos são capturados nos logs do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="d06df-129">These events are captured in the WinHTTP logs.</span></span>

<span data-ttu-id="d06df-130">O trecho de arquivo de log do WinHTTP a seguir mostra uma solicitação HTTP de saída gerada por um cliente WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="d06df-130">The following WinHTTP log file snippet shows an outbound HTTP request generated by a WSDAPI client.</span></span>

``` syntax
16:51:47.893 ::*0000004* :: WinHttpSendRequest(0x36aae0, "", 0, 0x0, 0, 658, 0)
16:51:47.893 ::*0000004* :: WinHttpSendRequest() returning TRUE
16:51:47.897 ::*0000004* :: sending data:
16:51:47.897 ::*0000004* :: 226 (0xe2) bytes
16:51:47.897 ::*0000004* :: <<<<-------- HTTP stream follows below ----------------------------------------------->>>>
16:51:47.897 ::*0000004* :: POST /dbe17c74-3b21-4f52-addc-b84b444f73a0 HTTP/1.1
16:51:47.897 ::*0000004* :: Content-Type: application/soap+xml
16:51:47.897 ::*0000004* :: User-Agent: WSDAPI
16:51:47.897 ::*0000004* :: Host: 192.168.0.1:5357
16:51:47.897 ::*0000004* :: Content-Length: 658
16:51:47.897 ::*0000004* :: Connection: Keep-Alive
16:51:47.897 ::*0000004* :: Cache-Control: no-cache
16:51:47.897 ::*0000004* :: Pragma: no-cache
16:51:47.897 ::*0000004* :: 
16:51:47.897 ::*0000004* :: 
16:51:47.897 ::*0000004* :: <<<<-------- End ----------------------------------------------->>>>
```

<span data-ttu-id="d06df-131">O trecho de arquivo de log do WinHTTP a seguir mostra uma mensagem [Get](get--metadata-exchange--http-request-and-message.md) .</span><span class="sxs-lookup"><span data-stu-id="d06df-131">The following WinHTTP log file snippet shows a [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span> <span data-ttu-id="d06df-132">Essa mensagem deve seguir imediatamente a solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="d06df-132">This message should immediately follow the HTTP request.</span></span>

``` syntax
16:51:47.898 ::*0000004* :: WinHttpWriteData(0x36aae0, 0x11aa7c4, 658, 0x0)
16:51:47.899 ::*0000004* :: sending data:
16:51:47.899 ::*0000004* :: 658 (0x292) bytes
16:51:47.899 ::*0000004* :: <<<<-------- HTTP stream follows below ----------------------------------------------->>>>
16:51:47.899 ::*0000004* :: <?xml version="1.0" encoding="utf-8" ?>
16:51:47.899 ::*0000004* :: <soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"><soap:Header><wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To><wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action><wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID><wsa:ReplyTo><wsa:Address>https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous</wsa:Address></wsa:ReplyTo><wsa:From><wsa:Address>urn:uuid:b32467b5-e7ee-4ae3-8a8e-f5aa417c23b6</wsa:Address></wsa:From></soap:Header><soap:Body></soap:Body></soap:Envelope>
16:51:47.899 ::*0000004* :: <<<<-------- End ----------------------------------------------->>>>
16:51:47.899 ::*0000004* :: WinHttpWriteData() returning TRUE
```

<span data-ttu-id="d06df-133">O elemento **Action** ( `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action>` ) identifica a mensagem como uma mensagem [Get](get--metadata-exchange--http-request-and-message.md) .</span><span class="sxs-lookup"><span data-stu-id="d06df-133">The **Action** element (`<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action>`) identifies the message as a [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span> <span data-ttu-id="d06df-134">Verifique se o valor do elemento **to** (por exemplo, `<wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To>` ) corresponde à ID do dispositivo anunciada pelo host nas mensagens de WS-Discovery UDP originais.</span><span class="sxs-lookup"><span data-stu-id="d06df-134">Verify that the value of the **To** element (for example, `<wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To>`) matches the device ID advertised by the host in the original UDP WS-Discovery messages.</span></span> <span data-ttu-id="d06df-135">A ID do dispositivo anunciada pelo host pode ser verificada usando o host de depuração WSD.</span><span class="sxs-lookup"><span data-stu-id="d06df-135">The device ID advertised by the host can be checked by using the WSD Debug Host.</span></span> <span data-ttu-id="d06df-136">Para obter mais informações, consulte [usando um host genérico e um cliente para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="d06df-136">For more information, see [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>

<span data-ttu-id="d06df-137">Além disso, a resposta do host para a solicitação de metadados pode ser encontrada nos logs do WinHTTP do cliente.</span><span class="sxs-lookup"><span data-stu-id="d06df-137">In addition, the host's response to the metadata request can be found in the client's WinHTTP logs.</span></span> <span data-ttu-id="d06df-138">O host gera uma mensagem [GetResponse](getresponse--metadata-exchange--message.md) em resposta à mensagem [Get](get--metadata-exchange--http-request-and-message.md) do cliente.</span><span class="sxs-lookup"><span data-stu-id="d06df-138">The host generates a [GetResponse](getresponse--metadata-exchange--message.md) message in response to the client's [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span>

<span data-ttu-id="d06df-139">O trecho de arquivo de log do WinHTTP a seguir mostra uma mensagem [GetResponse](getresponse--metadata-exchange--message.md) de entrada recebida por um cliente WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="d06df-139">The following WinHTTP log file snippet shows an inbound [GetResponse](getresponse--metadata-exchange--message.md) message received by a WSDAPI client.</span></span>

``` syntax
16:51:47.899 ::*0000004* :: WinHttpReceiveResponse(0x36aae0, 0x0)
16:51:47.899 ::*0000004* :: WinHttpReceiveResponse() returning TRUE
16:51:47.899 ::*Session* :: DllMain(0x73fc0000, DLL_THREAD_ATTACH, 0x0)
16:51:47.902 ::*0000004* :: received data:
16:51:47.902 ::*0000004* :: 1024 (0x400) bytes
16:51:47.902 ::*0000004* :: <<<<-------- HTTP stream follows below ----------------------------------------------->>>>
16:51:47.902 ::*0000004* :: HTTP/1.1 200 
16:51:47.902 ::*0000004* :: Content-Type: application/soap+xml
16:51:47.902 ::*0000004* :: Server: Microsoft-HTTPAPI/2.0
16:51:47.902 ::*0000004* :: Date: Fri, 15 Jun 2007 23:51:47 GMT
16:51:47.905 ::*0000004* :: Content-Length: 2228
16:51:47.905 ::*0000004* :: 
16:51:47.905 ::*0000004* :: <?xml version="1.0" encoding="utf-8" ?>
16:51:47.905 ::*0000004* :: <soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsx="https://schemas.xmlsoap.org/ws/2004/09/mex" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof" xmlns:un0="http://schemas.microsoft.com/windows/pnpx/2005/10" xmlns:pub="http://schemas.microsoft.com/windows/pub/2005/07"><soap:Header><wsa:To>https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous</wsa:To><wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action><wsa:MessageID>urn:uuid:2884cbcc-2848-4c35-9327-5ab5451a8729</wsa:MessageID><wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo></soap:Header><soap:Body><wsx:Metadata><wsx:MetadataSection Dialect="https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice"><wsdp:ThisDevice><wsd
16:51:47.905 ::*0000004* :: <<<<-------- End ----------------------------------------------->>>>
```

<span data-ttu-id="d06df-140">O elemento **Action** ( `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action>` ) identifica a mensagem como uma mensagem [GetResponse](getresponse--metadata-exchange--message.md) .</span><span class="sxs-lookup"><span data-stu-id="d06df-140">The **Action** element (`<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action>`) identifies the message as a [GetResponse](getresponse--metadata-exchange--message.md) message.</span></span> <span data-ttu-id="d06df-141">Verifique se o valor do elemento **RelatesTo** da mensagem GetResponse corresponde ao valor do elemento **MessageId** da mensagem [Get](get--metadata-exchange--http-request-and-message.md) .</span><span class="sxs-lookup"><span data-stu-id="d06df-141">Verify that the value of the **RelatesTo** element of the GetResponse message matches the value of the **MessageID** element of the [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span> <span data-ttu-id="d06df-142">Neste exemplo, o valor do elemento **RelatesTo** ( `<wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo>` ) corresponde ao valor do elemento **MessageId** da mensagem Get ( `<wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID>` ).</span><span class="sxs-lookup"><span data-stu-id="d06df-142">In this example, the value of the **RelatesTo** element (`<wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo>`) matches the value of the **MessageID** element of the Get message (`<wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID>`).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d06df-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d06df-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d06df-144">WinHTTP</span><span class="sxs-lookup"><span data-stu-id="d06df-144">WinHTTP</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[<span data-ttu-id="d06df-145">Capturando logs do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="d06df-145">Capturing WinHTTP Logs</span></span>](capturing-winhttp-logs.md)
</dt> <dt>

[<span data-ttu-id="d06df-146">Procedimentos de diagnóstico do WSDAPI</span><span class="sxs-lookup"><span data-stu-id="d06df-146">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="d06df-147">Introdução com a solução de problemas de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="d06df-147">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 
