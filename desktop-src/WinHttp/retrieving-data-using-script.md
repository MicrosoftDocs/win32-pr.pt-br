---
description: Este tópico inclui um exemplo de como escrever um script que obtém dados por meio do Microsoft Windows HTTP Services (WinHTTP) de forma síncrona ou assíncrona.
ms.assetid: 84b847f8-4d9e-4fea-9e87-df4c65b54a02
title: Recuperando dados usando script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 734516cf75f92cc43ab4cb15f22bd97aa803ec33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920650"
---
# <a name="retrieving-data-using-script"></a><span data-ttu-id="a8544-103">Recuperando dados usando script</span><span class="sxs-lookup"><span data-stu-id="a8544-103">Retrieving Data Using Script</span></span>

<span data-ttu-id="a8544-104">Este tópico inclui um exemplo de como escrever um script que obtém dados por meio do Microsoft Windows HTTP Services (WinHTTP) de forma síncrona ou assíncrona.</span><span class="sxs-lookup"><span data-stu-id="a8544-104">This topic includes an example of how to write a script that obtains data through Microsoft Windows HTTP Services (WinHTTP) either synchronously or asynchronously.</span></span> <span data-ttu-id="a8544-105">Os conceitos demonstrados neste exemplo fornecem a base para gravar aplicativos de servidor de cliente ou de camada intermediária que exigem acesso aos dados usando o protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="a8544-105">The concepts demonstrated in this example provide the basis for writing client or middle-tier server applications that require access to data using the HTTP protocol.</span></span>

-   [<span data-ttu-id="a8544-106">Pré-requisitos e requisitos</span><span class="sxs-lookup"><span data-stu-id="a8544-106">Prerequisites and Requirements</span></span>](#prerequisites-and-requirements)
-   [<span data-ttu-id="a8544-107">Recuperando dados de forma síncrona</span><span class="sxs-lookup"><span data-stu-id="a8544-107">Retrieving Data Synchronously</span></span>](#retrieving-data-synchronously)
-   [<span data-ttu-id="a8544-108">Recuperando dados de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="a8544-108">Retrieving Data Asynchronously</span></span>](#retrieving-data-asynchronously)
-   [<span data-ttu-id="a8544-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a8544-109">Related topics</span></span>](#related-topics)

## <a name="prerequisites-and-requirements"></a><span data-ttu-id="a8544-110">Pré-requisitos e requisitos</span><span class="sxs-lookup"><span data-stu-id="a8544-110">Prerequisites and Requirements</span></span>

<span data-ttu-id="a8544-111">Além de um conhecimento prático do Microsoft JScript, este exemplo requer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a8544-111">In addition to a working knowledge of Microsoft JScript, this example requires the following:</span></span>

-   <span data-ttu-id="a8544-112">A versão atual do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a8544-112">The current version of the Microsoft Windows Software Development Kit (SDK).</span></span>
-   <span data-ttu-id="a8544-113">A ferramenta de configuração de proxy para estabelecer as configurações de proxy para o Microsoft Windows HTTP Services (WinHTTP), se a conexão com a Internet for por meio de um servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="a8544-113">The proxy configuration tool to establish the proxy settings for Microsoft Windows HTTP Services (WinHTTP), if your connection to the Internet is through a proxy server.</span></span> <span data-ttu-id="a8544-114">Para obter mais informações, consulte [ProxyCfg.exe, uma ferramenta de configuração de proxy](proxycfg-exe--a-proxy-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="a8544-114">For more information, see [ProxyCfg.exe, a Proxy Configuration Tool](proxycfg-exe--a-proxy-configuration-tool.md).</span></span>
-   <span data-ttu-id="a8544-115">Familiaridade com a [terminologia](network-terminology.md) e os conceitos de rede.</span><span class="sxs-lookup"><span data-stu-id="a8544-115">A familiarity with [network terminology](network-terminology.md) and concepts.</span></span>

## <a name="retrieving-data-synchronously"></a><span data-ttu-id="a8544-116">Recuperando dados de forma síncrona</span><span class="sxs-lookup"><span data-stu-id="a8544-116">Retrieving Data Synchronously</span></span>

<span data-ttu-id="a8544-117">**Para criar um script que obtém o texto de uma página da Web de forma síncrona, faça o seguinte:**</span><span class="sxs-lookup"><span data-stu-id="a8544-117">**To create a script that obtains the text from a Web page synchronously, do the following:**</span></span>

1.  <span data-ttu-id="a8544-118">Abra um editor de texto.</span><span class="sxs-lookup"><span data-stu-id="a8544-118">Open a text editor.</span></span>
2.  <span data-ttu-id="a8544-119">Copie o código a seguir no editor de texto.</span><span class="sxs-lookup"><span data-stu-id="a8544-119">Copy the following code into the text editor.</span></span>

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

    

3.  <span data-ttu-id="a8544-120">Salve o arquivo como "Retrieve.js".</span><span class="sxs-lookup"><span data-stu-id="a8544-120">Save the file as "Retrieve.js".</span></span>
4.  <span data-ttu-id="a8544-121">Em um prompt de comando, digite "cscript Retrieve.js" e pressione ENTER.</span><span class="sxs-lookup"><span data-stu-id="a8544-121">From a command prompt, type "cscript Retrieve.js" and press ENTER.</span></span>

<span data-ttu-id="a8544-122">Agora você tem um script que usa um objeto [**WinHttpRequest**](winhttprequest.md) para obter o código-fonte HTML para a página da Web em https://www.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="a8544-122">You now have a script that uses a [**WinHttpRequest**](winhttprequest.md) object to obtain the HTML source code for the Web page at https://www.microsoft.com.</span></span> <span data-ttu-id="a8544-123">Talvez seja necessário aguardar vários segundos para que o código apareça.</span><span class="sxs-lookup"><span data-stu-id="a8544-123">You might have to wait several seconds for the code to appear.</span></span>

<span data-ttu-id="a8544-124">O aplicativo contém apenas uma função, "gettext".</span><span class="sxs-lookup"><span data-stu-id="a8544-124">The application contains only one function, "getText".</span></span> <span data-ttu-id="a8544-125">A primeira linha do script cria o objeto [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="a8544-125">The first line of the script creates the [**WinHttpRequest**](winhttprequest.md) object.</span></span>


```JScript
    // Create the WinHTTPRequest ActiveX Object.
    var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```



<span data-ttu-id="a8544-126">Quando o mecanismo JScript encontra essa linha, ele cria uma instância desse objeto.</span><span class="sxs-lookup"><span data-stu-id="a8544-126">When the JScript engine encounters this line, it creates an instance of this object.</span></span> <span data-ttu-id="a8544-127">Se você receber a mensagem de erro "o componente ActiveX não pode criar objeto", nessa linha, provavelmente a WinHttp.dll não foi corretamente registrada ou não está presente no sistema.</span><span class="sxs-lookup"><span data-stu-id="a8544-127">If you get the error message, "ActiveX component can't create object", on this line, most likely the WinHttp.dll was not properly registered or is not present on the system.</span></span>

<span data-ttu-id="a8544-128">A próxima linha do script chama o método [**Open**](iwinhttprequest-open.md) .</span><span class="sxs-lookup"><span data-stu-id="a8544-128">The next line of the script calls the [**Open**](iwinhttprequest-open.md) method.</span></span>


```JScript
    //  Create an HTTP request.
    WinHttpReq.Open("GET", "https://www.microsoft.com", false);
```



<span data-ttu-id="a8544-129">Três parâmetros especificam qual [*verbo http*](glossary.md) usar, o nome do recurso e se deseja usar o WinHTTP de forma síncrona ou assíncrona.</span><span class="sxs-lookup"><span data-stu-id="a8544-129">Three parameters specify which [*HTTP verb*](glossary.md) to use, the name of the resource, and whether to use WinHTTP synchronously or asynchronously.</span></span> <span data-ttu-id="a8544-130">Neste exemplo, o método está usando o *verbo http*"Get" para obter dados de https://www.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="a8544-130">In this example, the method is using the *HTTP verb*"GET" to obtain data from https://www.microsoft.com.</span></span> <span data-ttu-id="a8544-131">A especificação de **false** para o último parâmetro determina que a transação ocorre de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="a8544-131">Specifying **FALSE** for the last parameter determines that the transaction occurs synchronously.</span></span> <span data-ttu-id="a8544-132">O método [**Open**](iwinhttprequest-open.md) não estabelece uma conexão com o recurso, pois o nome pode implicar.</span><span class="sxs-lookup"><span data-stu-id="a8544-132">The [**Open**](iwinhttprequest-open.md) method does not establish a connection to the resource as the name might imply.</span></span> <span data-ttu-id="a8544-133">Em vez disso, ele inicializa as estruturas de dados internas que mantêm informações sobre a sessão, a conexão e a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a8544-133">Rather, it initializes the internal data structures that maintain information about the session, connection, and request.</span></span>

<span data-ttu-id="a8544-134">O método [**Send**](iwinhttprequest-send.md) monta os cabeçalhos de solicitação e envia a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a8544-134">The [**Send**](iwinhttprequest-send.md) method assembles the request headers and sends the request.</span></span> <span data-ttu-id="a8544-135">Quando chamado no modo síncrono, o método [**Send**](iwinhttprequest-send.md) também aguarda uma resposta antes de permitir que o aplicativo continue.</span><span class="sxs-lookup"><span data-stu-id="a8544-135">When called in synchronous mode, the [**Send**](iwinhttprequest-send.md) method also waits for a response before allowing the application to continue.</span></span>


```JScript
    // Send the HTTP request.
    WinHttpReq.Send();
```



<span data-ttu-id="a8544-136">Depois de enviar a solicitação, o script retorna o valor da propriedade [**ResponseText**](iwinhttprequest-responsetext.md) do objeto [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="a8544-136">After sending the request, the script returns the value of the [**ResponseText**](iwinhttprequest-responsetext.md) property of the [**WinHttpRequest**](winhttprequest.md) object.</span></span> <span data-ttu-id="a8544-137">Essa propriedade contém o corpo da entidade da resposta, nesse caso, a origem de um documento.</span><span class="sxs-lookup"><span data-stu-id="a8544-137">This property contains the entity body of the response, in this case, the source of a document.</span></span>


```JScript
    // Get the response text.
    return WinHttpReq.ResponseText;
```



<span data-ttu-id="a8544-138">A execução do script é pausada enquanto o texto inteiro do recurso é recuperado.</span><span class="sxs-lookup"><span data-stu-id="a8544-138">Execution of the script pauses while the entire text of the resource is retrieved.</span></span> <span data-ttu-id="a8544-139">O texto do recurso é retornado da função e exibido.</span><span class="sxs-lookup"><span data-stu-id="a8544-139">The resource text is returned from the function and displayed.</span></span>

<span data-ttu-id="a8544-140">O objeto [**WinHttpRequest**](winhttprequest.md) garante que todos os recursos internos alocados para a transação http sejam liberados.</span><span class="sxs-lookup"><span data-stu-id="a8544-140">The [**WinHttpRequest**](winhttprequest.md) object ensures that any internal resources that are allocated for the HTTP transaction are released.</span></span>

## <a name="retrieving-data-asynchronously"></a><span data-ttu-id="a8544-141">Recuperando dados de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="a8544-141">Retrieving Data Asynchronously</span></span>

<span data-ttu-id="a8544-142">Recuperar dados de maneira assíncrona usando o WinHTTP é muito semelhante a recuperar dados de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="a8544-142">Retrieving data asynchronously using WinHTTP is very similar to retrieving data synchronously.</span></span> <span data-ttu-id="a8544-143">Modifique o script da seção anterior fazendo duas pequenas alterações.</span><span class="sxs-lookup"><span data-stu-id="a8544-143">Modify the script from the previous section by making two small changes.</span></span>

1.  <span data-ttu-id="a8544-144">Defina o terceiro parâmetro do método [**Open**](iwinhttprequest-open.md) como "true" em vez de "false" para especificar que os métodos WinHTTP devem ser executados de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="a8544-144">Set the third parameter of the [**Open**](iwinhttprequest-open.md) method to "true" instead of "false" to specify that WinHTTP methods should be performed asynchronously.</span></span>
    ```JScript
       //  Create a HTTP request.
        var temp = WinHttpReq.Open("GET", strURL, true);
    ```

    

2.  <span data-ttu-id="a8544-145">Invoque o método [**WaitForResponse**](iwinhttprequest-waitforresponse.md) antes de acessar a propriedade [**ResponseText**](iwinhttprequest-responsetext.md) para garantir que toda a resposta tenha sido recebida.</span><span class="sxs-lookup"><span data-stu-id="a8544-145">Invoke the [**WaitForResponse**](iwinhttprequest-waitforresponse.md) method before accessing the [**ResponseText**](iwinhttprequest-responsetext.md) property to ensure that the entire response has been received.</span></span>
    ```JScript
        //  Send the HTTP request.
        WinHttpReq.Send();
            
        // Wait for the entire response.
        WinHttpReq.WaitForResponse();
            
        //  Retrieve the response text.
        strResult = WinHttpReq.ResponseText;
    ```

    

<span data-ttu-id="a8544-146">A principal vantagem de usar o WinHTTP de forma assíncrona no script é que o método [**Send**](iwinhttprequest-send.md) retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="a8544-146">The main advantage to using WinHTTP asynchronously in script is that the [**Send**](iwinhttprequest-send.md) method returns immediately.</span></span> <span data-ttu-id="a8544-147">A solicitação é preparada e enviada por um thread de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a8544-147">The request is prepared and sent by a worker thread.</span></span> <span data-ttu-id="a8544-148">Isso permite que seu aplicativo faça outras coisas enquanto está aguardando a resposta.</span><span class="sxs-lookup"><span data-stu-id="a8544-148">This enables your application to do other things while it is waiting for the response.</span></span> <span data-ttu-id="a8544-149">Antes de tentar acessar a resposta, verifique se toda a resposta foi recebida chamando o método [**WaitForResponse**](iwinhttprequest-waitforresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="a8544-149">Before attempting to access the response, ensure that the entire response has been received by calling the [**WaitForResponse**](iwinhttprequest-waitforresponse.md) method.</span></span> <span data-ttu-id="a8544-150">Caso contrário, poderá ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="a8544-150">Otherwise an error can occur.</span></span>

<span data-ttu-id="a8544-151">O método [**WaitForResponse**](iwinhttprequest-waitforresponse.md) também pode ser usado para especificar um valor de tempo limite para a transação.</span><span class="sxs-lookup"><span data-stu-id="a8544-151">The [**WaitForResponse**](iwinhttprequest-waitforresponse.md) method can also be used to specify a time-out value for the transaction.</span></span> <span data-ttu-id="a8544-152">Um parâmetro opcional permite que você especifique o valor de tempo limite em segundos.</span><span class="sxs-lookup"><span data-stu-id="a8544-152">An optional parameter enables you to specify the time-out value in seconds.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8544-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a8544-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8544-154">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="a8544-154">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="a8544-155">Solicitação de comentários de HTTP/1.1 (RFC 2616)</span><span class="sxs-lookup"><span data-stu-id="a8544-155">HTTP/1.1 Request for Comments (RFC 2616)</span></span>](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



