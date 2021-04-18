---
description: .
ms.assetid: f022374d-ea3f-477f-9b59-3188b775ed64
title: Manifesto do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf4fd1ae8a9f66dafbe65a3db09dd014dbef31e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812313"
---
# <a name="application-manifest"></a><span data-ttu-id="5c67a-103">Manifesto do aplicativo</span><span class="sxs-lookup"><span data-stu-id="5c67a-103">Application Manifest</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="5c67a-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="5c67a-104">Affected Platforms</span></span>

<span data-ttu-id="5c67a-105">**Clientes** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="5c67a-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="5c67a-106">**Servidores** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5c67a-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="5c67a-107">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="5c67a-107">Feature Impact</span></span>

 <span data-ttu-id="5c67a-108">**Severidade** -baixa</span><span class="sxs-lookup"><span data-stu-id="5c67a-108">**Severity** - Low</span></span>  
<span data-ttu-id="5c67a-109">**Frequência** -baixa</span><span class="sxs-lookup"><span data-stu-id="5c67a-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="5c67a-110">Description</span><span class="sxs-lookup"><span data-stu-id="5c67a-110">Description</span></span>

<span data-ttu-id="5c67a-111">O Windows 7 apresenta uma nova seção no manifesto do aplicativo chamada "Compatibility".</span><span class="sxs-lookup"><span data-stu-id="5c67a-111">Windows 7 introduces a new section in the application manifest called "Compatibility."</span></span> <span data-ttu-id="5c67a-112">Esta seção ajuda o Windows a determinar as versões do Windows que um aplicativo foi projetado para direcionar e permite que o Windows forneça o comportamento que o aplicativo espera com base na versão do Windows de destino do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5c67a-112">This section helps Windows determine the versions of Windows that an application was designed to target, and enables Windows to provide the behavior that the application expects based on the version of Windows that the application targeted.</span></span>

<span data-ttu-id="5c67a-113">A seção de compatibilidade permite que o Windows forneça um novo comportamento para o novo software criado pelo desenvolvedor, mantendo a compatibilidade para o software existente.</span><span class="sxs-lookup"><span data-stu-id="5c67a-113">The Compatibility section allows Windows to provide new behavior to new developer-created software while maintaining the compatibility for existing software.</span></span> <span data-ttu-id="5c67a-114">Esta seção também ajuda o Windows a fornecer maior compatibilidade em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="5c67a-114">This section also helps Windows deliver greater compatibility in future versions of Windows as well.</span></span> <span data-ttu-id="5c67a-115">Por exemplo, um aplicativo que declara suporte somente para o Windows 7 na seção de compatibilidade continuará a receber o comportamento do Windows 7 na versão futura do Windows.</span><span class="sxs-lookup"><span data-stu-id="5c67a-115">For example, an application declaring support only for Windows 7 in the Compatibility section will continue to receive Windows 7 behavior in future version of Windows.</span></span>

## <a name="manifestation-of-change"></a><span data-ttu-id="5c67a-116">Manifestação de alteração</span><span class="sxs-lookup"><span data-stu-id="5c67a-116">Manifestation of Change</span></span>

<span data-ttu-id="5c67a-117">Os aplicativos sem uma seção de compatibilidade em seu manifesto receberão o comportamento do Windows Vista por padrão no Windows 7 e em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="5c67a-117">Applications without a Compatibility section in their manifest will receive Windows Vista behavior by default on Windows 7 and future Windows versions.</span></span> <span data-ttu-id="5c67a-118">Observe que o Windows XP e o Windows Vista ignoram essa seção de manifesto e não têm nenhum impacto sobre elas.</span><span class="sxs-lookup"><span data-stu-id="5c67a-118">Note that Windows XP and Windows Vista ignore this manifest section and it has no impact on them.</span></span>

<span data-ttu-id="5c67a-119">Os seguintes componentes do Windows fornecem comportamento divergente com base na seção de compatibilidade do Windows 7:</span><span class="sxs-lookup"><span data-stu-id="5c67a-119">The following Windows components provide divergent behavior based on the Compatibility section in Windows 7:</span></span>

<span data-ttu-id="5c67a-120">**Pool de threads padrão RPC**</span><span class="sxs-lookup"><span data-stu-id="5c67a-120">**RPC Default Thread Pool**</span></span>

-   <span data-ttu-id="5c67a-121">**Windows 7:** Para melhorar a escalabilidade e reduzir as contagens de threads, o RPC alternou para o pool de threads NT (pool padrão).</span><span class="sxs-lookup"><span data-stu-id="5c67a-121">**Windows 7:** To improve scalability and reduce thread counts, RPC switched to the NT thread pool (default pool).</span></span> <span data-ttu-id="5c67a-122">Para o Windows Vista, o RPC usava um pool de threads privado.</span><span class="sxs-lookup"><span data-stu-id="5c67a-122">For Windows Vista, RPC used a private thread pool.</span></span>
    -   <span data-ttu-id="5c67a-123">Para binários compilados para o Win7, o pool padrão é usado</span><span class="sxs-lookup"><span data-stu-id="5c67a-123">For binaries compiled for Win7 the default pool is used</span></span>
    -   <span data-ttu-id="5c67a-124">Se I \_ RpcMgmtEnableDedicatedThreadPool for chamado antes de qualquer API RPC ser chamada, o pool de threads privado será usado (comportamento do vista)</span><span class="sxs-lookup"><span data-stu-id="5c67a-124">If I\_RpcMgmtEnableDedicatedThreadPool is called before any RPC API is called, the private thread pool is used (Vista behavior)</span></span>
    -   <span data-ttu-id="5c67a-125">Se eu \_ RpcMgmtEnableDedicatedThreadPool for chamado após uma chamada RPC, o pool padrão será usado, I \_ RpcMgmtEnableDedicatedThreadPool retornará o erro 1764 e a operação solicitada não terá suporte</span><span class="sxs-lookup"><span data-stu-id="5c67a-125">If I\_RpcMgmtEnableDedicatedThreadPool is called after an RPC call, the default pool is used, I\_RpcMgmtEnableDedicatedThreadPool returns the error 1764, and the requested operation is not supported</span></span>
-   <span data-ttu-id="5c67a-126">**Windows Vista (padrão):** Para binários compilados para o Windows Vista e versões anteriores, o pool privado é usado.</span><span class="sxs-lookup"><span data-stu-id="5c67a-126">**Windows Vista (default):** For binaries compiled for Windows Vista and below, the private pool is used.</span></span>

<span data-ttu-id="5c67a-127">**Bloqueio do DirectDraw**</span><span class="sxs-lookup"><span data-stu-id="5c67a-127">**DirectDraw Lock**</span></span>

-   <span data-ttu-id="5c67a-128">**Windows 7:** Os aplicativos manifestados para o Windows 7 não podem chamar a API de bloqueio em DDRAW para bloquear o buffer de vídeo da área de trabalho principal.</span><span class="sxs-lookup"><span data-stu-id="5c67a-128">**Windows 7:** Applications manifested for Windows 7 cannot call Lock API in DDRAW to lock the primary Desktop video buffer.</span></span> <span data-ttu-id="5c67a-129">Isso resultará em erro, e o ponteiro **NULL** para o primário será retornado.</span><span class="sxs-lookup"><span data-stu-id="5c67a-129">Doing so will result in error, and **NULL** pointer for the primary will be returned.</span></span> <span data-ttu-id="5c67a-130">Esse comportamento é imposto mesmo se Gerenciador de Janelas da Área de Trabalho composição não estiver ativada.</span><span class="sxs-lookup"><span data-stu-id="5c67a-130">This behavior is enforced even if Desktop Window Manager Composition is not turned on.</span></span> <span data-ttu-id="5c67a-131">Os aplicativos compatíveis com o Windows 7 não devem bloquear o buffer de vídeo primário para renderização.</span><span class="sxs-lookup"><span data-stu-id="5c67a-131">Windows 7 compatible applications must not lock the primary video buffer to render.</span></span>
-   <span data-ttu-id="5c67a-132">**Windows Vista (padrão):** Os aplicativos poderão adquirir um bloqueio no buffer de vídeo primário, pois os aplicativos herdados dependem desse comportamento.</span><span class="sxs-lookup"><span data-stu-id="5c67a-132">**Windows Vista (default):** Applications will be able to acquire a lock on the primary video buffer as legacy applications depend on this behavior.</span></span> <span data-ttu-id="5c67a-133">A execução do aplicativo é desativada Gerenciador de Janelas da Área de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="5c67a-133">Running the application turns off Desktop Window Manager.</span></span>

<span data-ttu-id="5c67a-134">**BLT (transferência de bloco de bits) do DirectDraw para primário sem janela de recorte**</span><span class="sxs-lookup"><span data-stu-id="5c67a-134">**DirectDraw Bit Block Transfer (Blt) to Primary without Clipping Window**</span></span>

-   <span data-ttu-id="5c67a-135">**Windows 7:** Os aplicativos manifestados para o Windows 7 são impedidos de executar BLT para o buffer de vídeo da área de trabalho principal sem uma janela de recorte.</span><span class="sxs-lookup"><span data-stu-id="5c67a-135">**Windows 7:** Applications manifested for Windows 7 are prevented from performing Blt's to the primary Desktop video buffer without a clipping window.</span></span> <span data-ttu-id="5c67a-136">Isso resultará em erro e a área de BLT não será renderizada.</span><span class="sxs-lookup"><span data-stu-id="5c67a-136">Doing so will result in error and the Blt area will not be rendered.</span></span> <span data-ttu-id="5c67a-137">O Windows impõe esse comportamento mesmo se você não ativar Gerenciador de Janelas da Área de Trabalho composição.</span><span class="sxs-lookup"><span data-stu-id="5c67a-137">Windows enforces this behavior even if you do not turn on Desktop Window Manager Composition.</span></span> <span data-ttu-id="5c67a-138">Os aplicativos compatíveis com o Windows 7 devem BLT a uma janela de recorte.</span><span class="sxs-lookup"><span data-stu-id="5c67a-138">Windows 7 compatible applications must Blt to a clipping window.</span></span>
-   <span data-ttu-id="5c67a-139">**Windows Vista (padrão):** Os aplicativos devem ser capazes de Bltr o primário sem uma janela de recorte, pois os aplicativos herdados dependem desse comportamento.</span><span class="sxs-lookup"><span data-stu-id="5c67a-139">**Windows Vista (default):** Applications must be able to Blt to the primary without a clipping window as legacy applications depend on this behavior.</span></span> <span data-ttu-id="5c67a-140">A execução desse aplicativo desativa o Gerenciador de Janelas da Área de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="5c67a-140">Running this application turns off the Desktop Window Manager.</span></span>

<span data-ttu-id="5c67a-141">**API GetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="5c67a-141">**GetOverlappedResult API**</span></span>

-   <span data-ttu-id="5c67a-142">**Windows 7:** Resolve uma condição de corrida em que um aplicativo multithread usando GetOverlappedResult pode retornar sem redefinir o evento na estrutura sobreposta, fazendo com que a próxima chamada a essa função retorne prematuramente.</span><span class="sxs-lookup"><span data-stu-id="5c67a-142">**Windows 7:** Resolves a race condition where a multithreaded app using GetOverlappedResult can return without resetting the event in the overlapped structure, causing the next call to this function to return prematurely.</span></span>
-   <span data-ttu-id="5c67a-143">**Windows Vista (padrão):** Fornece o comportamento com a condição de corrida na qual os aplicativos podem ter uma dependência.</span><span class="sxs-lookup"><span data-stu-id="5c67a-143">**Windows Vista (default):** Provides the behavior with the race condition that applications may have a dependency on.</span></span> <span data-ttu-id="5c67a-144">Os aplicativos que desejam evitar essa corrida antes do comportamento do Windows 7 devem aguardar no evento sobreposto e, quando sinalizado, chamar GetOverlappedResult com bWait = = **false**.</span><span class="sxs-lookup"><span data-stu-id="5c67a-144">Applications wishing to avoid this race prior to the Windows 7 behavior should wait on the overlapped event and when signaled, call GetOverlappedResult with bWait == **FALSE**.</span></span>

<span data-ttu-id="5c67a-145">**PCA (Assistente de compatibilidade do programa)**</span><span class="sxs-lookup"><span data-stu-id="5c67a-145">**Program Compatibility Assistant (PCA)**</span></span>

-   <span data-ttu-id="5c67a-146">**Windows 7:** Aplicativos com a seção de compatibilidade não obterão a mitigação do PCA.</span><span class="sxs-lookup"><span data-stu-id="5c67a-146">**Windows 7:** Applications with Compatibility section will not get the PCA mitigation.</span></span>
-   <span data-ttu-id="5c67a-147">**Windows Vista (padrão):** Os aplicativos que não forem instalados corretamente ou falharem durante o tempo de execução em algumas circunstâncias específicas obterão a mitigação do PCA.</span><span class="sxs-lookup"><span data-stu-id="5c67a-147">**Windows Vista (default):** Applications that fail to install properly or crash during runtime under some specific circumstances will get the PCA mitigation.</span></span> <span data-ttu-id="5c67a-148">Para obter mais detalhes, consulte a seção de referência.</span><span class="sxs-lookup"><span data-stu-id="5c67a-148">For more details, see the reference section.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="5c67a-149">Aproveitando os recursos do recurso</span><span class="sxs-lookup"><span data-stu-id="5c67a-149">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="5c67a-150">Atualize o manifesto do aplicativo com as informações de compatibilidade mais recentes para o suporte do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5c67a-150">Update the application manifest with the latest Compatibility information for operating system support.</span></span> <span data-ttu-id="5c67a-151">A seção descreve as adições ao manifesto:</span><span class="sxs-lookup"><span data-stu-id="5c67a-151">The section describes the additions to the manifest:</span></span>

-   <span data-ttu-id="5c67a-152">**Namespace:** Compatibility. v1 (xmlns = "urn: schemas-microsoft-com: Compatibility. v1" >)</span><span class="sxs-lookup"><span data-stu-id="5c67a-152">**Namespace:** Compatibility.v1 (xmlns="urn:schemas-microsoft-com:compatibility.v1">)</span></span>

-   <span data-ttu-id="5c67a-153">**Nome da seção:** Compatibilidade (nova seção)</span><span class="sxs-lookup"><span data-stu-id="5c67a-153">**Section Name:** Compatibility (new section)</span></span>

-   <span data-ttu-id="5c67a-154">**SupportedOS:** GUID do sistema operacional com suporte-os GUIDs que mapeiam para os sistemas operacionais com suporte são:</span><span class="sxs-lookup"><span data-stu-id="5c67a-154">**SupportedOS:** GUID of supported operating system - The GUIDs that map to the supported operating systems are:</span></span>

    -   <span data-ttu-id="5c67a-155">{e2011457-1546-43c5-a5fe-008deee3d3f0} para Windows Vista: esse é o valor padrão para o contexto Switchback.</span><span class="sxs-lookup"><span data-stu-id="5c67a-155">{e2011457-1546-43c5-a5fe-008deee3d3f0} for Windows Vista: This is the default value for the switchback context.</span></span>
    -   <span data-ttu-id="5c67a-156">{35138b9a-5d96-4fbd-8e2d-a2440225f93a} para Windows 7: os aplicativos que definem esse valor no manifesto do aplicativo obtêm o comportamento do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5c67a-156">{35138b9a-5d96-4fbd-8e2d-a2440225f93a} for Windows 7: Applications that set this value in the application manifest get the Windows 7 behavior.</span></span>

    > [!Note]  
    > <span data-ttu-id="5c67a-157">A Microsoft irá gerar e lançar GUIDs para versões futuras do Windows, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="5c67a-157">Microsoft will generate and post GUIDs for future Windows versions as needed.</span></span>

     

<span data-ttu-id="5c67a-158">Veja a seguir um exemplo de um manifesto atualizado.</span><span class="sxs-lookup"><span data-stu-id="5c67a-158">The following is an example of an updated manifest.</span></span>

> [!Note]  
> <span data-ttu-id="5c67a-159">O atributo e os nomes de marca no manifesto do aplicativo diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5c67a-159">The attribute and tag names in the application manifest are case sensitive.</span></span>

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?> 
  <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--The ID below indicates application support for Windows Vista --> 
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates application support for Windows 7 --> 
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/> 
      </application> 
    </compatibility>
  </assembly>
```



<span data-ttu-id="5c67a-160">O valor da adição de GUIDs para ambos os sistemas operacionais no exemplo acima é fornecer suporte de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="5c67a-160">The value of adding GUIDs for both operating systems in the above example is to provide down-level support.</span></span> <span data-ttu-id="5c67a-161">Os aplicativos que dão suporte a ambas as plataformas não precisariam de manifestos separados para cada plataforma.</span><span class="sxs-lookup"><span data-stu-id="5c67a-161">Applications that support both platforms would not need separate manifests for each platform.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="5c67a-162">Compatibilidade, desempenho, confiabilidade e teste de usabilidade</span><span class="sxs-lookup"><span data-stu-id="5c67a-162">Compatibility, Performance, Reliability, and Usability Testing</span></span>

1.  <span data-ttu-id="5c67a-163">Testar o aplicativo com a nova seção de compatibilidade e `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` garantir que o aplicativo funcione corretamente usando o comportamento mais recente do Windows 7</span><span class="sxs-lookup"><span data-stu-id="5c67a-163">Test the application with the new compatibility section and `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` to ensure that the application works properly using the latest Windows 7 behavior</span></span>
2.  <span data-ttu-id="5c67a-164">Testar o aplicativo com a nova seção de compatibilidade e `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` (ou sem essa seção inteiramente) para garantir que o aplicativo funcione corretamente usando os comportamentos do Windows Vista no Windows 7</span><span class="sxs-lookup"><span data-stu-id="5c67a-164">Test the application with the new compatibility section and `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` (or without this section entirely) to ensure that the application works properly using the Windows Vista behaviors on Windows 7</span></span>

## <a name="known-issues"></a><span data-ttu-id="5c67a-165">Problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="5c67a-165">Known Issues</span></span>

<span data-ttu-id="5c67a-166">**Incompatibilidade de contexto** Um aplicativo é executado em um contexto do Windows Vista em vez de em um contexto do Windows 7 em um computador que esteja executando uma edição x64 do Windows 7 ou do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="5c67a-166">**Context Mismatch** An application runs in a Windows Vista context instead of in a Windows 7 context on a computer that is running an x64 edition of either Windows 7 or Windows Server 2008 R2.</span></span>

<span data-ttu-id="5c67a-167">**Solução** de As atualizações estão disponíveis para corrigir isso para todas as versões compatíveis com base em x64 do Windows 7 e do Windows Server 2008 R2, bem como para todas as versões compatíveis com base em Itanium do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="5c67a-167">**Solution** Updates are available to correct this for all supported x64-based versions of Windows 7 and Windows Server 2008 R2, as well as for all supported Itanium-based versions of Windows Server 2008 R2.</span></span> <span data-ttu-id="5c67a-168">Vá para a página de Suporte da Microsoft para [KB 978637: um aplicativo é executado em um contexto do Windows Vista em vez de em um contexto do Windows 7 em um computador que esteja executando uma edição x64 do Windows 7 ou do Windows Server 2008 R2](https://support.microsoft.com/kb/978637) para obter detalhes adicionais e baixar a versão correta para o seu sistema.</span><span class="sxs-lookup"><span data-stu-id="5c67a-168">Go to the Microsoft Support page for [KB 978637: An application runs in a Windows Vista context instead of in a Windows 7 context on a computer that is running an x64 edition of Windows 7 or of Windows Server 2008 R2](https://support.microsoft.com/kb/978637) for additional details and to download the correct version for your system.</span></span>

<span data-ttu-id="5c67a-169">**Diagnóstico de despejo de memória bloqueado**</span><span class="sxs-lookup"><span data-stu-id="5c67a-169">**Crash dump diagnosis blocked**</span></span>

<span data-ttu-id="5c67a-170">**Solução** de Vá para a página de Suporte da Microsoft para [KB 976038: exceções que são geradas de um aplicativo executado em uma versão de 64 bits do Windows são ignoradas](https://support.microsoft.com/kb/976038) para obter detalhes adicionais.</span><span class="sxs-lookup"><span data-stu-id="5c67a-170">**Solution** Go to the Microsoft Support page for [KB 976038: Exceptions that are thrown from an application that runs in a 64-bit version of Windows are ignored](https://support.microsoft.com/kb/976038) for additional details.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="5c67a-171">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="5c67a-171">Links to Other Resources</span></span>

-   [<span data-ttu-id="5c67a-172">**Função QueryActCtxW**</span><span class="sxs-lookup"><span data-stu-id="5c67a-172">**QueryActCtxW Function**</span></span>](/windows/win32/api/winbase/nf-winbase-queryactctxw)
-   <span data-ttu-id="5c67a-173">[Manifesto do UAC](/previous-versions/bb756929(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="5c67a-173">[UAC manifest](/previous-versions/bb756929(v=msdn.10))</span></span>
-   [<span data-ttu-id="5c67a-174">Manifestos de aplicativo para aplicativos do Windows</span><span class="sxs-lookup"><span data-stu-id="5c67a-174">Application manifests for Windows applications</span></span>](../sbscs/application-manifests.md)
-   [<span data-ttu-id="5c67a-175">Gerenciador de Janelas da Área de Trabalho (DWM)</span><span class="sxs-lookup"><span data-stu-id="5c67a-175">Desktop Window Manager (DWM)</span></span>](../dwm/dwm-overview.md)
-   [<span data-ttu-id="5c67a-176">Atualização de incompatibilidade de contexto</span><span class="sxs-lookup"><span data-stu-id="5c67a-176">Context Mismatch Update</span></span>](https://support.microsoft.com/kb/978637)

 

 
