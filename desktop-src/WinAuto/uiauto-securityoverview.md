---
title: Considerações de segurança para tecnologias assistenciais
description: Tecnologias assistenciais são aplicativos que são executados na área de trabalho do Windows e ajudam os usuários de acessibilidade a interagir com o sistema operacional e outros aplicativos em execução no computador, incluindo aplicativos na nova interface do usuário do Windows.
ms.assetid: 0c3689e1-2124-4142-b0bd-233e95ee1285
f1_keywords:
- vs.debug.error.launch_elevation_requirements
keywords:
- atributo uiAccess
- Automação da interface do usuário, atributo uiAccess
- segurança, atributo uiAccess
- marca de requestedExecutionLevel
- Automação da interface do usuário, marca requestedExecutionLevel
- Automação da interface do usuário, considerações de segurança
- Automação da interface do usuário, arquivos de manifesto
- arquivos de manifesto
- controle de conta de usuário
- segurança, controle de conta de usuário
- segurança, arquivos de manifesto
- segurança, marca requestedExecutionLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f2f5cf006c0adaf9b170a4ed11abd9afd52012
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2020
ms.locfileid: "105760525"
---
# <a name="security-considerations-for-assistive-technologies"></a><span data-ttu-id="a6385-115">Considerações de segurança para tecnologias assistenciais</span><span class="sxs-lookup"><span data-stu-id="a6385-115">Security Considerations for Assistive Technologies</span></span>

<span data-ttu-id="a6385-116">Tecnologias assistenciais são aplicativos que são executados na área de trabalho do Windows e ajudam os usuários de acessibilidade a interagir com o sistema operacional e outros aplicativos em execução no computador, incluindo aplicativos na nova interface do usuário do Windows.</span><span class="sxs-lookup"><span data-stu-id="a6385-116">Assistive technologies are applications that run on the Windows desktop and help accessibility users interact with the operating system and other applications running on the computer, including applications in the new Windows UI.</span></span> <span data-ttu-id="a6385-117">Os aplicativos de tecnologia assistencial funcionam recuperando informações do sistema operacional e de outros aplicativos e, em seguida, apresentando as informações de uma maneira que possa ser acessada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="a6385-117">Assistive technology applications work by retrieving information from the operating system and other applications, and then presenting the information in a way that is accessible to the user.</span></span> <span data-ttu-id="a6385-118">Um aplicativo de tecnologia assistencial também pode "impulsionar" de forma programática o sistema operacional e outros aplicativos com base na entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="a6385-118">An assistive technology application can also programmatically "drive" the operating system and other applications based on input from the user.</span></span>

<span data-ttu-id="a6385-119">A natureza dos aplicativos de tecnologia assistencial exige que eles entrem em limites de processo e que tenham acesso a processos executados em um nível de integridade mais alto (IL) do que em si.</span><span class="sxs-lookup"><span data-stu-id="a6385-119">The nature of assistive technology applications requires that they cross process boundaries, and that they have access to processes that run at a higher integrity level (IL) than themselves.</span></span> <span data-ttu-id="a6385-120">(Um aplicativo de tecnologia assistencial é executado em IL médio.) Por exemplo, quando o usuário tenta executar uma tarefa que requer privilégios administrativos, o Windows apresenta uma caixa de diálogo solicitando que o usuário tenha consentimento para continuar.</span><span class="sxs-lookup"><span data-stu-id="a6385-120">(An assistive technology application runs at medium IL.) For example, when the user attempts to perform a task that requires administrative privileges, Windows presents a dialog box asking the user for consent to continue.</span></span> <span data-ttu-id="a6385-121">Essa caixa de diálogo é executada em um IL superior para protegê-la da comunicação entre processos, para que o software mal-intencionado não possa simular a entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="a6385-121">This dialog box runs at a higher IL to protect it from cross-process communication, so that malicious software cannot simulate user input.</span></span> <span data-ttu-id="a6385-122">Da mesma forma, a tela de logon da área de trabalho é executada em um IL superior para impedir que ele seja acessado por outros processos.</span><span class="sxs-lookup"><span data-stu-id="a6385-122">Similarly, the desktop logon screen runs at a higher IL to prevent it from being accessed by other processes.</span></span>

<span data-ttu-id="a6385-123">Aplicativos de tecnologia assistencial normalmente precisam de acesso aos elementos de interface do usuário do sistema protegido ou a outros processos que podem estar sendo executados em um nível de privilégio mais alto.</span><span class="sxs-lookup"><span data-stu-id="a6385-123">Assistive technology applications typically need access to the protected system UI elements, or to other processes that might be running at a higher privilege level.</span></span> <span data-ttu-id="a6385-124">Portanto, os aplicativos de tecnologia assistencial devem ser confiáveis pelo sistema e devem ser executados com privilégios especiais.</span><span class="sxs-lookup"><span data-stu-id="a6385-124">Therefore, assistive technology applications must be trusted by the system, and must run with special privileges.</span></span>

<span data-ttu-id="a6385-125">Para obter acesso a processos de IL mais altos, um aplicativo de tecnologia assistencial deve definir o sinalizador UIAccess no manifesto do aplicativo e ser iniciado por um usuário com privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="a6385-125">To get access to higher IL processes, an assistive technology application must set the UIAccess flag in the application's manifest and be launched by a user with administrator privileges.</span></span>

> [!NOTE]
> <span data-ttu-id="a6385-126">Os privilégios de acesso são restritos da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a6385-126">Access privileges are constrained as follows:</span></span>
>
> - <span data-ttu-id="a6385-127">Um aplicativo que não tem o UIAccess no manifesto começa com IL médio e não pode acessar a interface do usuário de processo com privilégios elevados ("média +" IL).</span><span class="sxs-lookup"><span data-stu-id="a6385-127">An application that doesn't have UIAccess in the manifest starts with medium IL and cannot access elevated ("medium+" IL) process UI.</span></span>
> - <span data-ttu-id="a6385-128">Um aplicativo que tem o UIAccess no manifesto e é iniciado por um usuário que não está no grupo Administradores, começa como IL "médio +" e não pode acessar a interface do usuário elevada (nada executando como IL "alta", como aplicativos iniciados por meio de um **clique com o botão direito do mouse > executar como administrador**).</span><span class="sxs-lookup"><span data-stu-id="a6385-128">An application that has UIAccess in the manifest and is launched by a user who is not in the administrators group, starts as "medium+" IL and cannot access elevated UI (nothing running as "high" IL, such as apps launched through a **Right click -> Run as administrator**).</span></span>
> - <span data-ttu-id="a6385-129">Um aplicativo tem acesso à interface de usuário e é iniciado por um usuário administrador inicia como IL "alta" e pode acessar a interface do usuário elevada porque ele tem o mesmo IL.</span><span class="sxs-lookup"><span data-stu-id="a6385-129">An application has UI Access and is launched by an admin user starts as "high" IL and can access elevated UI because it has the same IL.</span></span>
>
> <span data-ttu-id="a6385-130">O UIAccess não é suficiente para que um processo avance pelo limite de IL.</span><span class="sxs-lookup"><span data-stu-id="a6385-130">UIAccess is not enough for a process to move up through the IL boundary.</span></span>

<span data-ttu-id="a6385-131">Além de ter acesso a processos de IL mais altos, um aplicativo de tecnologia assistencial com esses privilégios pode ser executado como o aplicativo mais alto na ordem z a qualquer momento, o que significa que um aplicativo de tecnologia assistencial pode ficar visível e disponível sempre que o usuário precisar.</span><span class="sxs-lookup"><span data-stu-id="a6385-131">In addition to having access to higher IL processes, an assistive technology application with these privileges can run as the topmost application in the z-order at any time, meaning that an assistive technology application can be visible and available whenever the user needs it.</span></span>

> [!Important]
> <span data-ttu-id="a6385-132">Nenhum dos cenários listados anteriormente fornece acesso à interface do usuário em execução no IL do sistema.</span><span class="sxs-lookup"><span data-stu-id="a6385-132">None of the previously listed scenarios provide access to UI running under the system IL.</span></span> <span data-ttu-id="a6385-133">Isso só será possível se o processo for iniciado na área de trabalho do UAC (controle de conta de usuário) em sistema (e IL do sistema).</span><span class="sxs-lookup"><span data-stu-id="a6385-133">This is only possible if the process is launched in the user account control (UAC) desktop under SYSTEM (and system IL).</span></span> <span data-ttu-id="a6385-134">Nesse caso, a definição de UIAccess não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="a6385-134">In this case, setting UIAccess has no effect.</span></span>

## <a name="uiaccess-requirements-for-assistive-technology-applications"></a><span data-ttu-id="a6385-135">Requisitos de UIAccess para aplicativos de tecnologia assistencial</span><span class="sxs-lookup"><span data-stu-id="a6385-135">UIAccess Requirements for Assistive Technology Applications</span></span>

<span data-ttu-id="a6385-136">Um aplicativo de tecnologia assistencial é um aplicativo da área de trabalho do Windows Windows que interage com outros processos em execução na área de trabalho e na nova interface do usuário do Windows para obter informações do sistema e dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="a6385-136">An assistive technology application is a Windows Windows desktop application that interacts with other processes running on the desktop and in the new Windows UI to get information from the system and applications.</span></span> <span data-ttu-id="a6385-137">O aplicativo de tecnologia assistencial pode fornecer as informações aos usuários de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="a6385-137">The assistive technology application can then provide the information to accessibility users.</span></span>

<span data-ttu-id="a6385-138">Um aplicativo de tecnologia assistencial obtém acesso a outros processos definindo o sinalizador UIAccess no manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a6385-138">An assistive technology application gets access to other processes by setting the UIAccess flag in the application manifest.</span></span> <span data-ttu-id="a6385-139">Para usar o sinalizador UIAccess, um aplicativo de tecnologia assistencial deve atender aos seguintes requisitos.</span><span class="sxs-lookup"><span data-stu-id="a6385-139">To use the UIAccess flag, an assistive technology application must meet the following requirements.</span></span>

-   <span data-ttu-id="a6385-140">Exigir para exibir, interagir ou refletir informações de outro aplicativo para fornecer informações para um cenário de acessibilidade e/ou</span><span class="sxs-lookup"><span data-stu-id="a6385-140">Require to display, interact with, or reflect information from another application to provide information for an accessibility scenario, and/or</span></span>
-   <span data-ttu-id="a6385-141">Exigir a execução como a janela superior para obter ou exibir essas informações.</span><span class="sxs-lookup"><span data-stu-id="a6385-141">Require running as the top-most window to obtain or display this information.</span></span>

<span data-ttu-id="a6385-142">Para usar o UIAccess, um aplicativo de tecnologia assistencial precisa:</span><span class="sxs-lookup"><span data-stu-id="a6385-142">To use UIAccess, an assistive technology application needs to:</span></span>

-   <span data-ttu-id="a6385-143">Ser assinado com um certificado para interagir com aplicativos em execução em um nível de privilégio mais alto.</span><span class="sxs-lookup"><span data-stu-id="a6385-143">Be signed with a certificate to interact with applications running at a higher privilege level.</span></span>
-   <span data-ttu-id="a6385-144">Seja confiável pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="a6385-144">Be trusted by the system.</span></span> <span data-ttu-id="a6385-145">O aplicativo deve ser instalado em um local seguro que exija um prompt de controle de conta de usuário (UAC) para acesso.</span><span class="sxs-lookup"><span data-stu-id="a6385-145">The application must be installed in a secure location that requires a user account control (UAC) prompt for access.</span></span> <span data-ttu-id="a6385-146">Por exemplo, a pasta arquivos de programas.</span><span class="sxs-lookup"><span data-stu-id="a6385-146">For example, the Program Files folder.</span></span>
-   <span data-ttu-id="a6385-147">Seja criado com um arquivo de manifesto que inclui o sinalizador uiAccess.</span><span class="sxs-lookup"><span data-stu-id="a6385-147">Be built with a manifest file that includes the uiAccess flag.</span></span>

<span data-ttu-id="a6385-148">O UIAccess não deve ser usado:</span><span class="sxs-lookup"><span data-stu-id="a6385-148">UIAccess should not be used:</span></span>

-   <span data-ttu-id="a6385-149">Por aplicativos que não são tecnologias assistenciais.</span><span class="sxs-lookup"><span data-stu-id="a6385-149">By applications that are not assistive technologies.</span></span>
-   <span data-ttu-id="a6385-150">Por aplicativos de tecnologia assistencial que exibem informações ou interface do usuário que não são relevantes para o cenário de acessibilidade que eles visam.</span><span class="sxs-lookup"><span data-stu-id="a6385-150">By assistive technology applications that display information or UI that is not relevant to the accessibility scenario they target.</span></span>
-   <span data-ttu-id="a6385-151">Por aplicativos que só desejam aparecer acima de outros aplicativos na nova interface do usuário do Windows.</span><span class="sxs-lookup"><span data-stu-id="a6385-151">By applications that just want to appear above other applications in the new Windows UI.</span></span>
    > [!Note]  
    > <span data-ttu-id="a6385-152">Os aplicativos desenvolvidos para a nova interface do usuário do Windows não têm o UIAccess como uma opção disponível.</span><span class="sxs-lookup"><span data-stu-id="a6385-152">Applications developed for the new Windows UI do not have UIAccess as an available option.</span></span>

     

## <a name="setting-uiaccess-in-the-application-manifest-file"></a><span data-ttu-id="a6385-153">Definindo o UIAccess no arquivo de manifesto do aplicativo</span><span class="sxs-lookup"><span data-stu-id="a6385-153">Setting UIAccess in the Application Manifest File</span></span>

<span data-ttu-id="a6385-154">Para obter acesso à interface do usuário do sistema protegido, os aplicativos devem ser criados com um arquivo de manifesto que inclui um atributo especial no arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="a6385-154">To gain access to the protected system UI, applications must be built with a manifest file that includes a special attribute in the manifest file.</span></span> <span data-ttu-id="a6385-155">Esse atributo **UIAccess** é incluído na marca **requestedExecutionLevel** , conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a6385-155">This **uiAccess** attribute is included in the **requestedExecutionLevel** tag, as shown in the following code example.</span></span>


```XML
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3"> 
    <security> 
        <requestedPrivileges> 
        <requestedExecutionLevel 
            level="highestAvailable" 
            uiAccess="true" /> 
        </requestedPrivileges> 
    </security> 
</trustInfo> 
```



<span data-ttu-id="a6385-156">O valor do atributo **Level** neste código é apenas um exemplo.</span><span class="sxs-lookup"><span data-stu-id="a6385-156">The value of the **level** attribute in this code is an example only.</span></span>

<span data-ttu-id="a6385-157">O **UIAccess** é "false" por padrão.</span><span class="sxs-lookup"><span data-stu-id="a6385-157">**UIAccess** is "false" by default.</span></span> <span data-ttu-id="a6385-158">Se o atributo for omitido ou se não houver nenhum manifesto, o aplicativo não poderá obter acesso à interface do usuário protegida.</span><span class="sxs-lookup"><span data-stu-id="a6385-158">If the attribute is omitted, or if there is no manifest, the application cannot gain access to the protected UI.</span></span>

<span data-ttu-id="a6385-159">Para obter mais informações sobre a segurança do Windows, em aplicativos de assinatura e sobre como criar manifestos, consulte [a história do desenvolvedor do Windows Vista e do Windows Server 2008: requisitos de desenvolvimento de aplicativos do Windows Vista para o UAC (controle de conta de usuário)](/previous-versions/aa905330(v=msdn.10)) no msdn.</span><span class="sxs-lookup"><span data-stu-id="a6385-159">For more information on Windows security, on signing applications, and on creating manifests, see [The Windows Vista and Windows Server 2008 Developer Story: Windows Vista Application Development Requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10)) on MSDN.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6385-160">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a6385-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6385-161">Conceitos básicos de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="a6385-161">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
</dt> </dl>

 

 