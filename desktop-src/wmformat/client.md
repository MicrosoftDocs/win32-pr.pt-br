---
title: Log do cliente (Windows Media Format SDK 11)
description: Saiba mais sobre o registro em log do Windows Media Format 11 SDK. O registro em log fornece uma maneira para o servidor de mídia acompanhar a atividade dos clientes que se conectam a ele.
ms.assetid: 3e0d0fea-4370-41f8-b461-73a37de8d8bc
keywords:
- Windows Media Format SDK, registro em log do cliente
- Windows Media Format SDK, registro em log
- ASF (Advanced Systems Format), registro em log do cliente
- ASF (Formato de Sistemas Avançados), registro em log do cliente
- FORMATO DE SISTEMAS Avançados (ASF), registro em log
- ASF (Formato de Sistemas Avançados), registro em log
- registro em log do cliente
- registrando clientes em log
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095e01fcf0730fdec8d06a931a9a988ca79ea77f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406259"
---
# <a name="client-logging-windows-media-format-11-sdk"></a><span data-ttu-id="90c1c-112">Log do cliente (Windows Media Format SDK 11)</span><span class="sxs-lookup"><span data-stu-id="90c1c-112">Client Logging (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="90c1c-113">Quando o objeto leitor lê dados de um servidor, ele envia informações de log para o servidor.</span><span class="sxs-lookup"><span data-stu-id="90c1c-113">When the reader object reads data from a server, it sends logging information to the server.</span></span> <span data-ttu-id="90c1c-114">Os provedores de conteúdo normalmente usam essas informações para medir a qualidade do serviço, gerar informações de cobrança ou acompanhar a publicidade.</span><span class="sxs-lookup"><span data-stu-id="90c1c-114">Content providers typically use this information to measure quality of service, generate billing information, or track advertising.</span></span> <span data-ttu-id="90c1c-115">As informações de log não contêm dados pessoais.</span><span class="sxs-lookup"><span data-stu-id="90c1c-115">The logging information contains no personal data.</span></span>

<span data-ttu-id="90c1c-116">O aplicativo pode especificar algumas das informações registradas, chamando o método [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) no objeto de leitor.</span><span class="sxs-lookup"><span data-stu-id="90c1c-116">The application can specify some of the information that is logged, by calling the [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) method on the reader object.</span></span> <span data-ttu-id="90c1c-117">Por exemplo, você pode especificar a cadeia de caracteres user-agent, o nome do aplicativo player ou a página da Web que hospeda o player.</span><span class="sxs-lookup"><span data-stu-id="90c1c-117">For example, you can specify the user-agent string, the name of the player application, or the Web page that hosts the player.</span></span>

<span data-ttu-id="90c1c-118">As informações de log incluem um GUID que identifica a sessão.</span><span class="sxs-lookup"><span data-stu-id="90c1c-118">The logging information includes a GUID that identifies the session.</span></span> <span data-ttu-id="90c1c-119">Por padrão, o leitor gera uma ID de sessão anônima.</span><span class="sxs-lookup"><span data-stu-id="90c1c-119">By default, the reader generates an anonymous session ID.</span></span> <span data-ttu-id="90c1c-120">Opcionalmente, o leitor pode enviar uma ID que identifica exclusivamente o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="90c1c-120">Optionally, the reader can instead send an ID that uniquely identifies the current user.</span></span> <span data-ttu-id="90c1c-121">Para habilitar esse recurso, chame o método [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) com o **valor TRUE.**</span><span class="sxs-lookup"><span data-stu-id="90c1c-121">To enable this feature, call the [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) method with the value **TRUE**.</span></span>

<span data-ttu-id="90c1c-122">Você pode configurar o objeto de leitor para enviar as informações de log para outro servidor, além do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="90c1c-122">You can configure the reader object to send the logging information to another server, in addition to the originating server.</span></span> <span data-ttu-id="90c1c-123">Para fazer isso, chame o método [**IWMReaderNetworkConfig::AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) com a URL do servidor.</span><span class="sxs-lookup"><span data-stu-id="90c1c-123">To do so, call the [**IWMReaderNetworkConfig::AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) method with the URL of the server.</span></span> <span data-ttu-id="90c1c-124">Essa URL deve apontar para um script ou executável que possa lidar com solicitações HTTP GET e POST.</span><span class="sxs-lookup"><span data-stu-id="90c1c-124">This URL should point to a script or executable that can handle HTTP GET and POST requests.</span></span> <span data-ttu-id="90c1c-125">Você pode usar o Agente de Anúncio multicast e log (wmsiislog.dll) ou pode escrever um script ASP ou CGI personalizado para receber os dados de log.</span><span class="sxs-lookup"><span data-stu-id="90c1c-125">You can use the Multicast and Logging Advertisement Agent (wmsiislog.dll), or you can write a custom ASP or CGI script to receive the log data.</span></span>

> [!Note]  
> <span data-ttu-id="90c1c-126">Você pode obter a mesma funcionalidade criando uma playlist do lado do servidor com um **atributo logURL.**</span><span class="sxs-lookup"><span data-stu-id="90c1c-126">You can get the same functionality by creating a server-side playlist with a **logURL** attribute.</span></span>

 

<span data-ttu-id="90c1c-127">Quando o objeto de leitor envia o log, ele faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="90c1c-127">When the reader object sends the log, it does the following:</span></span>

1.  <span data-ttu-id="90c1c-128">Envia uma solicitação GET vazia para o servidor.</span><span class="sxs-lookup"><span data-stu-id="90c1c-128">Sends an empty GET request to the server.</span></span>
2.  <span data-ttu-id="90c1c-129">Analisar a resposta do servidor para uma das seguintes cadeias de caracteres:</span><span class="sxs-lookup"><span data-stu-id="90c1c-129">Parses the server response for one of the following strings:</span></span>
    -   `<body><h1>NetShow ISAPI Log Dll</h1>`
    -   <span data-ttu-id="90c1c-130">`<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` em que "0.0.0.0" é qualquer número de versão válido.</span><span class="sxs-lookup"><span data-stu-id="90c1c-130">`<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` where "0.0.0.0" is any valid version number.</span></span>
3.  <span data-ttu-id="90c1c-131">Envia uma solicitação POST com as informações de log.</span><span class="sxs-lookup"><span data-stu-id="90c1c-131">Sends a POST request with the log information.</span></span>

<span data-ttu-id="90c1c-132">O código a seguir mostra um script ASP de exemplo que recebe as informações de registro em log e as grava em um arquivo:</span><span class="sxs-lookup"><span data-stu-id="90c1c-132">The following code shows an example ASP script that receives the logging information and writes it to a file:</span></span>


```
<html>
<body>
<h1>WMS ISAPI Log Dll/9.00.00.00.00</h1>
<%@ Language=VBScript %>
<%
  Dim temp, i, post, file, fso

  ' Convert the binary data to a string.
  For i = 1 To Request.TotalBytes
    temp = Request.BinaryRead(1)
    pose = pose & Chr(AscB(temp))
  Next

  Set fso = createobject("Scripting.FileSystemObject")
  Set file = fso.OpenTextFile("C:\log.txt", 8, TRUE)

  file.writeline Now
  file.writeline post
  file.writeBlankLines 2 
%>
</body>
</html>
```



<span data-ttu-id="90c1c-133">Você pode especificar vários servidores para receber informações de log; basta chamar **AddLoggingUrl** uma vez com cada URL.</span><span class="sxs-lookup"><span data-stu-id="90c1c-133">You can specify multiple servers to receive logging information; just call **AddLoggingUrl** once with each URL.</span></span> <span data-ttu-id="90c1c-134">Para limpar a lista de servidores que recebem logs, chame o [**método IWMReaderNetworkConfig::ResetLoggingUrlList.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist)</span><span class="sxs-lookup"><span data-stu-id="90c1c-134">To clear the list of servers that receive logs, call the [**IWMReaderNetworkConfig::ResetLoggingUrlList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90c1c-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="90c1c-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90c1c-136">**Implementando a funcionalidade de rede**</span><span class="sxs-lookup"><span data-stu-id="90c1c-136">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> <dt>

[<span data-ttu-id="90c1c-137">**IWMReaderAdvanced Interface**</span><span class="sxs-lookup"><span data-stu-id="90c1c-137">**IWMReaderAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)
</dt> <dt>

[<span data-ttu-id="90c1c-138">**IWMReaderAdvanced2 Interface**</span><span class="sxs-lookup"><span data-stu-id="90c1c-138">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




