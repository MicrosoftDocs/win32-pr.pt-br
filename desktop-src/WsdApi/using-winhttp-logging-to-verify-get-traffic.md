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
# <a name="using-winhttp-logging-to-verify-get-traffic"></a>Usando o log do WinHTTP para verificar o tráfego de obtenção

Se o host genérico e o cliente forem bem-sucedidos, mas o host e o cliente reais ainda falharem, é possível que a solicitação de metadados não esteja sendo iniciada. O log de [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) pode ser usado para verificar se as mensagens de saída estão sendo geradas e enviadas corretamente.

Os aplicativos cliente baseados em WSDAPI usam o [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) para se conectar a dispositivos. Os hosts de dispositivo baseados em WSDAPI não usam o WinHTTP. Além disso, alguns proxies de terceiros não usam o WinHTTP. Ao solucionar problemas de um host ou proxy que não usa o WinHTTP, ignore este procedimento de diagnóstico e continue a solução de problemas seguindo os procedimentos em [inspecionar rastreamentos de rede para troca de metadados http](inspecting-network-traces-for-http-metadata-exchange.md).

O log de [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) não mostra todo o tráfego de nível de TCP. Pule para [inspecionar rastreamentos de rede para troca de metadados http](inspecting-network-traces-for-http-metadata-exchange.md) se o tráfego além do tráfego http for de seu interesse.

**Para usar o log de WinHTTP para verificar o tráfego de obtenção**

1.  [Capture os logs do WinHTTP.](capturing-winhttp-logs.md)
2.  Inicie o bloco de notas ou outro editor de texto. O editor de texto deve ser executado como administrador.
3.  Abra o arquivo de log do WinHTTP.
4.  Verifique se as solicitações HTTP necessárias e as mensagens de metadados foram enviadas.

Se uma mensagem [Get](get--metadata-exchange--http-request-and-message.md) para o host for encontrada nos logs do WinHTTP, as solicitações de metadados serão enviadas ao WinHTTP com êxito. Continue a solução de problemas seguindo os procedimentos em [inspecionar rastreamentos de rede para troca de metadados http](inspecting-network-traces-for-http-metadata-exchange.md).

Se uma mensagem [Get](get--metadata-exchange--http-request-and-message.md) não puder ser encontrada para o host nos logs do WinHTTP, a solicitação de metadados não será iniciada. Isso pode acontecer quando o host publica XAddrs inválida. Verifique se o XAddrs no host está em conformidade com as [regras de validação do XAddr](xaddr-validation-rules.md).

## <a name="verifying-that-the-required-http-requests-and-metadata-messages-were-sent"></a>Verificando se as solicitações HTTP necessárias e as mensagens de metadados foram enviadas

Os eventos a seguir devem ocorrer para uma troca de metadados bem-sucedida:

-   O cliente WSDAPI gera uma solicitação HTTP de saída. Essa solicitação é enviada para o host WSDAPI.
-   O cliente envia uma mensagem [Get](get--metadata-exchange--http-request-and-message.md) para o host.

Esses eventos são capturados nos logs do WinHTTP.

O trecho de arquivo de log do WinHTTP a seguir mostra uma solicitação HTTP de saída gerada por um cliente WSDAPI.

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

O trecho de arquivo de log do WinHTTP a seguir mostra uma mensagem [Get](get--metadata-exchange--http-request-and-message.md) . Essa mensagem deve seguir imediatamente a solicitação HTTP.

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

O elemento **Action** ( `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action>` ) identifica a mensagem como uma mensagem [Get](get--metadata-exchange--http-request-and-message.md) . Verifique se o valor do elemento **to** (por exemplo, `<wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To>` ) corresponde à ID do dispositivo anunciada pelo host nas mensagens de WS-Discovery UDP originais. A ID do dispositivo anunciada pelo host pode ser verificada usando o host de depuração WSD. Para obter mais informações, consulte [usando um host genérico e um cliente para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).

Além disso, a resposta do host para a solicitação de metadados pode ser encontrada nos logs do WinHTTP do cliente. O host gera uma mensagem [GetResponse](getresponse--metadata-exchange--message.md) em resposta à mensagem [Get](get--metadata-exchange--http-request-and-message.md) do cliente.

O trecho de arquivo de log do WinHTTP a seguir mostra uma mensagem [GetResponse](getresponse--metadata-exchange--message.md) de entrada recebida por um cliente WSDAPI.

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

O elemento **Action** ( `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action>` ) identifica a mensagem como uma mensagem [GetResponse](getresponse--metadata-exchange--message.md) . Verifique se o valor do elemento **RelatesTo** da mensagem GetResponse corresponde ao valor do elemento **MessageId** da mensagem [Get](get--metadata-exchange--http-request-and-message.md) . Neste exemplo, o valor do elemento **RelatesTo** ( `<wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo>` ) corresponde ao valor do elemento **MessageId** da mensagem Get ( `<wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID>` ).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[Capturando logs do WinHTTP](capturing-winhttp-logs.md)
</dt> <dt>

[Procedimentos de diagnóstico do WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Introdução com a solução de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 
