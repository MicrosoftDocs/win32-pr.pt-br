---
description: Os logs de WinHTTP podem ser usados para ajudar a solucionar problemas de aplicativos WSDAPI. Isso é útil quando a troca de metadados falha ou quando a negociação SSL/TLS falha.
ms.assetid: 75ba330d-afcd-4d8f-93c7-a1b9f80dd050
title: Capturando logs do WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378801e97b2eef8c1ea0c40a5973844d75a94e02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091368"
---
# <a name="capturing-winhttp-logs"></a><span data-ttu-id="c51cf-104">Capturando logs do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="c51cf-104">Capturing WinHTTP Logs</span></span>

<span data-ttu-id="c51cf-105">Os logs de [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) podem ser usados para ajudar a solucionar problemas de aplicativos WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="c51cf-105">[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) logs can be used to help troubleshoot WSDAPI applications.</span></span> <span data-ttu-id="c51cf-106">Isso é útil quando a troca de metadados falha ou quando a negociação SSL/TLS falha.</span><span class="sxs-lookup"><span data-stu-id="c51cf-106">This is helpful when metadata exchange fails or when SSL/TLS negotiation fails.</span></span>

<span data-ttu-id="c51cf-107">Este procedimento mostra como capturar logs do WinHTTP no PC cliente.</span><span class="sxs-lookup"><span data-stu-id="c51cf-107">This procedure shows how to capture WinHTTP logs on the client PC.</span></span> <span data-ttu-id="c51cf-108">O aplicativo cliente baseado em WSDAPI não deve estar em execução quando o log está habilitado.</span><span class="sxs-lookup"><span data-stu-id="c51cf-108">The WSDAPI-based client application must not be running when logging is enabled.</span></span> <span data-ttu-id="c51cf-109">Se o aplicativo cliente estiver em execução quando o log estiver habilitado, o cliente e/ou o PC deverão ser reiniciados antes de WS-Discovery e o tráfego de troca de metadados aparecerá nos logs do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="c51cf-109">If the client application is running when logging is enabled, the client and/or the PC must be restarted before WS-Discovery and metadata exchange traffic will appear in the WinHTTP logs.</span></span>

<span data-ttu-id="c51cf-110">**Para capturar logs do WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="c51cf-110">**To capture WinHTTP logs**</span></span>

1.  <span data-ttu-id="c51cf-111">Abra uma janela de prompt de comandos com privilégios elevados no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="c51cf-111">Open an elevated command prompt window on the client PC.</span></span>
2.  <span data-ttu-id="c51cf-112">Execute o seguinte comando: **netsh WinHTTP set tracing Trace-File-prefixo = "C: \\ temp \\ DPWS" level = verbose Format = estado ANSI = Enabled Max-Trace-File-Size = 1073741824**</span><span class="sxs-lookup"><span data-stu-id="c51cf-112">Run the following command: **netsh winhttp set tracing trace-file-prefix="C:\\Temp\\dpws" level=verbose format=ansi state=enabled max-trace-file-size=1073741824**</span></span>

    <span data-ttu-id="c51cf-113">Esse comando habilita o log do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="c51cf-113">This command enables WinHTTP logging.</span></span> <span data-ttu-id="c51cf-114">Todos os arquivos de log serão armazenados no diretório C: \\ temp e os nomes de arquivo começarão com o prefixo DPWS.</span><span class="sxs-lookup"><span data-stu-id="c51cf-114">All log files will be stored in the C:\\Temp directory, and the filenames will begin with the dpws prefix.</span></span> <span data-ttu-id="c51cf-115">No máximo 1 GB de arquivos de log serão armazenados.</span><span class="sxs-lookup"><span data-stu-id="c51cf-115">At most 1 GB of log files will be stored.</span></span>

3.  <span data-ttu-id="c51cf-116">Se o processo que usa o WinHTTP no cliente já estiver em execução, reinicie o computador.</span><span class="sxs-lookup"><span data-stu-id="c51cf-116">If the process using WinHTTP on the client is already running, restart the computer.</span></span> <span data-ttu-id="c51cf-117">Por exemplo, se as APIs de [descoberta de função](/previous-versions/windows/desktop/fundisc/fd-portal) estiverem sendo usadas, o computador deverá ser reiniciado.</span><span class="sxs-lookup"><span data-stu-id="c51cf-117">For example, if the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) APIs are being used, the computer must be restarted.</span></span> <span data-ttu-id="c51cf-118">As APIs de descoberta de função chamam WinHTTP de dentro de um host de serviço, que pode já ter começado quando o rastreamento foi habilitado.</span><span class="sxs-lookup"><span data-stu-id="c51cf-118">The Function Discovery APIs call WinHTTP from inside a service host, which may have already started when tracing was enabled.</span></span>
4.  <span data-ttu-id="c51cf-119">Inicie o aplicativo cliente baseado em WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="c51cf-119">Start the WSDAPI-based client application.</span></span> <span data-ttu-id="c51cf-120">O aplicativo que está sendo depurado ou o cliente de depuração WSD pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="c51cf-120">The application being debugged or the WSD Debug Client can be used.</span></span>
5.  <span data-ttu-id="c51cf-121">Reproduzir a falha do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c51cf-121">Reproduce the application failure.</span></span>
6.  <span data-ttu-id="c51cf-122">Encerrar o aplicativo cliente baseado em WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="c51cf-122">Terminate the WSDAPI-based client application.</span></span>
7.  <span data-ttu-id="c51cf-123">Se o processo que usa o WinHTTP não for encerrado com o aplicativo cliente, reinicie o computador.</span><span class="sxs-lookup"><span data-stu-id="c51cf-123">If the process using WinHTTP is not terminated with the client application, restart the computer.</span></span> <span data-ttu-id="c51cf-124">Por exemplo, se as APIs de [descoberta de função](/previous-versions/windows/desktop/fundisc/fd-portal) estiverem sendo usadas, o computador deverá ser reiniciado.</span><span class="sxs-lookup"><span data-stu-id="c51cf-124">For example, if the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) APIs are being used, the computer must be restarted.</span></span>
8.  <span data-ttu-id="c51cf-125">Execute o seguinte comando: **netsh WinHTTP definir estado de rastreamento = desabilitado**</span><span class="sxs-lookup"><span data-stu-id="c51cf-125">Run the following command: **netsh winhttp set tracing state=disabled**</span></span>

    <span data-ttu-id="c51cf-126">Este comando desabilita o log do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="c51cf-126">This command disables WinHTTP logging.</span></span>

9.  <span data-ttu-id="c51cf-127">Inspecione os logs do DPWS em C: \\ temp e verifique se as solicitações e mensagens necessárias foram enviadas.</span><span class="sxs-lookup"><span data-stu-id="c51cf-127">Inspect the DPWS logs in C:\\Temp and verify that the required requests and messages were sent.</span></span>
10. <span data-ttu-id="c51cf-128">Se a comunicação de canal seguro (HTTPS) estiver sendo usada, verifique se há falhas de SSL/TLS.</span><span class="sxs-lookup"><span data-stu-id="c51cf-128">If secure channel (HTTPS) communication is being used, check for SSL/TLS failures.</span></span>

<span data-ttu-id="c51cf-129">Depois que os logs do WinHTTP tiverem sido capturados, os logs poderão ser examinados para procurar a causa de uma falha do aplicativo WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="c51cf-129">Once WinHTTP logs have been captured, the logs can be examined to look for the cause of a WSDAPI application failure.</span></span> <span data-ttu-id="c51cf-130">Observe que o editor de texto usado para exibir esses logs deve ser executado como administrador.</span><span class="sxs-lookup"><span data-stu-id="c51cf-130">Note that the text editor used to view these logs must be run as Administrator.</span></span> <span data-ttu-id="c51cf-131">Para obter mais informações, consulte [usando o log do WinHTTP para verificar se há tráfego](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="c51cf-131">For more information, see [Using WinHTTP Logging to Verify Get Traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c51cf-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c51cf-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c51cf-133">WinHTTP</span><span class="sxs-lookup"><span data-stu-id="c51cf-133">WinHTTP</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[<span data-ttu-id="c51cf-134">Usando o log do WinHTTP para verificar o tráfego de obtenção</span><span class="sxs-lookup"><span data-stu-id="c51cf-134">Using WinHTTP Logging to Verify Get Traffic</span></span>](using-winhttp-logging-to-verify-get-traffic.md)
</dt>
</dl>
