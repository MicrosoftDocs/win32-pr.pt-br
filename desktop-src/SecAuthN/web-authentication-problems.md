---
description: Este tópico descreve dicas de solução de problemas para usar as APIs do Agente de Autenticação da Web para suas páginas da Web.
ms.assetid: 25A024AA-9A70-40A5-BF5E-452FD148D0D2
title: Problemas de autenticação da Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f996527c58b9620b8417ac3e6cdd6e0f61bd5217
ms.sourcegitcommit: 6377cd944d1f09f2dfe5727170ca8b330c8235bf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/07/2021
ms.locfileid: "113353659"
---
# <a name="web-authentication-problems"></a><span data-ttu-id="61e77-103">Problemas de autenticação da Web</span><span class="sxs-lookup"><span data-stu-id="61e77-103">Web authentication problems</span></span>

<span data-ttu-id="61e77-104">Este tópico descreve dicas de solução de problemas para usar as APIs do Agente de Autenticação da Web para suas páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="61e77-104">This topic describes troubleshooting tips for using the Web Authentication Broker APIs for your web pages.</span></span>

-   [<span data-ttu-id="61e77-105">Logs operacionais</span><span class="sxs-lookup"><span data-stu-id="61e77-105">Operational logs</span></span>](#operational-logs)
-   [<span data-ttu-id="61e77-106">Usando o Fiddler com o Agente de Autenticação da Web</span><span class="sxs-lookup"><span data-stu-id="61e77-106">Using Fiddler with Web Authentication Broker</span></span>](#using-fiddler-with-web-authentication-broker)
-   [<span data-ttu-id="61e77-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="61e77-107">Related topics</span></span>](#related-topics)

## <a name="operational-logs"></a><span data-ttu-id="61e77-108">Logs operacionais</span><span class="sxs-lookup"><span data-stu-id="61e77-108">Operational logs</span></span>

<span data-ttu-id="61e77-109">Geralmente é possível determinar o que não está funcionando usando logs operacionais.</span><span class="sxs-lookup"><span data-stu-id="61e77-109">Often you can determine what is not working by using the operational logs.</span></span> <span data-ttu-id="61e77-110">Há um canal de log de eventos dedicado Microsoft-Windows-WebAuth Operational que permite aos desenvolvedores de sites entender como suas páginas da Web estão sendo processadas pelo Agente de Autenticação \\ da Web.</span><span class="sxs-lookup"><span data-stu-id="61e77-110">There is a dedicated event log channel Microsoft-Windows-WebAuth\\Operational that allows website developers to understand how their web pages are being processed by the Web Authentication Broker.</span></span> <span data-ttu-id="61e77-111">Para habilita-lo, eventvwr.exe e habilitar o log operacional no Aplicativo e Serviços \\ Microsoft \\ Windows \\ WebAuth.</span><span class="sxs-lookup"><span data-stu-id="61e77-111">To enable it, launch eventvwr.exe and enable Operational log under the Application and Services\\Microsoft\\Windows\\WebAuth.</span></span> <span data-ttu-id="61e77-112">Além disso, o Agente de Autenticação da Web anexa uma cadeia de caracteres exclusiva à cadeia de caracteres do agente do usuário para se identificar no servidor Web.</span><span class="sxs-lookup"><span data-stu-id="61e77-112">Also, the Web Authentication Broker appends a unique string to the user agent string to identify itself on the web server.</span></span> <span data-ttu-id="61e77-113">A cadeia de caracteres é "MSAuthHost/1.0".</span><span class="sxs-lookup"><span data-stu-id="61e77-113">The string is "MSAuthHost/1.0".</span></span> <span data-ttu-id="61e77-114">Observe que o número da versão pode mudar no futuro, portanto você não deve depender do número daquela versão no seu código.</span><span class="sxs-lookup"><span data-stu-id="61e77-114">Note that the version number may change in the future, so you should not to depend on that version number in your code.</span></span> <span data-ttu-id="61e77-115">Um exemplo da cadeia de caracteres de agente de usuário completa é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="61e77-115">An example of the full user agent string is as follows:</span></span>

`User-Agent: Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.2; Win64; x64; Trident/6.0; MSAuthHost/1.0)`

<span data-ttu-id="61e77-116">Exemplo de uso de logs operacionais</span><span class="sxs-lookup"><span data-stu-id="61e77-116">Example of using operational logs</span></span>

1.  <span data-ttu-id="61e77-117">Habilitar logs operacionais</span><span class="sxs-lookup"><span data-stu-id="61e77-117">Enable operational logs</span></span>
2.  <span data-ttu-id="61e77-118">Executar aplicativo social da Contoso</span><span class="sxs-lookup"><span data-stu-id="61e77-118">Run Contoso social application</span></span>![visualizador de Eventos exibindo logs operacionais do webauth](images/wab-figure15.png)
3.  <span data-ttu-id="61e77-120">As entradas de logs geradas podem ser usadas para entender o comportamento do Agente de Autenticação da Web em mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="61e77-120">The generated logs entries can be used to understand the behavior of Web Authentication Broker in greater detail.</span></span> <span data-ttu-id="61e77-121">Nesse caso, elas podem ser:</span><span class="sxs-lookup"><span data-stu-id="61e77-121">In this case, these can include:</span></span>
    -   <span data-ttu-id="61e77-122">Início da Navegação: registra quando o AuthHost é iniciado e contém informações sobre as URLs de início e término.</span><span class="sxs-lookup"><span data-stu-id="61e77-122">Navigation Start: Logs when the AuthHost is started and contains information about the start and termination URLs.</span></span>
    -   ![ilustra os detalhes do início da navegação](images/wab-figure16.png)
    -   <span data-ttu-id="61e77-124">Navegação Completa: registra a conclusão do carregamento de uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="61e77-124">Navigation Complete: Logs the completion of loading a web page.</span></span>
    -   <span data-ttu-id="61e77-125">Marca meta: registra quando uma marca meta é encontrada, incluindo os detalhes.</span><span class="sxs-lookup"><span data-stu-id="61e77-125">Meta Tag: Logs when a meta-tag is encountered including the details.</span></span>
    -   <span data-ttu-id="61e77-126">Término da Navegação: navegação encerrada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="61e77-126">Navigation Terminate: Navigation terminated by the user.</span></span>
    -   <span data-ttu-id="61e77-127">Erro de Navegação: o AuthHost encontra um erro de navegação em uma URL, incluindo HttpStatusCode.</span><span class="sxs-lookup"><span data-stu-id="61e77-127">Navigation Error: AuthHost encounters a navigation error at a URL including HttpStatusCode.</span></span>
    -   <span data-ttu-id="61e77-128">Final da Navegação: a URL de término é encontrada.</span><span class="sxs-lookup"><span data-stu-id="61e77-128">Navigation End: Terminating URL is encountered.</span></span>

## <a name="using-fiddler-with-web-authentication-broker"></a><span data-ttu-id="61e77-129">Usando o Fiddler com o Agente de Autenticação da Web</span><span class="sxs-lookup"><span data-stu-id="61e77-129">Using Fiddler with Web Authentication Broker</span></span>

<span data-ttu-id="61e77-130">O depurador da Web fiddler pode ser usado com Windows 8 aplicativos.</span><span class="sxs-lookup"><span data-stu-id="61e77-130">The Fiddler web debugger can be used with Windows 8 apps.</span></span>

1.  <span data-ttu-id="61e77-131">Por o AuthHost executar no seu próprio contêiner de aplicativo para dar maior capacidade de rede privada, você deve definir uma chave de registro: Windows Registry Editor Version 5.00</span><span class="sxs-lookup"><span data-stu-id="61e77-131">Since the AuthHost runs in its own app container to give it the private network capability, you must set a registry key: Windows Registry Editor Version 5.00</span></span>

    <span data-ttu-id="61e77-132">**HKEY \_ LOCAL \_ MACHINE** SOFTWARE Microsoft Windows NT opções de execução de arquivo de imagem \\  \\  \\  \\ **CurrentVersion** \\  \\ **authhost.exe** \\ **EnablePrivateNetwork** = 00000001</span><span class="sxs-lookup"><span data-stu-id="61e77-132">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**Image File Execution Options**\\**authhost.exe**\\**EnablePrivateNetwork** = 00000001</span></span><dl> <dt>

                     Data type
</dt> <dd>                     <span data-ttu-id="61e77-133">DWORD</span><span class="sxs-lookup"><span data-stu-id="61e77-133">DWORD</span></span></dd> </dl>

2.  <span data-ttu-id="61e77-134">Adicione uma regra para o AuthHost, uma vez que é ele quem gera o tráfego de saída.</span><span class="sxs-lookup"><span data-stu-id="61e77-134">Add a rule for the AuthHost as this is what is generating the outbound traffic.</span></span>
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

    

3.  <span data-ttu-id="61e77-135">Adicione uma regra de firewall para o tráfego de entrada ao Fiddler.</span><span class="sxs-lookup"><span data-stu-id="61e77-135">Add a firewall rule for incoming traffic to Fiddler.</span></span>

<span data-ttu-id="61e77-136">Para obter mais informações, consulte [Blog sobre como usar o depurador da Web do Fiddler com Windows Store.](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications)</span><span class="sxs-lookup"><span data-stu-id="61e77-136">For more information, see [Blog on using Fiddler web debugger with Windows Store apps](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications).</span></span>

## <a name="related-topics"></a><span data-ttu-id="61e77-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="61e77-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61e77-138">Considerações para o desenvolvimento de páginas da Web</span><span class="sxs-lookup"><span data-stu-id="61e77-138">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="61e77-139">Perguntas frequentes sobre o Agente de Autenticação da Web</span><span class="sxs-lookup"><span data-stu-id="61e77-139">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.yml)
</dt> <dt>

[<span data-ttu-id="61e77-140">Aplicativo de exemplo do SDK do Agente de Autenticação da Web</span><span class="sxs-lookup"><span data-stu-id="61e77-140">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="61e77-141">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="61e77-141">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041&preserve-view=true)
</dt> </dl>

 

 
