---
description: Este tópico descreve as dicas de solução de problemas para usar as APIs do agente de autenticação da Web para suas páginas da Web.
ms.assetid: 25A024AA-9A70-40A5-BF5E-452FD148D0D2
title: Problemas de autenticação da Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc4611461effd9cbc5546059e71fc8ca3f1f0be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557586"
---
# <a name="web-authentication-problems"></a><span data-ttu-id="7658a-103">Problemas de autenticação da Web</span><span class="sxs-lookup"><span data-stu-id="7658a-103">Web authentication problems</span></span>

<span data-ttu-id="7658a-104">Este tópico descreve as dicas de solução de problemas para usar as APIs do agente de autenticação da Web para suas páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="7658a-104">This topic describes troubleshooting tips for using the Web Authentication Broker APIs for your web pages.</span></span>

-   [<span data-ttu-id="7658a-105">Logs operacionais</span><span class="sxs-lookup"><span data-stu-id="7658a-105">Operational logs</span></span>](#operational-logs)
-   [<span data-ttu-id="7658a-106">Usando o Fiddler com o agente de autenticação da Web</span><span class="sxs-lookup"><span data-stu-id="7658a-106">Using Fiddler with Web Authentication Broker</span></span>](#using-fiddler-with-web-authentication-broker)
-   [<span data-ttu-id="7658a-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7658a-107">Related topics</span></span>](#related-topics)

## <a name="operational-logs"></a><span data-ttu-id="7658a-108">Logs operacionais</span><span class="sxs-lookup"><span data-stu-id="7658a-108">Operational logs</span></span>

<span data-ttu-id="7658a-109">Geralmente é possível determinar o que não está funcionando usando logs operacionais.</span><span class="sxs-lookup"><span data-stu-id="7658a-109">Often you can determine what is not working by using the operational logs.</span></span> <span data-ttu-id="7658a-110">Há um canal de log de eventos dedicado Microsoft-Windows-webauth \\ operacional que permite aos desenvolvedores de sites entender como suas páginas da Web estão sendo processadas pelo agente de autenticação da Web.</span><span class="sxs-lookup"><span data-stu-id="7658a-110">There is a dedicated event log channel Microsoft-Windows-WebAuth\\Operational that allows website developers to understand how their web pages are being processed by the Web Authentication Broker.</span></span> <span data-ttu-id="7658a-111">Para habilitá-lo, inicie o eventvwr.exe e habilite o log operacional no aplicativo e serviços \\ Microsoft \\ Windows \\ webauth.</span><span class="sxs-lookup"><span data-stu-id="7658a-111">To enable it, launch eventvwr.exe and enable Operational log under the Application and Services\\Microsoft\\Windows\\WebAuth.</span></span> <span data-ttu-id="7658a-112">Além disso, o agente de autenticação da Web acrescenta uma cadeia de caracteres exclusiva à cadeia de caracteres do agente do usuário para se identificar no servidor Web.</span><span class="sxs-lookup"><span data-stu-id="7658a-112">Also, the Web Authentication Broker appends a unique string to the user agent string to identify itself on the web server.</span></span> <span data-ttu-id="7658a-113">A cadeia de caracteres é "MSAuthHost/1.0".</span><span class="sxs-lookup"><span data-stu-id="7658a-113">The string is "MSAuthHost/1.0".</span></span> <span data-ttu-id="7658a-114">Observe que o número da versão pode mudar no futuro, portanto você não deve depender do número daquela versão no seu código.</span><span class="sxs-lookup"><span data-stu-id="7658a-114">Note that the version number may change in the future, so you should not to depend on that version number in your code.</span></span> <span data-ttu-id="7658a-115">Um exemplo da cadeia de caracteres do agente de usuário completo é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7658a-115">An example of the full user agent string is as follows:</span></span>

`User-Agent: Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.2; Win64; x64; Trident/6.0; MSAuthHost/1.0)`

<span data-ttu-id="7658a-116">Exemplo de uso de logs operacionais</span><span class="sxs-lookup"><span data-stu-id="7658a-116">Example of using operational logs</span></span>

1.  <span data-ttu-id="7658a-117">Habilitar logs operacionais</span><span class="sxs-lookup"><span data-stu-id="7658a-117">Enable operational logs</span></span>
2.  <span data-ttu-id="7658a-118">Executar o aplicativo social da contoso</span><span class="sxs-lookup"><span data-stu-id="7658a-118">Run Contoso social application</span></span>![visualizador de Eventos exibindo logs operacionais do webauth](images/wab-figure15.png)
3.  <span data-ttu-id="7658a-120">As entradas de logs geradas podem ser usadas para entender o comportamento do agente de autenticação da Web com mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="7658a-120">The generated logs entries can be used to understand the behavior of Web Authentication Broker in greater detail.</span></span> <span data-ttu-id="7658a-121">Nesse caso, elas podem ser:</span><span class="sxs-lookup"><span data-stu-id="7658a-121">In this case, these can include:</span></span>
    -   <span data-ttu-id="7658a-122">Início da Navegação: registra quando o AuthHost é iniciado e contém informações sobre as URLs de início e término.</span><span class="sxs-lookup"><span data-stu-id="7658a-122">Navigation Start: Logs when the AuthHost is started and contains information about the start and termination URLs.</span></span>
    -   ![ilustra os detalhes do início da navegação](images/wab-figure16.png)
    -   <span data-ttu-id="7658a-124">Navegação Completa: registra a conclusão do carregamento de uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="7658a-124">Navigation Complete: Logs the completion of loading a web page.</span></span>
    -   <span data-ttu-id="7658a-125">Marca meta: registra quando uma marca meta é encontrada, incluindo os detalhes.</span><span class="sxs-lookup"><span data-stu-id="7658a-125">Meta Tag: Logs when a meta-tag is encountered including the details.</span></span>
    -   <span data-ttu-id="7658a-126">Término da Navegação: navegação encerrada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="7658a-126">Navigation Terminate: Navigation terminated by the user.</span></span>
    -   <span data-ttu-id="7658a-127">Erro de Navegação: o AuthHost encontra um erro de navegação em uma URL, incluindo HttpStatusCode.</span><span class="sxs-lookup"><span data-stu-id="7658a-127">Navigation Error: AuthHost encounters a navigation error at a URL including HttpStatusCode.</span></span>
    -   <span data-ttu-id="7658a-128">Final da Navegação: a URL de término é encontrada.</span><span class="sxs-lookup"><span data-stu-id="7658a-128">Navigation End: Terminating URL is encountered.</span></span>

## <a name="using-fiddler-with-web-authentication-broker"></a><span data-ttu-id="7658a-129">Usando o Fiddler com o agente de autenticação da Web</span><span class="sxs-lookup"><span data-stu-id="7658a-129">Using Fiddler with Web Authentication Broker</span></span>

<span data-ttu-id="7658a-130">O depurador da Web do Fiddler pode ser usado com aplicativos do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7658a-130">The Fiddler web debugger can be used with Windows 8 apps.</span></span>

1.  <span data-ttu-id="7658a-131">Por o AuthHost executar no seu próprio contêiner de aplicativo para dar maior capacidade de rede privada, você deve definir uma chave de registro: Windows Registry Editor Version 5.00</span><span class="sxs-lookup"><span data-stu-id="7658a-131">Since the AuthHost runs in its own app container to give it the private network capability, you must set a registry key: Windows Registry Editor Version 5.00</span></span>

    <span data-ttu-id="7658a-132">**HKEY \_ \_** \\  \\ Opções de execução de arquivo de imagem **do Microsoft** \\ **Windows NT** CurrentVersion de máquina local \\  \\  \\ **authhost.exe** \\ **EnablePrivateNetwork** = 00000001</span><span class="sxs-lookup"><span data-stu-id="7658a-132">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**Image File Execution Options**\\**authhost.exe**\\**EnablePrivateNetwork** = 00000001</span></span><dl> <dt>

                     Data type
</dt> <dd>                     <span data-ttu-id="7658a-133">DWORD</span><span class="sxs-lookup"><span data-stu-id="7658a-133">DWORD</span></span></dd> </dl>

2.  <span data-ttu-id="7658a-134">Adicione uma regra para o AuthHost, uma vez que é ele quem gera o tráfego de saída.</span><span class="sxs-lookup"><span data-stu-id="7658a-134">Add a rule for the AuthHost as this is what is generating the outbound traffic.</span></span>
    ```cmd
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.a.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
    D:\Windows\System32>CheckNetIsolation.exe LoopbackExempt -s
    List Loopback Exempted AppContainers
    [1] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
        SID:  S-1-15-2-1973105767-3975693666-32999980-3747492175-1074076486-3102532000-500629349
    [2] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
        SID:  S-1-15-2-166260-4150837609-3669066492-3071230600-3743290616-3683681078-2492089544
    [3] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.a.p_8wekyb3d8bbwe
        SID:  S-1-15-2-3506084497-1208594716-3384433646-2514033508-1838198150-1980605558-3480344935
    ```

    

3.  <span data-ttu-id="7658a-135">Adicione uma regra de firewall para o tráfego de entrada ao Fiddler.</span><span class="sxs-lookup"><span data-stu-id="7658a-135">Add a firewall rule for incoming traffic to Fiddler.</span></span>

<span data-ttu-id="7658a-136">Para obter mais informações, consulte o [blog sobre como usar o depurador da Web do Fiddler com aplicativos da Windows Store](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications).</span><span class="sxs-lookup"><span data-stu-id="7658a-136">For more information, see [Blog on using Fiddler web debugger with Windows Store apps](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7658a-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7658a-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7658a-138">Considerações para o desenvolvimento de páginas da Web</span><span class="sxs-lookup"><span data-stu-id="7658a-138">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="7658a-139">Perguntas frequentes sobre o agente de autenticação da Web</span><span class="sxs-lookup"><span data-stu-id="7658a-139">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.md)
</dt> <dt>

[<span data-ttu-id="7658a-140">Aplicativo de exemplo do SDK do agente de autenticação da Web</span><span class="sxs-lookup"><span data-stu-id="7658a-140">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="7658a-141">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="7658a-141">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041)
</dt> </dl>

 

 
