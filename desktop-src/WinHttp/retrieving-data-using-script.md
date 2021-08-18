---
description: este tópico inclui um exemplo de como escrever um script que obtém dados por meio do Microsoft Windows HTTP Services (WinHTTP) de forma síncrona ou assíncrona.
ms.assetid: 84b847f8-4d9e-4fea-9e87-df4c65b54a02
title: Recuperando dados usando script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9e018aa680808feddc021c7c03937d085b0d0f787c3213720cbb5e94a46a85c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133059"
---
# <a name="retrieving-data-using-script"></a>Recuperando dados usando script

este tópico inclui um exemplo de como escrever um script que obtém dados por meio do Microsoft Windows HTTP Services (WinHTTP) de forma síncrona ou assíncrona. Os conceitos demonstrados neste exemplo fornecem a base para gravar aplicativos de servidor de cliente ou de camada intermediária que exigem acesso aos dados usando o protocolo HTTP.

-   [Pré-requisitos e requisitos](#prerequisites-and-requirements)
-   [Recuperando dados de forma síncrona](#retrieving-data-synchronously)
-   [Recuperando dados de forma assíncrona](#retrieving-data-asynchronously)
-   [Tópicos relacionados](#related-topics)

## <a name="prerequisites-and-requirements"></a>Pré-requisitos e requisitos

além de um conhecimento prático do Microsoft JScript, este exemplo requer o seguinte:

-   a versão atual do Microsoft Windows Software Development Kit (SDK).
-   a ferramenta de configuração de proxy para estabelecer as configurações de proxy para o Microsoft Windows HTTP Services (WinHTTP), se a conexão com a Internet for por meio de um servidor proxy. Para obter mais informações, consulte [ProxyCfg.exe, uma ferramenta de configuração de proxy](proxycfg-exe--a-proxy-configuration-tool.md).
-   Familiaridade com a [terminologia](network-terminology.md) e os conceitos de rede.

## <a name="retrieving-data-synchronously"></a>Recuperando dados de forma síncrona

**Para criar um script que obtém o texto de uma página da Web de forma síncrona, faça o seguinte:**

1.  Abra um editor de texto.
2.  Copie o código a seguir no editor de texto.

    ```JScript
    function getText(strURL)
    {
        var strResult;
        
        try
        {
            // Create the WinHTTPRequest ActiveX Object.
            var WinHttpReq = new ActiveXObject(
                                      "WinHttp.WinHttpRequest.5.1");
            
            //  Create an HTTP request.
            var temp = WinHttpReq.Open("GET", strURL, false);

            //  Send the HTTP request.
            WinHttpReq.Send();
            
            //  Retrieve the response text.
            strResult = WinHttpReq.ResponseText;
        }
        catch (objError)
        {
            strResult = objError + "\n"
            strResult += "WinHTTP returned error: " + 
                (objError.number & 0xFFFF).toString() + "\n\n";
            strResult += objError.description;
        }
        
        //  Return the response text.
        return strResult;
    }

    WScript.Echo(getText("https://www.microsoft.com/default.htm"));
    ```

    

3.  Salve o arquivo como "Retrieve.js".
4.  Em um prompt de comando, digite "cscript Retrieve.js" e pressione ENTER.

Agora você tem um script que usa um objeto [**WinHttpRequest**](winhttprequest.md) para obter o código-fonte HTML para a página da Web em https://www.microsoft.com . Talvez seja necessário aguardar vários segundos para que o código apareça.

O aplicativo contém apenas uma função, "gettext". A primeira linha do script cria o objeto [**WinHttpRequest**](winhttprequest.md) .


```JScript
    // Create the WinHTTPRequest ActiveX Object.
    var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```



quando o mecanismo de JScript encontra essa linha, ele cria uma instância desse objeto. se você receber a mensagem de erro "o componente ActiveX não pode criar objeto", nessa linha, provavelmente a WinHttp.dll não foi corretamente registrada ou não está presente no sistema.

A próxima linha do script chama o método [**Open**](iwinhttprequest-open.md) .


```JScript
    //  Create an HTTP request.
    WinHttpReq.Open("GET", "https://www.microsoft.com", false);
```



Três parâmetros especificam qual [*verbo http*](glossary.md) usar, o nome do recurso e se deseja usar o WinHTTP de forma síncrona ou assíncrona. Neste exemplo, o método está usando o *verbo http*"Get" para obter dados de https://www.microsoft.com . A especificação de **false** para o último parâmetro determina que a transação ocorre de forma síncrona. O método [**Open**](iwinhttprequest-open.md) não estabelece uma conexão com o recurso, pois o nome pode implicar. Em vez disso, ele inicializa as estruturas de dados internas que mantêm informações sobre a sessão, a conexão e a solicitação.

O método [**Send**](iwinhttprequest-send.md) monta os cabeçalhos de solicitação e envia a solicitação. Quando chamado no modo síncrono, o método [**Send**](iwinhttprequest-send.md) também aguarda uma resposta antes de permitir que o aplicativo continue.


```JScript
    // Send the HTTP request.
    WinHttpReq.Send();
```



Depois de enviar a solicitação, o script retorna o valor da propriedade [**ResponseText**](iwinhttprequest-responsetext.md) do objeto [**WinHttpRequest**](winhttprequest.md) . Essa propriedade contém o corpo da entidade da resposta, nesse caso, a origem de um documento.


```JScript
    // Get the response text.
    return WinHttpReq.ResponseText;
```



A execução do script é pausada enquanto o texto inteiro do recurso é recuperado. O texto do recurso é retornado da função e exibido.

O objeto [**WinHttpRequest**](winhttprequest.md) garante que todos os recursos internos alocados para a transação http sejam liberados.

## <a name="retrieving-data-asynchronously"></a>Recuperando dados de forma assíncrona

Recuperar dados de maneira assíncrona usando o WinHTTP é muito semelhante a recuperar dados de forma síncrona. Modifique o script da seção anterior fazendo duas pequenas alterações.

1.  Defina o terceiro parâmetro do método [**Open**](iwinhttprequest-open.md) como "true" em vez de "false" para especificar que os métodos WinHTTP devem ser executados de forma assíncrona.
    ```JScript
       //  Create a HTTP request.
        var temp = WinHttpReq.Open("GET", strURL, true);
    ```

    

2.  Invoque o método [**WaitForResponse**](iwinhttprequest-waitforresponse.md) antes de acessar a propriedade [**ResponseText**](iwinhttprequest-responsetext.md) para garantir que toda a resposta tenha sido recebida.
    ```JScript
        //  Send the HTTP request.
        WinHttpReq.Send();
            
        // Wait for the entire response.
        WinHttpReq.WaitForResponse();
            
        //  Retrieve the response text.
        strResult = WinHttpReq.ResponseText;
    ```

    

A principal vantagem de usar o WinHTTP de forma assíncrona no script é que o método [**Send**](iwinhttprequest-send.md) retorna imediatamente. A solicitação é preparada e enviada por um thread de trabalho. Isso permite que seu aplicativo faça outras coisas enquanto está aguardando a resposta. Antes de tentar acessar a resposta, verifique se toda a resposta foi recebida chamando o método [**WaitForResponse**](iwinhttprequest-waitforresponse.md) . Caso contrário, poderá ocorrer um erro.

O método [**WaitForResponse**](iwinhttprequest-waitforresponse.md) também pode ser usado para especificar um valor de tempo limite para a transação. Um parâmetro opcional permite que você especifique o valor de tempo limite em segundos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Solicitação de comentários de HTTP/1.1 (RFC 2616)](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



