---
description: Se o cliente e o host não puderem trocar metadados, um host genérico e um cliente poderão ser substituídos pelo host e cliente personalizados para ajudar a solucionar o problema.
ms.assetid: 7e5c8444-b3ee-4e9c-984f-13d54f2bbfc0
title: Usando um host genérico e um cliente para a troca de metadados HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36827dde8aa03fa15fc4beaa5917f1f2c3c36eca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798382"
---
# <a name="using-a-generic-host-and-client-for-http-metadata-exchange"></a><span data-ttu-id="602f7-103">Usando um host genérico e um cliente para a troca de metadados HTTP</span><span class="sxs-lookup"><span data-stu-id="602f7-103">Using a Generic Host and Client for HTTP Metadata Exchange</span></span>

<span data-ttu-id="602f7-104">Se o cliente e o host não puderem trocar metadados, um host genérico e um cliente poderão ser substituídos pelo host e cliente personalizados para ajudar a solucionar o problema.</span><span class="sxs-lookup"><span data-stu-id="602f7-104">If the client and host cannot exchange metadata, then a generic host and client can be substituted for the custom host and client to help troubleshoot the issue.</span></span> <span data-ttu-id="602f7-105">Se o endereço do dispositivo ou os metadados do dispositivo não aparecerem na saída do cliente de depuração WSD, os endereços de transporte fornecidos ou o ambiente de rede poderão estar causando a falha.</span><span class="sxs-lookup"><span data-stu-id="602f7-105">If the device address or device metadata does not appear in the WSD Debug Client output, then the supplied transport addresses or the network environment may be causing the failure.</span></span> <span data-ttu-id="602f7-106">Para obter mais informações sobre o host e o cliente genéricos, consulte [ferramentas de depuração](debugging-tools.md).</span><span class="sxs-lookup"><span data-stu-id="602f7-106">For more information about the generic host and client, see [Debugging Tools](debugging-tools.md).</span></span>

<span data-ttu-id="602f7-107">Se tiver verificado que um host genérico e um cliente podem concluir a troca de metadados WS-Discovery e HTTP, esse procedimento de diagnóstico pode ser ignorado e a solução de problemas pode ser continuada seguindo os procedimentos em [como usar o log do WinHTTP para verificar se há tráfego](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="602f7-107">If it has been verified that a generic host and client can complete both WS-Discovery and HTTP metadata exchange, then this diagnostic procedure can be skipped and troubleshooting can be continued by following the procedures in [Using WinHTTP Logging to Verify Get Traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>

<span data-ttu-id="602f7-108">Se o host ou o cliente for um aplicativo em execução em um computador, o host ou cliente genérico deverá ser executado no mesmo contexto de segurança que o host ou cliente real.</span><span class="sxs-lookup"><span data-stu-id="602f7-108">If either the host or client is an application running on a PC, the generic host or client should be run in the same security context as the actual host or client.</span></span> <span data-ttu-id="602f7-109">Por exemplo, se o host ou o cliente real for executado como administrador, o host ou cliente genérico deverá ser executado como administrador.</span><span class="sxs-lookup"><span data-stu-id="602f7-109">For example, if the actual host or client runs as Administrator, then the generic host or client must run as Administrator.</span></span> <span data-ttu-id="602f7-110">Além disso, se o host ou o cliente for um dispositivo autônomo, ele deverá ser completamente substituído por um computador que esteja executando um cliente ou host genérico em um contexto de segurança que garanta acesso ilimitado à rede (por exemplo, executando como administrador).</span><span class="sxs-lookup"><span data-stu-id="602f7-110">Also, if either the host or client is a standalone device, it should be completely replaced by a PC running a generic host or client in a security context that guarantees unlimited network access (for example, running as Administrator).</span></span>

<span data-ttu-id="602f7-111">**Para usar um host genérico e um cliente para solucionar problemas de troca de metadados HTTP**</span><span class="sxs-lookup"><span data-stu-id="602f7-111">**To using a generic host and client to troubleshoot HTTP metadata exchange**</span></span>

1.  <span data-ttu-id="602f7-112">Abra una janela de prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="602f7-112">Open a command prompt window.</span></span>
2.  <span data-ttu-id="602f7-113">Execute o seguinte comando: **WSDDebug \_host.exe/Mode Metadata/Start**</span><span class="sxs-lookup"><span data-stu-id="602f7-113">Run the following command: **WSDDebug\_host.exe /mode metadata /start**</span></span>

    > [!Note]  
    > <span data-ttu-id="602f7-114">Uma caixa de diálogo **alerta de segurança do Windows** pode ser exibida.</span><span class="sxs-lookup"><span data-stu-id="602f7-114">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="602f7-115">Nesse caso, clique em **desbloquear** para permitir que o host de depuração WSD seja executado.</span><span class="sxs-lookup"><span data-stu-id="602f7-115">If so, click **Unblock** to allow the WSD Debug Host to run.</span></span>

     

    <span data-ttu-id="602f7-116">Esse comando gera uma saída semelhante à seguinte.</span><span class="sxs-lookup"><span data-stu-id="602f7-116">This command generates output similar to the following.</span></span> <span data-ttu-id="602f7-117">Anote a ID do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="602f7-117">Make a note of the device ID.</span></span>

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  <span data-ttu-id="602f7-118">Execute o seguinte comando: **WSDDebug \_client.exe/Mode Metadata/Hello off/resolve** *<id>* .</span><span class="sxs-lookup"><span data-stu-id="602f7-118">Run the following command: **WSDDebug\_client.exe /mode metadata /hello off /resolve** *<id>*.</span></span> <span data-ttu-id="602f7-119">Substitua *<id>* pela ID do dispositivo identificada na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="602f7-119">Replace *<id>* with the device ID identified in step 2.</span></span>
    > [!Note]  
    > <span data-ttu-id="602f7-120">Uma caixa de diálogo **alerta de segurança do Windows** pode ser exibida.</span><span class="sxs-lookup"><span data-stu-id="602f7-120">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="602f7-121">Nesse caso, clique em **desbloquear** para permitir que o cliente de depuração WSD seja executado.</span><span class="sxs-lookup"><span data-stu-id="602f7-121">If so, click **Unblock** to allow the WSD Debug Client to run.</span></span>

     

<span data-ttu-id="602f7-122">O cliente de depuração WSD gera uma saída semelhante à seguinte.</span><span class="sxs-lookup"><span data-stu-id="602f7-122">WSD Debug Client generates output similar to the following.</span></span>

``` syntax
WSDAPI Debug Client
Copyright (C) Microsoft Corporation 2007.  All rights reserved.
Client ID is urn:uuid:0f571af7-6b0e-4daf-8054-f2233ac27910
Hello mode is disabled
Client metadata>
*****************************************************************************
Add at 02/28/07 15:16:51
+ EPR:
  + Address:                 urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Types:
    (wsdp) https://schemas.xmlsoap.org/ws/2006/02/devprof:Device
+ XAddrs:
  https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Metadata version:          2
+ Instance ID:               1
+ Probe/Resolve tag:         WSDAPI debug_client
+ Remote transport address:  [::1]:3702
+ Local transport address:   ::1
+ Local interface GUID:      42133cd4-6a70-11db-bbc9-806e6f6e6963
Client metadata>
*****************************************************************************
Getting metadata for host at 02/28/07 15:16:51:
+ Endpoint reference:
  + Address:
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
Client metadata>
*****************************************************************************
Metadata for host:
+ Endpoint reference:
  + Address:           urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice
  + Friendly name:
    [no lang]: Debugging Host
  + Firmware version:  1.0
  + Serial number:     00000000
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisModel
  + Manufacturer:
    [no lang]: Microsoft Corporation
  + Manufacturer URL:  https://www.microsoft.com/
  + Model names:
    [no lang]: Microsoft Debugging Host
  + Model number:      https://www.microsoft.com/
End of metadata
Client metadata>
```

<span data-ttu-id="602f7-123">O cliente de depuração WSD pode gerar muita saída em uma rede com muitos dispositivos DPWS.</span><span class="sxs-lookup"><span data-stu-id="602f7-123">The WSD Debug Client may generate a lot of output on a network with many DPWS devices.</span></span> <span data-ttu-id="602f7-124">A saída pode ser redirecionada para um arquivo para facilitar a análise.</span><span class="sxs-lookup"><span data-stu-id="602f7-124">The output can be redirected to a file for easier analysis.</span></span> <span data-ttu-id="602f7-125">Digite o arquivo de **log** de texto *<filename>* no prompt do cliente de depuração WSD para redirecionar a saída para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="602f7-125">Type **log tee** *<filename>* at the WSD Debug Client prompt to redirect output to a file.</span></span> <span data-ttu-id="602f7-126">O redirecionamento de saída pode ser interrompido digitando o registro de tempo de **interrupção do log** no prompt do cliente de depuração WSD.</span><span class="sxs-lookup"><span data-stu-id="602f7-126">Output redirection can be stopped by typing **log tee stop** at the WSD Debug Client prompt.</span></span>

<span data-ttu-id="602f7-127">Anote o endereço de referência do ponto de extremidade (EPR).</span><span class="sxs-lookup"><span data-stu-id="602f7-127">Make a note of the endpoint reference (EPR) address.</span></span> <span data-ttu-id="602f7-128">Esse endereço de EPR deve corresponder à ID do dispositivo identificada na etapa 2 acima.</span><span class="sxs-lookup"><span data-stu-id="602f7-128">This EPR address should match the device ID identified in step 2 above.</span></span> <span data-ttu-id="602f7-129">Além disso, verifique se o cliente de depuração WSD imprimiu completamente os metadados do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="602f7-129">Also, verify that the WSD Debug Client completely printed the metadata for the device.</span></span> <span data-ttu-id="602f7-130">Os metadados do dispositivo começam com `Metadata for host` e terminam com `End of metadata` .</span><span class="sxs-lookup"><span data-stu-id="602f7-130">The device metadata begins with `Metadata for host` and ends with `End of metadata`.</span></span>

<span data-ttu-id="602f7-131">Se a ID do dispositivo e os metadados do dispositivo aparecerem corretamente na saída do cliente de depuração WSD, a falha do aplicativo provavelmente não estará relacionada aos endereços de transporte fornecidos, ao sistema operacional ou ao ambiente de rede.</span><span class="sxs-lookup"><span data-stu-id="602f7-131">If the device ID and device metadata appears correctly in the WSD Debug Client output, then the application failure is likely not related to the supplied transport addresses, the operating system, or the network environment.</span></span> <span data-ttu-id="602f7-132">Substitua o host genérico e o cliente pelo host e cliente personalizados e continue a solução de problemas seguindo os procedimentos em [como usar o log do WinHTTP para verificar o tráfego Get](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="602f7-132">Replace the generic host and client with the custom host and client, and continue troubleshooting by following the procedures in [Using WinHTTP Logging to Verify Get Traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>

<span data-ttu-id="602f7-133">Se o endereço do dispositivo e os metadados do dispositivo não aparecerem na saída do cliente de depuração WSD, a falha poderá ter uma ou mais das seguintes causas:</span><span class="sxs-lookup"><span data-stu-id="602f7-133">If the device address and device metadata do not appear in the WSD Debug Client output, then the failure could have one or more of the following causes:</span></span>

-   <span data-ttu-id="602f7-134">O endereço de transporte anunciado pelo host está incorreto ou malformado.</span><span class="sxs-lookup"><span data-stu-id="602f7-134">The transport address advertised by the host is incorrect or malformed.</span></span> <span data-ttu-id="602f7-135">O cliente de depuração WSD tenta obter os metadados do dispositivo da URL fornecida no elemento **XAddrs** de uma mensagem [ProbeMatches](probematches-message.md) ou [ResolveMatches](resolvematches-message.md) .</span><span class="sxs-lookup"><span data-stu-id="602f7-135">WSD Debug Client attempts to get device metadata from the URL provided in the **XAddrs** element of a [ProbeMatches](probematches-message.md) or [ResolveMatches](resolvematches-message.md) message.</span></span> <span data-ttu-id="602f7-136">A URL usada para troca de metadados aparece na saída do cliente de depuração WSD, prefixada pela frase `Using xAddr` .</span><span class="sxs-lookup"><span data-stu-id="602f7-136">The URL used for metadata exchange appears in the WSD Debug Client output, prefixed by the phrase `Using xAddr`.</span></span> <span data-ttu-id="602f7-137">O exemplo a seguir mostra o XAddrs usado para troca de metadados na saída do cliente de depuração WSD acima.</span><span class="sxs-lookup"><span data-stu-id="602f7-137">The following example shows the XAddrs used for metadata exchange in the above WSD Debug Client output.</span></span>

    ``` syntax
    Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
    ```

    <span data-ttu-id="602f7-138">Se o XAddrs fornecido não estiver em conformidade com as [regras de validação do XAddr](xaddr-validation-rules.md), o cliente de depuração WSD não poderá obter os metadados do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="602f7-138">If the supplied XAddrs do not conform to the [XAddr validation rules](xaddr-validation-rules.md), then the WSD Debug Client cannot get the device's metadata.</span></span>

-   <span data-ttu-id="602f7-139">O aplicativo está sendo executado no contexto de segurança incorreto.</span><span class="sxs-lookup"><span data-stu-id="602f7-139">The application is running in the wrong security context.</span></span> <span data-ttu-id="602f7-140">Verifique se o aplicativo está usando as credenciais corretas e se o cliente e o host têm permissão suficiente para acessar a rede.</span><span class="sxs-lookup"><span data-stu-id="602f7-140">Verify that the application is using the correct credentials and that the client and host have sufficient permission to access the network.</span></span>
-   <span data-ttu-id="602f7-141">A configuração do firewall está incorreta.</span><span class="sxs-lookup"><span data-stu-id="602f7-141">The firewall configuration is wrong.</span></span> <span data-ttu-id="602f7-142">Siga as instruções em [inspecionando as configurações de adaptador e firewall](inspecting-adapter-and-firewall-settings.md) para verificar se as configurações do firewall do Windows estão corretas e se não há outras regras descartando os pacotes.</span><span class="sxs-lookup"><span data-stu-id="602f7-142">Follow the instructions in [Inspecting Adapter and Firewall Settings](inspecting-adapter-and-firewall-settings.md) to verify that the Windows Firewall settings are correct and that there are no other rules dropping the packets.</span></span> <span data-ttu-id="602f7-143">O cliente e o host também podem ser copiados em um computador "original" (um com uma instalação padrão do sistema operacional que nunca tenha sido unida a um domínio) para tentar reproduzir a falha.</span><span class="sxs-lookup"><span data-stu-id="602f7-143">The client and host can also be copied onto a "pristine" machine (one with a default operating system installation that has never been joined to a domain) in order to attempt to reproduce the failure.</span></span>
-   <span data-ttu-id="602f7-144">Uma política IPSec está bloqueando o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="602f7-144">An IPSec policy is blocking the application.</span></span> <span data-ttu-id="602f7-145">Copie o cliente e o host em um computador que não esteja sujeito a diretivas IPSec e tente reproduzir a falha.</span><span class="sxs-lookup"><span data-stu-id="602f7-145">Copy the client and host onto a machine that is not subject to IPSec policies and try to reproduce the failure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="602f7-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="602f7-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="602f7-147">Procedimentos de diagnóstico do WSDAPI</span><span class="sxs-lookup"><span data-stu-id="602f7-147">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="602f7-148">Introdução com a solução de problemas de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="602f7-148">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



