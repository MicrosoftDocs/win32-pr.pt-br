---
description: Se o cliente e o host não puderem ver uns aos outros na rede, um host genérico e um cliente poderão ser substituídos pelo host e cliente personalizados para ajudar a solucionar o problema.
ms.assetid: e82ce911-b2a7-4a57-a2f0-9aca6b74478f
title: Usando um host genérico e um cliente para UDP WS-Discovery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3289f5205e4e417fe8162b401be6c608432cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164855"
---
# <a name="using-a-generic-host-and-client-for-udp-ws-discovery"></a><span data-ttu-id="691d6-103">Usando um host genérico e um cliente para UDP WS-Discovery</span><span class="sxs-lookup"><span data-stu-id="691d6-103">Using a Generic Host and Client for UDP WS-Discovery</span></span>

<span data-ttu-id="691d6-104">Se o cliente e o host não puderem ver uns aos outros na rede, um host genérico e um cliente poderão ser substituídos pelo host e cliente personalizados para ajudar a solucionar o problema.</span><span class="sxs-lookup"><span data-stu-id="691d6-104">If the client and host cannot see each other on the network, then a generic host and client can be substituted for the custom host and client to help troubleshoot the issue.</span></span> <span data-ttu-id="691d6-105">Se o endereço do dispositivo não aparecer na saída do cliente de depuração WSD, o ambiente de rede provavelmente está causando a falha.</span><span class="sxs-lookup"><span data-stu-id="691d6-105">If the device address does not appear in the WSD Debug Client output, then the network environment is probably causing the failure.</span></span> <span data-ttu-id="691d6-106">Para obter mais informações sobre o host e o cliente genéricos, consulte [ferramentas de depuração](debugging-tools.md).</span><span class="sxs-lookup"><span data-stu-id="691d6-106">For more information about the generic host and client, see [Debugging Tools](debugging-tools.md).</span></span>

<span data-ttu-id="691d6-107">Se o host ou o cliente for um aplicativo em execução em um computador, o host ou cliente genérico deverá ser executado no mesmo contexto de segurança que o host ou cliente real.</span><span class="sxs-lookup"><span data-stu-id="691d6-107">If either the host or client is an application running on a PC, the generic host or client should be run in the same security context as the actual host or client.</span></span> <span data-ttu-id="691d6-108">Por exemplo, se o host ou o cliente real for executado como administrador, o host ou cliente genérico deverá ser executado como administrador.</span><span class="sxs-lookup"><span data-stu-id="691d6-108">For example, if the actual host or client runs as Administrator, then the generic host or client must run as Administrator.</span></span> <span data-ttu-id="691d6-109">Além disso, se o host ou o cliente for um dispositivo autônomo, ele deverá ser completamente substituído por um computador que esteja executando um cliente ou host genérico.</span><span class="sxs-lookup"><span data-stu-id="691d6-109">Also, if either the host or client is a standalone device, it should be completely replaced by a PC running a generic host or client.</span></span>

<span data-ttu-id="691d6-110">**Para usar um host genérico e um cliente para solucionar problemas de descoberta de WS-Discovery**</span><span class="sxs-lookup"><span data-stu-id="691d6-110">**To using a generic host and client to troubleshoot UDP WS-Discovery**</span></span>

1.  <span data-ttu-id="691d6-111">Abra una janela de prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="691d6-111">Open a command prompt window.</span></span>
2.  <span data-ttu-id="691d6-112">Execute o seguinte comando: **WSDDebug \_host.exe/Mode Metadata/Start**</span><span class="sxs-lookup"><span data-stu-id="691d6-112">Run the following command: **WSDDebug\_host.exe /mode metadata /start**</span></span>

    > [!Note]  
    > <span data-ttu-id="691d6-113">Uma caixa de diálogo **alerta de segurança do Windows** pode ser exibida.</span><span class="sxs-lookup"><span data-stu-id="691d6-113">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="691d6-114">Nesse caso, clique em **desbloquear** para permitir que o host de depuração WSD seja executado.</span><span class="sxs-lookup"><span data-stu-id="691d6-114">If so, click **Unblock** to allow the WSD Debug Host to run.</span></span>

     

    <span data-ttu-id="691d6-115">Esse comando gera uma saída semelhante à seguinte.</span><span class="sxs-lookup"><span data-stu-id="691d6-115">This command generates output similar to the following.</span></span> <span data-ttu-id="691d6-116">Anote a ID do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="691d6-116">Make a note of the device ID.</span></span>

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  <span data-ttu-id="691d6-117">Execute o seguinte comando: **WSDDebug \_client.exe/Mode Metadata/Hello off/resolve** *<id>* .</span><span class="sxs-lookup"><span data-stu-id="691d6-117">Run the following command: **WSDDebug\_client.exe /mode metadata /hello off /resolve** *<id>*.</span></span> <span data-ttu-id="691d6-118">Substitua *<id>* pela ID do dispositivo identificada na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="691d6-118">Replace *<id>* with the device ID identified in step 2.</span></span>
    > [!Note]  
    > <span data-ttu-id="691d6-119">Uma caixa de diálogo **alerta de segurança do Windows** pode ser exibida.</span><span class="sxs-lookup"><span data-stu-id="691d6-119">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="691d6-120">Nesse caso, clique em **desbloquear** para permitir que o cliente de depuração WSD seja executado.</span><span class="sxs-lookup"><span data-stu-id="691d6-120">If so, click **Unblock** to allow the WSD Debug Client to run.</span></span>

     

<span data-ttu-id="691d6-121">O cliente de depuração WSD gera uma saída semelhante à seguinte.</span><span class="sxs-lookup"><span data-stu-id="691d6-121">WSD Debug Client generates output similar to the following.</span></span>

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
```

<span data-ttu-id="691d6-122">O cliente de depuração WSD pode gerar muita saída em uma rede com muitos dispositivos DPWS.</span><span class="sxs-lookup"><span data-stu-id="691d6-122">The WSD Debug Client may generate a lot of output on a network with many DPWS devices.</span></span> <span data-ttu-id="691d6-123">A saída pode ser redirecionada para um arquivo para facilitar a análise.</span><span class="sxs-lookup"><span data-stu-id="691d6-123">The output can be redirected to a file for easier analysis.</span></span> <span data-ttu-id="691d6-124">Digite o arquivo de **log** de texto *<filename>* no prompt do cliente de depuração WSD para redirecionar a saída para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="691d6-124">Type **log tee** *<filename>* at the WSD Debug Client prompt to redirect output to a file.</span></span> <span data-ttu-id="691d6-125">O redirecionamento de saída pode ser interrompido digitando o registro de tempo de **interrupção do log** no prompt do cliente de depuração WSD.</span><span class="sxs-lookup"><span data-stu-id="691d6-125">Output redirection can be stopped by typing **log tee stop** at the WSD Debug Client prompt.</span></span>

<span data-ttu-id="691d6-126">Anote o endereço de referência do ponto de extremidade (EPR).</span><span class="sxs-lookup"><span data-stu-id="691d6-126">Make a note of the endpoint reference (EPR) address.</span></span> <span data-ttu-id="691d6-127">Esse endereço de EPR deve corresponder à ID do dispositivo identificada na etapa 2 acima.</span><span class="sxs-lookup"><span data-stu-id="691d6-127">This EPR address should match the device ID identified in step 2 above.</span></span> <span data-ttu-id="691d6-128">Se esse for o caso, a falha do aplicativo provavelmente não estará relacionada ao sistema operacional ou ao ambiente de rede.</span><span class="sxs-lookup"><span data-stu-id="691d6-128">If this is the case, then the application failure is likely not related to the operating system or the network environment.</span></span> <span data-ttu-id="691d6-129">Substitua o host genérico e o cliente pelo host e cliente personalizados e continue a solução de problemas seguindo os procedimentos em [usando o cliente de depuração WSD para verificar o tráfego multicast](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="691d6-129">Replace the generic host and client with the custom host and client, and continue troubleshooting by following the procedures in [Using WSD Debug Client to Verify Multicast Traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>

<span data-ttu-id="691d6-130">Se a ID do dispositivo não corresponder ao endereço EPR, a falha do aplicativo provavelmente estará relacionada ao sistema operacional ou ao ambiente de rede.</span><span class="sxs-lookup"><span data-stu-id="691d6-130">If the device ID does not match the EPR address, then the application failure is probably related to the operating system or the network environment.</span></span> <span data-ttu-id="691d6-131">A falha pode ter uma ou mais das seguintes causas:</span><span class="sxs-lookup"><span data-stu-id="691d6-131">The failure could have one or more of the following causes:</span></span>

-   <span data-ttu-id="691d6-132">O aplicativo está sendo executado no contexto de segurança incorreto.</span><span class="sxs-lookup"><span data-stu-id="691d6-132">The application is running in the wrong security context.</span></span> <span data-ttu-id="691d6-133">Verifique se o aplicativo está usando as credenciais corretas e se o cliente e o host têm permissão suficiente para acessar a rede.</span><span class="sxs-lookup"><span data-stu-id="691d6-133">Verify that the application is using the correct credentials and that the client and host have sufficient permission to access the network.</span></span>
-   <span data-ttu-id="691d6-134">A configuração do firewall está incorreta.</span><span class="sxs-lookup"><span data-stu-id="691d6-134">The firewall configuration is wrong.</span></span> <span data-ttu-id="691d6-135">Siga as instruções em [inspecionando as configurações de adaptador e firewall](inspecting-adapter-and-firewall-settings.md) para verificar se as configurações do firewall do Windows estão corretas e se não há outras regras descartando os pacotes.</span><span class="sxs-lookup"><span data-stu-id="691d6-135">Follow the instructions in [Inspecting Adapter and Firewall Settings](inspecting-adapter-and-firewall-settings.md) to verify that the Windows Firewall settings are correct and that there are no other rules dropping the packets.</span></span> <span data-ttu-id="691d6-136">O cliente e o host também podem ser copiados em um computador "original" (um com uma instalação padrão do sistema operacional que nunca tenha sido unida a um domínio) para tentar reproduzir a falha.</span><span class="sxs-lookup"><span data-stu-id="691d6-136">The client and host can also be copied onto a "pristine" machine (one with a default operating system installation that has never been joined to a domain) in order to attempt to reproduce the failure.</span></span>
-   <span data-ttu-id="691d6-137">Uma política IPSec está bloqueando o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="691d6-137">An IPSec policy is blocking the application.</span></span> <span data-ttu-id="691d6-138">Copie o cliente e o host em um computador que não esteja sujeito a diretivas IPSec e tente reproduzir a falha.</span><span class="sxs-lookup"><span data-stu-id="691d6-138">Copy the client and host onto a machine not subject to IPSec policies and try to reproduce the failure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="691d6-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="691d6-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="691d6-140">Procedimentos de diagnóstico do WSDAPI</span><span class="sxs-lookup"><span data-stu-id="691d6-140">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="691d6-141">Introdução com a solução de problemas de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="691d6-141">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



