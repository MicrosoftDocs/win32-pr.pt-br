---
title: Facilidade de acesso de registro de tecnologia assistencial
description: Este artigo explica como registrar um aplicativo de acessibilidade com o centro de facilidade de acesso. Ele também explica como personalizar seu aplicativo de acessibilidade para que ele funcione bem com a área de trabalho segura.
ms.assetid: 6F1F2AAE-B2E4-4F26-8BDF-A3DE8F5C5460
ms.topic: article
ms.date: 04/02/2019
ms.openlocfilehash: 66901cd899fc578b032f86e3752fcdcac0788ba1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105789328"
---
# <a name="ease-of-access---assistive-technology-registration"></a><span data-ttu-id="f3c34-104">Facilidade de acesso de registro de tecnologia assistencial</span><span class="sxs-lookup"><span data-stu-id="f3c34-104">Ease of Access   Assistive Technology Registration</span></span>

<span data-ttu-id="f3c34-105">Este artigo explica como registrar um aplicativo de acessibilidade com o centro de facilidade de acesso.</span><span class="sxs-lookup"><span data-stu-id="f3c34-105">This article explains how to register an accessibility application with the Ease of Access Center.</span></span> <span data-ttu-id="f3c34-106">Ele também explica como personalizar seu aplicativo de acessibilidade para que ele funcione bem com a área de trabalho segura.</span><span class="sxs-lookup"><span data-stu-id="f3c34-106">It also explains how to tailor your accessibility application so it works well with the secure desktop.</span></span>

<span data-ttu-id="f3c34-107">O centro de facilidade de acesso é um aplicativo de painel de controle para o Microsoft Windows que reúne a funcionalidade de acessibilidade e facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="f3c34-107">The Ease of Access Center is a Control Panel application for Microsoft Windows brings together functionality for accessibility and ease of use.</span></span> <span data-ttu-id="f3c34-108">Usando a central de facilidade de acesso, os usuários podem configurar seus computadores para atender às suas necessidades físicas e cognitivas.</span><span class="sxs-lookup"><span data-stu-id="f3c34-108">By using the Ease of Access Center, users can configure their computers to suit their physical and cognitive needs.</span></span>

<span data-ttu-id="f3c34-109">Uma função da central de facilidade de acesso é ajudar os usuários a iniciar aplicativos de acessibilidade, incluindo o narrador, o teclado virtual e a lupa.</span><span class="sxs-lookup"><span data-stu-id="f3c34-109">One function of the Ease of Access Center is to help users launch accessibility applications, including Narrator, On-Screen Keyboard, and Magnifier.</span></span> <span data-ttu-id="f3c34-110">Os aplicativos de terceiros registrados também aparecem no centro de facilidade de acesso e podem ser iniciados diretamente a partir daí.</span><span class="sxs-lookup"><span data-stu-id="f3c34-110">Registered third-party applications also appear in the Ease of Access Center and can be launched directly from there.</span></span>

<span data-ttu-id="f3c34-111">Os aplicativos de acessibilidade precisam trabalhar sem problemas com a área de trabalho segura.</span><span class="sxs-lookup"><span data-stu-id="f3c34-111">Accessibility applications need to work smoothly with the secure desktop.</span></span> <span data-ttu-id="f3c34-112">A área de trabalho segura é a interface do usuário que aparece quando o computador está bloqueado (no logon ou quando o usuário bloqueou a área de trabalho) e quando o usuário é solicitado a permitir uma ação potencialmente não segura.</span><span class="sxs-lookup"><span data-stu-id="f3c34-112">The secure desktop is the user interface that appears when the computer is locked (at log-on or when the user has locked the desktop), and when the user is prompted to allow a potentially unsafe action.</span></span> <span data-ttu-id="f3c34-113">Por motivos de segurança, o Windows coloca os limites de software de terceiros em execução na área de trabalho segura.</span><span class="sxs-lookup"><span data-stu-id="f3c34-113">For security reasons, Windows places limits on third-party software running on the secure desktop.</span></span> <span data-ttu-id="f3c34-114">Se você quiser que seu aplicativo de acessibilidade seja executado na área de trabalho segura, você precisará registrar o aplicativo com o centro de facilidade de acesso.</span><span class="sxs-lookup"><span data-stu-id="f3c34-114">If you want your accessibility application to run on the secure desktop, you need to register the application with the Ease of Access Center.</span></span>

## <a name="registering-with-the-ease-of-access-center"></a><span data-ttu-id="f3c34-115">Registrando com o centro de facilidade de acesso</span><span class="sxs-lookup"><span data-stu-id="f3c34-115">Registering with the Ease of Access Center</span></span>

<span data-ttu-id="f3c34-116">Os aplicativos de acessibilidade se registram com o centro de facilidade de acesso criando uma ou mais chaves do registro quando o aplicativo é instalado.</span><span class="sxs-lookup"><span data-stu-id="f3c34-116">Accessibility applications register with the Ease of Access Center by creating one or more registry keys when the application is installed.</span></span> <span data-ttu-id="f3c34-117">A tabela a seguir lista as informações contidas nas chaves do registro.</span><span class="sxs-lookup"><span data-stu-id="f3c34-117">The following table lists the information contained in the registry keys.</span></span>



| <span data-ttu-id="f3c34-118">Nome</span><span class="sxs-lookup"><span data-stu-id="f3c34-118">Name</span></span>                        | <span data-ttu-id="f3c34-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3c34-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="f3c34-120">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="f3c34-120">Mandatory/Optional</span></span> | <span data-ttu-id="f3c34-121">Idioma</span><span class="sxs-lookup"><span data-stu-id="f3c34-121">Language</span></span>      |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|---------------|
| <span data-ttu-id="f3c34-122">Nome do Aplicativo</span><span class="sxs-lookup"><span data-stu-id="f3c34-122">Application Name</span></span>            | <span data-ttu-id="f3c34-123">O nome do aplicativo, que está em um arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="f3c34-123">The name of the application, which is in a resource file.</span></span> <span data-ttu-id="f3c34-124">Esse valor de registro contém uma cadeia de caracteres em um formato especificado.</span><span class="sxs-lookup"><span data-stu-id="f3c34-124">This registry value contains a string in a specified format.</span></span> <span data-ttu-id="f3c34-125">Essa pode ser uma versão localizada do nome do aplicativo, se o aplicativo estiver localizado em idiomas diferentes do inglês.</span><span class="sxs-lookup"><span data-stu-id="f3c34-125">This could be a localized version of the application name, if the application is localized in languages other than English.</span></span> <span data-ttu-id="f3c34-126">O nome aparece na central de facilidade de acesso.</span><span class="sxs-lookup"><span data-stu-id="f3c34-126">The name appears in the Ease of Access Center.</span></span><br/>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="f3c34-127">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f3c34-127">Mandatory</span></span>          | <span data-ttu-id="f3c34-128">Localizado</span><span class="sxs-lookup"><span data-stu-id="f3c34-128">Localized</span></span>     |
| <span data-ttu-id="f3c34-129">ATExe</span><span class="sxs-lookup"><span data-stu-id="f3c34-129">ATExe</span></span>                       | <span data-ttu-id="f3c34-130">O nome do arquivo executável do aplicativo ou da imagem.</span><span class="sxs-lookup"><span data-stu-id="f3c34-130">The name of the application executable file or image.</span></span> <span data-ttu-id="f3c34-131">O Windows usa esse valor para determinar se o aplicativo de acessibilidade está em execução.</span><span class="sxs-lookup"><span data-stu-id="f3c34-131">Windows uses this value to determine whether the accessibility application is running.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="f3c34-132">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f3c34-132">Mandatory</span></span>          | <span data-ttu-id="f3c34-133">Não localizado</span><span class="sxs-lookup"><span data-stu-id="f3c34-133">Not localized</span></span> |
| <span data-ttu-id="f3c34-134">CopySettingsToLockedDesktop</span><span class="sxs-lookup"><span data-stu-id="f3c34-134">CopySettingsToLockedDesktop</span></span> | <span data-ttu-id="f3c34-135">Um valor **DWORD** que indica se as configurações do aplicativo de acessibilidade devem ser copiadas na área de trabalho bloqueada.</span><span class="sxs-lookup"><span data-stu-id="f3c34-135">A **DWORD** value that indicates whether to copy the accessibility application's settings to the locked desktop.</span></span><br/> <span data-ttu-id="f3c34-136">Se esse valor for 1, o aplicativo poderá gravar configurações em um local no registro do usuário e o Windows copiará as configurações para o mesmo local no registro do usuário para a área de trabalho bloqueada.</span><span class="sxs-lookup"><span data-stu-id="f3c34-136">If this value is 1, the application can write settings to a location in the user registry, and Windows copies the settings to the same location in the user registry for the locked desktop.</span></span> <span data-ttu-id="f3c34-137">Isso permite que o aplicativo persista seu estado da área de trabalho "normal" para a área de trabalho bloqueada.</span><span class="sxs-lookup"><span data-stu-id="f3c34-137">This enables the application to persist its state from the "normal" desktop to the locked desktop.</span></span><br/>                                                                                                                                                             | <span data-ttu-id="f3c34-138">Opcional</span><span class="sxs-lookup"><span data-stu-id="f3c34-138">Optional</span></span>           | <span data-ttu-id="f3c34-139">Não localizado</span><span class="sxs-lookup"><span data-stu-id="f3c34-139">Not localized</span></span> |
| <span data-ttu-id="f3c34-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3c34-140">Description</span></span>                 | <span data-ttu-id="f3c34-141">Uma breve descrição do aplicativo, de um arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="f3c34-141">A brief description of the application, from a resource file.</span></span> <span data-ttu-id="f3c34-142">Esse valor de registro contém uma cadeia de caracteres em um formato especificado.</span><span class="sxs-lookup"><span data-stu-id="f3c34-142">This registry value contains a string in a specified format.</span></span> <span data-ttu-id="f3c34-143">Essa pode ser uma versão localizada da descrição, se o aplicativo estiver localizado em idiomas diferentes do inglês.</span><span class="sxs-lookup"><span data-stu-id="f3c34-143">This could be a localized version of the description, if the application is localized in languages other than English.</span></span> <span data-ttu-id="f3c34-144">O comprimento dessa cadeia de caracteres deve ter menos de 512 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f3c34-144">The length of this string must be less than 512 characters.</span></span><br/> <span data-ttu-id="f3c34-145">A descrição é exibida na central de facilidade de acesso para fornecer informações adicionais sobre o aplicativo de acessibilidade ao usuário.</span><span class="sxs-lookup"><span data-stu-id="f3c34-145">The description appears in the Ease of Access Center to provide additional information about the accessibility application to the user.</span></span><br/> <span data-ttu-id="f3c34-146">Esse valor também pode ser usado para notificar o usuário de que o aplicativo não é usado na área de trabalho segura.</span><span class="sxs-lookup"><span data-stu-id="f3c34-146">This value can also be used to notify the user that the application is not used on the secure desktop.</span></span><br/>      | <span data-ttu-id="f3c34-147">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f3c34-147">Mandatory</span></span>          | <span data-ttu-id="f3c34-148">Localizado</span><span class="sxs-lookup"><span data-stu-id="f3c34-148">Localized</span></span>     |
| <span data-ttu-id="f3c34-149">Perfil</span><span class="sxs-lookup"><span data-stu-id="f3c34-149">Profile</span></span>                     | <span data-ttu-id="f3c34-150">Uma pequena parte do XML que especifica as acomodações que o aplicativo fornece.</span><span class="sxs-lookup"><span data-stu-id="f3c34-150">A short piece of XML that specifies the accommodations that the application provides.</span></span> <span data-ttu-id="f3c34-151">Ele garante que o aplicativo aparece sob a categoria correta no centro de facilidade de acesso.</span><span class="sxs-lookup"><span data-stu-id="f3c34-151">It ensures that the application appears under the correct category in the Ease of Access Center.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="f3c34-152">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f3c34-152">Mandatory</span></span>          | <span data-ttu-id="f3c34-153">Não localizado</span><span class="sxs-lookup"><span data-stu-id="f3c34-153">Not localized</span></span> |
| <span data-ttu-id="f3c34-154">PassiveAutoStartBehavior</span><span class="sxs-lookup"><span data-stu-id="f3c34-154">PassiveAutoStartBehavior</span></span>    | <p><span data-ttu-id="f3c34-155">Um valor **DWORD** que indica se o comportamento de início automático herdado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f3c34-155">A **DWORD** value that indicates whether legacy auto-start behavior is enabled.</span></span></p><p><span data-ttu-id="f3c34-156">O valor padrão é 0, o que indica que um AT requer comportamento de início automático herdado.</span><span class="sxs-lookup"><span data-stu-id="f3c34-156">The default value is 0, which indicates that an AT requires legacy auto-start behavior.</span></span> <span data-ttu-id="f3c34-157">Isso faz com que a configuração "iniciar após a entrada" para que a seja verificada na opção OOBE (configuração inicial pelo uso) e no painel de controle (consulte **painel de controle-> facilidade de acesso-> facilidade de acesso – > alterar as configurações de entrada**) e inicia automaticamente o UAC e a tela de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="f3c34-157">This  causes the “Start after sign-in” setting for that AT to be checked in the Out Of Box Experience (OOBE) and Control Panel (see **Control Panel -> Ease of Access -> Ease of Access Center -> Change sign-in settings**), and automatically starts the AT after UAC and lock-screen.</span></span></p><p><span data-ttu-id="f3c34-158">Um valor de 1 indica que o AT deve usar o novo comportamento de início automático em que a configuração "iniciar após a entrada" para isso em não é marcada na opção OOBE (configuração inicial pelo usuário) e no painel de controle, e o AT é iniciado automaticamente uma vez por sessão de usuários (no logon) somente se a configuração "iniciar após a entrada" estiver marcada.</span><span class="sxs-lookup"><span data-stu-id="f3c34-158">A value of 1 indicates that the AT should use the new auto-start behavior where the “Start after sign-in” setting for that AT is not checked in the Out Of Box Experience (OOBE) and Control Panel, and the AT is automatically started once per user session (at login) only if the “start after sign-in” setting is checked.</span></span></p>                                                                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="f3c34-159">Opcional</span><span class="sxs-lookup"><span data-stu-id="f3c34-159">Optional</span></span>          | <span data-ttu-id="f3c34-160">Não localizado</span><span class="sxs-lookup"><span data-stu-id="f3c34-160">Not localized</span></span> |
| <span data-ttu-id="f3c34-161">SecureDesktopAccommodation</span><span class="sxs-lookup"><span data-stu-id="f3c34-161">SecureDesktopAccommodation</span></span>  | <span data-ttu-id="f3c34-162">O nome de um aplicativo de acessibilidade alternativo a ser executado na área de trabalho segura no lugar deste aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f3c34-162">The name of an alternate accessibility application to run on the secure desktop in the place of this application.</span></span> <span data-ttu-id="f3c34-163">A alternativa pode ser um aplicativo diferente, uma versão diferente do mesmo aplicativo, um dos aplicativos de acessibilidade incluídos no Windows ou "nenhum" se você não quiser executar nenhum aplicativo de acessibilidade na área de trabalho segura.</span><span class="sxs-lookup"><span data-stu-id="f3c34-163">The alternate can be a different application, a different version of the same application, one of the accessibility applications that is included in Windows, or "none" if you do not want to run any accessibility application on the secure desktop.</span></span> <br/>                                                                                                                                                                                                               | <span data-ttu-id="f3c34-164">Opcional</span><span class="sxs-lookup"><span data-stu-id="f3c34-164">Optional</span></span>           | <span data-ttu-id="f3c34-165">Não localizado</span><span class="sxs-lookup"><span data-stu-id="f3c34-165">Not localized</span></span> |
| <span data-ttu-id="f3c34-166">Perfil simples</span><span class="sxs-lookup"><span data-stu-id="f3c34-166">Simple Profile</span></span>              | <span data-ttu-id="f3c34-167">Um valor que descreve como classificar o aplicativo em uma palavra ou duas: leitor de tela, lupa ou teclado na tela, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="f3c34-167">A value that describes how to classify the application in a word or two: Screen reader, Magnifier, or On-screen keyboard, for example.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="f3c34-168">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f3c34-168">Mandatory</span></span>          | <span data-ttu-id="f3c34-169">Não localizado</span><span class="sxs-lookup"><span data-stu-id="f3c34-169">Not localized</span></span> |
| <span data-ttu-id="f3c34-170">StartExe</span><span class="sxs-lookup"><span data-stu-id="f3c34-170">StartExe</span></span>                    | <span data-ttu-id="f3c34-171">O caminho completo do executável.</span><span class="sxs-lookup"><span data-stu-id="f3c34-171">The full path of the executable.</span></span> <span data-ttu-id="f3c34-172">Esse valor é usado para iniciar o aplicativo de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="f3c34-172">This value is used to launch the accessibility application.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="f3c34-173">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f3c34-173">Mandatory</span></span>          | <span data-ttu-id="f3c34-174">Não localizado</span><span class="sxs-lookup"><span data-stu-id="f3c34-174">Not localized</span></span> |
| <span data-ttu-id="f3c34-175">StartParams</span><span class="sxs-lookup"><span data-stu-id="f3c34-175">StartParams</span></span>                 | <span data-ttu-id="f3c34-176">Argumentos de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f3c34-176">Command-line arguments.</span></span> <span data-ttu-id="f3c34-177">Esses valores são usados junto com StartExe para iniciar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f3c34-177">These values are used along with StartExe to start the application.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="f3c34-178">Opcional</span><span class="sxs-lookup"><span data-stu-id="f3c34-178">Optional</span></span>           | <span data-ttu-id="f3c34-179">Não localizado</span><span class="sxs-lookup"><span data-stu-id="f3c34-179">Not localized</span></span> |
| <span data-ttu-id="f3c34-180">TerminateOnDesktopSwitch</span><span class="sxs-lookup"><span data-stu-id="f3c34-180">TerminateOnDesktopSwitch</span></span>    | <span data-ttu-id="f3c34-181">Um valor **DWORD** que especifica como o aplicativo de acessibilidade responde a transições de ou para a área de trabalho segura.</span><span class="sxs-lookup"><span data-stu-id="f3c34-181">A **DWORD** value that specifies how the accessibility application responds to transitions to or from the secure desktop.</span></span><br/> <span data-ttu-id="f3c34-182">Se esse valor não existir ou for 1, o Windows terminará e reiniciará o aplicativo em cada transição de ou para a área de trabalho segura.</span><span class="sxs-lookup"><span data-stu-id="f3c34-182">If this value does not exist or is 1, Windows terminates and restarts the application on each transition to or from the secure desktop.</span></span> <span data-ttu-id="f3c34-183">Esse é o comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="f3c34-183">This is the default behavior.</span></span><br/> <span data-ttu-id="f3c34-184">Se esse valor for 0, o Windows não encerrará o aplicativo de acessibilidade em uma transição de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f3c34-184">If this value is 0, Windows does not terminate the accessibility application on a desktop transition.</span></span> <span data-ttu-id="f3c34-185">O aplicativo continuará a ser executado na área de trabalho anterior e o Windows iniciará uma nova instância na nova área de trabalho se uma instância ainda não estiver em execução lá.</span><span class="sxs-lookup"><span data-stu-id="f3c34-185">The application continues to run on the previous desktop, and Windows starts a new instance on the new desktop if an instance is not already running there.</span></span><br/> | <span data-ttu-id="f3c34-186">Opcional</span><span class="sxs-lookup"><span data-stu-id="f3c34-186">Optional</span></span>           | <span data-ttu-id="f3c34-187">Não localizado</span><span class="sxs-lookup"><span data-stu-id="f3c34-187">Not localized</span></span> |


 

### <a name="localization"></a><span data-ttu-id="f3c34-188">Localização</span><span class="sxs-lookup"><span data-stu-id="f3c34-188">Localization</span></span>

<span data-ttu-id="f3c34-189">Os valores do registro do nome do aplicativo e da descrição precisam ser localizáveis para dar suporte à MUI (Multilingual User interface).</span><span class="sxs-lookup"><span data-stu-id="f3c34-189">The registry values of Application Name and Description need to be localizable to support Multilingual User Interface (MUI).</span></span>

<span data-ttu-id="f3c34-190">Essas cadeias de caracteres estão no formato a seguir, em que os colchetes angulares significam elementos e colchetes obrigatórios significam um elemento opcional.</span><span class="sxs-lookup"><span data-stu-id="f3c34-190">These strings are in the following format, where angle brackets signify required elements and square brackets signify an optional element.</span></span>

<span data-ttu-id="f3c34-191">*@ <ResDllPath \\ ResDLLFilename>,- <resID> \[ ;<comment>\]*</span><span class="sxs-lookup"><span data-stu-id="f3c34-191">*@<ResDllPath\\ResDLLFilename>,-<resID>\[;<comment>\]*</span></span>

<span data-ttu-id="f3c34-192">*<ResDllPath \\ ResDLLFilename>* é o caminho para a DLL de recursos.</span><span class="sxs-lookup"><span data-stu-id="f3c34-192">*<ResDllPath\\ResDLLFilename>* is the path to the resource DLL.</span></span> <span data-ttu-id="f3c34-193">O caminho pode conter variáveis ambientais.</span><span class="sxs-lookup"><span data-stu-id="f3c34-193">The path can contain environmental variables.</span></span>

<span data-ttu-id="f3c34-194">*<resID>* é a ID de recurso para a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f3c34-194">*<resID>* is the resource ID for the string.</span></span>

<span data-ttu-id="f3c34-195">o *\[ comentário \]* contém comentários opcionais.</span><span class="sxs-lookup"><span data-stu-id="f3c34-195">*\[comment\]* contains any optional comments.</span></span>

<span data-ttu-id="f3c34-196">Veja um exemplo:</span><span class="sxs-lookup"><span data-stu-id="f3c34-196">Here is an example:</span></span>


```
@%SystemRoot%\system32\anyAT.dll,-5020
```



<span data-ttu-id="f3c34-197">Para obter mais informações sobre o MUI, consulte [centro de conhecimento do MUI do Windows](../intl/about-multilingual-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="f3c34-197">For more information about MUI, see [Windows MUI Knowledge Center](../intl/about-multilingual-user-interface.md).</span></span>

### <a name="hci-profile"></a><span data-ttu-id="f3c34-198">Perfil de HCI</span><span class="sxs-lookup"><span data-stu-id="f3c34-198">HCI Profile</span></span>

<span data-ttu-id="f3c34-199">O perfil de HCI (interação humana do computador) é uma maneira de determinar quais acomodações fornecer com base nas necessidades do usuário.</span><span class="sxs-lookup"><span data-stu-id="f3c34-199">The Human Computer Interaction (HCI) profile is a way to determine what accommodations to provide based on the needs of the user.</span></span> <span data-ttu-id="f3c34-200">Os aplicativos de acessibilidade devem registrar informações sobre o tipo de deficiência que o aplicativo ajuda a acomodar.</span><span class="sxs-lookup"><span data-stu-id="f3c34-200">Accessibility applications should register information about the kind of disability the application helps to accommodate.</span></span>

<span data-ttu-id="f3c34-201">O valor do registro de perfil contém XML que descreve o tipo de deficiência de destino do aplicativo de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="f3c34-201">The Profile registry value contains XML that describes the kind of disability targeted by the accessibility application.</span></span> <span data-ttu-id="f3c34-202">Esse XML tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="f3c34-202">This XML has the following format:</span></span>


```XML
<HCIModel>
<Accommodation type="disability"/>
</HCIModel>
```



<span data-ttu-id="f3c34-203">Os valores válidos para o atributo **tipo de acomodação** são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="f3c34-203">The valid values for the **Accommodation type** attribute are as follows:</span></span>

-   <span data-ttu-id="f3c34-204">visão leve</span><span class="sxs-lookup"><span data-stu-id="f3c34-204">mild vision</span></span>
-   <span data-ttu-id="f3c34-205">visão severa</span><span class="sxs-lookup"><span data-stu-id="f3c34-205">severe vision</span></span>
-   <span data-ttu-id="f3c34-206">percepção leve</span><span class="sxs-lookup"><span data-stu-id="f3c34-206">mild cognitive</span></span>
-   <span data-ttu-id="f3c34-207">cognitiva severo</span><span class="sxs-lookup"><span data-stu-id="f3c34-207">severe cognitive</span></span>
-   <span data-ttu-id="f3c34-208">destreza leve</span><span class="sxs-lookup"><span data-stu-id="f3c34-208">mild dexterity</span></span>
-   <span data-ttu-id="f3c34-209">destreza severa</span><span class="sxs-lookup"><span data-stu-id="f3c34-209">severe dexterity</span></span>
-   <span data-ttu-id="f3c34-210">audição leve</span><span class="sxs-lookup"><span data-stu-id="f3c34-210">mild hearing</span></span>
-   <span data-ttu-id="f3c34-211">audição severa</span><span class="sxs-lookup"><span data-stu-id="f3c34-211">severe hearing</span></span>
-   <span data-ttu-id="f3c34-212">Fala leve</span><span class="sxs-lookup"><span data-stu-id="f3c34-212">mild speech</span></span>
-   <span data-ttu-id="f3c34-213">Fala severa</span><span class="sxs-lookup"><span data-stu-id="f3c34-213">severe speech</span></span>

> [!Note]  
> <span data-ttu-id="f3c34-214">Estes valores diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f3c34-214">These values are case sensitive.</span></span>

 

<span data-ttu-id="f3c34-215">Se um aplicativo de acessibilidade oferecer suporte a várias acomodações, o valor do registro de perfil deverá incluir um atributo de **tipo de acomodação** para cada acomodação.</span><span class="sxs-lookup"><span data-stu-id="f3c34-215">If an accessibility application supports multiple accommodations, the Profile registry value should include an **Accommodation type** attribute for each accommodation.</span></span>

### <a name="ease-of-access-registry-details"></a><span data-ttu-id="f3c34-216">Detalhes do registro de facilidade de acesso</span><span class="sxs-lookup"><span data-stu-id="f3c34-216">Ease of Access registry details</span></span>

<span data-ttu-id="f3c34-217">Para registrar seu aplicativo de acessibilidade, você precisa criar uma chave para seu aplicativo no local do registro a seguir e preenchê-lo com pares de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="f3c34-217">To register your accessibility application, you need to create a key for your application at the following registry location and populate it with name-value pairs.</span></span>

<span data-ttu-id="f3c34-218">**HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATS\\**</span><span class="sxs-lookup"><span data-stu-id="f3c34-218">**HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATs\\**</span></span>

<span data-ttu-id="f3c34-219">Nomeie a chave do registro do seu aplicativo usando o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="f3c34-219">Name your application's registry key using the following format:</span></span>

<span data-ttu-id="f3c34-220">*"CompanyName \_ NomeDoProduto \_ v \# "*</span><span class="sxs-lookup"><span data-stu-id="f3c34-220">*"CompanyName\_ProductName\_v\#"*</span></span>

<span data-ttu-id="f3c34-221">Por exemplo, "Contoso \_ lupa \_ v 2.0".</span><span class="sxs-lookup"><span data-stu-id="f3c34-221">For example, "Contoso\_Magnifier\_v2.0".</span></span>

<span data-ttu-id="f3c34-222">Para adicionar valores de registro, o programa de instalação deve estar em execução com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="f3c34-222">To add registry values, your installation program must be running with elevated privileges.</span></span>

### <a name="secure-desktop-accommodation"></a><span data-ttu-id="f3c34-223">Acomodação de área de trabalho segura</span><span class="sxs-lookup"><span data-stu-id="f3c34-223">Secure desktop accommodation</span></span>

<span data-ttu-id="f3c34-224">A chave do registro **SecureDesktopAccommodation** permite especificar como seu aplicativo de acessibilidade responde à área de trabalho segura.</span><span class="sxs-lookup"><span data-stu-id="f3c34-224">The **SecureDesktopAccommodation** registry key lets you specify how your accessibility application responds to the secure desktop.</span></span> <span data-ttu-id="f3c34-225">Por padrão, a central de facilidade de acesso iniciará seu aplicativo na área de trabalho segura se ele já estiver em execução na área de trabalho normal ou se estiver configurado para ser executado na área de trabalho de logon.</span><span class="sxs-lookup"><span data-stu-id="f3c34-225">By default, the Ease of Access Center launches your application on the secure desktop if it was already running on the normal desktop, or if it is configured to run on the logon desktop.</span></span> <span data-ttu-id="f3c34-226">Usando a chave **SecureDesktopAccommodation** , você pode:</span><span class="sxs-lookup"><span data-stu-id="f3c34-226">By using the **SecureDesktopAccommodation** key, you can:</span></span>

-   <span data-ttu-id="f3c34-227">Especifique uma versão alternativa do seu aplicativo para uso na área de trabalho segura.</span><span class="sxs-lookup"><span data-stu-id="f3c34-227">Specify an alternate version of your application for use on the secure desktop.</span></span> <span data-ttu-id="f3c34-228">Por exemplo, você pode ter uma versão alternativa que desabilita recursos não seguros ou é otimizado para usar menos memória e ser iniciado mais rapidamente.</span><span class="sxs-lookup"><span data-stu-id="f3c34-228">For example, you might have an alternate version that disables unsecured features, or is optimized to use less memory and launch faster.</span></span>

    <span data-ttu-id="f3c34-229">Para especificar a versão alternativa, defina a chave **SecureDesktopAccommodation** como o nome da versão alternativa.</span><span class="sxs-lookup"><span data-stu-id="f3c34-229">To specify the alternate version, set the **SecureDesktopAccommodation** key to the name of the alternate version.</span></span> <span data-ttu-id="f3c34-230">Por exemplo, se você registrou seu aplicativo na chave do leitor de tela da Contoso \_ \_ v 1.0, você poderia registrar a versão alternativa na tela da Contoso \_ ReaderSecure \_ v 1.0.</span><span class="sxs-lookup"><span data-stu-id="f3c34-230">For example, if you registered your application at the Contoso\_Screen Reader\_v1.0 key, you could register the alternate version at Contoso\_Screen ReaderSecure\_v1.0.</span></span> <span data-ttu-id="f3c34-231">Em seguida, defina a chave **SecureDesktopAccommodation** do Contoso \_ Screen Reader \_ v 1.0 como "Contoso \_ Screen ReaderSecure \_ v 1.0".</span><span class="sxs-lookup"><span data-stu-id="f3c34-231">Then, set the **SecureDesktopAccommodation** key of Contoso\_Screen Reader\_v1.0 to "Contoso\_Screen ReaderSecure\_v1.0".</span></span>

-   <span data-ttu-id="f3c34-232">Especifique um aplicativo de acessibilidade da Microsoft para usar na área de trabalho segura em vez de seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f3c34-232">Specify a Microsoft accessibility application to use on the secure desktop in place of your application.</span></span> <span data-ttu-id="f3c34-233">Para essa opção, defina **SecureDesktopAccommodation** como o nome do aplicativo de acessibilidade da Microsoft específico: "OSK", "magnifierpane" ou "Narrator".</span><span class="sxs-lookup"><span data-stu-id="f3c34-233">For this option, set **SecureDesktopAccommodation** to the name of the particular Microsoft accessibility application: "osk", "magnifierpane", or "Narrator".</span></span>
-   <span data-ttu-id="f3c34-234">Especifique que o aplicativo não deve ser executado na área de trabalho segura e nenhum aplicativo alternativo.</span><span class="sxs-lookup"><span data-stu-id="f3c34-234">Specify that your application should not run on the secure desktop, and neither should any alternate application.</span></span> <span data-ttu-id="f3c34-235">Para essa opção, defina **SecureDesktopAccommodation** como "None" (recomendado) ou o nome de um aplicativo inexistente.</span><span class="sxs-lookup"><span data-stu-id="f3c34-235">For this option, set **SecureDesktopAccommodation** to "none" (recommend) or the name of a nonexistent application.</span></span>

<span data-ttu-id="f3c34-236">Se a chave do registro **SecureDesktopAccommodation** para seu aplicativo de acessibilidade especificar um aplicativo de acessibilidade da Microsoft para ser executado na área de trabalho segura em vez de seu aplicativo, o Windows notificará o usuário sobre isso ao fazer a transição para a área de trabalho segura.</span><span class="sxs-lookup"><span data-stu-id="f3c34-236">If the **SecureDesktopAccommodation** registry key for your accessibility application specifies a Microsoft accessibility application to run on the secure desktop in place of your application, Windows notifies the user of this when making the transition to the secure desktop.</span></span> <span data-ttu-id="f3c34-237">Para notificar o usuário, o Windows exibe a cadeia de caracteres especificada na chave do registro de descrição para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f3c34-237">To notify the user, Windows displays the string specified in the Description registry key for your application.</span></span> <span data-ttu-id="f3c34-238">Por exemplo, se o aplicativo ScreenReader Deluxe 1,0 usar o Microsoft Narrator na área de trabalho segura, ele incluiria uma cadeia de caracteres de descrição como "o Microsoft Narrator será usado nos desktops bloqueados, de logon e em outras áreas de trabalho seguras no lugar do ScreenReader Deluxe 1,0".</span><span class="sxs-lookup"><span data-stu-id="f3c34-238">For example, if the ScreenReader Deluxe 1.0 application uses Microsoft Narrator on the secure desktop, it would include a Description string such as, "Microsoft Narrator will be used in the locked, logon, and other secure desktops in place of ScreenReader Deluxe 1.0."</span></span>

<span data-ttu-id="f3c34-239">Se a chave **SecureDesktopAccommodation** do seu aplicativo for definida como "None", use a tecla **Description** para informar ao usuário que seu aplicativo não está disponível na área de trabalho segura e nenhuma alternativa é fornecida.</span><span class="sxs-lookup"><span data-stu-id="f3c34-239">If your application's **SecureDesktopAccommodation** key is set to "none", use the **Description** key to tell the user your application is not available on the secure desktop and no alternative is provided.</span></span>

<span data-ttu-id="f3c34-240">O Windows exibe o texto de descrição nos locais relevantes na central de facilidade de acesso.</span><span class="sxs-lookup"><span data-stu-id="f3c34-240">Windows displays the Description text in the relevant locations in the Ease of Access Center.</span></span>

### <a name="running-at-installation-and-on-the-logon-desktop"></a><span data-ttu-id="f3c34-241">Em execução na instalação e na área de trabalho de logon</span><span class="sxs-lookup"><span data-stu-id="f3c34-241">Running at installation and on the logon desktop</span></span>

<span data-ttu-id="f3c34-242">Se você acrescentar o nome de chave registrado do aplicativo de acessibilidade à cadeia de caracteres no seguinte local do registro, o Windows iniciará o aplicativo imediatamente após a instalação.</span><span class="sxs-lookup"><span data-stu-id="f3c34-242">If you append your accessibility application's registered key name to the string at the following registry location, Windows will launch your application immediately after it is installed.</span></span> <span data-ttu-id="f3c34-243">Além disso, o Windows executará automaticamente o aplicativo sempre que a área de trabalho de logon estiver ativa.</span><span class="sxs-lookup"><span data-stu-id="f3c34-243">Also, Windows will automatically run your application whenever the logon desktop is active.</span></span>

<span data-ttu-id="f3c34-244">**\\Configuração de \\ acessibilidade do software HKCU Microsoft \\ Windows NT \\ CurrentVersion \\ \\**</span><span class="sxs-lookup"><span data-stu-id="f3c34-244">**HKCU\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\Configuration**</span></span>

<span data-ttu-id="f3c34-245">A chave de configuração é uma cadeia de caracteres delimitada por vírgula.</span><span class="sxs-lookup"><span data-stu-id="f3c34-245">The Configuration key is a comma-delimited string.</span></span> <span data-ttu-id="f3c34-246">Para adicionar seu aplicativo, acrescente uma cadeia de caracteres igual à chave do registro do seu aplicativo em HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATS \\ .</span><span class="sxs-lookup"><span data-stu-id="f3c34-246">To add your application, append a string that is the same as your application's registry key at HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATs\\.</span></span>

### <a name="running-in-a-job"></a><span data-ttu-id="f3c34-247">Executando em um trabalho</span><span class="sxs-lookup"><span data-stu-id="f3c34-247">Running in a job</span></span>

<span data-ttu-id="f3c34-248">Se a chave do registro **TerminateOnDesktopSwitch** não estiver presente ou estiver definida como diferente de zero, o Windows executará o aplicativo no contexto de um trabalho, encerrando e reiniciando o aplicativo com cada transição da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f3c34-248">If the **TerminateOnDesktopSwitch** registry key is not present or is set to non-zero, Windows runs the application in the context of a job, terminating and restarting the application with each desktop transition.</span></span> <span data-ttu-id="f3c34-249">A execução em um trabalho garante que apenas uma única instância do aplicativo seja executada em um determinado momento e libera o aplicativo de ter que monitorar o estado da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f3c34-249">Running in a job ensures that only a single instance of the application is running at a particular time, and frees the application from having to monitor the desktop state.</span></span> <span data-ttu-id="f3c34-250">As desvantagens da execução em um trabalho incluem:</span><span class="sxs-lookup"><span data-stu-id="f3c34-250">The disadvantages of running in a job include:</span></span>

-   <span data-ttu-id="f3c34-251">O aplicativo incorre em um custo de inicialização com cada transição da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f3c34-251">The application incurs a startup cost with each desktop transition.</span></span>
-   <span data-ttu-id="f3c34-252">O aplicativo só pode ser iniciado por meio da central de facilidade de acesso.</span><span class="sxs-lookup"><span data-stu-id="f3c34-252">The application can be started only through the Ease of Access Center.</span></span>
-   <span data-ttu-id="f3c34-253">O aplicativo deve salvar suas configurações continuamente, pois ele pode ser encerrado a qualquer momento por uma transição de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f3c34-253">The application must continually save its settings because it can be terminated at any time by a desktop transition.</span></span>

<span data-ttu-id="f3c34-254">Se a chave **TerminateOnDesktopSwitch** existir e for definida como 0, o Windows não executará o aplicativo de acessibilidade em um trabalho.</span><span class="sxs-lookup"><span data-stu-id="f3c34-254">If the **TerminateOnDesktopSwitch** key exists and is set to 0, Windows doesn't run the accessibility application in a job.</span></span> <span data-ttu-id="f3c34-255">Tem estas vantagens:</span><span class="sxs-lookup"><span data-stu-id="f3c34-255">This has the following advantages:</span></span>

-   <span data-ttu-id="f3c34-256">Nenhum custo de inicialização é associado a transições de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f3c34-256">No startup costs are associated with desktop transitions.</span></span>
-   <span data-ttu-id="f3c34-257">O aplicativo pode ser iniciado fora do centro de facilidade de acesso.</span><span class="sxs-lookup"><span data-stu-id="f3c34-257">The application can be started outside of the Ease of Access Center.</span></span>

<span data-ttu-id="f3c34-258">As desvantagens de não estar em execução em um trabalho incluem:</span><span class="sxs-lookup"><span data-stu-id="f3c34-258">The disadvantages of not running in a job include:</span></span>

-   <span data-ttu-id="f3c34-259">Como o aplicativo não é reiniciado em transições de área de trabalho, ele deve detectar quando a área de trabalho atual está inativa e responder adequadamente.</span><span class="sxs-lookup"><span data-stu-id="f3c34-259">Because the application isn t restarted on desktop transitions, it must detect when the current desktop is inactive and respond appropriately.</span></span> <span data-ttu-id="f3c34-260">Por exemplo, o aplicativo deve ceder o controle do hardware para que a versão da área de trabalho segura do aplicativo possa usá-lo, e o aplicativo deve entrar no modo de suspensão para evitar o uso de recursos do processador.</span><span class="sxs-lookup"><span data-stu-id="f3c34-260">For example, the application must relinquish control of hardware so the secure desktop version of the application can use it, and the application should enter sleep mode to avoid using processor resources.</span></span>
-   <span data-ttu-id="f3c34-261">Se o aplicativo puder ser iniciado por meio do menu Iniciar, do Windows Explorer ou da linha de comando, o centro de facilidade de acesso precisará ser informado.</span><span class="sxs-lookup"><span data-stu-id="f3c34-261">If the application can be started through the Start menu, Windows Explorer, or the command line, the Ease of Access Center needs to be informed.</span></span> <span data-ttu-id="f3c34-262">Para obter mais informações, consulte a tecla com o **logotipo do Windows + U**.</span><span class="sxs-lookup"><span data-stu-id="f3c34-262">For more information, see **Windows Logo key + U**.</span></span>
-   <span data-ttu-id="f3c34-263">Como várias cópias do aplicativo podem ser executadas simultaneamente em áreas de trabalho diferentes, o aplicativo deve ser escrito para dar suporte a várias cópias em execução.</span><span class="sxs-lookup"><span data-stu-id="f3c34-263">Because multiple copies of the application can run simultaneously on different desktops, the application must be written to support multiple running copies.</span></span>

### <a name="windows-logo-key--u"></a><span data-ttu-id="f3c34-264">Tecla com o logotipo do Windows + U</span><span class="sxs-lookup"><span data-stu-id="f3c34-264">Windows Logo key + U</span></span>

<span data-ttu-id="f3c34-265">Se seu aplicativo de acessibilidade estiver configurado para ser executado em um trabalho, o código de inicialização do aplicativo deverá incluir uma chamada para a função [**IsProcessInJob**](/windows/desktop/api/jobapi/nf-jobapi-isprocessinjob) para determinar se o aplicativo está iniciando em um trabalho.</span><span class="sxs-lookup"><span data-stu-id="f3c34-265">If your accessibility application is configured to run in a job, your application's startup code should include a call to the [**IsProcessInJob**](/windows/desktop/api/jobapi/nf-jobapi-isprocessinjob) function to determine whether the application is starting in a job.</span></span> <span data-ttu-id="f3c34-266">Se for, o aplicativo deverá iniciar o centro de facilidade de acesso e, em seguida, sair.</span><span class="sxs-lookup"><span data-stu-id="f3c34-266">If it is, the application should start the Ease of Access Center and then exit.</span></span> <span data-ttu-id="f3c34-267">O exemplo a seguir mostra como chamar **IsProcessInJob**.</span><span class="sxs-lookup"><span data-stu-id="f3c34-267">The following example shows how to call **IsProcessInJob**.</span></span>


```C++
BOOL fAlreadyInJob;
BOOL fSuccess = IsProcessInJob(GetCurrentProcess(), NULL, &fAlreadyInJob); 
```



<span data-ttu-id="f3c34-268">Se o aplicativo de acessibilidade estiver configurado para ser executado fora de um trabalho, ele deverá notificar o centro de facilidade de acesso que o aplicativo está iniciando e continuar normalmente.</span><span class="sxs-lookup"><span data-stu-id="f3c34-268">If the accessibility application is configured to run outside of a job, it should notify the Ease of Access Center that the application is starting and continue as normal.</span></span>

<span data-ttu-id="f3c34-269">Independentemente de como o aplicativo é configurado, se ele fornece uma maneira de sair de dentro do aplicativo, como um botão fechar, o aplicativo deve notificar o centro de facilidade de acesso que ele está saindo.</span><span class="sxs-lookup"><span data-stu-id="f3c34-269">Regardless of how the application is configured, if it provides a way to exit from within the application, such as a Close button, the application must notify the Ease of Access Center that it is exiting.</span></span>

<span data-ttu-id="f3c34-270">Um aplicativo notifica a central de facilidade de acesso definindo uma chave de registro temporária e, em seguida, injetando a tecla de logotipo do Windows + a combinação de tecla U no fluxo de entrada.</span><span class="sxs-lookup"><span data-stu-id="f3c34-270">An application notifies the Ease of Access Center by setting a temporary registry key and then injecting the Windows Logo key + U key combination into the input stream.</span></span>

<span data-ttu-id="f3c34-271">O aplicativo deve criar a chave temporária no seguinte local.</span><span class="sxs-lookup"><span data-stu-id="f3c34-271">The application should create the temporary key at the following location.</span></span>

<span data-ttu-id="f3c34-272">**HKCU \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ AccessibilityTemp**</span><span class="sxs-lookup"><span data-stu-id="f3c34-272">**HKCU\\Software\\Microsoft\\Windows NT\\CurrentVersion\\AccessibilityTemp**</span></span>

<span data-ttu-id="f3c34-273">A chave temporária deve ter o mesmo nome que o nome do aplicativo registrado, como "o \_ leitor de tela da Contoso \_ v 1.0".</span><span class="sxs-lookup"><span data-stu-id="f3c34-273">The temporary key should have the same name as the registered application name, such as "Contoso\_Screen Reader\_v1.0".</span></span> <span data-ttu-id="f3c34-274">O valor da chave é um **DWORD** definido como 0x0003 quando está sendo iniciado, ou 0x0002 quando o aplicativo está sendo encerrado.</span><span class="sxs-lookup"><span data-stu-id="f3c34-274">The value of the key is a **DWORD** set to 0x0003 when it is starting, or 0x0002 when the application is exiting.</span></span>


```C++
INPUT input[4] = {0};

input[0].type = INPUT_KEYBOARD;
input[0].ki.wVk = VK_LWIN;
input[0].ki.dwFlags = 0;

input[1].type = INPUT_KEYBOARD;
input[1].ki.wVk = 0x55; // U key
input[1].ki.dwFlags = 0;

input[2].type = INPUT_KEYBOARD;
input[2].ki.wVk = 0x55; // U key
input[2].ki.dwFlags = KEYEVENTF_KEYUP;

input[3].type = INPUT_KEYBOARD;
input[3].ki.wVk = VK_LWIN;
input[3].ki.dwFlags = KEYEVENTF_KEYUP;

SendInput(ARRAYSIZE(input), input, sizeof(input[0]));
```



### <a name="windows-logo-key--volume-up"></a><span data-ttu-id="f3c34-275">Tecla com o logotipo do Windows + volume up</span><span class="sxs-lookup"><span data-stu-id="f3c34-275">Windows Logo key + Volume Up</span></span>

<span data-ttu-id="f3c34-276">Quando o usuário inicia seu aplicativo de acessibilidade pressionando a tecla com o logotipo do Windows + a combinação de teclas de volume (como em um dispositivo de Tablet), o centro de facilidade de acesso passa o seguinte argumento de linha de comando para o aplicativo:</span><span class="sxs-lookup"><span data-stu-id="f3c34-276">When the user starts your accessibility application by pressing the Windows Logo key + Volume Up key combination (such as on a tablet device), the Ease of Access Center passes the following command-line argument to the application:</span></span>

<span data-ttu-id="f3c34-277">**/hardwarebuttonlaunch**</span><span class="sxs-lookup"><span data-stu-id="f3c34-277">**/hardwarebuttonlaunch**</span></span>

<span data-ttu-id="f3c34-278">Seu aplicativo pode usar esse argumento para determinar se deve iniciar normalmente ou ajustar o comportamento de acordo.</span><span class="sxs-lookup"><span data-stu-id="f3c34-278">Your application can use this argument to determine whether to start normally, or to adjust behavior accordingly.</span></span>

### <a name="transferring-secure-desktop-settings"></a><span data-ttu-id="f3c34-279">Transferindo configurações de área de trabalho segura</span><span class="sxs-lookup"><span data-stu-id="f3c34-279">Transferring secure desktop settings</span></span>

<span data-ttu-id="f3c34-280">Se seu aplicativo de acessibilidade der suporte à área de trabalho segura, você poderá usar o registro para copiar as configurações quando o aplicativo passar para a área de trabalho segura.</span><span class="sxs-lookup"><span data-stu-id="f3c34-280">If your accessibility application supports the secure desktop, you can use the registry to copy settings when the application transitions to the secure desktop.</span></span> <span data-ttu-id="f3c34-281">A cópia das configurações ajuda a tornar a transição para a área de trabalho segura mais direta para o usuário.</span><span class="sxs-lookup"><span data-stu-id="f3c34-281">Copying settings helps makes the transition to the secure desktop more seamless for the user.</span></span>

<span data-ttu-id="f3c34-282">Para copiar as configurações, defina a chave do registro CopySettingsToLockedDesktop do aplicativo como 1 e armazene as configurações no seguinte local do registro.</span><span class="sxs-lookup"><span data-stu-id="f3c34-282">To copy settings, set the application's CopySettingsToLockedDesktop registry key to 1, and store the settings in the following registry location.</span></span>

<span data-ttu-id="f3c34-283">**HKCU \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATConfig\\<AT Key Name>**</span><span class="sxs-lookup"><span data-stu-id="f3c34-283">**HKCU\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATConfig\\<AT Key Name>**</span></span>

<span data-ttu-id="f3c34-284">A central de facilidade de acesso monitora esse local do registro enquanto o aplicativo está em execução.</span><span class="sxs-lookup"><span data-stu-id="f3c34-284">The Ease of Access Center monitors this registry location while the application is running.</span></span> <span data-ttu-id="f3c34-285">Quando ocorre uma transição para a área de trabalho segura, a central de facilidade de acesso copia as configurações para o mesmo local no hive HKCU da área de trabalho segura.</span><span class="sxs-lookup"><span data-stu-id="f3c34-285">When a transition to the secure desktop occurs, the Ease of Access Center copies the settings to the same location in the secure desktop s HKCU hive.</span></span> <span data-ttu-id="f3c34-286">O aplicativo pode, então, ler as configurações e retomar seu estado.</span><span class="sxs-lookup"><span data-stu-id="f3c34-286">The application can then read the settings and resume its state.</span></span>

<span data-ttu-id="f3c34-287">Seu aplicativo de acessibilidade deve gravar suas configurações em intervalos regulares ou sempre que os valores forem alterados.</span><span class="sxs-lookup"><span data-stu-id="f3c34-287">Your accessibility application should write its settings at regular intervals or whenever the values change.</span></span> <span data-ttu-id="f3c34-288">A gravação de configurações na saída do aplicativo não funcionará.</span><span class="sxs-lookup"><span data-stu-id="f3c34-288">Writing settings on application exit will not work.</span></span> <span data-ttu-id="f3c34-289">Se o aplicativo estiver sendo executado em um trabalho, ele será encerrado na transição para fora da área de trabalho segura, antes que o código de saída tenha a oportunidade de ser executado.</span><span class="sxs-lookup"><span data-stu-id="f3c34-289">If the application is running in a job, it is terminated on the transition away from the secure desktop, before the exit code has a chance to run.</span></span> <span data-ttu-id="f3c34-290">Se o aplicativo não estiver em execução em um trabalho, o aplicativo não será encerrado na transição para fora da área de trabalho segura.</span><span class="sxs-lookup"><span data-stu-id="f3c34-290">If the application is not running in a job, the application is not terminated on the transition away from the secure desktop.</span></span>

### <a name="caution"></a><span data-ttu-id="f3c34-291">Cuidado</span><span class="sxs-lookup"><span data-stu-id="f3c34-291">Caution</span></span>

<span data-ttu-id="f3c34-292">Como as chaves do Registro descritas aqui são gravadas no modo de usuário, elas não são seguras.</span><span class="sxs-lookup"><span data-stu-id="f3c34-292">Because the registry keys described here are written in user mode, they are not secure.</span></span> <span data-ttu-id="f3c34-293">Se o seu aplicativo de acessibilidade ler o conteúdo dessas chaves, ele deverá verificar cuidadosamente os dados e usá-los com cautela.</span><span class="sxs-lookup"><span data-stu-id="f3c34-293">If your accessibility application reads the contents of these keys, it should carefully check the data and use it with caution.</span></span> <span data-ttu-id="f3c34-294">Especificamente, o aplicativo deve fazer uma verificação de limites em valores **DWORD** , ter cuidado com comprimentos de cadeia de caracteres, não deve ler nomes de DLL de plug-in e não deve executar nenhum comando encontrado em cadeias.</span><span class="sxs-lookup"><span data-stu-id="f3c34-294">Specifically, your application should do a bounds check on **DWORD** values, be careful with string lengths, should not read plug-in DLL names, and should not execute any commands found in strings.</span></span>

## <a name="registry-examples"></a><span data-ttu-id="f3c34-295">Exemplos de registro</span><span class="sxs-lookup"><span data-stu-id="f3c34-295">Registry Examples</span></span>

<span data-ttu-id="f3c34-296">O exemplo a seguir mostra os valores de registro possíveis para um produto fictício chamado contoso ScreenReader versão 2,0, cujo nome localizado é armazenado como um recurso.</span><span class="sxs-lookup"><span data-stu-id="f3c34-296">The following example shows the possible registry values for a fictitious product called Contoso ScreenReader version 2.0, whose localized name is stored as a resource.</span></span>

<span data-ttu-id="f3c34-297">Os valores na tabela estão sob a seguinte chave:</span><span class="sxs-lookup"><span data-stu-id="f3c34-297">The values in the table are under the following key:</span></span>

<span data-ttu-id="f3c34-298">**HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ acessibilidade \\ ATS \\ Contoso \_ Screen Reader \_ v 2.0**</span><span class="sxs-lookup"><span data-stu-id="f3c34-298">**HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATs\\Contoso\_Screen Reader\_v2.0**</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3c34-299">Nome</span><span class="sxs-lookup"><span data-stu-id="f3c34-299">Name</span></span></th>
<th><span data-ttu-id="f3c34-300">Tipo</span><span class="sxs-lookup"><span data-stu-id="f3c34-300">Type</span></span></th>
<th><span data-ttu-id="f3c34-301">Dados</span><span class="sxs-lookup"><span data-stu-id="f3c34-301">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f3c34-302">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="f3c34-302">ApplicationName</span></span></td>
<td><span data-ttu-id="f3c34-303">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f3c34-303">REG_SZ</span></span></td>
<td><span data-ttu-id="f3c34-304">@% SystemRoot% \system32\ContosoRes.dll,-5020</span><span class="sxs-lookup"><span data-stu-id="f3c34-304">@%SystemRoot%\system32\ContosoRes.dll,-5020</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3c34-305">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3c34-305">Description</span></span></td>
<td><span data-ttu-id="f3c34-306">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f3c34-306">REG_SZ</span></span></td>
<td><span data-ttu-id="f3c34-307">@% SystemRoot% \system32\ContosoRes.dll,-5040</span><span class="sxs-lookup"><span data-stu-id="f3c34-307">@%SystemRoot%\system32\ContosoRes.dll,-5040</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3c34-308">Perfil</span><span class="sxs-lookup"><span data-stu-id="f3c34-308">Profile</span></span></td>
<td><span data-ttu-id="f3c34-309">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f3c34-309">REG_SZ</span></span></td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3c34-310">XML</span><span class="sxs-lookup"><span data-stu-id="f3c34-310">XML</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3c34-311">SimpleProfile</span><span class="sxs-lookup"><span data-stu-id="f3c34-311">SimpleProfile</span></span></td>
<td><span data-ttu-id="f3c34-312">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f3c34-312">REG_SZ</span></span></td>
<td><span data-ttu-id="f3c34-313">ScreenReader</span><span class="sxs-lookup"><span data-stu-id="f3c34-313">ScreenReader</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3c34-314">StartExe</span><span class="sxs-lookup"><span data-stu-id="f3c34-314">StartExe</span></span></td>
<td><span data-ttu-id="f3c34-315">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f3c34-315">REG_SZ</span></span></td>
<td><span data-ttu-id="f3c34-316">C:\ContosoTools\Bin\ContosoSR.exe</span><span class="sxs-lookup"><span data-stu-id="f3c34-316">C:\ContosoTools\Bin\ContosoSR.exe</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3c34-317">StartParams</span><span class="sxs-lookup"><span data-stu-id="f3c34-317">StartParams</span></span></td>
<td><span data-ttu-id="f3c34-318">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f3c34-318">REG_SZ</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f3c34-319">SecureDesktopAccommodation</span><span class="sxs-lookup"><span data-stu-id="f3c34-319">SecureDesktopAccommodation</span></span></td>
<td><span data-ttu-id="f3c34-320">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f3c34-320">REG_SZ</span></span></td>
<td><span data-ttu-id="f3c34-321">Narrator</span><span class="sxs-lookup"><span data-stu-id="f3c34-321">Narrator</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f3c34-322">Se o aplicativo fornecer um leitor de tela e uma lupa de tela em um único executável, os valores para o componente de leitor de tela poderão ter esta aparência:</span><span class="sxs-lookup"><span data-stu-id="f3c34-322">If the application provides both a screen reader and a screen magnifier in a single executable, the values for the screen reader component might look like this:</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3c34-323">Nome</span><span class="sxs-lookup"><span data-stu-id="f3c34-323">Name</span></span></th>
<th><span data-ttu-id="f3c34-324">Tipo</span><span class="sxs-lookup"><span data-stu-id="f3c34-324">Type</span></span></th>
<th><span data-ttu-id="f3c34-325">Dados</span><span class="sxs-lookup"><span data-stu-id="f3c34-325">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f3c34-326">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="f3c34-326">ApplicationName</span></span></td>
<td><span data-ttu-id="f3c34-327">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f3c34-327">REG_SZ</span></span></td>
<td><span data-ttu-id="f3c34-328">@C:\Program Files\Contoso\Contosores.dll,-30</span><span class="sxs-lookup"><span data-stu-id="f3c34-328">@C:\Program Files\Contoso\Contosores.dll,-30</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3c34-329">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3c34-329">Description</span></span></td>
<td><span data-ttu-id="f3c34-330">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f3c34-330">REG_SZ</span></span></td>
<td><span data-ttu-id="f3c34-331">@C:\Program Files\Contoso\Contosores.dll,-32</span><span class="sxs-lookup"><span data-stu-id="f3c34-331">@C:\Program Files\Contoso\Contosores.dll,-32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3c34-332">Perfil</span><span class="sxs-lookup"><span data-stu-id="f3c34-332">Profile</span></span></td>
<td><span data-ttu-id="f3c34-333">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f3c34-333">REG_SZ</span></span></td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3c34-334">XML</span><span class="sxs-lookup"><span data-stu-id="f3c34-334">XML</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3c34-335">SimpleProfile</span><span class="sxs-lookup"><span data-stu-id="f3c34-335">SimpleProfile</span></span></td>
<td><span data-ttu-id="f3c34-336">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f3c34-336">REG_SZ</span></span></td>
<td><span data-ttu-id="f3c34-337">ScreenReader</span><span class="sxs-lookup"><span data-stu-id="f3c34-337">ScreenReader</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3c34-338">StartExe</span><span class="sxs-lookup"><span data-stu-id="f3c34-338">StartExe</span></span></td>
<td><span data-ttu-id="f3c34-339">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f3c34-339">REG_SZ</span></span></td>
<td><span data-ttu-id="f3c34-340">C:\Arquivos de Files\Contoso\Bin\ContosoSR.exe</span><span class="sxs-lookup"><span data-stu-id="f3c34-340">C:\Program Files\Contoso\Bin\ContosoSR.exe</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3c34-341">StartParams</span><span class="sxs-lookup"><span data-stu-id="f3c34-341">StartParams</span></span></td>
<td><span data-ttu-id="f3c34-342">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f3c34-342">REG_SZ</span></span></td>
<td><span data-ttu-id="f3c34-343">/r</span><span class="sxs-lookup"><span data-stu-id="f3c34-343">/r</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f3c34-344">Os valores para o componente lupa seriam na seguinte chave:</span><span class="sxs-lookup"><span data-stu-id="f3c34-344">The values for the magnifier component would be in the following key:</span></span>

<span data-ttu-id="f3c34-345">**HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Contosoibility \\ ATS \\ Contoso \_ lupa \_ v 2.0**</span><span class="sxs-lookup"><span data-stu-id="f3c34-345">**HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Contosoibility\\ATs\\Contoso\_Magnifier\_v2.0**</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3c34-346">Nome</span><span class="sxs-lookup"><span data-stu-id="f3c34-346">Name</span></span></th>
<th><span data-ttu-id="f3c34-347">Tipo</span><span class="sxs-lookup"><span data-stu-id="f3c34-347">Type</span></span></th>
<th><span data-ttu-id="f3c34-348">Dados</span><span class="sxs-lookup"><span data-stu-id="f3c34-348">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f3c34-349">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="f3c34-349">ApplicationName</span></span></td>
<td><span data-ttu-id="f3c34-350">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f3c34-350">REG_SZ</span></span></td>
<td><span data-ttu-id="f3c34-351">@c:\Program Files\Contoso\Contosores.dll,-31</span><span class="sxs-lookup"><span data-stu-id="f3c34-351">@c:\Program Files\Contoso\Contosores.dll,-31</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3c34-352">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3c34-352">Description</span></span></td>
<td><span data-ttu-id="f3c34-353">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f3c34-353">REG_SZ</span></span></td>
<td><span data-ttu-id="f3c34-354">@c:\Program Files\Contoso\Contosores.dll,-42</span><span class="sxs-lookup"><span data-stu-id="f3c34-354">@c:\Program Files\Contoso\Contosores.dll,-42</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3c34-355">Perfil</span><span class="sxs-lookup"><span data-stu-id="f3c34-355">Profile</span></span></td>
<td><span data-ttu-id="f3c34-356">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f3c34-356">REG_SZ</span></span></td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3c34-357">XML</span><span class="sxs-lookup"><span data-stu-id="f3c34-357">XML</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;mild vision&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3c34-358">SimpleProfile</span><span class="sxs-lookup"><span data-stu-id="f3c34-358">SimpleProfile</span></span></td>
<td><span data-ttu-id="f3c34-359">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f3c34-359">REG_SZ</span></span></td>
<td><span data-ttu-id="f3c34-360">Amplia</span><span class="sxs-lookup"><span data-stu-id="f3c34-360">Magnification</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3c34-361">StartExe</span><span class="sxs-lookup"><span data-stu-id="f3c34-361">StartExe</span></span></td>
<td><span data-ttu-id="f3c34-362">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f3c34-362">REG_SZ</span></span></td>
<td><span data-ttu-id="f3c34-363">C:\Arquivos de Files\Contoso\Bin\ContosoSR.exe</span><span class="sxs-lookup"><span data-stu-id="f3c34-363">c:\Program Files\Contoso\Bin\ContosoSR.exe</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3c34-364">StartParams</span><span class="sxs-lookup"><span data-stu-id="f3c34-364">StartParams</span></span></td>
<td><span data-ttu-id="f3c34-365">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f3c34-365">REG_SZ</span></span></td>
<td><span data-ttu-id="f3c34-366">/m</span><span class="sxs-lookup"><span data-stu-id="f3c34-366">/m</span></span></td>
</tr>
</tbody>
</table>



 

 

