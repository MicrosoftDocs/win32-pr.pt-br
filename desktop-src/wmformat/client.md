---
title: Log de cliente (SDK do Windows Media Format 11)
description: Log de cliente
ms.assetid: 3e0d0fea-4370-41f8-b461-73a37de8d8bc
keywords:
- SDK do Windows Media Format, log do cliente
- Windows Media Format SDK, registro em log
- ASF (Advanced Systems Format), log de cliente
- ASF (formato de sistemas avançados), log de cliente
- ASF (Advanced Systems Format), registro em log
- ASF (formato de sistemas avançados), registro em log
- log de cliente
- registrando clientes em log
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856f2df4c2377b94edc40574c3e2efcced34aa81
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085038"
---
# <a name="client-logging-windows-media-format-11-sdk"></a><span data-ttu-id="c9045-111">Log de cliente (SDK do Windows Media Format 11)</span><span class="sxs-lookup"><span data-stu-id="c9045-111">Client Logging (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="c9045-112">Quando o objeto leitor lê dados de um servidor, ele envia informações de log para o servidor.</span><span class="sxs-lookup"><span data-stu-id="c9045-112">When the reader object reads data from a server, it sends logging information to the server.</span></span> <span data-ttu-id="c9045-113">Os provedores de conteúdo normalmente usam essas informações para medir a qualidade do serviço, gerar informações de cobrança ou acompanhar anúncios.</span><span class="sxs-lookup"><span data-stu-id="c9045-113">Content providers typically use this information to measure quality of service, generate billing information, or track advertising.</span></span> <span data-ttu-id="c9045-114">As informações de registro em log não contêm dados pessoais.</span><span class="sxs-lookup"><span data-stu-id="c9045-114">The logging information contains no personal data.</span></span>

<span data-ttu-id="c9045-115">O aplicativo pode especificar algumas das informações que são registradas, chamando o método [**IWMReaderAdvanced:: SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) no objeto Reader.</span><span class="sxs-lookup"><span data-stu-id="c9045-115">The application can specify some of the information that is logged, by calling the [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) method on the reader object.</span></span> <span data-ttu-id="c9045-116">Por exemplo, você pode especificar a cadeia de caracteres do agente do usuário, o nome do aplicativo de Player ou a página da Web que hospeda o Player.</span><span class="sxs-lookup"><span data-stu-id="c9045-116">For example, you can specify the user-agent string, the name of the player application, or the Web page that hosts the player.</span></span>

<span data-ttu-id="c9045-117">As informações de log incluem um GUID que identifica a sessão.</span><span class="sxs-lookup"><span data-stu-id="c9045-117">The logging information includes a GUID that identifies the session.</span></span> <span data-ttu-id="c9045-118">Por padrão, o leitor gera uma ID de sessão anônima.</span><span class="sxs-lookup"><span data-stu-id="c9045-118">By default, the reader generates an anonymous session ID.</span></span> <span data-ttu-id="c9045-119">Opcionalmente, o leitor pode, em vez disso, enviar uma ID que identifica exclusivamente o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="c9045-119">Optionally, the reader can instead send an ID that uniquely identifies the current user.</span></span> <span data-ttu-id="c9045-120">Para habilitar esse recurso, chame o método [**IWMReaderAdvanced2:: SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) com o valor **true**.</span><span class="sxs-lookup"><span data-stu-id="c9045-120">To enable this feature, call the [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) method with the value **TRUE**.</span></span>

<span data-ttu-id="c9045-121">Você pode configurar o objeto leitor para enviar as informações de log para outro servidor, além do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="c9045-121">You can configure the reader object to send the logging information to another server, in addition to the originating server.</span></span> <span data-ttu-id="c9045-122">Para fazer isso, chame o método [**IWMReaderNetworkConfig:: AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) com a URL do servidor.</span><span class="sxs-lookup"><span data-stu-id="c9045-122">To do so, call the [**IWMReaderNetworkConfig::AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) method with the URL of the server.</span></span> <span data-ttu-id="c9045-123">Essa URL deve apontar para um script ou executável que pode manipular solicitações HTTP GET e POST.</span><span class="sxs-lookup"><span data-stu-id="c9045-123">This URL should point to a script or executable that can handle HTTP GET and POST requests.</span></span> <span data-ttu-id="c9045-124">Você pode usar o agente de anúncio de log e multicast (wmsiislog.dll) ou pode gravar um script ASP ou CGI personalizado para receber os dados de log.</span><span class="sxs-lookup"><span data-stu-id="c9045-124">You can use the Multicast and Logging Advertisement Agent (wmsiislog.dll), or you can write a custom ASP or CGI script to receive the log data.</span></span>

> [!Note]  
> <span data-ttu-id="c9045-125">Você pode obter a mesma funcionalidade criando uma lista de reprodução no lado do servidor com um atributo **LogURL** .</span><span class="sxs-lookup"><span data-stu-id="c9045-125">You can get the same functionality by creating a server-side playlist with a **logURL** attribute.</span></span>

 

<span data-ttu-id="c9045-126">Quando o objeto do leitor envia o log, ele faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c9045-126">When the reader object sends the log, it does the following:</span></span>

1.  <span data-ttu-id="c9045-127">Envia uma solicitação GET vazia para o servidor.</span><span class="sxs-lookup"><span data-stu-id="c9045-127">Sends an empty GET request to the server.</span></span>
2.  <span data-ttu-id="c9045-128">Analisa a resposta do servidor para uma das seguintes cadeias de caracteres:</span><span class="sxs-lookup"><span data-stu-id="c9045-128">Parses the server response for one of the following strings:</span></span>
    -   `<body><h1>NetShow ISAPI Log Dll</h1>`
    -   <span data-ttu-id="c9045-129">`<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` onde "0.0.0.0" é qualquer número de versão válido.</span><span class="sxs-lookup"><span data-stu-id="c9045-129">`<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` where "0.0.0.0" is any valid version number.</span></span>
3.  <span data-ttu-id="c9045-130">Envia uma solicitação POST com as informações de log.</span><span class="sxs-lookup"><span data-stu-id="c9045-130">Sends a POST request with the log information.</span></span>

<span data-ttu-id="c9045-131">O código a seguir mostra um exemplo de script ASP que recebe as informações de registro em log e grava-as em um arquivo:</span><span class="sxs-lookup"><span data-stu-id="c9045-131">The following code shows an example ASP script that receives the logging information and writes it to a file:</span></span>


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



<span data-ttu-id="c9045-132">Você pode especificar vários servidores para receber informações de registro em log; Basta chamar **AddLoggingUrl** uma vez com cada URL.</span><span class="sxs-lookup"><span data-stu-id="c9045-132">You can specify multiple servers to receive logging information; just call **AddLoggingUrl** once with each URL.</span></span> <span data-ttu-id="c9045-133">Para limpar a lista de servidores que recebem logs, chame o método [**IWMReaderNetworkConfig:: ResetLoggingUrlList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) .</span><span class="sxs-lookup"><span data-stu-id="c9045-133">To clear the list of servers that receive logs, call the [**IWMReaderNetworkConfig::ResetLoggingUrlList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9045-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9045-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9045-135">**Implementando a funcionalidade de rede**</span><span class="sxs-lookup"><span data-stu-id="c9045-135">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> <dt>

[<span data-ttu-id="c9045-136">**Interface IWMReaderAdvanced**</span><span class="sxs-lookup"><span data-stu-id="c9045-136">**IWMReaderAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)
</dt> <dt>

[<span data-ttu-id="c9045-137">**Interface IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="c9045-137">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




