---
title: Habilitando o rastreamento do EAPHost
description: O pode ajudar os usuários a encontrar as causas raiz dos problemas que ocorrem durante o processo de autenticação EAP. As informações de depuração podem incluir chamadas de API executadas, chamadas de função internas executadas e transições de estado executadas.
ms.assetid: 5f401101-59aa-4ee8-825a-0b998489eed9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fdee8a5516b218e51f0151e1964885789560d82
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104008640"
---
# <a name="enabling-eaphost-tracing"></a><span data-ttu-id="2a10d-104">Habilitando o rastreamento do EAPHost</span><span class="sxs-lookup"><span data-stu-id="2a10d-104">Enabling EAPHost Tracing</span></span>

<span data-ttu-id="2a10d-105">Os logs de rastreamento que contêm informações de depuração podem ajudar os usuários a encontrar as causas raiz dos problemas que ocorrem durante o processo de autenticação EAP.</span><span class="sxs-lookup"><span data-stu-id="2a10d-105">Trace logs containing debugging information can assist users in finding the root causes of issues that occur during the EAP authentication process.</span></span> <span data-ttu-id="2a10d-106">As informações de depuração podem incluir chamadas de API executadas, chamadas de função internas executadas e transições de estado executadas.</span><span class="sxs-lookup"><span data-stu-id="2a10d-106">The debugging information can include API calls performed, internal function calls performed, and state transitions performed.</span></span>

<span data-ttu-id="2a10d-107">O rastreamento pode ser habilitado tanto no lado do cliente quanto no lado do autenticador.</span><span class="sxs-lookup"><span data-stu-id="2a10d-107">Tracing can be enabled on both the client side and the authenticator side.</span></span> <span data-ttu-id="2a10d-108">O rastreamento também pode ser habilitado para chamadas para as APIs [RRAS (serviço de roteamento e acesso remoto)](/windows/desktop/RRAS/routing-start-page) .</span><span class="sxs-lookup"><span data-stu-id="2a10d-108">Tracing can also be enabled for calls to the [Routing and Remote Access Service (RRAS)](/windows/desktop/RRAS/routing-start-page) APIs.</span></span> <span data-ttu-id="2a10d-109">Para obter mais informações, consulte [rastreamento no serviço de roteamento e acesso remoto](#tracing-on-the-routing-and-remote-access-service).</span><span class="sxs-lookup"><span data-stu-id="2a10d-109">For more information, see [Tracing on the Routing and Remote Access Service](#tracing-on-the-routing-and-remote-access-service).</span></span>

> [!Note]  
> <span data-ttu-id="2a10d-110">Os logs de rastreamento estão disponíveis apenas em inglês.</span><span class="sxs-lookup"><span data-stu-id="2a10d-110">Trace logs are available in English only.</span></span>

 

<span data-ttu-id="2a10d-111">Quando o rastreamento EAPHost está habilitado, as informações de log são armazenadas em um arquivo. etl em um local especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="2a10d-111">When EAPHost tracing is enabled, logging information is stored in an .etl file in a user-specified location.</span></span> <span data-ttu-id="2a10d-112">Se ocorrerem erros durante a autenticação EAP, o rastreamento gerará um arquivo. etl que pode ser enviado ao Microsoft Suporte Developer para análise da causa raiz.</span><span class="sxs-lookup"><span data-stu-id="2a10d-112">If errors occur during EAP authentication, tracing generates an .etl file that can be sent to Microsoft Developer Support for root cause analysis.</span></span> <span data-ttu-id="2a10d-113">Os parceiros que têm acesso ao Microsoft Windows Build compartilhamentos, símbolos e arquivos traceformat podem converter os arquivos. etl em um arquivo de texto sem formatação usando a ferramenta **Tracerpt** .</span><span class="sxs-lookup"><span data-stu-id="2a10d-113">Partners that have access to Microsoft windows build shares, symbols, and traceformat files can convert the .etl files into a plain text file using the **tracerpt** tool.</span></span>

<span data-ttu-id="2a10d-114">Falhas de servidor de diretivas de rede (NPS) não são capturadas nos logs do EAPHost.</span><span class="sxs-lookup"><span data-stu-id="2a10d-114">Network policy server (NPS) failures are not captured in the EAPHost logs.</span></span> <span data-ttu-id="2a10d-115">Se você estiver tentando solucionar uma falha de NPS, exiba o IASSAM. LOG e [IASNAP. ](https://go.microsoft.com/fwlink/p/?linkid=84108) Arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="2a10d-115">If you are trying to troubleshoot a NPS failure, view the IASSAM.LOG and [IASNAP.LOG](https://go.microsoft.com/fwlink/p/?linkid=84108) files.</span></span>

## <a name="tracing-on-the-client"></a><span data-ttu-id="2a10d-116">Rastreamento no cliente</span><span class="sxs-lookup"><span data-stu-id="2a10d-116">Tracing on the Client</span></span>

<span data-ttu-id="2a10d-117">Para habilitar o rastreamento no lado do cliente:</span><span class="sxs-lookup"><span data-stu-id="2a10d-117">To enable tracing on the client side:</span></span>

1.  <span data-ttu-id="2a10d-118">Abra uma janela de prompt de comando elevado.</span><span class="sxs-lookup"><span data-stu-id="2a10d-118">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="2a10d-119">Execute o seguinte comando: **logman** **Start Trace** **EapHostPeer** **-o** **. \\ EapHostPeer. etl** **-p** **{5F31090B-D990-4e91-B16D-46121D0255AA} 0x4000ffff 0** **-ETS**</span><span class="sxs-lookup"><span data-stu-id="2a10d-119">Run the following command: **logman** **start trace** **EapHostPeer** **-o** **.\\EapHostPeer.etl** **-p** **{5F31090B-D990-4e91-B16D-46121D0255AA} 0x4000ffff 0** **-ets**</span></span>
3.  <span data-ttu-id="2a10d-120">Reproduza o cenário que você deseja rastrear.</span><span class="sxs-lookup"><span data-stu-id="2a10d-120">Reproduce the scenario that you want to trace.</span></span>
4.  <span data-ttu-id="2a10d-121">Execute o seguinte comando: **logman** **Stop** **EapHostPeer** **-ETS**</span><span class="sxs-lookup"><span data-stu-id="2a10d-121">Run the following command: **logman** **stop** **EapHostPeer** **-ets**</span></span>
5.  <span data-ttu-id="2a10d-122">Converta o arquivo ETL em texto usando o seguinte comando **: Tracerpt EapHostPeer. etl** **– PDB** **&lt; &gt; PDBPath** **-TP** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostPeer.txt**</span><span class="sxs-lookup"><span data-stu-id="2a10d-122">Convert the etl file into text using the following command: **tracerpt EapHostPeer.etl** **–pdb** **&lt;pdbpath&gt;** **-tp** **&lt;tracemessagefilesdirectorypath&gt;** **-o** **EapHostPeer.txt**</span></span>
    > [!Note]  
    > <span data-ttu-id="2a10d-123">Se você não tiver acesso à ferramenta tracerpt, evite a última etapa e envie o arquivo. ETL para o Microsoft Suporte Developer.</span><span class="sxs-lookup"><span data-stu-id="2a10d-123">If you do not have access to the tracerpt tool, avoid the last step and send the .etl file to Microsoft Developer Support.</span></span>

     

## <a name="tracing-on-the-authenticator"></a><span data-ttu-id="2a10d-124">Rastreamento no autenticador</span><span class="sxs-lookup"><span data-stu-id="2a10d-124">Tracing on the Authenticator</span></span>

<span data-ttu-id="2a10d-125">Para habilitar o rastreamento no lado do autenticador:</span><span class="sxs-lookup"><span data-stu-id="2a10d-125">To enable tracing on the authenticator side:</span></span>

1.  <span data-ttu-id="2a10d-126">Abra uma janela de prompt de comando elevado.</span><span class="sxs-lookup"><span data-stu-id="2a10d-126">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="2a10d-127">Execute o seguinte comando: **logman** **Start Trace** **EapHostAuthr** **-o** **. \\ EapHostAuthr. etl** **-p** **{F6578502-DF4E-4A67-9661-E3A2F05D1D9B} 0x4000ffff 0** **-ETS**</span><span class="sxs-lookup"><span data-stu-id="2a10d-127">Run the following command: **logman** **start trace** **EapHostAuthr** **-o** **.\\EapHostAuthr.etl** **-p** **{F6578502-DF4E-4a67-9661-E3A2F05D1D9B} 0x4000ffff 0** **-ets**</span></span>
3.  <span data-ttu-id="2a10d-128">Reproduza o cenário que você deseja rastrear.</span><span class="sxs-lookup"><span data-stu-id="2a10d-128">Reproduce the scenario that you want to trace.</span></span>
4.  <span data-ttu-id="2a10d-129">Execute o seguinte comando: **logman** **Stop** **EapHostAuthr** **-ETS**</span><span class="sxs-lookup"><span data-stu-id="2a10d-129">Run the following command: **logman** **stop** **EapHostAuthr** **-ets**</span></span>
5.  <span data-ttu-id="2a10d-130">Converta o arquivo ETL em texto usando o seguinte comando **: Tracerpt EapHostAuthr. etl** **– PDB** **&lt; &gt; PDBPath** **-TP** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostAuthr.txt**</span><span class="sxs-lookup"><span data-stu-id="2a10d-130">Convert the etl file into text using the following command: **tracerpt EapHostAuthr.etl** **–pdb** **&lt;pdbpath&gt;** **-tp** **&lt;tracemessagefilesdirectorypath&gt;** **-o** **EapHostAuthr.txt**</span></span>
    > [!Note]  
    > <span data-ttu-id="2a10d-131">Se você não tiver acesso à ferramenta tracerpt, evite a última etapa e, em vez disso, envie o arquivo. ETL para o Microsoft Suporte Developer.</span><span class="sxs-lookup"><span data-stu-id="2a10d-131">If you do not have access to the tracerpt tool, avoid the last step and instead send the .etl file to Microsoft Developer Support.</span></span>

     

## <a name="event-tracing"></a><span data-ttu-id="2a10d-132">Rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="2a10d-132">Event tracing</span></span>

<span data-ttu-id="2a10d-133">No Windows 7 e versões posteriores do Windows, o EapHost fornece rastreamento baseado em evento no autenticador e no par.</span><span class="sxs-lookup"><span data-stu-id="2a10d-133">In Windows 7 and later versions of Windows, EapHost provides event based tracing on the authenticator and the peer.</span></span> <span data-ttu-id="2a10d-134">A vantagem do rastreamento baseado em eventos é que nenhum arquivo de símbolo é necessário para exibir as mensagens de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="2a10d-134">The advantage of event based tracing is that no symbol files are needed to view the trace messages.</span></span> <span data-ttu-id="2a10d-135">Para habilitar o rastreamento de eventos:</span><span class="sxs-lookup"><span data-stu-id="2a10d-135">To enable event tracing:</span></span>

1.  <span data-ttu-id="2a10d-136">Abra **Visualizador**.</span><span class="sxs-lookup"><span data-stu-id="2a10d-136">Open **EventViewer**.</span></span>
2.  <span data-ttu-id="2a10d-137">As mensagens importantes do EapHost são registradas em: "eventos administrativos de exibições personalizadas \\ "</span><span class="sxs-lookup"><span data-stu-id="2a10d-137">Critical EapHost messages are logged under: “Custom Views\\Administrative Events”</span></span>
3.  <span data-ttu-id="2a10d-138">Mensagens não críticas são registradas em: "aplicativos e serviços \\ Microsoft \\ Windows \\ EapHost</span><span class="sxs-lookup"><span data-stu-id="2a10d-138">Non-critical messages are logged under: “Applications and Services\\Microsoft\\Windows\\EapHost</span></span>
4.  <span data-ttu-id="2a10d-139">As mensagens de evento "analítica" e "depurar" podem ser vistas no mesmo caminho selecionando **Mostrar logs analíticos e de depuração** no menu **Exibir** na barra de título.</span><span class="sxs-lookup"><span data-stu-id="2a10d-139">"Analytic" and "Debug" type event messages can be seen under the same path by selecting **Show Analytic and Debug Logs** from the **view** menu in the title bar.</span></span>

## <a name="tracing-on-the-routing-and-remote-access-service"></a><span data-ttu-id="2a10d-140">Rastreamento no serviço de roteamento e acesso remoto</span><span class="sxs-lookup"><span data-stu-id="2a10d-140">Tracing on the Routing and Remote Access Service</span></span>

<span data-ttu-id="2a10d-141">Para habilitar o rastreamento RRAS:</span><span class="sxs-lookup"><span data-stu-id="2a10d-141">To enable RRAS tracing:</span></span>

1.  <span data-ttu-id="2a10d-142">Abra uma janela de prompt de comando elevado.</span><span class="sxs-lookup"><span data-stu-id="2a10d-142">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="2a10d-143">Execute o seguinte comando: **netsh** **RAS** **set** **TR** **\* *_ _* en**</span><span class="sxs-lookup"><span data-stu-id="2a10d-143">Run the following command: **netsh** **ras** **set** **tr** **\**_ _\* en*\*</span></span>
3.  <span data-ttu-id="2a10d-144">Abrir o **\\ rastreamento de% systemroot%** para exibir os RASTREAMENTOs de Ras</span><span class="sxs-lookup"><span data-stu-id="2a10d-144">Open **%systemroot%\\tracing** to view RAS traces</span></span>

<span data-ttu-id="2a10d-145">Para desabilitar o rastreamento RRAS:</span><span class="sxs-lookup"><span data-stu-id="2a10d-145">To disable RRAS tracing:</span></span>

1.  <span data-ttu-id="2a10d-146">Abra uma janela de prompt de comando elevado.</span><span class="sxs-lookup"><span data-stu-id="2a10d-146">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="2a10d-147">Execute o seguinte comando: **netsh** **RAS** **set** **TR** **\* *_ _* dis**</span><span class="sxs-lookup"><span data-stu-id="2a10d-147">Run the following command: **netsh** **ras** **set** **tr** **\**_ _\* dis*\*</span></span>

<span data-ttu-id="2a10d-148">Para obter mais informações, consulte [comandos netsh](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="2a10d-148">For more information, see [Netsh Commands](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a10d-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2a10d-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a10d-150">Usando o EAPHost</span><span class="sxs-lookup"><span data-stu-id="2a10d-150">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="2a10d-151">Serviço de Roteamento e Acesso Remoto (RRAS)</span><span class="sxs-lookup"><span data-stu-id="2a10d-151">Routing and Remote Access Service (RRAS)</span></span>](/windows/desktop/RRAS/routing-start-page)
</dt> </dl>

 

 